# Session Hijacking

Session hijacking you can gain access to an user's Minecraft account using only their username and session token.

**Overview**

When you log into your Minecraft account or launch the Minecraft client, the Mojang authorization server generates a temporary session token. Using a modified Minecraft client, you can hijack the account. This is done by changing the client's session username and token. When joining a premium server, you send your client's information to the Mojang authorization server, to confirm the session is valid.

**Gaining the token**

There are different ways to get a user's session token. One way of doing it, is by making the target user run a Python script developed by WodX. Download it [here](https://github.com/WodxTV/Minecraft-Session-Token-Stealer). 

In the \<1.9 versions of Minecraft, the latest session token can be found in the top of the latest.log file located at **%appdata%%\.minecraft\logs\latest.log**.

All latest session tokens are cached in the **launcher_profiles.json** file located at **%appdata%%\.minecraft\launcher_profiles.json**

**Prevention**

Never share any Minecraft logs or the launcher_profiles.json file, and never run any suspicious files.