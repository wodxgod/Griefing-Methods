# UUIDSpoof - Fix Bypass
A lot of griefers abuses the Bungeecord subserver vulnerability called UUID spoofing. UUID spoofing makes you able to spoof your UUID to any player's UUID, which all player data is bound to. This means that you'll have their permissions, rank etc.

**What is UUIDSpoof - Fix?**
UUIDSpoof-Fix is a Spigot plugin developed by zPirroZ3007, designed to prevent players from exploiting the UUID spoof vulnerability.

A lot of server owners and administrators don't change the plugin configs. In this case, it's very important, to prevent players from bypassing UUIDSpoof - Fix.

In the source code of the plugin, you can see that you can whitelist players, making them able to bypass the UUID spoof checks when joining the server.
```java
@EventHandler(priority = EventPriority.MONITOR)
public void onPlayerLogin(final PlayerLoginEvent event) {
    ...
    if (ConfigManager.exempt().getList("whitelist").contains(event.getPlayer().getName())) {
        return;
    }
    ...
 }
 ```

 As default in the exempt.yml (./plugins/UUIDSpoofFix/exempt.yml) file, "zPirroZ3007" is whitelisted.
 ```yaml
 # All players in this list will be exempted from UUID check
whitelist:
- "zPirroZ3007"
```

By spoofing your username to be "zPirroZ3007" and spoofing your UUID to be any operators UUID, you are able to bypass the plugin.

**How do I prevent players from being able to bypass UUIDSpoof - Fix?**
Simply remove "zPirroZ3007" from the whitelist in the YAML file exempt.yml.