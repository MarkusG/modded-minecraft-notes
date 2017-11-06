# Applied Energistics 2
Applied Energistics 2 is a mod based around the manipulation of items. It allows you to create expansive storage networks, automatically import/export items out of networks, automatically craft items, and manage structures in space. It also allows you to create tunnels for items, fluids, redstone, light, various types of power, and ME Channels (more on that later).

I won't cover any crafting in this guide as most recipes are available via JEI. If you get lost at any point, [AE's website](http://ae-mod.info/) should provide all the help you need.

# Basic Network
Your first AE network will look a little like [this](https://i.imgur.com/V6Hpr9S.png). It consists of an Energy Acceptor, an ME Drive, a Terminal, and a piece of cable. Terminals must be attached directly to non-dense cables. This network can support up to 8 channels.

## Essential Items
For more details on these items or for a complete list of items, see AE's website.

* [Energy Acceptor](http://ae-mod.info/Energy-Acceptor/) - Allows the input of external power into the network
* [ME Drive](http://ae-mod.info/ME-Drive/) - Contains 10 Storage Cells used to store items
* Terminals
    * [ME Terminal](http://ae-mod.info/ME-Terminal/) - Allows deposit and withdrawal of items
    * [ME Crafting Terminal](http://ae-mod.info/ME-Crafting-Terminal/) - Allows for deposit and withdrawal of items as well as a crafting table that can access network items
* [ME Glass Cable](http://ae-mod.info/ME-Glass-Cable/) - Connects network devices together

## Channels
An AE network without a controller (also called an [Ad Hoc network](http://ae-mod.info/Ad-Hoc-Networks/)) can only support 8 channels. Any device that requires more than power from the network requires a channel to operate.

When you get to a point at which you require more than 8 channels in your network, an [ME Controller](http://ae-mod.info/ME-Controller/) is required. ME Controllers output 32 channels on each side and can be constructed as multiblocks. [Dense Cables](http://ae-mod.info/ME-Dense-Cable/) can carry 32 channels compared to the 8 carried by normal cables.

Channels are allocated to devices on a nearest-first basis. This means that having more than 32 devices on one dense cable (or more than 8 devices on one non-dense cable) will not invalidate the entire cable, but prevent the devices furthest from the controller from functioning. See [AE's website](http://ae-mod.info/Channels/) for more information and diagrams describing this concept.

# Auto-Crafting
AE2 provides a system to automatically craft using items stored in the network. The relevant items for auto-crafting are listed below:
* [Crafting CPU](http://ae-mod.info/1k-Crafting-Storage/) - Provide temporary storage for crafting components (analagous to RAM in a computer) (can be constructed with Co-Processing Units as a multiblock)
* [Crafting Co-Processing Unit](http://ae-mod.info/Crafting-Co-Processing-Unit/) - Allows for faster crafting via parallel operations (multiple machines on one interface or multiple interfaces)
* [ME Interface](http://ae-mod.info/ME-Interface/) - "Links" your network to crafting machines (can also input/output items, but that's mostly irrelevant to auto-crafting)
* [ME Pattern Terminal](http://ae-mod.info/ME-Pattern-Terminal/) - Allows for the encoding of patterns and crafting using only network items
* [ME Interface Terminal](http://ae-mod.info/ME-Interface-Terminal/) - Allows for the management of all interfaces selected to show on the network
* [Molecular Assembler](http://ae-mod.info/Molecular-Assembler/) - Auto-crafting machine

Auto-crafting requires a CPU of adequate size for your crafting job and an Interface containing an encoded pattern for the desired item and adjacent to a Molecular Assembler. At that point, the item should appear in any deposit/withdrawal terminal with the word "Craft" where the item count would be. Click it to begin placing a crafting order (if the item is already present in the system, you can mouse over the item and press Alt to place a crafting order). The ordering process is fairly simple. Select the amount of items you want and the desired CPU (or leave it on the default "Automatic"), then click "Start".

## The Process of Auto-Crafting
After the crafting order is placed, the components will be instantly moved from the network's storage devices into the selected CPU. The CPU will then begin moving the components into the available Molecular Assemblers through their interfaces (speed is determined by the number of Craftin Co-Processing Units). The Molecular Assemblers will craft the items and deposit the products back into the network. The CPU will be unavailable until all items have been moved out of the CPU (or the job is canceled).

You can view ongoing jobs through either a deposit/withdrawal terminal (click the hammer in the very top-right corner) or by clicking on the CPU itself.

## Auto-Processing
A Molecular Assembler can be replaced with the appropriate processing machine to process items rather than craft them (e.g. Iron Ore -> Iron Ingots in an Alloy Smelter from Ender IO). Instead of Crafting Patterns, the interface should contain a Processing Pattern, which is also encoded in a Pattern Terminal. To switch between crafting/processing pattern modes, click the Crafting Table or Furnace in the top-right corner of the crafting section (directly under the scroll bar of the item section). It should be noted that processing machines have to be set to receive and deposit items from and to the network. This can be achieved by either piping the items back into the interface or by using machines supporting push/pull sides. Also, machines cannot receive items from interfaces through pipes. They must be adjacent to the interface.

### A note on CPU multiblocks
Each CPU multiblock counts as one CPU, and multiblocks must be solid rectangular prisms. 3 adjacent 1k CPU blocks will register on the network as one CPU with 3072 bytes available, and only take up one channel.

### Images
* [A basic auto-crafting setup](https://i.imgur.com/U98RInm.png)
* [A Pattern Terminal with an Iron Ingot as an available crafting item (note the hammer and crafting table mentioned earlier)](https://i.imgur.com/TeAwCyt.png)
* [An ME Interface containing the pattern for the Iron Ingot](https://i.imgur.com/LQgkBQf.png)

# Advanced Storage
The [Storage Bus](http://ae-mod.info/ME-Storage-Bus/) can be used to register external inventories as networked storage devices. They can be configured to only handle certain items, as well as whether to only extract items, only insert items, or both. These can be especially useful with Storage Drawer Controllers to network storage of massive amounts of a few types of items, as to not clog up drives. The Storage Bus is also key to creating subnetworks.

## Subnetworks
Imagine 2 networks: Network A, and Network B. Network B contains 6 ME Drives, all of which have Storage Cells in them. Network A has no storage devices. By connecting a Storage Bus on Network A to an interface on Network B, Network A can access all of Network B's items as if it were an inventory. You can chain these subnetworks. Network B can be a parent network to Network C, which contains more drives. This allows for massive amounts of storage, as well as easier management, as you can manage several smaller sub-networks of storage instead of one large network.

### Images
* [A simple subnetwork setup. The blue terminal can access items from both drives. The green terminal can only access items from the rightmost drive. Note the red cable at the back. Power is not transferred over the Storage Bus/Interface, so it must be transferred via cables. Quartz Fiber allows for the transfer of power, but not channels, from one cable to another.](https://i.imgur.com/SfmPTwF.png)
* [A more complex subnetwork setup. Each cluster of drives contains 2 networks: The drives themselves (and a blue cable/terminal) and the management subnetwork (green cables connecting Storage Buses). Each cluster's terminal can only access/manage its associated cluster. The terminals at the front can access/manage all clusters. This setup is infinitely expandable, because you can create subnetworks of several clusters each.](https://i.imgur.com/wx0T2UT.png)

# Automation
AE2 offers solutions for automating processes without the need for any user interaction whatsoever. There's not much to explain in this section, so I'll just include a list of useful items:
* [ME Import Bus](http://ae-mod.info/ME-Import-Bus/) - Imports items from inventories into the network
* [ME Export Bus](http://ae-mod.info/ME-Export-Bus/) - Exports items from the network into inventories
* [ME IO Port](http://ae-mod.info/ME-IO-Port/) - Allows for the transfer of items between the network and storage cells
* [ME Level Emitter](http://ae-mod.info/ME-Level-Emitter/) - Emits a redstone signal based on the amount of an item in the network

# Misc
* [ME Wireless Access Point](http://ae-mod.info/ME-Wireless-Access-Point/) - Allows for wireless access to the network via a [Wireless Terminal](http://ae-mod.info/Wireless-Terminal/)
* [ME Security Terminal](http://ae-mod.info/ME-Security-Terminal/) - Used to restrict access to the network via a permissions system as well as link wireless terminals to the network

# P2P Tunnels
Point-to-point (P2P) tunnels can be used to create a "tunnel" between two points. Use a [Memory Card](http://ae-mod.info/Memory-Card/) to link one P2P Tunnel to another. These tunnels can transfer a variety of things, but in this section I'll focus on their ability to tunnel ME Channels. This ability is very useful because it allows you to effectively "condense" several channels down to two. For instance, you can place 4 P2P tunnels on 4 faces of an ME Controller, hook them all up to one cable, then create a tunnel anywhere else and have access to 128 channels without needing to run 4 dense cables all the way to your destination. P2P Tunnels also support one-to-many connections, meaning that you can access the same face of a Controller from multiple locations.

### Images
* [Using P2P tunnels to tunnel 4 sides of an ME Controller to 4 dense cables](https://i.imgur.com/z84sFAa.jpg)
* [A one-to-many relationship between one side of an ME Controller and 7 dense cables (note that there are still only 32 channels available in total)](https://i.imgur.com/DlXDfn0.png)

# Spatial Storage
TODO: Learn how this works

# [Quantum Network Bridge](http://ae-mod.info/ME-Quantum-Network-Bridge/)
[Creates a way to connect network devices wirelessly across space and other dimensions.](https://i.imgur.com/IlvUZyK.png)

# Miscellaneous
* Priority - Priority can be set by right-clicking on a storage device and clicking on the wrench in the top-right. Devices with a higher priority will receive items first. If two devices have the same priority, the system will prefer the device that already contains one of the item. If both or neither device contains the item, it will be placed in the device closest to the controller.
* Cable Separation - Cables of different colors will not connect to each other, but all cables will connect to Fluix cables. Use cable anchors to prevent cables of the same color from connecting to each other. They also function as ladders if placed above another cable anchor.
* Shift+RClick with an empty Storage Cell in hand to remove the Storage Component from it.
* Use [Cable Facades](http://ae-mod.info/Cable-Facade/) to hide cables and [add a background block to terminals in the world](https://i.imgur.com/Ecvo61r.png).