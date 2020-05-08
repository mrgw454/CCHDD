# CCHDD
YA-DOS-0.5a (and up) compatible HDD image for use with the Tandy/Radio Shack Color Computers

As some of you know, I'm a huge fan of Brett Gordon's YA-DOS and Michael Furman's pyDriveWire.  I wanted to create something to share with the community that uses both products.

I've created a Coco compatible hard drive image that contains over 3,000 virtual floppy disks.  All of the disk images are provided by Guillaume Major's excellent TRS-80 Color Computer Archive website.
Included with the hard drive image is a PDF document that contains a listing (index) of all the floppy disk images contained inside the hard drive image.

A teaser video can be found here:

https://www.youtube.com/watch?v=riNy1nA0_GI


In order to use this hard drive image, you will need a copy of the latest version of YA-DOS (0.5a at the time of this document) which has been included in this ZIP file.  In addition, you will need a working installation of pyDriveWire.

The hard drive image itself has been tested on the following Coco platforms:


Real Coco 1, 2 & 3 (pyDriveWire, CoCoSDC (SD card), SuperIDE (Compact Flash card))
----------------------------------------------------------------------------------
This will require flashing YA-DOS to an available flash bank on the CoCoSDC or SuperIDE.  Brett's YA-DOS-0.5a distribution DSK image contains a CoCoSDC compatible flash utility to do this.  If using a SuperIDE, you will need the original utilities disk provided for that device.
In both cases, the YADOS.ROM is the file that will need be flashed.

More information about the CoCoSDC can be found here:  http://cocosdc.blogspot.com/
More information about the SuperIDE can be found here:  https://www.frontiernet.net/~mmarlette/Cloud-9/Hardware/SuperIDE.html


CoCo3FPGA (pyDriveWire or onboard SD card)
------------------------------------------
This will require flashing YA-DOS to one of the CoCo3FPGA's virtual MPI flash banks (specifically SLOT2 @ 0x3fc000).

More information about the CoCo3FPGA can be found here:  http://www.davebiz.com/wiki/CoCo3FPGA
Additional documentation can be found here (requires groups.io account):  https://groups.io/g/CoCo3FPGA/files/Documentation/CoCo3FPGA_4_1.pdf


MAME emulator (pyDriveWire and MAME's internal HD support)
----------------------------------------------------------
As a Coco 3 example, launch MAME using a command line similar to the following:

mame coco3 -ramsize 512K -cart /path/to/yados.rom -ext fdcv11

The current CoCoPi3 distribrution already has a working menu option that supports this hard drive image.

More information about MAME can be found here:  https://docs.mamedev.org/


VCC/OVCC emulator (pyDriveWire and VCC/OVCC's internal HD support)
------------------------------------------------------------------
VCC/OVCC will need to be configured with MPI support.  The Becker module will needed to be added to one of the MPI slots and the YA-DOS ROM will need to be added to another MPI slot.  

More information about VCC can be found here:  https://github.com/VCCE/VCC/releases
More information about OVCC can be found here:  https://github.com/WallyZambotti/OVCC


XRoar
-----
It should be noted that XRoar does support the use of virtual hard drive images, but is currently limited to 256MB in size.  As such, this larger hard drive image will not work (yet) until that limitation has been removed.  I have made a smaller version of this hard drive image and plan to release that soon.

More information about XRoar can be found here:  https://www.6809.org.uk/xroar/



pyDriveWire set up
------------------
Mount the hard drive image (DECBVHD.DSK) in the Disk 0 slot in pyDriveWire
Set HDBDOS translation to FALSE (off)

When your Coco boots with YA-DOS, it should automatically detect the use of pyDriveWire and automount the hard drive image.



YA-DOS, pyDriveWire & The Color Computer Archive
------------------------------------------------


More information about Brett Gordon's YA-DOS can be found in the README.txt inside the yados-0.5a.zip file.
Brett's website for YA-DOS is located here:  https://sites.google.com/site/cocoboot2/ya-dos

More information about Michael Furman's pyDriveWire can be found here:  https://github.com/n6il/pyDriveWire

More information about Guilluame Major's TRS-80 Color Computer archive can be found here:  https://colorcomputerarchive.com/







