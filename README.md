# Pulsar #
## What ##
Pulsar is a fork of Paper.

## LICENSE / Support / Usage of Patches ##
All patches written by Aikar, Starlis LLC, Contractors of Starlis LLC that has been included inside of Pulsar
are licensed MIT, and are free to be used in your own fork.

We offer ABSOLUTELY NO SUPPORT for these patches. If you wish to use them, you must take the effect to extract them
from our repo, apply them to your own, and repair any code changes to get it to compile (note: we use a .callEvent()
utility method on the Event class for nearly all Custom Events to reduce diff.)

If we make a breaking change, and you wish to pull the patch to update it after that, it's your job to fix the changes!


## OS Support / Scripts##
We only directly support Linux for the shell scripts. Btw I use arch.

Many scripts will try to push to our repo's, please change that if you fork :)

### scripts/importmcdev ###
Imports specific files from mc-dev that CB/Spigot doesn't use but we need.

### scripts/updatespigot ###
updates the Bukkit/CraftBukkit/Spigot baseline when passed --update, otherwise regenerates the baseline with changes
to mcdev from importmcdev

Run `scripts/applypatches` then `scripts/rebuildpatches` immediately after

### scripts/generatesources ###
Generates an mc-dev folder that can be added to IDE for the other mc-dev files located in minecraft-server.jar

### scripts/rebuildpatches ###
Rebuilds patch state from the EmpireCraft-* repo's current state. Automatically handles patch deletion and renaming
for you unlike Spigots version of these scripts.

### scripts/applypatches ###
Takes current patches/{bukkit,craftbukkit} and applys them on latest spigot upstream
