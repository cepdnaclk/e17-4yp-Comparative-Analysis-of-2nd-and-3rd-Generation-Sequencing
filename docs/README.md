---
layout: home
permalink: index.html

# Please update this with your repository name and title
repository-name: e17-4yp-Comparative-Analysis-of-2nd-and-3rd-Generation-Sequencing
title: Comparative Analysis of 2nd and 3rd Generation Sequencing
---

[comment]: # "This is the standard layout for the project, but you can clean this and use your own template"

# Comparative Analysis of 2nd and 3rd Generation Sequencing

#### Team

- E/17/100, Gunathilaka R.M.S.M., [e17100@eng.pdn.ac.lk](mailto:e17100@eng.pdn.ac.lk)
- E/17/240, Pathum T.N.D., [e17240@eng.pdn.ac.lk](mailto:e17240@eng.pdn.ac.lk)
- E/17/246, Perera K.S.D., [e17246@eng.pdn.ac.lk](mailto:e17246@eng.pdn.ac.lk)

#### Supervisors

- Dr. Asitha Bandaranayake, [asithab@eng.pdn.ac.lk](mailto:asithab@eng.pdn.ac.lk)
- Prof. Pradeepa Bandaranayake, [email](mailto:pradeepag@agri.pdn.ac.lk)
- Mr. Hiruna Samarakoon, [email](mailto:hiruna@unsw.edu.au)

#### Table of content

1. [Abstract](#abstract)
2. [Related works](#related-works)
3. [Methodology](#methodology)
4. [Experiment Setup and Implementation](#experiment-setup-and-implementation)
5. [Results and Analysis](#results-and-analysis)
6. [Conclusion](#conclusion)
7. [Publications](#publications)
8. [Links](#links)

---

## Abstract
In this research, a thorough comparison between Illumina (second-generation) and Nanopore (third-generation) DNA sequencing methods was conducted, focusing on tomato and cinnamon genomes. The goal of the research is to determine how these DNA sequencing methods work with different computing resources.  Illumina, which produces shorter DNA reads, completed the assembly process faster, but resulted in a larger number of contigs. This implies that the assembled DNA was in more, smaller fragments. In contrast, Nanopore, known for its longer reads, took longer to assemble the genomes due to the complex process of matching these long sequences. On the other hand, it yielded assemblies with fewer contigs and higher N50 values, indicating more continuous and more accurate genome representations. An important observation from the research was the impact of increased computational resources. Particularly RAM, on the assembly quality and speed for both Illumina and Nanopore. It was noted that while adding more RAM significantly improved assembly outcomes, the benefit diminished beyond a certain point.

For Nanopore sequencing, challenges such as lower base calling pass rates and the need for high read coverage, especially in de-novo assembly, were highlighted. These factors are important in choosing the appropriate sequencing method for genomic studies. Depending on the specific research requirements, these sequencing technologies should be chosen. This research aims to provide results obtained from the 2nd and 3rd generation genome assembly of the Tomatto genome. It highlights how important it is that computational power and the properties of genomic data be considered in genomic research. This study provides information about the potential and constraints of second and third-generation sequencing technologies for genome assembly. 

## Related works
### Introduction
---

The field of bioinformatics has undergone tremendous changes in recent years due to the combination of computer engineering and molecular biology study. This change is mostly due to the advent of two different DNA sequencing technologies: third-generation (Nanopore) and second-generation (Illumina). These techniques have created new opportunities for scientific research because they leverage state-of-the-art computing power. The primary objective of this study is to compare objectively the second-generation (Illumina) and third-generation (Nanopore) DNA sequencing techniques with an emphasis on genome assembly. The aim is to evaluate and compare the effectiveness and caliber of these technologies, and at the same time investigate the impact of computing power on the assembly of the genome.

The introduction of second-generation sequencing, or Next Generation Sequencing (NGS), marked a turning point in genomics research. Known for its rapid sequencing capabilities and cost-effectiveness, NGS has made genomic studies more accessible and comprehensive. Its precision has enhanced the accuracy and reliability of genomic data, leading to a deeper understanding of complex genetic information.

Third-generation sequencing (TGS), or long-read sequencing, emerged as a response to certain limitations of NGS, notably providing longer read lengths for a more complete genomic view. Each of these sequencing technologies, however, presents unique advantages and challenges, influencing their application in genome assembly and analysis.

The core objective of this research is to provide an unbiased comparison of these technologies in terms of their performance in genome assembly and the quality of the assembled genomic data. Additionally, this study aims to explore the influence of varying computational resources on the efficiency and effectiveness of these genome assembly processes.

Drawing from diverse academic sources, this paper seeks to offer a thorough resource for those involved in computer engineering, genomics, and related fields. The comparative analysis aims to clarify the capabilities and limitations of Illumina and Nanopore sequencing technologies in the evolving landscape of genomic research.

### Literature review
---

The emergence of second-generation sequencing technologies, such as the Roche 454 GS Junior (GS Jr), Life Technologies Ion PGM, and Illumina MiSeq, heralded a transformative period in the field of genomic studies. These technologies, with their combination of affordability, efficiency, and high-throughput capabilities, have pushed the boundaries of genetic research and significantly accelerated the understanding of various genomic complexities [1].

At the core of these second-generation platforms is the ability to achieve single-base precision in DNA sequencing. Such unprecedented resolution has provided a clearer picture of the microcosm of life, revealing genetic information on a genome-wide scale with impressive detail and accuracy [2]. This technology not only expanded the readouts from a variety of DNA preparation protocols but also greatly enhanced the scope and quality of genomic information obtained, thereby establishing a firm foundation for subsequent genetic and biological research [2].

Among these second-generation sequencers, Ion PGM, or Ion Torrent platform, has particularly made a significant impact in the scientific community, especially in microbiology. Its high-speed sequencing abilities have redefined scalability and proven to be a powerful tool in time-sensitive studies [3]. With its rapid DNA sequencing capability, Ion PGM has democratized the field of DNA sequencing, placing considerable sequencing capacity into the hands of individual investigators, and hence transforming the landscape of genomic research.

On the other hand, the GS Jr has carved a unique niche for itself within the realm of second-generation platforms, thanks to its relatively longer read lengths. While the other platforms generally produce shorter reads, the GS Jr's reads range from 400 to 800 base pairs. These longer reads have been integral to traditional sequencing projects, providing an unprecedented level of detail in the exploration of the genomic landscape [4]. As the field moves toward faster-re-sequencing approaches, these long-read lengths continue to hold significant value, underpinning the ability to develop new, fast, and economical approaches to re-sequencing [4].

The progression of genomics research has been immensely driven by the arrival of third-generation sequencing technologies, prominently embodied by the Pacific Biosciences RS sequencer (PacBio). This marked evolution from the previous generation of sequencing platforms heralded a significant departure in DNA sequencing by delivering long-read sequencing capabilities [5].

The hallmark feature of third-generation sequencing platforms like PacBio lies in their exceptional ability to read extensive stretches of DNA sequences, sometimes extending up to tens of kilobases, in a single reaction. This remarkable capacity distinguishes third-generation sequencing platforms from their second-generation counterparts and radically enhances the genomic research landscape.

Such long-read sequencing has opened up new avenues for intricate genomic investigations, notably improving the assembly of complex genomic regions. By being able to read long fragments of DNA continuously, PacBio technology allows the reconstruction of larger, more complex genomic segments with significantly reduced gaps. This has led to a more comprehensive and coherent understanding of the genome and its many intricacies.

Moreover, third-generation sequencing technologies have considerably enhanced the identification and characterization of structural variants at the base-pair level. The longer reads provide an extended view of the genomic landscape, making it possible to detect larger structural variants that may be missed by shorter reads. This has led to the discovery of previously unidentified genetic variation, broadening our understanding of genomic diversity. [12]

The realm of genomics research has seen remarkable advancements with the introduction of third-generation sequencing platforms, particularly the Pacific Biosciences RS sequencer (PacBio). One of the compelling illustrations of its superiority over second-generation platforms is presented in a study conducted on the genome of Vibrio Parahaemolyticus, a bacterium characterized by a complex 5-Mb genome composed of two circular chromosomes [6]. When PacBio was juxtaposed against the second-generation sequencing platforms – Roche 454 GS Junior, Life Technologies Ion PGM, and Illumina MiSeq, it was the former's long-read capabilities that set it apart. These capabilities allowed it to generate contigs of greater length, thereby enabling it to reconstruct a larger part of the genome. While the second-generation platforms have undeniably advanced our understanding of genomics, they often stumble upon challenges when dealing with multiple chromosomes and abundant repetitive sequences. Such features, common in complex genomes, can confound the assembly process and are inadequately addressed by short-read sequencing technologies. In contrast, the PacBio platform, leveraging its unique long-read sequencing capabilities, manages to bypass these roadblocks, achieving a genome assembly of "finished grade." This suggests the platform's exceptional potential in assembling even more complex genomes, reinforcing its position as a vital asset in genomics research. The advent of PacBio has therefore expanded the horizons of genomic studies, providing researchers with powerful tools to delve deeper into the intricacies of genetic information.





<table>
  <thead>
    <tr>
      Sequencer
    </tr>
    <tr>
      GS Jr 
    </tr>
    <tr>
      Ion PGM
    </tr>
    <tr>
      MiSeq
    </tr>
    <tr>
      PacBio 
    </tr>
  </thead>
  <tbody>
    
  </tbody>
</table>



| Sequencer            | GS Jr     | Ion PGM | MiSeq | PacBio 
|:---------------------|:----------
| Number of reads      | 115611    |
4982888
39656630
120230*
Total bp
1443005019
9953814130 
374942687
48285593 
Coverage
9
279
1927
73
Mean length
418
290
251
3119
Assembler
Newbler 
Newbler
CLC
Sprai
Number of bp used for assembly
48285593 
400000107 
299809460 
374942687
Number of reads used
115611
1380757
1194460
120230*
Coverage
9
77
58
73
Number of contigs
309
61
34
31
Total bases
5053921
5075085
5103771
5298335
Max length	
164926
895358
732626
3288561
N50 contig length
30451
392606
431440
3288561


Data statistics for sequence run and assemblies

According to the sequencing run data, the total number of reads ranged from 115,611 for GS Jr to approximately 39,656,630 for MiSeq, with PacBio generating 120,230 reads. These figures directly correlate with the total base pairs (bp) sequenced, where GS Jr produced 48,285,593 bp, while MiSeq achieved an impressive 9,953,814,130 bp. Interestingly, despite the lower read numbers, PacBio was able to sequence a total of 374,942,687 bp due to its long-read capability.

The coverage, calculated as the number of times a particular base in the genome was sequenced, was significantly higher for MiSeq at 1,927, compared to 73 for PacBio. Despite lower coverage, PacBio excelled in terms of mean read length, providing an average of 3,119 bp, considerably surpassing the others. This exemplifies the long-read sequencing strength of third-generation platforms.

Looking at assembly results, the number of contigs, or contiguous sequences, resulting from the assembly process, was lowest for PacBio (31), indicating a more contiguous, or 'complete,' assembly. Also, PacBio demonstrated a notably longer maximum contig length (3,288,561 bp) and N50 contig length (a metric indicating the length at which half of the total genome is in contigs of that size or longer), standing at 3,288,561 bp. This underlines the ability of third-generation sequencing platforms to handle complex genomes effectively.

A striking example of its potential comes from a study where this third-generation sequencing technology was utilized to sequence and analyze a haploid human genome, known as CHM1 [7].

The advent of long-read sequencing has been heralded as a significant advancement in genomics, most notably illustrated by the Pacific Biosciences RS sequencer (PacBio). A striking example of its potential comes from a study where this third-generation sequencing technology was utilized to sequence and analyze a haploid human genome, known as CHM1 [5].

The application of real-time DNA sequencing in this research achieved remarkable results, leading to the closure or considerable extension of over 55% of the remaining gaps in the human GRCh37 reference genome. Notably, many of these gaps were characterized by extended runs of repetitive DNA sequences embedded within genomic regions abundant in guanine (G) and cytosine (C) bases.

Moreover, this sequencing approach allowed for a deeper understanding of structural variation in the genome at an unprecedented level. The complete sequences of more than 26,000 structural variants within euchromatic (gene-rich) regions were resolved down to individual base pairs. Significantly, the majority of these identified changes were previously unreported, highlighting the superior sensitivity of long-read sequencing in uncovering genetic variation, especially for events smaller than 5 kilobases in size.

These findings point to a previously underappreciated complexity of the human genome, characterized by variation in longer and more complex repetitive DNA sequences. With the advent of longer-read sequencing technology, much of this complexity can now be resolved, offering promising directions for future research in human genetics.


Despite the significant strides achieved by third-generation sequencing technologies, it is important to note that these platforms are not without their challenges. A key limitation that has emerged in these technologies pertains to the high error rates they present, compared to their second-generation counterparts. Pacific Biosciences (PacBio) RS sequencer, a flagship third-generation platform, has been observed to manifest error rates that rise to as high as 13%, a stark contrast to the less than 1% error rates reported in some second-generation platforms such as Illumina [7].

The predominant errors detected in PacBio sequencing are primarily insertions and deletions, often referred to as 'indels.' These are particularly frequent in homopolymer regions of the genome, sequences with identical consecutive nucleotides. This elevated error rate can complicate the subsequent bioinformatics analyses which rely on accurate readouts from the sequencing stage. The presence of 'indels' can distort the interpretation of the genetic data, thereby potentially obstructing the precise identification and annotation of genetic variants. These inaccuracies underline the need for robust error-correction strategies and algorithms in data analysis to fully exploit the advantages of long-read sequencing platforms [13].


Another third-generation sequencing platform that wrestles with the issue of high error rates is the Oxford Nanopore MinION. Early examinations of this device unveiled alarming error rates that surged up to 38%. Nevertheless, through a series of advancements and optimizations, the MinION device's error rates have been attenuated to around 12-15%. While this represents significant progress, it is essential to note that these rates remain considerably higher compared to the less than 1% error rates often associated with second-generation platforms [9].

This underscores the pressing challenge of achieving higher accuracy in third-generation sequencing technologies without sacrificing the advantage of longer read lengths. Future improvements in these technologies and associated data analysis algorithms will likely be directed toward finding a more satisfactory balance between read length and accuracy.


The selection between second and third-generation sequencing platforms is primarily influenced by the specific demands of the research in question. Second-generation technologies such as GS Jr, Ion PGM, and MiSeq, have been instrumental due to their high-throughput capabilities and cost-effectiveness. These platforms have significantly contributed to tasks that require single-base precision such as identifying single-nucleotide polymorphisms (SNPs), small insertions and deletions (indels), and measuring gene expression levels, leading to profound advancements in genomics and transcriptomics [1][2].

Third-generation sequencing technologies like the Pacific Biosciences RS sequencer (PacBio), in contrast, leverage their long-read sequencing capabilities to tackle more complex genomic landscapes. The longer read lengths of these technologies are particularly advantageous in de novo genome assembly, where they help piece together extensive regions of the genome that can be otherwise challenging to assemble due to repetitive sequences. They have also demonstrated exceptional potential in providing a comprehensive view of transcriptomes by sequencing full-length transcripts, a task that is arduous to achieve with second-generation technologies due to their shorter read lengths. Moreover, third-generation sequencing has been valuable in mapping large structural variations, furthering our understanding of the intricate organization of genomes [10][11].

## Methodology

## Experiment Setup and Implementation

## Results and Analysis

## Conclusion

## Publications
[//]: # "Note: Uncomment each once you uploaded the files to the repository"

<!-- 1. [Semester 7 report](./) -->
<!-- 2. [Semester 7 slides](./) -->
<!-- 3. [Semester 8 report](./) -->
<!-- 4. [Semester 8 slides](./) -->
<!-- 5. Author 1, Author 2 and Author 3 "Research paper title" (2021). [PDF](./). -->


## Links

[//]: # ( NOTE: EDIT THIS LINKS WITH YOUR REPO DETAILS )

- [Project Repository](https://github.com/cepdnaclk/repository-name)
- [Project Page](https://cepdnaclk.github.io/repository-name)
- [Department of Computer Engineering](http://www.ce.pdn.ac.lk/)
- [University of Peradeniya](https://eng.pdn.ac.lk/)

[//]: # "Please refer this to learn more about Markdown syntax"
[//]: # "https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet"
