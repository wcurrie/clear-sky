Can systemd launch docker containers?
-------------------------------------

According to [chimercoder]("http://chimeracoder.github.io/docker-without-docker/#30") the following will launch a container:

``$ machinectl pull-dkr chimeracoder/nginx-nspawn --dkr-index-url https://index.docker.io``

This seems to be saying download the image and explode it on disk. The man page seems a little [light on detail]("http://www.freedesktop.org/software/systemd/man/machinectl.html").

Added [Jan 2015]("https://github.com/systemd/systemd/commit/3d7415f43f0fe6a821d7bc4a341ba371e8a30ef3
"). Seems to require ``machinectl --version`` to report 220. Code in [pull-dkr.c]("https://github.com/systemd/systemd/blob/master/src/import/pull-dkr.c").

systemd-nspawn
--------------

Built as tool to test that systemd ran ok in containers ([lwn]("https://lwn.net/Articles/572957/")):

> a tool that does much of what LXC and libvirt LXC do, but is easier to use. It is targeted at "building, testing, debugging, and profiling", not at deployment. systemd-nspawn uses the same kernel APIs that the other two tools use, but is not a competitor to them because it is not targeted at running in a production environment.

libvirt
-------

Software to manage VMs, their storage and networks. Include an API library, a daemon (libvirtd), and a command line utility (virsh). It's not a hypervisor it's a layer to hide the differences between the many hypervisors. [project [FAQ]("http://wiki.libvirt.org/page/FAQ")].
