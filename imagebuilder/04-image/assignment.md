---
slug: image
id: xodrmeueh9af
type: challenge
title: Create an image.
tabs:
- title: Terminal
  type: terminal
  hostname: rhel
- title: RHEL Web Console
  type: external
  url: https://rhel.${_SANDBOX_ID}.instruqt.io:9090
difficulty: basic
timelimit: 1
---
## Building an Image

You are now ready to build your first image of this new Red Hat Enterprise
Linux build with Node.js and NGINX packages installed.  Click the *Create image* button near the top of the interface.

![Create image](../assets/Create-Image.png)

The resulting dialog will ask several questions about how to build the image.
The first, and most important question is *Type*.  There are several different
output types supported by Image Builder:
* Amazon Web Services (.raw)
* OpenStack (.qcow2)
* QEMU Image (.qcow2)
* RHEL for Edge Commit (.tar)
* RHEL for Edge Container (.tar)
* RHEL for Edge Installer (.iso)
* Disk Archive (.tar)
* Microsoft Azure (.vhd)
* VMware VSphere (.vmdk)

For this lab, select the *Type* as __QEMU Image (.qcow2)__ this makes a
virtual machine image that is compatible with the native virtualization
provided as part of Red Hat Enterprise Linux. However, you can see from the
list that you can make images for cloud providers or other virtualization
hypervisors.

![Selecting a format](../assets/image-create.png)

Once you have specified the __QEMU Image (.qcow2)__ as the *Type* select
the *Create* button to create an image of this output format.

Click `Next`.

We'll enter a hostname `node-app-server` for the image.

![hostname](../assets/hostname.png)

Click `Next` until you reach Packages.

Add in the first package, `nodejs`, into the `Available packages` search bar. Once the filter has been applied, you should now see packages with `nodejs` included in their name.

![add nodejs](../assets/add-nodejs.png)

1) Click on `nodejs`.
2) Click the `>` symbol to add it.

Repeat these actions for the `nginx` package and then click `Next`.

![added](../assets/packages-added.png)

You can review the blueprint you've created in this menu. Click `Save blueprint`

![save blueprint](../assets/save-image.png)

Now click `Create image`.

![create image](../assets/create-image-new.png)

To view the progress of the image build, click on the `blueprint` name `node-app-server`.

![blueprint name](../assets/blueprint-name.png)

Click on `Images`.

![images](../assets/click-images.png)

Then you'll be taken to the status of the image build.

![status](../assets/image-build-status.png)

When the image build is complete, you can download the image by clicking on the kebab icon and `Download`.

![download](../assets/download.png)

That completes this lab.
