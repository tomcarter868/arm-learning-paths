---
title: Create a Google Axion C4A virtual machine on Google Cloud
weight: 3

### FIXED, DO NOT MODIFY
layout: learningpathall
---

## Create a Google Axion C4A VM

In this section, you'll provision a Google Axion C4A VM on Google Cloud Platform (GCP) using the `c4a-standard-4` machine type, which provides four vCPUs and 16 GB of memory.

{{% notice Note %}}
For general guidance on setting up a Google Cloud account and project, see the Learning Path [Getting started with Google Cloud Platform](https://learn.arm.com/learning-paths/servers-and-cloud-computing/csp/google).
{{% /notice %}}

### Provision a Google Axion C4A VM in the Google Cloud Console

1. Open the [Google Cloud Console](https://console.cloud.google.com/) and go to **Compute Engine** > **VM instances**.
2. Select **Create instance**. Give the instance a name, and choose your preferred **Region** and **Zone**.
3. Under **Machine configuration**, set the following:
	- **Series:** C4A
	- **Machine type:** c4a-standard-4

![Screenshot of the Google Cloud Console VM creation page showing the C4A series and c4a-standard-4 machine type selected. This confirms you are creating an Arm-based C4A instance.#center](images/gcp-vm.png "Creating a Google Axion C4A VM in the Google Cloud Console")

4. Under **OS and storage**, select **Change** and choose an Arm64-based image. For this Learning Path, select **SUSE Linux Enterprise Server** with the **Pay as you go** license type, then select **Select** to apply.
5. Under **Networking**, enable **Allow HTTP traffic** and **Allow HTTPS traffic**.
6. Select **Create** to launch the VM.

After the instance starts, select **SSH** next to the VM in the instance list to open a browser-based terminal session.

Alternatively, if you have the [gcloud CLI](/install-guides/gcloud/) installed, you can connect from a local terminal using `gcloud`. From the **SSH** drop down, select `View gcloud command` and run that command from your terminal.

![Screenshot of the Google Cloud Console VM instances list showing the SSH button for a running C4A instance. Use SSH to open a terminal session on the new VM.#center](images/gcp-ssh.png "Connecting to a running C4A VM using SSH")

A new browser window opens with a terminal connected to your VM.

![Screenshot of a browser-based terminal window showing a command prompt on a SUSE Linux VM running on Google Axion C4A. Use this terminal to install OpenJDK and run the PAC/BTI validation script.#center](images/gcp-shell.png "Terminal session connected to the VM")

## What you've learned and what's next

In this section, you created a Google Cloud C4A virtual machine and opened an SSH session to the VM. Next, you'll install OpenJDK and run the PAC/BTI validation script.
