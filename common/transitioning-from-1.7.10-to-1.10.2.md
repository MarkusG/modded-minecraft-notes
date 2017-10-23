# Table of Contents #

1. Introduction
2. Discontinued Mods
3. Power Generation
4. Power Transmission
5. Mining
6. Storage
7. Movement/Transportation
8. Tools

# 1. Introduction #

I'm writing this for my friends at DUMB and Nobody Expects, but I figure I'll make it public in case anyone else wants to use it. This document serves as a TL;DR of the changes between 1.7.10 modpacks (our last game was FTB Infinity Evolved) and 1.10.2 modpacks (our upcoming game will be FTB Beyond + a couple additions).

# 2. Discontinued Mods #

The following significant 1.7.10 mods are not available in 1.10.2:

* Thaumcraft
* MineFactory Reloaded
* BuildCraft (available in 1.11)
* Mystcraft

# 3. Power Generation #

There are a few new ways of generating power at various stages of progression in 1.10.2.

## Actually Additions - Oil ##

Actually Additions adds a very good early-game power generation system involving pressing Canola into oil and burning that oil for decent early-game RF generation. When paired with Immersive Engineering's Garden Cloches, this setup is extremely powerful even into the mid-game (challenging upgrades to the oil-making process can bump production up to 350 RF/t/generator). See the in-game books for more information.

## Thermal Expansion - Refined Fuel ##

This process uses power to turn Coal into Refined Fuel, which can be burned in a Compression Dynamo to produce RF. A very basic setup looks like [this](https://i.imgur.com/5eY9v1N.png) (Don't mind those orange crystals. I'll cover them in the "Energy Transfer" section.). The machines in that screenshot are, from left to right, the Pulverizer (Coal -> Pulverized Coal), the Magma Crucible (Pulverized Coal -> Liquifacted Coal), two Fractionating Stills (Liquifacted Coal -> Naptha; Naptha -> Refined Fuel), and the dynamo.

## [Deep Resonance](https://minecraft.curseforge.com/projects/deep-resonance) ##

I've never used this power generation method myself, so that's on you, reader, to look up for yourself. Feel free to PR a short description of it.

# 4. Power Transmission #

There are a couple fun new wireless and interdimensional ways to tramsit power in 1.10.2.

## Draconic Evolution - Crystals ##

As shown in the screenshot above, Draconic Evolution introduces a new wireless energy transfer system in 1.10.2. It's based on three items:

1. Energy I/O Crystal - Beams power from a block (such as a capacitor bank) to another crystal
2. Energy Relay Crystal - Receives power from other crystals and trasmits power to other crystals
3. Wireless Energy Crystal - Receives power from other crystals and beams power to blocks

As soon as you've acquired Draconium, Ender Pearls, and Blaze Rods, I strongly advise using these crystals over wires, as they are much less of a headache and have an infinite transfer rate (as far as I know).

## FluxNetworks ##

FluxNetworks introduces a power transmission system based on abstract networks. These networks are analagous to FTB's Team system (what we use chunk-load). It's based on two items:

1. Flux Plug - Power input point
2. Flux Point - Power output point
3. (Optional) Flux Storage - Networked energy storage

These networks are inter-dimensional and have privacy settings to protect against other players stealing your power.

# 5. Mining #

The Ender Quarry is dead. Long live the Quantum Quarry! For our playthrough, I'm going to discourage the use of "traditional" quarries such as RFTools' Builder unless needed due to progression stage. I encourage you to move to a void miner or quantum quarry as soon as your progression permits. This is all for the sake of Tyler's precious server resources.

## Environmental Tech - Void Ore/Resource Miner ##

The ET Void Miners are multiblock structures that require a line of sight from their center block directly down to bedrock (or the void). When supplied power, they will produce ores or resources at a rate depending on their tier and deposit it into an adjacent inventory.

[A tier 1 void miner (right) and a tier 4 void miner (left). Resource and ore miners are identical except for their controllers, which are similar in recipes.](https://i.imgur.com/eH8APjy.png)

These will yield all ore/resource types. See JEI for rates.

## [Extra Utilities 2 - Quantum Quarry](https://ftb.gamepedia.com/Quantum_Quarry) ##

It takes a hefty amount of RF to mine blocks from an alternate dimension. See the link for more details.

This can mine all ore/resource types.

## [Immersive Engineering - Excavator](https://ftb.gamepedia.com/Excavator_(Immersive_Engineering))

It mines pure ores from veins in the ground. These veins don't physically exist. They're abstract chunk data. See the link for more details.

This will mine specific ores depending on its chunk location. I don't believe it supports non-IE mod ores.

## Advanced Rocketry - Asteroid Mining ##

I'll update this with a more descriptive description when I get a little more experience with it. TL;DR: You send a rocket to an asteroid, it mines ores from the asteroid, and brings them back to Earth.

This cannot mine very many ore types depending on server configuration. Our server is set to the default, which makes asteroids contain Iron, Gold, Copper, Tin, and Redstone.

# 6. Storage #

## [Refined Storage](https://refinedstorage.raoulvdberge.com/) ##

The easiest way to describe Refined Storage is "Applied Energistics 2 for Dummies." RS is a networked storage system similar to AE2. The significant differences between the two are:

* RS does not have a channel or subnetwork system like AE2. You can have as many devices on a single cable as you want, and they'll all be part of the same network.
* RS has built-in fluid handling. In 1.7.10, AE2 could support fluids through the Extra Cells 2 addon, but that addon does not support 1.10.2.
* RS drives can store an infinite number of types and simply have a maximum number of items they can store. A 64k drive can store 64,000 items.
* [RS autocrafting](https://refinedstorage.raoulvdberge.com/wiki/autocrafting) is simpler and slower than AE2 autocrafting.

Side note: MFR is dead and, with it, Deep Storage Units. Don't worry though, because we now have Quantum Storage Units, which, from what I can tell, are the same thing! They're cheaper too, and have a liquid equivalent (they also probably don't turn in to ME trash cans if you set them up incorrectly)! Hooray!

## Applied Energistics 2 Subnetworks ##

Not new, but I had no idea this existed in our last game and it didn't seem like anyone else did either. This allows for crazy builds like [this](https://i.imgur.com/Uki442s.jpg) and infinite expandability of your AE2 network.

Seriously. Use AE2 over RS unless you're boring and hate a challenge.

# 7. Movement/Transportation #

## Extra Utilities 2 - Angel Ring ##

This isn't new, but I figure I should include it because I'm not sure how many people knew about it in our last game. It allows creative flight at the cost of GP. See [XU's wiki page](https://ftb.gamepedia.com/Extra_Utilities_2) for details on GP.

## Draconic Evolution - Advanced Dislocator ##

Also not new, but very useful. It's a handheld device, fueled by Ender Pearls, that allows you to bookmark multiple locations (interdimensional too!) and teleport to them at the cost of one Ender Pearl per teleport.

## Thermal Expansion - Viaducts ##

Impractical by and large, but fun for intra-base transport. [Whee!](https://i.imgur.com/EEn3kNe.gifv)

# 8. Tools #

## Actually Additions - Drill ##

Actually Additions' drill is a highly versatile mining tool that runs off of RF. It mines pickaxe/shovel blocks at a high speed (even higher with upgrades). It has a modular upgrade system which allows for hot-swapping out of the following upgrades (augments) which increase RF usage:

* Speed 1, 2, 3
* Silk Touch
* Fortune 1, 2
* Mining Augment (3x3, 5x5)
* Placing Augment (replaces blocks you mine)

Actually Additions has a very descriptive in-game book. Check it out for details.

## Tinker's Construct - Tool XP ##

Tinker's Construct tools/weapons now amass XP with use and have several milestones, each with increasing XP thresholds. With each level up, you gain an additional modifier slot.

## [Psi](https://psi.vazkii.us/) ##

Psi is an extremely powerful (and cheap) mod. It allows you to program custom spells that can do anything from conjuring a bridge out of thin air to giving your closest enemy a Wither debuff. See the link for more information. The in-game walkthrough is also very in-depth.