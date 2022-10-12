![Banner](https://raw.githubusercontent.com/Yukkuricraft/YukkuricraftBugReports/master/banners/YukkuriBanner%20-%20hat%203%20variantCircle.png)

# What The HECK Is This

This is the Yukkuricraft Github organization that houses various repos of tools used to run and administer [Yukkuricraft](https://yukkuricraft.net).

Our tools and repos are generally broken into various categories:

- (Minecraft) Server Management Tools
- Non-Server Management Tools
- Minecraft plugins

# Who the HECK Are You?

We're Yukkuricraft - The online community that created a fully explorable rendition of Gensokyo of Touhou Project fame in Minecraft!

## Website

The [Yukkuricraft/yukkuricraft.net](https://github.com/Yukkuricraft/yukkuricraft.net) repo contains our website sourcecode.

## How is Server Run

The Yukkuricraft server ~~is~~ will eventually be run with tooling contained in three repos:

- `Yukkuricraft/Yukkuricraft`
- `Yukkuricraft/YakumoDash`
- `Yukkuricraft/Patchouli`

(It's currently still running in the legacy monohost setup)

#### Yukkuricraft/Yukkuricraft

This repo primarily contains the containerized Minecraft server setup utilizing a Minecraft proxy in front. Our setup is capable of freely spinning up as many extra "environments" as hardware allows. Each "environment" is a completely decoupled container cluster with all necessary containers to run a full server.

This repo also contains the python source code for both the config generators to enable our dynamic env generation as well as the API code which exposes a method for interacting with the backend from `Yukkuricraft/YakumoDash`

#### Yukkuricraft/Patchouli

Patchouli solves the problem of wanting to separate out the dozens of various Minecraft config files into a VCS for all the great VCS benefits.

Patchouli will identify and operate on any config files it finds and integrates with the FS layout assumptions of `Yukkuricraft/Yukkuricraft` to allow additional functionality like copying or syncing configs from one environment to another.

#### Yukkuricraft/YakumoDash

YakumoDash is our server cluster management web interface.

YakumoDash allows users to manage `Yukkuricraft/Yukkuricraft` from a web interface to do everything from creating, deleting, or editing environments, attaching to and interacting with a console for any running Minecraft server in any environment, managing the server filesystems for plugin and other general management, and more.
