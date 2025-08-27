# Files

Early PC operating system were “disk operating systems”, that is where the term DOS comes from. The requirement in these early systems was to allow a user to easily access programs and data on floppy disks. For security reasons, to prevent users deleting files, there was a read-only flag which could be set. Depending on the early OS, there were flags like “hidden”, so that the file did not appear in directory listings, or archive, to mark a file which had been backed up.

These are probably the simplest type of file permission.

Long before this, in the early 1960s, the first multi-process time sharing systems began to emerge and the need for file permissions arose. The Compatible Time-Sharing System (CTSS) was developed at MIT; each user had their own directory and there were certain permissions or modes. Unix borrowed some of these concepts and extended them into what we will call the classic Unix permissions model. It is a very simple model with little granularity.

Computing was very heterogenous in the 1960s and 1970s and the wheel was reinvented many times in many different shapes! Vendors developed unique solutions which were not interoperable. To overcome this, the IEEE established the POSIX standard \[1]. This introduced far more [advanced access control](https://www.usenix.org/legacy/publications/library/proceedings/usenix03/tech/freenix03/full_papers/gruenbacher/gruenbacher_html/main.html) to Unix and later, Linux.

Access Control Lists (ACLs) are an old concept and I haven’t found an origin. I can find papers from the 1970s using the term (if anybody finds the origin, please tell me!). With ACLs, each line specifying restriction is an Access Control Entry (ACE) and permissions can be very granular, assigning a trustee specific rights of an object.

There are a few categories of access control list. The most commonly used is the Discretionary Access Control list (DACL), where the end user can set permissions directly. Mandatory Access Control (MAC) is used in highly secure environments and is enforced by policies. There are higher levels of access control, but these are normally only used in military/intelligence environments.

VMS was introduced c. 1977 and was one of the more technically advanced operating systems of its time. One of the novel features was the presence of ACLs integrated with the file system. In the 1990s, when Microsoft considered the mess that was MS-DOS and Windows 95, they decided the solution was a rebuild from scratch. Dave Cutler was a visionary developer, having been responsible for VMS development from c. 1975. Cutler moved to Microsoft and lead the development of their next-generation operating system, Windows NT.  The new file system (NTFS) included all the features of VMS and more, including ACLs.

Some coincidence/conspiracy theories!

In in classic movie, “2001 a Space odyssey”, the evil computer was called HAL. What happens if you take the acronym IBM and do a one-letter shift?

If you worked on VMS and then developed the next operating system and did a one letter shift, what would the options be?  &#x20;

\[1] IEEE Std 1003.1988
