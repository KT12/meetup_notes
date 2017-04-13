### Paul Burt - CoreOS
Talk given at How [Big Data Impacts Startups](https://www.meetup.com/NYDataScientists/events/238912944/)

Container is a TAR file + Cgroups, Chroot, Unshare, Nsenter, Bind mounts
Containers have been around since 80's, but popular now.  can restrict waht they do to system.  Similar to VM, but share resources naturally.

Why use them?
Hell is other dev's envs
Allow you to zip up what you need to run and keep them together
Don't get crazy conflicts (we should all be using Py3)
Less time wasted on silly things that are difficult to track down
Containers are more efficient to bin pack
Isolation, security are also benefits

`docker run -p 8088:2015 quay.io/ryanj/metrics-k8s`

Msg queue is where you put data when you're not ready to write to DB
Convenient way to pass info
Recs RabbitMQ
Container + MQ's are great

Result is:
Insured data delivery
Fault tolerance
Easy distro of work

Con is MQ's need to be HA (use a managed service)

Need orchestration to run a lot of containers
kubernetes

Planet Labs has a good talk on data
