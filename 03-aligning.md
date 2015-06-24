---
layout: page
title: Finding Causative Mutations With A Candidate SNP Approach
subtitle: Aligning Reads To A Reference
minutes: 25
---

> ## Learning Objectives {.objectives}
> * Understanding Alignment
> * Know how to run the correct BWA alignment
> * Understand the SAM/BAM format and relationship

> ## Culture clash {.callout}
> **If you're a bioinformatician** - you may be wondering why I'm not using the words 'mapping' reads here. Well, the geneticists in the crowd have a much older technique called [mapping](reference.html#genetic_mapping) that does something completely different. I have honestly had conversations where it has been insisted that I can't possibly map a read.
>
> **If you're a geneticist** - bioinformaticians claim they can do amazing things with reads, mapping them down to the single read level! Of course they usually just mean they're aligning them to whatever reference sequence they have. 
> 

> ## To Do {.todo}
> Make two read sets, 1 long for bwa mem, one short
> challenge: align. Pick parameters? How do we make them equivalent?
> challenge: merge BAMs, extract SAM.
> challenge: Visualise? Find average depth, get depth stats?
> challenge: Study alignment qualities.