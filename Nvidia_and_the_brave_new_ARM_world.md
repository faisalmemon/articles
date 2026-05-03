# Nvidia and the brave new (ARM) world

> Faisal Memon 3rd May 2026.

![DGX Spark supercomputer on desk](./dgx_spark.jpg)

I've been working for a while on the topic of sovereign AI. That is, where you have full control of your compute, data, and algorithms. A localised castle to fend off the turbulence of token prices.

What I have been working on is desktop drug discovery. It is known as the protein-ligand problem. This domain has been dominated by cloud provided services running on H100 clusters from Nvidia. That is Hopper GPU on an amd64 CPU. H100 prices have seen a bath tub pricing curve. That is, they started off high, when Hopper was new, dipped down as better technologies emerged, and then jumped back up as the compute crunch came (token apocalypse) forced us to consume any available hardware.

Now with the availability of the DGX Spark, we can have a supercomputer sitting on your desk. The only drawback is that this Grace Blackwell architecture is Grace CPU (ARM) with Blackwell GPU. Not much software has made the amd64 to arm64 leap.

If you have heard of "DLL hell" from the Windows world, you'll know the world of pain I am in.

But I now see the green shoots of recovery. I've been able to port the main set of biotech libraries from H100 clusters onto Grace Blackwell. The next layer up is the application layer; DiffDock (molecular docking). That is where you take a candidate drug (known as a ligand) and see how it would attach to a protein, or not attach depending on where you want a therapeutic change, and where you want to avoid a harmful change.

It is in the early stages of hacking at the moment, over at https://github.com/faisalmemon/DiffDock/tree/faisalm/attempt-0, but I hope to demonstrate drug discovery before the end of the year. It is just a System AI engineering challenge.

Unfortunately I need to send back my DGX Spark (electrical issue) but I might take a crack at Apple with Metal GPU acceleration in the intervening month.

The take home message from the trenches is that local AI compute is real, will only get more important, and over time will reach the "good enough" bar for most practical purposes. Almost any modern car has more than enough performance for our transportation needs, and the same will apply for AI appliances in the home, or at work.

## Copyright

<p xmlns:cc="http://creativecommons.org/ns#" xmlns:dct="http://purl.org/dc/terms/"><a property="dct:title" rel="cc:attributionURL" href="https://github.com/faisalmemon/articles/blob/main/Nvidia_and_the_brave_new_ARM_world.md">Nvidia and the brave new (ARM) world</a> by <span property="cc:attributionName">Faisal Memon</span> is licensed under <a href="https://creativecommons.org/licenses/by/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">CC BY 4.0<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1" alt=""><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1" alt=""></a></p>
