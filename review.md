# Review

## Info

Reviewer Name: Zhiwei Liang

Paper Title: Disco: Running Commodity Operating Systems on Scalable Multiprocessors

## Summary

### Problem and why we care

Scalable multiprocessor hardware often delivered without corresponding operating system and system software that can take the advantage of the advanced hardware. Solving this problem by modifying existing operating system can be complicated and often need much more time.

### Gap in current approaches

1. Current system designs for the shared memory machine require significant OS changes.

2. Current VMM runs on host OS has problems in huge overhead, resource management, and communication among the VMs.


### Hypothesis, Key Idea, or Main Claim

Building a VMM called Disco, as a layer between the hardware and the software. It can establish multiple VMs with current commodity operating systems such as Windows and Unix. This will be a convenient way to take advantage of multiprocessor hardware.

### Method for Proving the Claim

Showing the overhead is minimal, performance is great with multiple optimization and communication techniques.

### Method for evaluating

Running different type of application on multiple VMs with the OS on top of Disco and compare the results with IRIX OS that developed to support the multiprocessor hardware.

### Contributions: what we take away

Providing a better way (multiple VMs on top of Disco) to improve the application performance on the large scale hardware.

## Pros (3-6 bullets)

1. Easy to develop
2. Better performance
3. Don't have to modify current commodity OS

## Cons (3-6 bullets)

1. Overhead still exist
2. Memory miss rate is high for some types of application
3. Need to run application in parallel on different VMs



### What is your analysis of the proposed?

I think it is a great since it remove all unnecessary parts of an OS at the VMM layer and directly provides VM on top of the hardware. But it remains unclear how it is compared with the distributed system that built with multiple physical machine.

## Details Comments, Observations, Questions

It is an interesting idea and could potentially be used in modern cloud infrastructure.

Do we use any similar type of VMM on the cloud? If not, why?

Can we use the technique to support distributed system built by multiple machines instead of a single multiprocessor machine?
