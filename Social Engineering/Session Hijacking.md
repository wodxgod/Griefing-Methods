# Session Hijacking

With session hijacking you can gain temporary unauthorized access to a user's Minecraft account using only their latest session token.

**Overview**

When logging in to your Minecraft account or launch the Minecraft client, the Mojang authentication server generates a temporary session token. Using a modified Minecraft client, you can gain access to the account using only their username and token. This is done by changing the client's session username and token.

When joining a premium server, you send your client's information to a authentication server owned by Mojang, to make it confirm the session is valid. 

It is not possible for the hacker to gain full access to an account using only the session token. They will only be able to play on servers on their account.

This method can be used to gain access to an owner/administrator's account and OP yourself on the target server.

**Getting the token**

There are different ways to get a user's session token. One way of doing it, is by making the target user run a Python script developed by me (wodx). Download it [here](https://github.com/wodxgod/Minecraft-Session-Token-Stealer). 

In the 1.8.9 versions of Minecraft and below, the latest session token can be found in the top of the latest.log file located at `%appdata%\.minecraft\logs\latest.log`.

All latest session tokens are cached in the `launcher_profiles.json` file located at `%appdata%\.minecraft\launcher_profiles.json` in any version of the game.

**Prevention**

Never share any Minecraft logs or the `launcher_profiles.json` file, and never run any suspicious scripts and executables on your PC.