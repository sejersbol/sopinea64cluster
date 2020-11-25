I have lately (2020) started to look into Kubernetes and also took an online course, and I decided that I wanted to experiment with building a Kubernetes cluster. So I started looking at running a Kubernetes cluster on cloud resources from AWS, Google Cloud, Digital Ocean, or other cloud providers. If you go down that road, you will quickly realize that running a Kubernetes cluster with a few nodes will make you endure a substantial monthly cost. As this would merely be a side project for me, it would annoy me that I had to shut down the cluster to save some dollars every time I had finished experimenting with it.

Because of this, I started to look at potential DIY hardware alternatives that I could have running right here in my home office, without worrying about remembering to shut down the cluster after use. I also thought that I might learn a thing or two from building a hardware cluster for Kubernetes.

I have created this page to keep track of my project progress and document my findings along the way. I will update this page as I advance with the project.


## Choice of Hardware

As you have probably noticed from the title of this page, I decided to build my cluster of ARM-based single-board computers (SBCs) from [Pine64](https://pine64.com). At first, it was not obvious to me that the Pine64 modules would provide a viable solution, and I also investigated the possibility of using Raspberry Pi's for the cluster. However, when I read the post [Build your own Kubernetes cluster with 6 Pine64s for less than 400€](https://itnext.io/create-a-kubernetes-cluster-with-pine64-428fc62d72e7) by Ralf Strobel I decided to look more into the possibility of using Pine64 modules for the cluster.
