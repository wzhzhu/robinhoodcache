# RobinHood: Tail Latency-Aware Caching

RobinHood is a research caching system for application servers in large web services.
A single user request to such an application server results in multiple queries to complex, diverse backend services (databases, recommender systems, ad systems, etc.).

### Key Ideas

RobinHood dynamically partition the cache space between the different backend services and continuously optimizes the partition sizes.

RobinHood's goal is to

  - repartition cache space such as to minimize the request tail latency
  - be compatible with off-the-shelf in-memory caches (such as memcached)
  - to facilitate research into different resource allocation policies and tail latency

### The RobinHood Algorithm and Implementation Details

[Presentation at USENIX OSDI](https://www.usenix.org/conference/osdi18/presentation/berger)

[Paper (PDF)](https://www.usenix.org/system/files/osdi18-berger.pdf). Cite as:

    RobinHood: Tail Latency Aware Caching - Dynamic Reallocation from Cache-Rich to Cache-Poor
    Daniel S. Berger, Benjamin Berg, Timothy Zhu, Siddhartha Sen, Mor Harchol-Balter. 
    USENIX OSDI, October 2018.
