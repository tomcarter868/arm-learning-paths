
---
title: Verify OpenJDK PAC/BTI on Google Cloud C4A VMs
description: Validate PAC/BTI support in OpenJDK on a Google Cloud C4A Arm-based VM and interpret JVM security readiness for Armv9 workloads.
minutes_to_complete: 30

who_is_this_for: This Learning Path is for developers who want to validate OpenJDK PAC/BTI support on Google Cloud C4A Arm-based virtual machines.

learning_objectives: 
    - Provision a Google Cloud C4A Arm-based virtual machine with SUSE Linux Enterprise Server.
    - Install OpenJDK on the Arm-based VM.
    - Verify PAC/BTI readiness in the installed JVM runtime.

prerequisites:
    - A [Google Cloud Platform (GCP)](https://cloud.google.com/free) account with billing enabled
    - [gcloud CLI](/install-guides/gcloud/) (optional, for local terminal access)
author: Doug Anson

### Tags
skilllevels: Introductory
subjects:
    - Performance and Architecture
cloud_service_providers:
 - Google Cloud    

armips:
    - Neoverse

tools_software_languages:
    - Java
    - OpenJDK
    - Bash

operatingsystems:
    - Linux

further_reading:
    - resource:
            title: Understand Arm Pointer Authentication
            link: https://learn.arm.com/learning-paths/servers-and-cloud-computing/pac/
            type: website
    - resource:
            title: Google Axion C4A machine series
            link: https://cloud.google.com/compute/docs/general-purpose-machines#c4a_series
            type: documentation
    - resource:
            title: OpenJDK 17 project page
            link: https://openjdk.org/projects/jdk/17/
            type: documentation
    - resource:
            title: Arm A64 instruction set architecture reference
            link: https://developer.arm.com/documentation/100076/latest/
            type: documentation
---

## Introduction

This Learning Path guides you through validating Armv9 Pointer Authentication (PAC) and Branch Target Identification (BTI) support in OpenJDK on a Google Cloud C4A Arm-based virtual machine (VM). You'll learn how to provision a C4A VM, install OpenJDK, and verify that your Java runtime and platform are ready for enhanced security on Arm.

## Prerequisites

- A Google Cloud Platform (GCP) account with billing enabled
- Optionally, the [gcloud CLI](/install-guides/gcloud/) for local terminal access

## Learning objectives

By the end of this Learning Path, you will be able to:

- Provision a Google Cloud C4A Arm-based VM with SUSE Linux Enterprise Server
- Install OpenJDK on the Arm-based VM
- Verify PAC/BTI readiness in the installed JVM runtime

---
...existing code...


### FIXED, DO NOT MODIFY
# ================================================================================
weight: 1                       # _index.md always has weight of 1 to order correctly
layout: "learningpathall"       # All files under learning paths have this same wrapper
learning_path_main_page: "yes"  # This should be surfaced when looking for related content. Only set for _index.md of learning path content.
---