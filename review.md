# Review

## Info

Reviewer Name: Zhaocheng Huang

Paper Title: When Virtual Is Better Than Real

## Summary

### Problem and why we care

Virtualization enhances security and mobility.

### Gap in current approaches

Putting watchdog services in OS is less secure, because the attack surface os OS is large. Migrating an application to another machine can be difficult, because it has dependencies on the OS.

### Hypothesis, Key Idea, or Main Claim

VMM can increase security and portability. Security is enhanced because VMM is smaller than an OS and less vulnerable to attack. Portability is enhanced because the whold VM is migrated, users don't need to deal with the dependencies between application and OS.

### Method for Proving the Claim

The author stated how to use VMM's characteristics of small interface to achieve the goals.

### Method for evaluating

N/A

### Contributions: what we take away

Relocating apps and OSes to VM increases security and portability.

## Pros (3-6 bullets)

- Easier to verify the code and trust

- Less likely to have vulnerbilities

- Extra layer of protection between OS and VMM, harder to seize VMM than OS

- Easier to migrate, less modification

## Cons (3-6 bullets)

- Performance overhead

- Levels above are affected if it goes wrong

- Space overhead

### What is your analysis of the proposed?

I think the author's statements make sense for scenarios that requires audit, security and portability. But virtual machines bring overhead, so we need other solutions for other scenarios.

## Details Comments, Observations, Questions

How well can other virtualization approaches work on these three areas?

Others use cases of VM?

Compare VM and hardware approach of secure logging, Intrusion prevention and detection

Is putting every feature of secure logging in VMM a good idea?

What level of portability do we need?