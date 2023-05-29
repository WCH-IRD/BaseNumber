# Evaluation of BaseNumber, a GPU-accelerated variant calling tool on whole genome sequencing datasets
We comprehensively evaluated the germline variant calling of a GPU-based acceleration tool, BaseNumber, using WGS datasets from various sources. These included standards of whole genome sequencing (WGS) data from the Genome in a Bottle (GIAB) and the Golden Standard of China Genome (GSCG) projects, resequenced GSCG samples, and 100 in-house samples from the Genome Sequencing of Rare Diseases (GSRD) project. The variant calling outputs were compared to the reference and the results generated by the Burrows-Wheeler Aligner (BWA) and Genome Analysis Toolkit (GATK) pipeline. BaseNumber demonstrated high precision (99.32%) and recall (99.86%) rates in variant calls compared to the standard reference. The output comparison between BaseNumber and GATK pipelines yielded nearly identical results with a mean F1 score of 99.69%. Additionally, BaseNumber took 23 minutes on average to analyze a 48X WGS sample, which was 215.33 times shorter than the GATK workflow.

![Evaluation workflow](https://github.com/WCH-IRD/BaseNumber/blob/main/image/fig1.jpg)
<p align="center"> Figure 1. The workflow of evaluation study </p>



![Accuracy](https://github.com/WCH-IRD/BaseNumber/blob/main/image/fig2-1.png)
<p align="center"> Figure 2. The precision and recall of BaseNumber calling results compared with GIAB and GSCS standards</p>


![Efficiency and consistency](https://github.com/WCH-IRD/BaseNumber/blob/main/image/fig2-1.png)
<p align="center"> Figure 3. The comparison of speed and consistency of BaseNumber and GATK</p>


The "ouputs" folder of this repo contained the VCFs generated from fastq files of GIAB and GSCG standards. 

BaseNumber is available for trial on the AWS US East (N. Virginia) via https://us-east-1.console.aws.amazon.com/. To obtain the AMI image, please contact bufengxiao@wchscu.cn.
