# The Next Generation of High-Performance Computing Community Charter -- Project Initiatives

## Purpose
The purpose of this document is to introduce you to, and better define, the Next Generation of High-Performance Computing (HPCng) community, including its community and development goals. This document is a work in progress and feedback, comments, and suggestions are encouraged.

## Research & Development Working Groups
Moving forward, there are many opportunities to further modernize HPC. The subject areas defined below  are starting points to build out a full technical vision and requirements for HPC of the future. . The research areas and needs will grow as the HPCng community expands and evolves. 

### Workflows
HPC has moved beyond just traditional HPC and the “Long Tail of Science” is now swallowing the system. As a result, there is an increasing variety of different kinds of work being done on today’s HPC clusters. For example, there are traditional tightly-coupled parallel jobs, loose coupled parallel jobs, threaded, serial, multiple variants of MPI, services, dependencies, pipelines, dependencies, job arrays, etc.

The next generation of HPC infrastructure must be able to handle these diverse workloads, dependencies, and job and data orchestration to enable both traditional parallel jobs and non-traditional HPC jobs. Users need the ability to define complex workflows and control policies to drive execution of each phase of the workflow.

Status: Active  
Group Lead: Ian Kaneshiro

### Cluster Management and Provisioning
There are multiple ways and options to manage HPC clusters. It is still a challenge to blend HPC workloads and integrate well with enterprise computing environments. The goal of this group is to help modernize cluster management and provisioning for greater flexibility to handle traditional tightly coupled computation as well as emerging models used more in enterprise and A.I. computation.

Status: Active  
Group Lead: Chuck Gilbert

### Orchestration
There are several orchestration systems being widely utilized for enterprise, some of which are also being considered for performance critical workloads (e.g., Kubernetes and Nomad). This group will define the requirements of utilizing orchestration to execute complex workflows. 

Status: Seeking Group Lead  
Group Lead: none

### Container Meta-data and Annotations
Containerization of applications is popular in enterprise. With the introduction of Singularity, containerization has also grown as a mechanism to deploy some HPC applications. Singularity, while popular and widespread in the community, is not the only container system being used. Other container runtimes including Shifter, CharlieCloud, and Sarus, are also utilized. It becomes crucial to ensure that containers provide appropriate information that automation layers need for job placement regardless of the container runtime layer. This group will explore and create the requirements of meta-data and container annotation independent of the container runtime used.

Status: Active  
Group Lead: Garima Kochar

### Public Key Infrastructure
Singularity supports its own key management paradigm and leverages standard HKP (Horowitz Keyserver Protocol), but it needs to be extended to completely support Synchronizing Key Server (SKS) Pools and the Notary container standard currently being developed.

Status: Not Active  
Group Lead: none

### Secrets Management
Encryption of containers is possible with Singularity, and due to its container image format, SIF, when used, can run containers directly from an encrypted format. While this can already be used with Singularity to manage secrets and decryption, it is not well integrated and can not operate well with orchestration systems today like cloud hosted Kubernetes.

Status: Not Active  
Group Lead: none

### CI/CD Integration
Continuous Integration and Continuous Deployment (CI/CD) is a method of automating, accelerating, and testing software from SCM (Source Code Management) to production. Containers are the default portable output format (artifact) from these CI/CD pipelines and are currently being used widely in enterprise deployments.

Integrating this process into HPC workflows can bring similar benefits to HPC environments as well as providing trusted software stacks leveraging cryptographic validation on all workloads that come out of the CI/CD pipeline providing 100% trust and validity.

Status: Not Active  
Group Lead: none

### Hybrid-Location Federated HPC
More and more, people are interested in leveraging additional resources for computing involving multiple systems, on-prem, off-prem, cloud, multi-cloud, etc. We have various capabilities being offered in the cloud (AWS, Azure Batch, Rescale, Ubercloud, Atrio, etc.), but we don’t have a suitable mechanism for making workloads or data hybrid-capable. Data platforms like Globus, RStor, OpenDrives, Wasabi, as well as self-hosted deployments of Ceph and/or Minio could be a suitable backend for global data migration, but we still need a way to tie that directly to the workloads.

Another consideration is that once many locations are involved in handling a single workload, another immediate issue that arises is a common, secure software distribution platform that performs well over a wide area, and scales to very large numbers of nodes. This can be done via a distributed file system (perhaps CVMFS as an option) or a distributed caching system which works in conjunction with the orchestration and workflow engine.

Status: Active  
Group Lead: Luke Wilson

### Reproducibility/Trust
Reproducibility in science is a critical problem to solve so we can have confidence in the software environments that we are running in. While we can’t solve it for the entire stack (e.g. hardware), we can solve it for the software stack. The answer to reproducibility and compliance is trust and assurance.

The ability to tag a workload with a cryptographic signature allows for not only validation but also accountability. Containers, being the basic building block moving forward, allows us to gain strong confidence in the environments we are running within, but we are not completely there yet.

We still need the control surface necessary to manage not only the containers, but also the cryptographic and secure materials needed to guarantee trust.

Note, this is related to the PKI focus area above but offers additional capabilities around computational use cases and controls compliance like FDA and FAA software stack regulations.

Status: Not Active  
Group Lead: none

### Composable Hardware
The HPC of the future will consist of not only complex schedulers, software stacks, and data flows, but many different hardware components, ranging from continuing evolution of CPUs and GPUs to more domain-specific accelerators purpose built to support complex computational workflows. HPC must be able to effectively and dynamically “compose” complex hardware topologies leveraging next generation memory semantic fabrics, such as GenZ and CXL. 


Status: Not Active  
Group Lead: none

### MPI and InfiniBand Container integration
While leveraging MPI through containers has been largely accomplished and MPI is now moving into enterprise workloads like AI training via Horovod, there are a number of areas that can still be further addressed for building, running, and maintaining MPI based containers. Additionally, the libraries and host/kernel dependencies and Application Binary Interfaces (ABI) communication pathways (e.g., OFED) still need to be more universally addressed.

Status: Not Active  
Group Lead: none

### OCP/Hyper-scale
There have been significant advances in the hyper-scale space for very efficient and scalable hardware designs, but almost nobody in HPC is leveraging these capabilities. It is advantageous for HPC to be part of the OCP community, and the hyper-scale “scale-up” architecture is highly advantageous, and can (in theory) be used very well for HPC use-cases.

Status: Not Active  
Group Lead: none

### Service Mesh and Service Discovery
There is much room for improvement in the traditional HPC space for Service Mesh (think Istio and Hashicorp’s Consul) and Service Discovery. These technologies could be adopted/augmented and leveraged to provide container, service information, and intelligence (health, capabilities, address information, etc.) to enhance the capabilities of HPC, allowing for self-healing and scaling, among other uses.

Status: Not Active  
Group Lead: none

### Storage Agnostic Layers
There is a need for HPCng to have a broad support for different storage methodologies and types in order to gain maximum scalability and functionality. Storage considerations for HPC are usually designed for the task at hand, rather than general purpose. HPC 2.0 needs to be able to ingest and consume storage of many disparate types and present them in a way (perhaps using a service mesh) to jobs that are run to match the appropriate storage to its job type. This is sometimes leveraged through job schedulers such as SLURM via `--hint` style options for CPU architectures — this type of design could be implemented for storage as well.

There are many more initiatives that still need to be identified, as well as goals for this community. This is only meant as a starting point and should be fleshed out with time and collaboration. Please add comments to any of the above ideas, or feel free to write your own to the list.

Status: Not Active  
Group Lead: none


