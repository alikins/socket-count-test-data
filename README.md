Overview
========

This is a collection of hardware profile dumps used for
testing subscription-managers hardware detection.

Mostly just a collection of various /proc and /sys
entries for different platforms.

Most of the files here come from the test cases for
util-linux.

util-linux:

>  <ftp://ftp.kernel.org/pub/linux/utils/util-linux/>

>  <https://github.com/karelzak/util-linux>


Copying
=======

The README.license for util-linux states:

> _The /COPYING file (GPLv2+) is the default license for code without an explicitly defined license._

The info dumps don't have an explicititly defined license, so GPLv2+
it is.



Adding More
===========

Using the hwloc-gather-topology script from the 'hwloc'
<http://www.open-mpi.org/projects/hwloc/> project seems
to work well.

util-linux includes some tools to do it as well, but
it needs a source checkout to run. 

Something like:

```
tar -c /proc/cpuinfo /proc/sysinfo /sys/devices/system/cpu /sys/devices/system/node > arch-some-description.tar
```

Should work as well.
