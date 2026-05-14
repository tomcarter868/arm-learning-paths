---
title: Understand PAC/BTI and OpenJDK on Google Cloud C4A

weight: 2

layout: "learningpathall"
---

## Understand Google Cloud C4A instances

Google Axion C4A is a family of Arm-based virtual machines (VMs) built on Google's custom Axion processors, which use Arm Neoverse-V2 cores. These VMs deliver high performance and improved energy efficiency for modern cloud workloads, including CI/CD pipelines, microservices, media processing, and general-purpose applications.

For more details, see [Introducing Google Axion Processors, our new Arm-based CPUs](https://cloud.google.com/blog/products/compute/introducing-googles-new-arm-based-cpu).

## Learn about OpenJDK and Armv9 PAC/BTI

OpenJDK is the open-source reference implementation of Java Platform, Standard Edition (Java SE). It provides the core compiler, runtime, and class libraries to build and run Java applications across operating systems and hardware platforms. Most modern Java distributions are based on OpenJDK, with different vendors providing their own builds and support.

Armv9 introduces two key security features: Pointer Authentication (PAC) and Branch Target Identification (BTI). These features make control-flow attacks more difficult.

- **Pointer Authentication (PAC):** Adds a cryptographic signature to return addresses and pointers, which is checked before use. This helps detect tampering, such as return-oriented programming attacks.
- **Branch Target Identification (BTI):** Restricts where indirect branches can land, preventing attackers from jumping into unintended instruction sequences.

Together, PAC and BTI strengthen software defenses at the instruction-set level, especially for modern operating systems, hypervisors, and applications that need improved resistance to memory-corruption exploits.

### How PAC/BTI protects Java applications

PAC and BTI protection in Java applications comes from two layers:

1. **System libraries:** Native code linked into the JVM process—including the C runtime (`libc`), cryptographic libraries, and other shared libraries—can be compiled with PAC/BTI support. When the OS loads these libraries, the kernel enforces BTI landing-pad checks and validates PAC signatures on return addresses. This protects the native portions of the JVM process before any Java bytecode runs.
2. **The JVM itself:** OpenJDK's JIT compiler (C2) generates native machine code at runtime for hot Java methods. When the JVM is built with PAC/BTI support, the JIT emits `PACIASP`/`AUTIASP` instructions to sign and authenticate return addresses in JIT-compiled frames, and marks valid branch targets with `BTI` landing-pad instructions. This extends hardware-enforced control-flow integrity into the dynamically generated code that runs your Java application.

A fully protected deployment requires both system libraries compiled with PAC/BTI and a JVM binary built with PAC/BTI enabled. You can verify both conditions on a running JVM, which is what the next steps of this Learning Path cover.

## What you've learned and what's next

You now understand the basics of Google Cloud C4A, OpenJDK, and Armv9 PAC/BTI features.

Next, you'll create an Arm-based Google Cloud VM, install OpenJDK, and validate PAC/BTI readiness in the installed JVM.
