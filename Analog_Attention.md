# Analog In-Memory Attention
> Faisal Memon 1st October 2025.

![Analog Electronics solving digital problems](./alan_analog.png)

https://arxiv.org/pdf/2409.19315

An Analog In-Memory Computing (IMC) architecture is poised to fundamentally rework the economic and performance model of Artificial Intelligence. A groundbreaking new research paper presents an architecture with startling claims: a ×300 speedup and a staggering ×90,000 energy reduction compared to the Nvidia RTX 4090 for the crucial attention mechanism alone.

This plucky, boundary-pushing approach mirrors the foundational genius of Alan Turing himself—who, at the dawn of the computer revolution, faced a similar vexing engineering challenge. More on that later!

The proposed architecture targets the most significant bottleneck in Large Language Models (LLMs): the self-attention mechanism. Loading the Key-Value (KV) cache for attention is a major bottleneck because the energy required for data access—constantly shuttling it between High Bandwidth Memory (HBM) and SRAM in GPUs—often exceeds the energy needed for the computations themselves, leading to massive energy consumption and latency.

The IMC design is based on emerging charge-based memories called gain cells. These gain cells store token projections in a capacitor and enable parallel analog computation. The architecture performs the core of the attention mechanism—two dot-products, scaling, and the activation function—fully in the analog domain using charge-based integration. This approach achieves up to five orders of magnitude lower energy consumption and up to two orders of magnitude lower latency compared to GPUs when performing the attention computation.

When comparing to specific modern GPUs for the attention mechanism alone, the architecture can lead to a speedup of ×7,000 compared to Nvidia Jetson Nano (an embedded application GPU) and ×300 compared to Nvidia RTX 4090. It can achieve an energy reduction of ×40,000 compared to Jetson Nano and ×90,000 compared to RTX 4090. Since the analog circuits introduce non-idealities like decay and non-linear behavior, the current research relies on circuit modeling and simulation (using the SPICE tool), combined with a unique software-to-hardware methodology to map pre-trained models while maintaining high accuracy, achieving performance comparable to GPT-2.

## Practical Applications and Deployment Potential

The dramatic improvements in speed and energy efficiency provided by this Analog IMC architecture make it highly suitable for deployment in devices with strict power and latency requirements. The architecture can benefit from OSFET transistors that enable dense 3D integration, offering potential for very compact implementations of large networks. This potential for high energy efficiency and compact size is key to integrating powerful AI into edge devices. These energy-efficiency gains mark an important step toward ultra-fast, energy-efficient generative AI. This means powerful AI can be brought to the mobile phone handset, or home robot, or other autonomous technology like driver-less cars.

## A nod to Alan Turing

While reading through this work on using physical analog systems (charge-based capacitors) to solve a digital memory problem, I caught a glimpse of the foundational genius in all of this, Alan Turing.

Turing's era faced a similar vexing engineering challenge. When working on the first digital computers, engineers needed to overcome the vast inefficiency of vacuum tubes, which required 17,468 tubes just to store twenty ten-digit numbers on the ENIAC. J. Presper Eckert adapted radar technology to create the mercury delay line, an analog system that used sound waves traveling through liquid mercury to store a series of binary pulses in a permanent loop. This mercury line memory was vastly more efficient, allowing a single tube to store as much data as 550 vacuum tubes.

Alan Turing, working on the UK’s Electronic Delay Storage Automatic Calculator (EDSAC), offered a cheeky twist on this concept. Turing noted to Sir Maurice Wilkes that room-temperature gin had effectively the same essential physical properties as mercury for creating the necessary acoustic delay. Turing jokingly proposed that the EDSAC team could stock up on cocktails instead of requisitioning large quantities of the expensive and poisonous mercury.

Although the EDSAC team actually fitted their computer with thirty-two tanks of mercury, Turing’s anecdote highlights that, both then and now, major leaps in computing efficiency are achieved by moving beyond conventional digital components and leveraging the precise, sometimes non-ideal, physical properties of materials. Ultimately, this new analog approach demonstrates the profound, continuous promise of using volatile, low-power physical systems—whether it's the specific acoustic properties of mercury (or gin!) or the precise decay of a charge-based capacitor—to solve massive digital problems, offering a clear path toward ultra-compact and efficient implementations of large neural networks.

## Copyright

<p xmlns:cc="http://creativecommons.org/ns#" xmlns:dct="http://purl.org/dc/terms/"><a property="dct:title" rel="cc:attributionURL" href="https://github.com/faisalmemon/articles/blob/main/Analog_Attention.md">Analog Attention</a> by <span property="cc:attributionName">Faisal Memon</span> is licensed under <a href="https://creativecommons.org/licenses/by/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">CC BY 4.0<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1" alt=""><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1" alt=""></a></p>
