---
description: Just enough information for scripters!
---

# File System Permissions

Some form of basic file permissions exists consistently in all forms of UNIX, based on a very early draft of the POSIX standard. There are three scopes where permissions were applied: user, group, and others. The owner of a file can be changed using the chown command and the group can be changed using chgrp. Look these commands up and understand how to use them.

Every filesystem object is

* Owned by a user (U) and has permissions that relate specifically to that user.
* Assigned to a group (G) which has specific permissions.
* Accessible by any other (O) user, dependent on specific permissions.

<figure><img src="../.gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure>

Permissions are very simple, read (R), write (W), and execute (X) and in original UNIX systems were represented using octal codes.

<figure><img src="../.gitbook/assets/image (3) (1).png" alt=""><figcaption></figcaption></figure>

When I write a script, I will often give it permissions of **755**. This allows me as the owner to read, write and execute. It allows anyone else to read and execute, but not to change my script!

There is an alternative way to do this using symbolic representation. To add read permission for a group, you could just use the command&#x20;

**chmod g+r&#x20;**_**filename**_

To remove the execute permission for others, you could use the command&#x20;

**chmod o-x&#x20;**_**filename**_

For each permission (R, W, X) and each entity (U, G, O) you can either allocate (+) or remove (-) the specific permission.

From 1997 onwards, more complex ACLs were introduced to Unix via the POSIX standards. I won’t be covering these in this note set.
