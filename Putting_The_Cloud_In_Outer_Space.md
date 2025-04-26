# Putting The Cloud In Outer Space

One of the nice things about babies is that wherever you leave them, when you return, they are where you last left them.  Every parent goes through a shock when they start to crawl (potentially the stairs) and are no longer where you last left them.

In the old days, computers were pretty much wherever you last placed them.  Depending on how grey your hair is, a computer was a large hunk of metal and plastic and not easily transported.

A corollary here is that where your data and compute is is well known.

Nowadays the default answer for where you place your data and compute is the "cloud".  We should ask, why wasn't this the case right from the beginning?

Hardware capabilities, software functionality and economics have come into play to create a cycle of consolidation, then dis-aggregation, and then back to consolidation.

Skipping over the ancient history of computing to focus on the last cycle, where office-based data centers were switched out for cloud hosting is where we'll start our journey.

When commodity chips, such as the Intel chip, natively were friendly to "virtualization" it meant software could be written to pretend to upper layers of the software stack that you were running
on your own computer despite the fact you were actually sharing the hardware with someone else.  The same idea spread to network interfaces and graphical processing units in time.

Furthermore the base level capabilities improved.  In the prior generation if you had an application that needed fast writes to big data stores, you'd need to custom order your server computer
and stuff it with IO boards so you could hook up your storage devices.  If you instead had an application that did a lot of network related work, you'd configure your custom computer
differently, preferring network boards over IO boards.  With modern hardware, a generally capable computer could be a standard configuration suitable for many application needs.

This meant that with only a small number of physical hardware configurations, almost all applications could nicely be hosted.  You just needed a big configuration general purpose computer and
the facility of virtualization meant each customer could carve out the preferred sized slice of cake available.

High speed networking meant there was no problems the hosting provider being far from you.  The real distance is the time taken to reach your customers of the application.  For consumer
facing applications the cloud offers content delivery networks, basically replicating often asked for information on the edges of the network near the customer.  So that's an additional win for
using the cloud.

Things have been going well, but there is trouble brewing.  We need to circle back again onto hardware capabilities, and software functionality.

You know you are in trouble when a standard cookie cutter build out of yet another data center is scrapped half way through and you need to start again.  This happened to a large social media company just
recently cira 2024.  Why?

When Rap music came out, it didn't obsolete Country & Western music.  The world just got richer in its multiplicity of tastes.

The modern apps are AI-driven and these come with their own sound track.  This is a technology stack that sits on fast data coordination of highly parallelized matrix mathematics across multiple GPUs.

Now there is a massive ramp up of power needs, and cooling needs.  Air cooling is not enough, we need water cooled systems.  Those require their own support systems and infrastructure.

The power demands are such that a large AI-focused data center has its own electrical substation stepping down the voltage from the grid to feed the air conditioning systems and the computer systems.
Depending on the design, sometimes huge water sources are also needed.

Power efficiency has become king.  When you deal with huge power, exacting efficiency is needed to minimise the overhead costs.  Every data center needs a custom set of electrical transformers to operate
with efficiency.  Think of it as a tailor made suit, one year in the craft of making and fitting.

If we think of the output of AI as tokens (consider them word fragments, so say 3 tokens per word), then the equation is cost of electricity (and water) going in, for producing a token going out.

That is the cost of intelligence.  Your per token cost.

We are at a stage where the limiting factor is how easy would it be to setup up a gas powered electrical generator, and order the right transformers to feed my AI chips.  Then getting hold of the said chips is the second problem.

Software is still part of the story.  Orchestrating >100, 000 GPUs is its own complex software dance and those that optimise here and elsewhere have a competitive advantage.

It might seem that we are heading for a predictable future where all you need to do is to work out how to generate cheap electricity, and the cost of intelligence is a mere spreadsheet calculation away.

But here things can get weird.  We need to go back to first principles.

Where is the best place for a human to live?  Well we need oxygen, water, a stable environment.  Hopefully somewhere sunny but not too hot.

If we look at the population distribution of the world, people tend to live near water and prefer the comfortable climates - where wearing a T-shirt is possible at least some time during the year.

Where is the best place for AI to live?

Well, we need a good reliable source of energy.  Maybe we need water.  But most of all it can't be too hot.  We need data channels (in bound and out bound).  We need stability.  Oxygen is not needed.  T-shirts are not needed, but electrical parts need their own shielding.

As the title of this article alludes, outer space?

Putting a data center in space has its allure.  The Sun is five times stronger in space.  Solar panels work well.  They need some shielding, as do electronics, but that is a solved problem.
Data communication is now possible since the internet reaches into space via StarLink.  Cooling is not a problem because outer space is cold.  Well nearly.

If you face the Sun in orbit, you can heat up to say +125 degrees Celcius, 257 degrees Fahrenheit.  But you have lots of energy to hand.
If you are in the shade from the Sun, your temperature dips significantly, but your cooling needs also drop.
In a way a kind of stability can be achieved.

Already AI data farms (data centers) are so big, the working assumption is that a percentage of the components, namely GPUs, will be faulty.  You just use software to route around that.  It is not worth
interrupting processing to cure those issues.  You just need the coherence of the whole to be good.  So having computers in space, far from human hands is not a maintenance problem.

There is an economic cross roads we face.  As the per kg payload launch costs come down due to re-usable rocket technology (SpaceX Starship), the inherent trade-off is the cost of fuel to escape earth gravity per kg of payload versus the value in tokens produced by that kg of electronics over its lifetime (say 5 years).

This hypothesis is currently being tested but it seems the numbers do add up.

But it leads us to an uncomfortable philosophical question.  Is AI, in particular strong AI, destined for Outer Space?  Is that its natural home?  A self-sustaining AI in space no longer
constrained by Earth bound resources.  Where would it lead in the limit?  God?

<p xmlns:cc="http://creativecommons.org/ns#" xmlns:dct="http://purl.org/dc/terms/"><a property="dct:title" rel="cc:attributionURL" href="https://github.com/faisalmemon/articles/blob/main/Putting_The_Cloud_In_Outer_Space.md">Putting The Cloud In Outer Space</a> by <span property="cc:attributionName">Faisal Memon</span> is licensed under <a href="https://creativecommons.org/licenses/by/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">CC BY 4.0<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1" alt=""><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1" alt=""></a></p>
