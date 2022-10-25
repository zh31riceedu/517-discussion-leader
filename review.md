# Review

## Info

Reviewer Name: Zhaocheng Huang

Paper Title: When Virtual Is Better Than Real

## Summary

### Problem and why we care

We want a better structure to help us with secure logging, intrusion prevention and detection and environment migration. Secure logging, intrusion prevention and detection are important because they can help us prevent or detect an attack before or after it happens. And we want a more secure structure where the processes can keep working even if the guest OS is compromised. Environment migration is important because we want less change and configure to our application when we are switching to another machine.

### Gap in current approaches

Putting services for secure logging, intrusion prevention and detection in OS is less secure, because the attack surface os OS is large, and the processes will be affected when the OS is compromised. For example, the attacker can delete the logs after invading the system, making the secure logging useless. 

Migrating an application to another machine can be difficult, because it has dependencies on the OS. User needs to rewrite or reconfigure the application, and the amount of work depends on how many dependencies the application has on the OS, which can be very large.

### Hypothesis, Key Idea, or Main Claim

VMM can increase security and portability. Security is enhanced because VMM is smaller than an OS and less vulnerable to attack. Even if the OS is compromised, the monitoring services are unaffected as long as the small interface between OS and VMM is secure.

Portability is enhanced because the whold VM is migrated, users don't need to deal with the dependencies between application and OS. User only needs to care about the small interface between OS and VMM, and very few changes are needed to make.

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

https://docs.google.com/presentation/d/18AfxrwLjk59qoTxsSIRxsxNiR4opkL59bkQn6qj9j2w/edit?usp=sharing