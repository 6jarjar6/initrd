initial RAM disk (initrd)
===================================

Written 1996 by Werner Almesberger <almesber@lrc.epfl.ch> and
		Hans Lermen <lermen@elserv.ffm.fgan.de>
	
initrd adds the capability to load a RAM disk by the boot loader. This
RAM disk can then be mounted as the root file system and programs can be
run from it. Afterwards, a new root file system can be mounted from a
different device. The previous root (from initrd) is then either moved
to the directory /initrd or it is unmounted.

initrd is mainly designed to allow system startup to occur in two phases,
where the kernel comes up with a minimum set of compiled-in drivers, and
where additional modules are loaded from initrd.
