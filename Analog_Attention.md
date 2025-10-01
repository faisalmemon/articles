# Analog In-Memory Attention

I've been reading a groundbreaking research paper presenting an Analog In-Memory Computing (IMC) architecture with startling claims which, if converted into a product, could fundamentally rework the economic and performance model of Artificial Intelligence. Specifically, the architecture achieves a speedup of $\times 300$ and an energy reduction of $\times 90,000$ compared to the Nvidia RTX 4090 for the attention mechanism alone.

The plucky approach mirrors that of Alan Turing himself many years ago at the beginning of the computer revolution - more on that later!

The proposed architecture targets the most significant bottleneck in Large Language Models (LLMs): the self-attention mechanism, specifically the constant transfer of the Key-Value (KV) cache between High Bandwidth Memory (HBM) and SRAM in GPUs. Loading the KV-cache for attention is a major bottleneck, causing increased energy consumption and latency in LLMs because the energy for data access often exceeds the energy required for computations.

The IMC design is based on emerging charge-based memories called gain cells. These gain cells store token projections in a capacitor and enable parallel analog computation. The architecture performs the core of the attention mechanism—two dot-products, scaling, and the activation function—fully in the analog domain using charge-based integration. This approach achieves up to five orders of magnitude lower energy consumption and up to two orders of magnitude lower latency compared to GPUs when performing the attention computation.

When comparing to specific modern GPUs for the attention mechanism alone, the architecture can lead to a speedup of $\times 7,000$ compared to Nvidia Jetson Nano (an embedded application GPU) and $\times 300$ compared to Nvidia RTX 4090. It can achieve an energy reduction of $\times 40,000$ compared to Jetson Nano and $\times 90,000$ compared to RTX 4090. Since the analog circuits introduce non-idealities like decay and non-linear behavior, the current research relies on circuit modeling and simulation (using the SPICE tool), combined with a unique software-to-hardware methodology to map pre-trained models while maintaining high accuracy, achieving performance comparable to GPT-2.

## Practical Applications and Deployment Potential

The dramatic improvements in speed and energy efficiency provided by this Analog IMC architecture make it highly suitable for deployment in devices with strict power and latency requirements.
The architecture can benefit from OSFET transistors that enable dense 3D integration, offering potential for very compact implementations of large networks. This potential for high energy efficiency and compact size is key to integrating powerful AI into edge devices.
These energy-efficiency gains mark an important step toward ultra-fast, energy-efficient generative AI. This means powerful AI can be brought to the mobile phone handset, or home robot, or other autonomous technology like driver-less cars.

While reading through this work on using physical analog systems (charge-based capacitors) to solve a digital memory problem, I caught a glimpse of the foundational genius in all of this, Alan Turing.

Turing's era faced a similar vexing engineering challenge. When working on the first digital computers, engineers needed to overcome the vast inefficiency of vacuum tubes, which required 17,468 tubes just to store twenty ten-digit numbers on the ENIAC. J. Presper Eckert adapted radar technology to create the mercury delay line, an analog system that used sound waves traveling through liquid mercury to store a series of binary pulses in a permanent loop. This mercury line memory was vastly more efficient, allowing a single tube to store as much data as 550 vacuum tubes.

Alan Turing, working on the UK’s Electronic Delay Storage Automatic Calculator (EDSAC), offered a cheeky twist on this concept. Turing noted to Sir Maurice Wilkes that room-temperature gin had effectively the same essential physical properties as mercury for creating the necessary acoustic delay. Turing jokingly proposed that the EDSAC team could stock up on cocktails instead of requisitioning large quantities of the expensive and poisonous mercury.

Although the EDSAC team actually fitted their computer with thirty-two tanks of mercury, Turing’s anecdote highlights that, both then and now, major leaps in computing efficiency are achieved by moving beyond conventional digital components and leveraging the precise, sometimes non-ideal, physical properties of materials. This new analog approach demonstrates the promise of using volatile, low-power memory for attention-based neural networks, offering a path toward very compact implementations of large networks.
