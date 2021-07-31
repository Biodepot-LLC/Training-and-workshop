# Training-and-workshop

## A graphical front-end for rapid and scalable execution of bioinformatics workflows using serverless cloud computing.

Presenters: Ling-Hong Hung, Varik Hoang, Wes Lloyd, Ka Yee Yeung.

August 1, 2021 at the 12th ACM Conference on Bioinformatics, Computational Biology, and Health Informatics (ACM BCB) (https://acm-bcb.org/)

## Abstract 
We present a hands-on tutorial of the BioDepot-workflow-builder (Bwb), a drag and drop graphical user interface that allows users to assemble, modify and execute Docker workflows. Bwb represents individual software modules as widgets that can be assembled into interactive workflows.  In the first unit of the tutorial, we will present an optimized method that yields a 1100-fold computational speedup. Specifically, the alignment time for a 640 million read human RNA-sequencing dataset is reduced from ~20 hours to ~1 minute using serverless cloud computing. This makes it possible to adjust alignment parameters in real-time and to iteratively improve the final lists of differentially expressed genes. Participants will acquire hands-on experience deploying this accelerated workflow on Amazon Web Services (AWS) using the Bwb graphical interface. 

In the second unit of the tutorial, we will focus on cancer genomic workflows integrated with the Cancer Research Data Commons (CRDC).  Participants will acquire hands-on experience using the Bwb graphical interface to execute the National Cancer Institute (NCI) Genomic Data Commons (GDC) DNA sequencing and RNA sequencing workflows.  We will also demonstrate Bwb’s integration of the Toil job scheduler, and support for workflows defined using the Common Workflow Language (CWL), and the Workflow Description Language (WDL).

## Tutorial Description
Objectives of the tutorial: We aim to give participants a hands-on experience using the Bwb for genomic analyses on the cloud.   We will provide additional resources at the end of the tutorial, so that participants can continue to explore these topics.

Upon successful completion of this tutorial, the participants will be able to:
* Discuss the applications and challenges of analyzing cancer genomic data.
* Acquire hands-on experience using the Bwb to deploy genomic workflows on the cloud.
* Understand the applications of cloud computing for the analyses of genomic data.
* Gain hands-on experience deploying genomic workflows on AWS using the Bwb’s graphical user interface.

## Resources
GDC DNA sequencing workflow (https://docs.gdc.cancer.gov/Data/Bioinformatics_Pipelines/DNA_Seq_Variant_Calling_Pipeline/)

GDC mRNA sequencing workflow (https://docs.gdc.cancer.gov/Data/Bioinformatics_Pipelines/Expression_mRNA_Pipeline/)

Bwb Github (https://github.com/BioDepot/BioDepot-workflow-builder)

## References
Building containerized workflows using the BioDepot-workflow-Builder (BwB). Ling-Hong Hung, Jiaming Hu, Trevor Meiss, Alyssa Ingersoll, Wes Lloyd, Daniel Kristiyanto, Yuguang Xiong, Eric Sobie, Ka Yee Yeung. Cell Systems 2019, v9, issue 5, pages 508-514.E3 (https://doi.org/10.1016/j.cels.2019.08.007)

Accessible and interactive RNA sequencing analysis using serverless computing. Ling-Hong Hung, Xingzhi Niu, Wes Lloyd, Ka Yee Yeung. bioRxiv 576199v2 2020. (https://www.biorxiv.org/content/10.1101/576199v2)
