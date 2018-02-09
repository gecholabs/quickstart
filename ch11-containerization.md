# Containers and Virtual Machines

I’m really into containers and VMs … Why? What the? How?

Why?

I wrote my dissertation with a specific set of tools and libraries. Five years later, when I finally wanted to publish the last chapter, I could barely run the scripts. The setup time was a massive obstacle to make a quick revision. It got me wondering, what if I’d had a perfect snapshot of that environment, a version of R and the Gibbs sampler \(JAGS\) I was using, frozen in time. So I’d just need to spin it up make a tweak and go. Indeed a new release had been issued which broke other dependencies and ultimately gave different results. Hmmm, reproducible science much?

Virtual Machines \(VMs\) allow you to freeze an environment. You can stick them on a USB and spin them up later. These also work great for teaching workshops or running hackathons.; however, they take up masses of space and can be flakey.

Containers are like the ingredients for a VM but can be run on demand. There is less space, they don’t consume compute resources when not in use, and you can find VMs already entirely setup for data science.

Docker is an excellent example

[https://www.docker.com/what-docker](https://www.docker.com/what-docker)

This resource from Jupyter has fully configured environments for data science. Fully opinionated, just like this UG.

[https://github.com/jupyter/docker-stacks](https://github.com/jupyter/docker-stacks)

The “data science” notebook has just about everything you need: Python, R, Julia.

![](/assets/image8.png)

