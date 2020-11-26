I have lately (2020) started to look into Kubernetes and also took an online course, and I decided that I wanted to experiment with building a Kubernetes cluster. So I started looking at running a Kubernetes cluster on cloud resources from AWS, Google Cloud, Digital Ocean, or other cloud providers. If you go down that road, you will quickly realize that running a Kubernetes cluster with a few nodes will make you incur a substantial monthly cost. As this would merely be a side project for me, it would annoy me that I had to shut down the cluster to save some dollars every time I had finished experimenting with it.

Because of this, I started to look at potential single-board computer (SBC) hardware alternatives that I could have running right here in my home office, without worrying about remembering to shut down the cluster after use. I also thought that I might learn a thing or two from building a hardware cluster for Kubernetes.

I have created this page to keep track of my project progress and document my findings along the way. I will update this page as I advance with the project.


## Choice of Hardware

As you have probably noticed from the title of this page, I decided to build my cluster of ARM-based SBCs from [Pine64](https://pine64.com). At first, it was not obvious to me that the Pine64 modules would provide a viable solution, and I also investigated the possibility of using Raspberry Pi's for the cluster. However, when I read the post [Build your own Kubernetes cluster with 6 Pine64s for less than 400€](https://itnext.io/create-a-kubernetes-cluster-with-pine64-428fc62d72e7) by Ralf Strobel I decided to look more into the possibility of using Pine64 modules for the cluster.

As Ralf Strobel mentions in his post, the Pine A64 SBC has better specs than the Raspberry Pi 3, but since then a lot has happened and, the Raspberry Pi 4 now easily beats the SBCs build on the Pine A64. BUT the Pine A64 also comes in a compute module called the SOPINE A64 Compute Module, which has the same form factor as a SODIMM-DDR3 module with 2 GB of RAM for only $29. That is not all; for $100 you can buy a Pine64 Clusterboard that fits 7 SOPINE A64 Compute Modules. (All prices are Q3 2020 from the [Pine64 store](https://pine64.com).) The Pine64 Clusterbaord supplies the SOPINE A64 Compute Modules with a backplane that includes Gigabit Ethernet, pinouts, power, USB, and more. That is, you can buy and build a very cheap 7-node cluster without having to wire up 7 SBCs with a switch and several power cords.

To summarize, you could buy Raspberry Pi 4's, a switch, power adapters, and build a more potent hobby cluster, but it could cost you more, and you would also have to mingle with more cables and a complex cabinet build. Did I mention the Pine64 Clusterboard has the mini-ITX form factor that makes it easy to install in a cabinet?

I ordered the Pine64 Clusterboard and 7 SOPINE A64 Compute Modules together with the DC Jack Power Supply. It arrived a few weeks later from China.

![The SOPINE Compute Modules](/assets/images/image-2.jpeg)
