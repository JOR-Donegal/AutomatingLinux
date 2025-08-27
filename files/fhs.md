---
description: File System Hierarchy Standard
---

# FHS

Long, long ago, folks in the Linux Foundation decided to standardise on File System layouts. Where you need applications to run, they need to know what folders they should be using, where things should be kept. The standard was generally agreed and Linux, BSD, OS-X all tend to conform to this.

The agreement is called the _Filesystem Hierarchy Standard_ \[1].

Its very old and in reality, most distros do have non-conformities. And some of the layouts are confusing. For example, there two locations for sbin.

/sbin; for essential system libraries.

/usr/sbin; for non-essential system libraries.

Some distro providers think this is nonsense and combine them. Try checking this in CentOS and Ubuntu. What is their status? One of them may be links!

And like everything else in computing, this information is only accurate when it was written.

<table data-header-hidden><thead><tr><th width="148"></th><th width="146"></th><th></th></tr></thead><tbody><tr><td><strong>Directory</strong></td><td><p><strong>Application</strong></p><p><strong>Binaries</strong></p></td><td><strong>Description</strong></td></tr><tr><td>/bin</td><td>Yes</td><td>Essential command line utilities for all users</td></tr><tr><td>/usr</td><td>Yes</td><td><p>Should be mounted read-only; not implemented!</p><p>Binaries intended to be shared between users. On desktop machines, everything gets dumped in here!</p></td></tr><tr><td>/sbin</td><td>Yes</td><td>System binaries, needed to boot up</td></tr><tr><td>/usr/sbin</td><td>Yes</td><td>The rest of the system commands (the ones that are none essential)</td></tr><tr><td>/opt</td><td>Yes</td><td>Optional applications (mostly user applications, may be empty)</td></tr><tr><td>/boot</td><td> </td><td><p>Almost always a separate partition, holds the kernel, bootloader, etc</p><p>This may be mounted read-only.</p></td></tr><tr><td>/dev</td><td> </td><td>All the devices. In Linux, every device is represented as a device file</td></tr><tr><td>/etc</td><td> </td><td>Configuration files, almost all text files</td></tr><tr><td>/home</td><td> </td><td>Users home folders, on a busy system, this will be a separate partition</td></tr><tr><td>/lib</td><td> </td><td>32-bit shared system libraries</td></tr><tr><td>/lib64</td><td> </td><td>64-bit shared system libraries</td></tr><tr><td>/mnt</td><td> </td><td>Optional, used for mounting CDs, DVDs, etc.</td></tr><tr><td>/run</td><td> </td><td>Optional, used for mounting CDs, DVDs, etc. (not in FHS!!)</td></tr><tr><td>/proc</td><td> </td><td>A virtual file system. Every process is represented as a file here. The numbers are all process IDs</td></tr><tr><td>/sys</td><td> </td><td>A virtual file system. Everything about the system</td></tr><tr><td>/var</td><td> </td><td>Various! Log files, print spooler, etc. Temporary stuff which is not critical to the operating system.</td></tr></tbody></table>

\[1] http://www.pathname.com/fhs/
