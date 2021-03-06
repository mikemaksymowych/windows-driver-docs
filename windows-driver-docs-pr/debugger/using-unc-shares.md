---
title: Using UNC Shares
description: Using UNC Shares
ms.assetid: 7baf157d-e8c3-4ad5-a56e-58f8983da4d9
---

# Using UNC Shares


The Cv2http.cmd, Cv2http.pl, and Walk (Walk.cmd) scripts are used to provide source files from a simple UNC share. The files Cv2http.cmd and Cv2http.pl extract the SrcSrv stream, modify it using a Perl script, and put the altered stream back in the .pdb file. The syntax is as follows:

```
cv2http.cmd PDB Alias SourceRoot
```

where *PDB* specifies the name of the .pdbfile to modify, *Alias* specifies the logical name to apply to your Web site, and *SourceRoot* specifies the root of the UNC share to which you extracted the source files. Note that the *Alias* parameter is stored in the PDB as a varaible name that can be overridden on the debugger client in Scrsrv.ini, should you ever move the location of the Web site.

This script requires that all the standard SrcSrv tools be available in the path because it calls both SrcTool and PDBStr. Remember that Cv2http.pl is a Perl script and can be modified to meet your needs.

The third file, the Walk (walk.cmd) script, modifies an entire set of .pdb files. For example:

```
walk.cmd *.pdb cv2http.cmd SourceRoot \\server\share
```

The preceding command calls Cv2http.cmd on every .pdb file in a tree, using SourceRoot for the alias and \\\\server\\share for the UNC share. For more details on Walk, see [Extracting Source Files](extracting-source-files.md).

After this command is executed on a tree of .pdb files, they are ready for installation into the Web site or whatever location in which you want to put them. Remember that you can use SrcTool and PDBStr to examine the changes to the .pdb files.

 

 

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20[debugger\debugger]:%20Using%20UNC%20Shares%20%20RELEASE:%20%285/15/2017%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")




