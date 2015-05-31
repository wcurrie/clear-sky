Can systemd launch docker containers?
-------------------------------------

According to [chimercoder]("http://chimeracoder.github.io/docker-without-docker/#30") the following will launch a container:

``$ machinectl pull-dkr chimeracoder/nginx-nspawn --dkr-index-url https://index.docker.io``

This seems to be saying download the image and explode it on disk. The man page seems a little [light on detail]("http://www.freedesktop.org/software/systemd/man/machinectl.html").

Added [Jan 2015]("https://github.com/systemd/systemd/commit/3d7415f43f0fe6a821d7bc4a341ba371e8a30ef3
"). Seems to require ``machinectl --version`` to report 220. Code in [pull-dkr.c]("https://github.com/systemd/systemd/blob/master/src/import/pull-dkr.c")
