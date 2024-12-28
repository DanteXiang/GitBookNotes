# Collective

## To Learn

* Nvidia Spectrum-X





## Concepts / Acronym

### Software Stack

NCCL > OFI-NCCL-Plugin > Libfabric > EFA

### MPI - Message Passing Interface

* MPICH / OpenMPI&#x20;
* MPI Communications
* MPI Datatypes/primitives
* MPI Barrier function

### EFA

released in 2018, < 15 micro second latency , 100Gbps

another PCI device, bypass OS. EFA Kernel module&#x20;

* SRD - Scalable Reliable Datagram protocol(Annapurna team in Isreal), inspired by Infiniband Reliable Datagram(< 10 micro latency)&#x20;
  * TCP: Loss based congestion control&#x20;
  * SRD: Dynamic throttling&#x20;
* Constraints
  * Subnet-local communication
  * both allow all traffic within security group
  * 1 EFA ENI per instance

### OFI - OpenFabric Interfaces&#x20;

OFI-NCCL plugin before OFI-NCCL, NCCL can only use socket or InfiniBand. when it came to AWS, it was using TCP. 2X training time

* Tensor / TensorFlow, PyTorch Libfabric - open source user-space library, hardware agnostic

### DDP

* Distributed Data Parallel
* Direct Data Placement Protocol

### FSDP - Fully Sharded Data Parallel



### RDMA

* Common RDMA implementations include the [Virtual Interface Architecture](https://en.wikipedia.org/wiki/Virtual_Interface_Architecture), [RDMA over Converged Ethernet](https://en.wikipedia.org/wiki/RDMA_over_Converged_Ethernet) (RoCE), [InfiniBand](https://en.wikipedia.org/wiki/InfiniBand), [Omni-Path](https://en.wikipedia.org/wiki/Omni-Path) and [iWARP](https://en.wikipedia.org/wiki/IWARP).
* GPU Direct RDMA
* InfiniBand < RoCE (RMDA over Converged Ethernet)
  *

      <figure><img src="../.gitbook/assets/SEO-《浅谈RDMA》-配图02 (1).png" alt=""><figcaption></figcaption></figure>
  * Vervbs API

###

### AWS Launch Template: can be used in multiple services&#x20;

### RxR: libfabrics interface over RDM&#x20;

* does all the MPI things, ordering

## Appendix

* [https://en.wikipedia.org/wiki/Collective\_operation](https://en.wikipedia.org/wiki/Collective_operation)
* [https://www.youtube.com/watch?v=CcqpPAscMog](https://www.youtube.com/watch?v=CcqpPAscMog)
* [https://www.youtube.com/watch?v=PDuq1-ERIfM](https://www.youtube.com/watch?v=PDuq1-ERIfM), [https://www.youtube.com/watch?v=GjbsCzYwh24](https://www.youtube.com/watch?v=GjbsCzYwh24)
* [https://github.com/aws/aws-ofi-nccl](https://github.com/aws/aws-ofi-nccl) - The aws-ofi-nccl plugin maps NCCL's connection-oriented transport APIs to Libfabric's connection-less reliable interface. This enables you to use Libfabric as a network provider while running NCCL-based applications\


##
