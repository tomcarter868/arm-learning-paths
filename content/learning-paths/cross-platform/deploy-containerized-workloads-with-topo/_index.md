---
title: Deploy containerized workloads to Arm-based Linux targets with Topo
description: Use Topo to detect Arm processor capabilities on a target device, select a compatible container template, and deploy containerized workloads to Arm-based Linux targets over SSH.
weight: 1
layout: "learningpathall"
minutes_to_complete: 30
author: Matt Cossins
skilllevels: Introductory
subjects: Containers and Virtualization
armips:
  - Neoverse
  - Cortex-A
  - Cortex-M
tools_software_languages:
  - Topo
  - Docker
  - SSH
operatingsystems:
  - Linux
  - macOS
  - Windows
further_reading:
  - resource:
      title: Topo repository
      link: https://github.com/arm/topo
      type: documentation
  - resource:
      title: Topo template format
      link: https://github.com/arm/topo-template-format
      type: documentation
  - resource:
      title: Topo releases
      link: https://github.com/arm/topo/releases/latest
      type: website
  - resource:
      title: remoteproc-runtime
      link: https://github.com/arm/remoteproc-runtime
      type: documentation

---

## Introduction

This Learning Path guides you through deploying containerized workloads to Arm-based Linux targets using Topo. You'll learn how to detect Arm processor features, select compatible container templates, and automate deployment over SSH.

## Prerequisites

Before you begin, make sure you have:
- A host machine (x86 or Arm) with Linux, macOS, or Windows
- An Arm-based Linux target accessible over SSH (for example, a Raspberry Pi, AWS Graviton instance, or NXP i.MX 93)
- [Docker](/install-guides/docker/) installed on both host and target
- `lscpu` installed on the target (pre-installed on most Linux distributions)
- Basic familiarity with containers and CLI tools

## Learning objectives

By the end of this Learning Path, you will be able to:
- Install Topo and verify that the host and target environments are ready for deployment
- Run health checks and generate a target description to identify compatible Arm processor features and templates
- Clone a Topo template and deploy a containerized workload to an Arm-based Linux target
- (Optional) Deploy firmware and applications to heterogeneous Cortex-A + Cortex-M devices using remoteproc-runtime

...existing code...



### FIXED, DO NOT MODIFY
# ================================================================================
weight: 1                       # _index.md always has weight of 1 to order correctly
layout: "learningpathall"       # All files under learning paths have this same wrapper
learning_path_main_page: "yes"  # This should be surfaced when looking for related content. Only set for _index.md of learning path content.
---
