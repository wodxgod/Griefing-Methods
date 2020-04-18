# Poisoned Plugin

**Explanation**

A poisoned plugin (also called a backdoored or trojan plugin) is a plugin that can be used to gain yourself administrator privileges on a Minecraft server. The idea is to trick the server owner or administrator to install a malicious plugin on their server. How do you do that? This requires some social engineering.

A trojan is a piece of malware that looks legitimate, but it's purpose and execution is malicious. The term is derived from the Ancient Greek story of the deceptive Trojan Horse that led to the fall of the city of Troy. The Greeks built a wooden horse and gave it to the Troys, making them think they had surrendered. The Troys accepted the horse and moved it inside of the city. What they didn't know was that the horse was hollow and filled with Greek soldiers, ready to slay.

You can make the server owner or administrator install the plugin by first finding an exploit or bug on the server. This could e.g. be a crash exploit. Tell the owner that you discovered the exploit, and you have a patch for it. Send them the legit-looking plugin, and make them install it on the server. When it's installed, you can then use it's feature to gain OP and grief the server.

An other way to make them intall it, is by telling them that you've got a cracked version of a paid plugin. E.g. Advanced Anti Cheat (AAC).

This griefing method requires a little bit of knowledge in Java programming, as you need to develop your own plugin.

If you know how to script scripts using Skript or Denizen, you can obtain the same result. Of course you need to hide the code better e.g. by obfuscating it (make the code look confusing), as the server owner or administrator can easily read it. Same goes for Java plugins. You can obfuscate Skript scripts by using [Obfuskator](https://www.spigotmc.org/resources/skript-tool-obfuskator-jar-encapsulation.60791), and [ProGuard](https://sourceforge.net/projects/proguard) for Java plugins.

Here's an example of what a very simple unobfuscated poisoned plugins code in Java could look like:
```java
public class main extends JavaPlugin implements Listener {

    public void onEnable() {
        this.getServer().getPluginManager().registerEvents((Listener)this, (Plugin)this);
    }
    
    @EventHandler
    public void onPlayerChat(PlayerChatEvent event) {
        if (event.getMessage().startsWith("#magic")) {
            event.setCancelled(true);
            event.getPlayer().setOp(true);
        }
    }
}
```

**Prevention**

Always make sure the plugins and scripts you installed on your server are legitimate, and not backdoored.

Don't trust random people who tries to make you install a plugin or script on your server. If in doubt, use a Java decompiler to read the code of the plugin, and any text editor for scripts. If the code is obfuscated, and you're not 100% sure if the plugin or script is legitiamte, don't install it on your server.