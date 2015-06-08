ar vs tar
---------
tar maintains directory structure, while ar just contains a flat set of files

ar was never officially standardized. It can't hold a tree structure of file names (directory hierarchy).

concurrent vs parallel
----------------------

**Concurrency** is the appearance of things happening at the 'same time'. **Parallelism** is actually doing things at the same time. Concurrency is a mental model.

Parallelism is hardware. Parallelism requires the data to be partitioned amongst N workers.

Concurrency is multitasking a single processor. Allow a second job to continue whilst the first is blocked on I/O (from a human or hardware).

Paraphrasing [stackoverflow]("http://stackoverflow.com/questions/1050222/concurrency-vs-parallelism-what-is-the-difference")

public vs private cloud
-----------------------

**Public** is somebody else's hardware. Typically pay-as-you-go. Scale resources (up and down) based on demand. Typically developers don't have access to the Machine/VM/OS. Deploy and configure using published APIs.

**Private** your hardware. Either on your site or somebody else's. Install the hardware, the OS (maybe with a hypervisor). Deploy the apps, maybe within a guest OS and/or container (Eg Docker, LXC, Rocket). Maybe expose some AWS like APIs to internal teams to make this easier.

**Hybrid** analogous to base load power generation with peak/burst generators. You own some hardware but can rent more when required. Maybe have consistent deployment/configuration APIs for both hosting environments.
