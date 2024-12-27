# Collective

## Concepts / Acronym

* Software Stack
  * NCCL > OFI-NCCL-Plugin > Libfabric > EFA
* MPI - Message Passing Interface MPICH / OpenMPI MPI Communications
  * MPI Datatypes/primitives MPI Barrier function
* EFA - released in 2018, < 15 micro second latency , 100Gbps&#x20;
  * another PCI device, bypass OS. EFA Kernel module
  * SRD - Scalable Reliable Datagram protocol(Annapurna team in Isreal), inspired by Infiniband Reliable Datagram(< 10 micro latency)
    * TCP: Loss based congestion control&#x20;
    * SRD: Dynamic throttling&#x20;
  * Constraints
    * Subnet-local communication&#x20;
    * both allow all traffic within security group&#x20;
    * 1 EFA ENI per instance
* OFI - OpenFabric Interfaces&#x20;
  * Tensor / TensorFlow, PyTorch Libfabric - open source user-space library, hardware agnostic
* OFI-NCCL plugin before OFI-NCCL, NCCL can only use socket or InfiniBand. when it came to AWS, it was using TCP. 2X training time
* GPU Direct RDMA&#x20;
* AWS Launch Template: can be used in multiple services&#x20;
* RxR: libfabrics interface over RDM&#x20;
  * does all the MPI things, ordering
* DDP - Distributed Data ParallelFSDP - Fully Sharded Data Parallel

## Appendix

* [https://en.wikipedia.org/wiki/Collective\_operation](https://en.wikipedia.org/wiki/Collective_operation)
* [https://www.youtube.com/watch?v=CcqpPAscMog](https://www.youtube.com/watch?v=CcqpPAscMog)
* [https://www.youtube.com/watch?v=PDuq1-ERIfM](https://www.youtube.com/watch?v=PDuq1-ERIfM), [https://www.youtube.com/watch?v=GjbsCzYwh24](https://www.youtube.com/watch?v=GjbsCzYwh24)
* [https://github.com/aws/aws-ofi-nccl](https://github.com/aws/aws-ofi-nccl) - The aws-ofi-nccl plugin maps NCCL's connection-oriented transport APIs to Libfabric's connection-less reliable interface. This enables you to use Libfabric as a network provider while running NCCL-based applications\


##
