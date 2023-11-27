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

<table border="1">
  <tr>
    <th>Sequencer</th>
    <th>GS Jr</th>
    <th>Ion PGM</th>
    <th>MiSeq</th>
    <th>PacBio</th>
  </tr>
  <tr>
    <td>Number of reads</td>
    <td>115611</td>
    <td>4982888</td>
    <td>39656630</td>
    <td>120230*</td>
  </tr>
  <tr>
    <td>Total bp</td>
    <td>1443005019</td>
    <td>9953814130</td>
    <td>374942687</td>
    <td>48285593</td>
  </tr>
  <tr>
    <td>Coverage</td>
    <td>9</td>
    <td>279</td>
    <td>1927</td>
    <td>73</td>
  </tr>
  <tr>
    <td>Mean length</td>
    <td>418</td>
    <td>290</td>
    <td>251</td>
    <td>3119</td>
  </tr>
  <tr>
    <td>Assembler</td>
    <td>Newbler</td>
    <td>Newbler</td>
    <td>CLC</td>
    <td>Sprai</td>
  </tr>
  <tr>
    <td>Number of bp used for assembly</td>
    <td>48285593</td>
    <td>40000107</td>
    <td>299809460</td>
    <td>374942687</td>
  </tr>
  <tr>
    <td>Number of reads used</td>
    <td>115611</td>
    <td>1380757</td>
    <td>1194460</td>
    <td>120230*</td>
  </tr>
  <tr>
    <td>Coverage</td>
    <td>9</td>
    <td>77</td>
    <td>58</td>
    <td>73</td>
  </tr>
  <tr>
    <td>Number of contigs</td>
    <td>309</td>
    <td>61</td>
    <td>34</td>
    <td>31</td>
  </tr>
  <tr>
    <td>Total bases</td>
    <td>5053921</td>
    <td>5075085</td>
    <td>5103771</td>
    <td>5298335</td>
  </tr>
  <tr>
    <td>Max length</td>
    <td>164926</td>
    <td>895358</td>
    <td>732626</td>
    <td>3288561</td>
  </tr>
  <tr>
    <td>N50 contig length</td>
    <td>30451</td>
    <td>392606</td>
    <td>431440</td>
    <td>3288561</td>
  </tr>
</table>


Data statistics for sequence runs and assemblies

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

The methodology of this study focused on a detailed comparison of second-generation and third-generation DNA sequencing methods, with respect to the computational domain. To ensure that the comparison was fair and the results reliable, a number of careful steps were followed. All the DNA assembly work—where sequencing reads of DNA data are put together to form a complete picture—was carried out on a high-performance server provided by AgBC. This server has been specially designed to handle large and complex data computation, which is critical for DNA sequencing. By using this powerful server, it was made sure that the computing power was not a limiting factor and that the assembly process was consistent across all tests.

The comparative analysis mainly focused on the Tomato Genome.  The sequencing, or reading of the DNA, was not conducted within the scope of this study. Instead, pre-collected DNA data from second-generation and third-generation were used. For the Second-generation sequencing, the Illumina was used, and for the third-generation sequencing, Nanopore was used. Multiple assemblies of the tomato DNA were performed separately for each of these technologies. To have the reliability and accuracy of the comparative analysis as well as to understand how the variable computational resources affect the assembly, this repetitive process was important. By considering variable parameters such as processing power, memory, and storage, it was aimed to observe the impact on the assembly process with respect to the assembly method. This included examining how the quality of the assembled genome was affected by changes in resources and how quickly the assembly could be completed. The differences between the outcomes of the second and third-generation sequencing technologies made it possible to evaluate how useful each technique was in assembling the tomato genome in relation to the others.

![image](https://github.com/ShenalPerera/e17-4yp-Comparative-Analysis-of-2nd-and-3rd-Generation-Sequencing/assets/73387610/86b2ff9e-b681-4c7d-821c-42bbcfe4c95a)

In the methodology of the study, a structured approach was taken to assemble DNA data from tomatoes, following a sequence of steps applicable to both second-generation and third-generation DNA assembly methods. Initially, DNA data were accessed from available databases. Once accessed, the DNA sequences underwent a process of quality control. This step is crucial to have since may reduce the error contained in the data due to gathered data from both two methods. Any data that doesn't meet these standards are removed.

Following quality control, two distinct assembly methods were used on the DNA sequences. The first method, reference-based assembly, involved aligning the sequences against a previously mapped genome of tomato to identify and position the DNA sequences correctly. The second method, de-novo assembly, involved assembling the sequences without any reference genome, relying solely on the data to piece together the genome sequence.

The quality of the assembled genome was assessed following the assembly process. The accuracy and completeness of the assembled sequences were verified by this quality assessment. It's a crucial stage that ensures the final genome assembly is reliable and appropriate for further study. Combining these efforts produced the basic pipeline for putting together DNA data about tomatoes, which was necessary to compare the accuracy and effectiveness of sequencing assemblies made by the second and third generations.

![image](https://github.com/ShenalPerera/e17-4yp-Comparative-Analysis-of-2nd-and-3rd-Generation-Sequencing/assets/73387610/ba744fb0-97f3-4ef0-9ed5-40f9c0769386)

In the workflow of the research, a thorough process was followed, beginning with a quality check of the DNA sequences. This step was to ensure the data's suitability for assembly. Subsequently, the sequences were subjected to a trimming process, where unwanted sections were removed, including any adapters that might interfere with the reconstruction of the genome. Once the data were prepared, a de-novo assembly was undertaken. In this step, the genome sequence was built entirely from scratch without consulting a previously mapped genome. To ensure the integrity of the assembly, the assembled genome was subjected to a quality assessment prior to the study's conclusion, in order to determine its accuracy and completeness.

In the research workflow, a structured approach was undertaken to compare sequencing methods for a specific species using both Illumina (second-generation) and Nanopore (third-generation) sequencing data. Raw DNA data were initially gathered from Nanopore sequencing technology in the form of fast5 files. These files are like the first rough notes about the DNA's characteristics as it passes through the tiny holes of the Nanopore technology. To make sense of these interactions, the data need to be converted into a sequence of DNA bases. This conversion, known as base calling, transforms the fast5 files into fastq files. Fastq files provide a readable sequence of DNA, listing the order of bases—adenine (A), thymine (T), cytosine (C), and guanine (G)—which are the fundamental components of DNA. Each base is accompanied by a quality score indicating the level of certainty regarding its identification in the sequence.

The Illumina technology, on the other hand, directly provides the data in Fastq format. But before we can use this data, it must be cleaned up. Trimming is the process of removing portions of the data that are not trustworthy or clear enough to be used for in-depth analysis. For the Nanopore data, base calling was performed to convert the initial fast5 files into Fastq format, aligning with the format provided by Illumina. After this conversion, both the newly converted Nanopore data and the original Illumina data were trimmed. The Illumina data were subjected to a trimming process to eliminate low-quality reads, ensuring that only high-quality reads were retained for further analysis. Simultaneously, the Nanopore data not only went through a similar process to remove low-quality reads but also to shorten the longer DNA sequences. This step was crucial to make the raw data sizes of both Illumina and Nanopore technologies similar, bringing them to a common starting point for comparison. Once trimmed, the data from both technologies were brought to a common ground, meaning they were processed to a point where they could be directly compared.

After the standardization of the DNA data lengths, the assembly process was performed repeatedly for both the Illumina (second-generation) and Nanopore (third-generation) datasets. Verifying the accuracy and consistency of the assembly results was the aim of these multiple assemblies. In this phase, the allocation of computational resources was varied to observe the effects on the assembly process. Different amounts of threads, RAM, storage space, and processor capacity were allocated during each assembly run. Because of this variation in resource allocation, the study was able to investigate how variations in computational input might affect the quality and speed of genome assembly for both Illumina and Nanopore.


## Experiment Setup and Implementation

Experiments were carried out to compare second-generation (2nd Gen) and third-generation (3rd Gen) genome assemblies. The DNA data for two different species, tomato and cinnamon, were used in the study. Specifically, DNA sequences from the tomato were used for both 2nd Gen and 3rd Gen assemblies, while cinnamon DNA data were used exclusively for 2nd Gen assembly. For the 2nd Gen assembly, the DNA data were obtained using Illumina technology, which is known for providing short but very accurate sequences of DNA. On the other hand, for the 3rd Gen assembly, the DNA data were sourced from Nanopore technology, which can read longer reads of DNA.

The Illumina DNA data for cinnamon, essential for the assembly process, were obtained from AgBC at the University of Peradeniya. This specific data was used to examine how the Illumina sequencing data could be assembled to form the complete genome of cinnamon, showcasing the assembly capabilities of 2nd Gen technology.

For the tomato, both Illumina and Nanopore DNA data were gathered from the National Center for Biotechnology Information (NCBI).Additionally, Nanopore DNA data for Nanopore were also acquired from AgBC. This allowed for a comparative study within the same species, contrasting the assembly results from 2nd-Gen Illumina and 3rd-Gen Nanopore technologies.

For the tomato genome, a total of eight datasets were collected from the National Center for Biotechnology Information (NCBI). Four of these datasets were obtained using Illumina sequencing technology, and the other four were acquired using Nanopore sequencing technology. Each of these eight datasets underwent the assembly process five times. The purpose of repeating the assembly multiple times was to see how changes in the allocation of computational resources affected the assembly results. Different settings for computational resources, such as the amount of memory used, the number of processing threads, and the storage capacity, were adjusted in each of these assembly runs.

For Illumina assembly, specific software tools were used at different stages to ensure the accuracy and quality of the DNA assembly. Initially, the software FastQC was employed to perform a quality check on the Illumina data. After analyzing the DNA sequences, FastQC creates a variety of graphs and charts that show the data quality and whether any odd patterns exist that could point to errors. Following the quality check, the software Trimmomatic was utilized. By eliminating adapter sequences that were erroneously added to the DNA during the sequencing process and trimming sequences that do not match the quality threshold, this tool is intended to clean up the data. To further refine the information, SortMeRNA was used to remove ribosomal RNA (rRNA) sequences from the data that are not necessary for assembling the DNA sequences.

After the data were cleaned, the assembly process was carried out using the tool Trinity. Trinity pieces together the high-quality reads that overlap with each other to create longer contiguous sequences, known as contigs. The organism's reconstructed DNA sequences are represented by these contigs. Lastly, the program QUAST was used to evaluate the quality of the assembled DNA sequence. In order to make sure the assembly satisfies the strict requirements needed for precise genomic analysis, QUAST assesses it by offering metrics that quantify the length and accuracy of the contigs. By using these tools in the workflow, the Illumina DNA data were processed and assembled, and the quality of the assembled genome was verified to confirm the reliability of the assembly process.

In the research conducted, the Nanopore sequencing dataset obtained from AgBC was organized into six separate barcodes, each corresponding to different environmental conditions. Initially, an assembly was attempted for each barcode set individually. However, this approach resulted in a low coverage error, indicating that the data were insufficient for a complete assembly. In response to this issue, all the barcoded datasets were combined in an attempt to increase the overall coverage. In this assembly, the coverage increased to 0.12x, yet it remained insufficient for a successful assembly of the genome. Subsequently, a high-accuracy base calling was executed on the combined data. Through this process, the coverage was raised to 0.59x by converting the sequencing signals into a more precise sequence of DNA bases. Despite this improvement, the coverage was still below the level required for assembly.

Therefore, a new dataset was chosen from NCBI to carry out the research. This dataset provided a higher coverage of 5.42x, bringing the data closer to the required threshold for assembly. This level of coverage meant that, on average, each part of the DNA was read over five times, providing a more complete set of data for assembly. The assembly process was done by using a specialized tool called Canu. It is typically designed to operate with a minimum coverage of 10x for the best results. However, given the lower coverage from the NCBI dataset, adjustments within Canu's settings were required. The parameter known as 'stopOnLowCoverage' was reduced from the default setting of 10x to 5x. This adjustment allowed the assembly process to continue using the available data, despite the lower-than-preferred number of reads.


## Results and Analysis

A total of 40 assemblies were performed to do the comparative analysis. They are all related to the Tomato genome. Eight datasets were selected for this purpose, evenly divided between Illumina and Nanopore sequencing technologies, with each Illumina dataset having a corresponding Nanopore counterpart. This pairing was based on the datasets having approximately the same raw data size, allowing for four direct comparisons between the two sequencing methods. Out of the paired datasets, one was approximately 10Gb in size, representing a larger genomic dataset, while another was about 1Gb, exemplifying a smaller dataset. The comparison intended to reveal the strengths and weaknesses of Illumina(2nd Gen) and Nanopore(3rd Gen). 

As quality matrics N50 value and the number of contigs were studied. The N50 value serves as an indicator of the assembly's contiguity. A higher N50 suggests that the DNA sequences are assembled into longer stretches.\ A lower number of contigs means that the genome is represented by fewer and longer sequences. It suggests that more comprehensive and connected assembly. These two metrics provide a measure of the quality of the assembled genome. It indicates how closely the assembled genome resembles the organism's actual DNA sequence. Performance, on the other hand, was measured by the assembly time, which reflects the efficiency of the sequencing and computational process. Shorter assembly times are generally preferred, as they indicate a faster turnaround from raw data to a usable genomic sequence. Therefore quality metrics address how well the genome is assembled. The performance metrics (assembly time) address how fast the assembly is achieved. Both of these performance and quality metrics are crucial for the practical use of sequencing technologies in real-world applications.

![image](https://github.com/ShenalPerera/e17-4yp-Comparative-Analysis-of-2nd-and-3rd-Generation-Sequencing/assets/73387610/fcf69b58-26ec-4839-915b-eb81dc1b93f3)

<table border="1">
  <tr>
    <th>Resource Allocation</th>
    <th>Illumina (2nd Gen)</th>
    <th>Nanopore (3rd Gen)</th>
  </tr>
  <tr>
    <td>CPU: 26 Threads<br>RAM: 50GB</td>
    <td>Time: 8 Hours<br>N50: 20 kb<br>Contigs: 4k</td>
    <td>Time: 14 Hours<br>N50: 100 kb<br>Contigs: 0.3k</td>
  </tr>
  <tr>
    <td>CPU: 26 Threads<br>RAM: 150GB</td>
    <td>Time: 6 Hours<br>N50: 24kb<br>Contigs: 3k</td>
    <td>Time: 12 Hours<br>N50: 110 kb<br>Contigs: 0.25k</td>
  </tr>
  <tr>
    <td>CPU: 40 Threads<br>RAM: 50GB</td>
    <td>Time: 6 Hours<br>N50: 27kb<br>Contigs: 3.5k</td>
    <td>Time: 10 Hours<br>N50: 120kb<br>Contigs: 0.2k</td>
  </tr>
  <tr>
    <td>CPU: 40 Threads<br>RAM: 150GB</td>
    <td>Time: 5 Hours<br>N50: 30kb<br>Contigs: 2.5k</td>
    <td>Time: 8 Hours<br>N50: 130 kb<br>Contigs: 0.15k</td>
  </tr>
</table>

![image](https://github.com/ShenalPerera/e17-4yp-Comparative-Analysis-of-2nd-and-3rd-Generation-Sequencing/assets/73387610/bf50617e-fe39-4d3c-a17f-a96a40638280)

![image](https://github.com/ShenalPerera/e17-4yp-Comparative-Analysis-of-2nd-and-3rd-Generation-Sequencing/assets/73387610/48af006a-3579-46fb-9c95-8089b5351fe1)

In the analysis of a 10Gb dataset for genome assembly, the results indicated notable differences between the Illumina (second-generation) and Nanopore (third-generation) sequencing technologies. For the Illumina assemblies, the N50 values showed an increasing trend with the enhancement of computational resources, specifically RAM. Starting with an N50 of 41 Kb when using 50GB of RAM, the figure rose to 63 Kb with 150GB of RAM. However, the number of contigs, representing the fragments of assembled DNA, decreased from 17k to 9k, suggesting that while the assemblies became less fragmented, there was still a notable number of separate pieces. In contrast, the Nanopore assemblies demonstrated a higher N50 from the outset, starting at 253 Kb and increasing to 306 Kb, which suggests that the DNA was assembled into fewer, longer stretches, potentially indicating a more contiguous and higher quality assembly compared to Illumina. The number of contigs was significantly lower, decreasing from 1.2k to 0.6k as computational resources were increased. 

When considering performance matrices, Nanopore assemblies were slower compared to Illumina assemblies. It took 63 hours with 50GB of RAM, this time decreased to 37 hours with 150GB of RAM, showing improvement with additional resources. Illumina assemblies were faster. It took 37 hours with 50GB of RAM and reduced to 19 hours with 150GB of RAM. When more computer power and memory were used for the assemblies, the assembly time became shorter for both the Illumina and Nanopore technologies. However, the more computer power and memory added, the less time was saved. So, at a certain point, adding even more power and memory didn't speed things up by much. Moreover, it was observed that an increase in RAM had a greater effect on optimizing assembly time and quality than the addition of CPU threads. This suggests that having more memory to manage the data during assembly is more beneficial than simply having more CPU threads to handle multiple tasks simultaneously.

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">

</head>
<body>

<table>
  <tr>
    <th>Resource Allocation</th>
    <th>Illumina (2nd Gen)</th>
    <th>Nanopore (3rd Gen)</th>
  </tr>
  <tr>
    <td rowspan="2">CPU: 26 Threads<br>RAM: 50GB</td>
    <td>Time: 8 Hours<br>N50: 20 kb<br>Contigs: 4k</td>
    <td>Time: 14 Hours<br>N50: 100 kb<br>Contigs: 0.3k</td>
  </tr>
  <tr>
    <td>Time: 6 Hours<br>N50: 24kb<br>Contigs: 3k</td>
    <td>Time: 12 Hours<br>N50: 110 kb<br>Contigs: 0.25k</td>
  </tr>
  <tr>
    <td rowspan="2">CPU: 40 Threads<br>RAM: 50GB</td>
    <td>Time: 6 Hours<br>N50: 27kb<br>Contigs: 3.5k</td>
    <td>Time: 10 Hours<br>N50: 120kb<br>Contigs: 0.2k</td>
  </tr>
  <tr>
    <td>Time: 5 Hours<br>N50: 30kb<br>Contigs: 2.5k</td>
    <td>Time: 8 Hours<br>N50: 130 kb<br>Contigs: 0.15k</td>
  </tr>
</table>

</body>
</html>

In terms of performance, it was observed that both Illumina and Nanopore technologies required less time to assemble the 1Gb dataset compared to the larger 10Gb dataset. With Illumina, the assembly duration ranged from 8 hours with basic computational resources to 5 hours with enhanced resources. Nanopore showed assembly times decreasing from 14 hours to 8 hours as computational resources were increased.

For the quality of assembly, Illumina's N50 values improved modestly from 20 Kb to 30 Kb with additional resources, whereas Nanopore's N50 values increased from 100 Kb to 130 Kb. This suggests that, for the Nanopore assemblies, the assembled genome is stitched together into significantly longer stretches. The number of contigs decreased with the allocation of more computational power. Illumina assemblies produced between 4,000 to 2,500 contigs, and Nanopore assemblies ranged from 300 to 150 contigs, indicating a more cohesive assembly for Nanopore, likely due to its ability to produce longer reads.

When comparing these results with the 10Gb dataset, a clear trend was observed that larger datasets tend to increase both the assembly time and the number of contigs, while possibly decreasing the N50 value. This is expected as larger datasets are more complex and contain more information to process and assemble. These results highlight the balance between the allocated computational resources and the desired outcome of the assembly process. They also emphasize the differences in how Illumina and Nanopore sequencing technologies respond to changes in resource allocation, with each technology having its own strengths and limitations in the context of genome assembly.

During the research, in addition to the specific results obtained from the genome assembly process, several general insights were gained. Firstly, it was noted that the time taken for error corrections was significantly higher in Nanopore sequencing compared to Illumina sequencing. This difference is largely due to the Overlap-Layout-Consensus (OLC) approach used in Nanopore sequencing. The OLC method, which is critical in assembling the long reads characteristic of Nanopore technology, involves finding overlaps between sequences, organizing these sequences in a specific order, and then deriving a consensus sequence. The longer read lengths in Nanopore sequencing make the process of identifying correct overlaps more complex and time-intensive. Additionally, the base calling pass rate for Nanopore data was considerably lower than that for Illumina data. Base calling, the process of determining the nucleotide bases (adenine, thymine, cytosine, guanine) from raw sequencing data, is more challenging with Nanopore technology due to its higher error rate. In contrast, Illumina technology, which produces shorter reads, generally achieves a higher pass rate, indicating that a larger proportion of its sequencing data is of sufficient quality to be used in assembly without extensive correction. 

Another important observation was the crucial role of read coverage in a successful Nanopore de-novo assembly. De-novo assembly, where the genome is assembled without a reference sequence, depends heavily on achieving sufficient coverage of reads. The required level of coverage is dependent on the size of the genome being sequenced, with larger genomes needing more extensive coverage.  With the advantage of longer reads in Nanopore,  It can be proven that Nanopore is beneficial for assembling more complex genomes. However, Nanopore consists of more challenges in error correction and read coverage.

## Conclusion

In this research, a thorough comparison between Illumina (second-generation) and Nanopore (third-generation) DNA sequencing methods was conducted, focusing on tomato and cinnamon genomes. Evaluating these technologies' performance with varying data sizes and computational conditions was the goal.

The analysis showed clear variations in each technology's output and performance. Illumina, which produces shorter DNA reads, completed the assembly process faster, but resulted in a larger number of contigs. This implies that the assembled DNA was in more, smaller fragments. In contrast, Nanopore, known for its longer reads, took longer to assemble the genomes due to the complex process of matching these long sequences. On the other hand, it yielded assemblies with fewer contigs and higher N50 values, indicating more continuous and possibly more accurate genome representations.

The impact of increased processing power, particularly RAM, on assembly quality and speed for both Illumina and Nanopore was the study's key finding. It was noted that while adding more RAM significantly improved assembly outcomes, the benefit diminished beyond a certain point.

For Nanopore sequencing, challenges such as lower base calling pass rates and the need for high read coverage, especially in de-novo assembly, were highlighted. Depending on the particular needs of the research, these considerations are critical in selecting the right sequencing method for genomic studies.
In the context of genome assembly, this research offers valuable insights into the capabilities and limitations of the use of Illumina (2nd gen) and Nanopore (3rd gen) genome assembly techniques. It focuses on the computational power aspect of the genomic assembly process, compared to both technologies. These results offer a helpful framework for researchers to make defensible decisions in genomic studies as sequencing technologies advance.


[//]: # "Note: Uncomment each once you uploaded the files to the repository"

<!-- 1. [Semester 7 report](./) -->
<!-- 2. [Semester 7 slides](./) -->
<!-- 3. [Semester 8 report](./) -->
<!-- 4. [Semester 8 slides](./) -->
<!-- 5. Author 1, Author 2 and Author 3 "Research paper title" (2021). [PDF](./). -->


## Links

[//]: # ( NOTE: EDIT THIS LINKS WITH YOUR REPO DETAILS )

- [Project Repository](https://github.com/cepdnaclk/e17-4yp-Comparative-Analysis-of-2nd-and-3rd-Generation-Sequencing)
- [Project Page](https://cepdnaclk.github.io/e17-4yp-Comparative-Analysis-of-2nd-and-3rd-Generation-Sequencing/)
- [Department of Computer Engineering](http://www.ce.pdn.ac.lk/)
- [University of Peradeniya](https://eng.pdn.ac.lk/)

[//]: # "Please refer this to learn more about Markdown syntax"
[//]: # "https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet"
