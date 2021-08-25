# The Next Generation of High-Performance Computing Community Charter -- Overview

## Purpose

The purpose of this document is to introduce you to, and better define, the Next Generation of High-Performance Computing (HPCng) community, including its community and development goals. This document is a work in progress and feedback, comments, and suggestions are encouraged.

## Background

Modernizing high performance computing (HPC) means making life simpler for users to focus on domain-specific work. Traditional HPC users had the need and burden to be keenly aware of system design in order to utilize and achieve supercomputing results. The complexity and expertise required was enormous, but now is the time to stand on the shoulders of giants. The emerging HPC users need the complexity abstracted, and they need the ability to blend new types of computing with the traditional HPC applications. Now is the time to make HPC easy to use.

HPC is moving from niche use-cases and has grown rapidly in terms of applicability over the last several years. We are seeing large scale, tightly integrated HPC resources beginning to run non-traditional HPC workloads in what we commonly refer to as “the long tail of scientific computing.” As that long tail is growing, it is becoming increasingly common for new applications, use-cases, and science domains to be making use of traditional high-performance computing infrastructures. Additionally, HPC adoption is growing beyond traditional scientific use-cases and into the enterprise through the advent of artificial intelligence training as well as compute and data-driven analytics.

When we refer to HPC today, we no longer are referring only to those tightly coupled parallel Message Passing Interface (MPI) based applications. We are referring to any application, or series of applications, which are designed to run a given workload as fast as the hardware will allow. This usually means that the performance-critical application will utilize a given subsystem of a hardware stack completely, whether that be CPU, memory, storage, network, GPU, PCI, etc. This could be on a single compute node, a massive GPU workhorse, CPU farm, or a tightly coupled parallel processing infrastructure. For the purpose of this charter, HPC inclusively refers to all of these types of workloads as HPC.

While “HPC” is becoming increasingly diverse, the architecture to which it is built has not changed considerably over the past two-and-a half decades. This base architecture, commonly referred to as the “Beowulf” design, is predisposed to being flat, isolated, and discrete, which has imposed difficulties with integration of non-HPC specific capabilities like, orchestration, CI/CD and DevOps integration, security process, accountability, and data management (more information below).

To loosely quote an anonymous venture capitalist:

> There are clearly two parties going on: one in HPC, and one in enterprise.

This divide has been increasingly causing separation as enterprise architectures, like micro-services, containers, orchestration, etc., have been readily innovating over the past decade and creating a lot of opportunities for optimization of development, operations, security, automation, reliability, and scale. But these new capabilities are not easily transcribed into the HPC sector due to misalignments of base architectures, and thus cross-pollination is not occurring. This leads to the replication of technology and a lack of benefit of experience and capabilities for everyone.

HPCng strives to build a community of diverse brilliant people to consider these challenges and work together on solutions.

# Goals
[Goals](Goals.md)

# In the Nature of Open Source
[In the Nature of Open Source](Nature_of_Open_Source.md)

# Challenges
There are some challenges that are already foreseen, and we’re sure more will arise. These
include:  
 - Refining the early messaging (the text in this document)  
 - Getting the word out about what we are doing  
 - Engagement with the community  
 - Balancing the load (it shouldn’t be a small number of people doing all the work)  
 - Infrastructure management  
 - Volunteering  
This is where we will need help, discussions, and volunteers.

# More details
More details on this charter are in three sections:
1. [Community Structure](Community_Structure.md)
2. [Projects Initiatives](Projects_Initiatives.md)
3. [Security Policy](Security_Policy.md)

# Call-To-Action
Join the HPCng community [Slack team](https://join.slack.com/t/hpcng/shared_invite/zt-gy0st6mt-ijgUaSvfdeEOhfXXfIstrQ), join the channels you are interested in being part of,
and introduce yourself to us!