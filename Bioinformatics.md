

# **Xinshuai Qi's Summary and Notes on Bioinformatics**
#    -- by Xinshuai Qi
（last update on 12-4-2017）

* [HarvardX Biomedical Data Science Open Online Training](http://rafalab.github.io/pages/harvardx.html)
  * [PH525x series - Biomedical Data Science](http://genomicsclass.github.io/book/)
  * [Bioconductor for Genomic Data Science](http://kasperdanielhansen.github.io/genbioconductor/)

* [Rosalind](http://rosalind.info/problems/locations/#)

* [Introduction to Next Generation Sequencing (NGS) Data Analysis - UCI](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=1&cad=rja&uact=8&ved=0ahUKEwjJ7fDmk8vWAhVY4WMKHZLACpIQFggqMAA&url=http%3A%2F%2Fcbt.bio.uci.edu%2Ffiles%2F2016%2F01%2FPresentation-2-jwu_4Jan16.pdf&usg=AFQjCNE7T56mHrL5Lyt3ttpEdDVkrI_Efg)

# Transcrptome Assembly
* Raw reads clean
* De novo Assembly
  * Trinity
	  * 279 citation since 2011
  * Velvet
	  * 6837 citation since 2008
* SOAPdenovoTrans
	* 359 since 2014




* **Reference-based Assembly**
  * Samtools
  * VCFtools
  * BCFtools

* Picard
	*  manipulating high-throughput sequencing (HTS) data and formats such as SAM/BAM/CRAM and VCF.


# Genome assembly
* [ABySS](http://www.bcgsc.ca/platform/bioinfo/software/abyss)
	* [paper](https://genome.cshlp.org/content/19/6/1117.short)	
	* 2458 citation since 2009

* [AllPATH LG](http://software.broadinstitute.org/allpaths-lg/blog/)
	* designed for at least 2 short reads library, high coverage; not support polyploid
	* **graph based results**
	* from the Computational Research and Development group at the Broad Institute	
	* 773 citation since 2008


### PacBio assembly
* FALCON
* HGAP 
	* developed by PacBio
* PBJelly 

improvement
* PILON https://github.com/broadinstitute/pilon/wiki
* Quiver https://github.com/PacificBiosciences/GenomicConsensus


## evaluation of the quality 

**Genome**
* [QUEST](http://quast.bioinf.spbau.ru/manual.html)
	* [paper](https://academic.oup.com/bioinformatics/article/29/8/1072/228832)
	*	2013 citation: 879
* BUSCO: Benchmarking Universal Single-Copy Orthologs, named BUSCO.
	* 
* [PEAPR](http://www.sanger.ac.uk/science/tools/reapr)forcus on the error rate. 
	* [paper](/genomebiology.biomedcentral.com/articles/10.1186/gb-2013-14-5-r47) 
* [GAGE (Genome Assembly Gold-standard Evaluations)](https://genome.cshlp.org/content/22/3/557.full.pdf+html)
	* data quality is more important than the assembler
	* 各自软件差异很大
	* 
[paper: # A Practical Comparison of  _De Novo_  Genome Assembly Software Tools for Next-Generation Sequencing Technologies](http://journals.plos.org/plosone/article?id=10.1371/journal.pone.0017915)
* string-based assemblers
* overlap-layout-consensus (OLC) assemblers
* _De Bruijn_ graph-based assemblers: good for large short-reads dataset

**Transcriptome**
* transrate
* detonate


## polyploid SNP calling
[polycat](https://udall-lab.byu.edu/Research/CottonResearch/polyCatReadmappingincotton.aspx)## evaluate the quality of assembly


# Genome Evolution and Genomics
  * OrthoFinder
  * Circos
  * SnpEff
  * Gene Ontology
  * LeafJ
  * [LTR retriever](https://gitlab.msu.edu/oushujun/LTR_retriever/blob/master/LTR_retriever)
  * [Omictools](https://omictools.com/)

# Phylogenetics
  * RAxML
  * PAML
  * BEAST
  * TreeMix
  * [Detecting trait-dependent
evolutionary rate shifts
in sequence sites](http://traitrate.tau.ac.il/prop/)
  * (ABBA/BABA test)[http://www.popgen.dk/angsd/index.php/Abbababa]

# Population Genetics and phylogeography
[Population genetics and genomics in R](https://grunwaldlab.github.io/Population_Genetics_in_R/TOC.html)


  * STRUCTURE
  * PCA and smartPCA
  * Provean
  * [BAD-Mutations](https://github.com/MorrellLAB/BAD_Mutations)
  * HAPMIX
  * ∂a∂i
  * DIY-ABC
  * fastSimCoal
  * SLiM2
  * TCS
  * Ecological Niche Modeling
    * WorldClim
   * **SMC++** [github](https://github.com/popgenmethods/smcpp)
	   *   a program for estimating the size history of populations from whole genome sequence data.
	* [ABBA-BABA test](http://www.popgen.dk/angsd/index.php/Abbababa) 
		* also called the D-statistic
		* tests for ancient admixture 



# RNASeq
wiki tools for RNASeq
https://en.wikipedia.org/wiki/List_of_RNA-Seq_bioinformatics_tools

[RNASeq Course](http://sites.tufts.edu/cbi/resources/rna-seq-course/)
## Fastaq trim
* [Sickle]() 
* SnoWhite
* Trimmonatic

## denovo assembly
* Volvet
* Trinity
* SOAPdenovoTrans

evaluation:
* DETONATE score
* TransRate
* Ultra-conserved elements (UCEs)


## RNA-Seq aligner => generate SAM file [RNASeq Course](http://sites.tufts.edu/cbi/resources/rna-seq-course/)


#### Differential Expression
  * TopHat
  * Cufflinks
 
 * [STAR RNA-Seq aligner](https://github.com/alexdobin/STAR)
	 * to use cufflinks, you need to set FLAGS while run. 
 * [**HISAT**](http://www.ccb.jhu.edu/software/hisat/index.shtml)
	 * **[Tophat](http://www.ccb.jhu.edu/software/tophat/index.shtml)的升级版**
	##  * use hierarchical , large set of small indexes. NOT one global index for the genome. 
	* build on Bowtie2
	  * use [FM-index](https://en.wikipedia.org/wiki/FM-index)
	 
	 * [salmon](https://combine-lab.github.io/salmon/getting_started/)
	* [**RSEM**](http://deweylab.github.io/RSEM/README.html)
	* [HyLite gene expression in hybrid or poly]()
		* [paper](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/s12859-014-0433-8)

  * [Subreads, Limma and EdgeR]()
  * [kallisto](https://pachterlab.github.io/kallisto/about) and [sleuth](https://pachterlab.github.io/sleuth/) by [pachterlab](https://pachterlab.github.io)

-----
* [HISAT, StringTie and Ballgown](http://www.nature.com.ezproxy2.library.arizona.edu/articles/nprot.2016.095)
	* A replacement of the old TOPHAT and Cufflinks solution. 
	* 



**HISAT vs STAR vs TopHat**(https://plus.google.com/+MarkZiemann1/posts/FcoyDzJ7khU)
基本上差不多










## Samtools: SAM to BAM

#### evaluation of RNA-Seq alignment
* mapped reads %
* 



## Functional analysis (enrichment, co-expression)
* [ Functional visualization --Guangchuang Yu UHK](https://www.bioconductor.org/packages/3.7/bioc/vignettes/clusterProfiler/inst/doc/clusterProfiler.html)
* [ClusterProfiler](https://guangchuangyu.github.io/clusterProfiler/)
Differential Expression
  * TopHat
  * Cufflinks

  * [Subreads, Limma and EdgeR]()
  * [kallisto](https://pachterlab.github.io/kallisto/about) and [sleuth](https://pachterlab.github.io/sleuth/) by [pachterlab](https://pachterlab.github.io)


#### eQTL
  * [eQTL mapping using RNA-Seq data](https://github.com/molgenis/systemsgenetics/wiki/eQTL-mapping-analysis-cookbook-for-RNA-seq-data)
#### Enrichment and Coexpression
  * [DAVID](https://david.ncifcrf.gov/)
  * [Gene Set Enrichment Analysis (GSEA)](http://software.broadinstitute.org/gsea/index.jsp)
  * WGCNA (https://labs.genetics.ucla.edu/horvath/CoexpressionNetwork/Rpackages/WGCNA/)
 

## eQTL
  * [eQTL mapping using RNA-Seq data](https://github.com/molgenis/systemsgenetics/wiki/eQTL-mapping-analysis-cookbook-for-RNA-seq-data)
 

## Alternative splicing
* classification
	* Skipped exon
		* A-B-C
		* A-_-C
	* Alternative 5' splice site
		* A-C
		* B-C
	* Alternative 3' splice site
		* A-B
		* A-C
	* Mutually exclusive exons
		*  A-B-D
		*  A-C-D
	*  Retained intron
		* A-B
		* A-(intron)-B

* Steps:
	* exon reads GDE
	* isoforms GDE
	* junctions	

#### Tools
* RSEM 
	* aligns reads to transcripts using Bowtie
	* Output isoform level expression level
* [DEXSeq]()
	* [Analyzing RNA-seq data for differential exon usage with the "DEXSeq" package](http://bioconductor.org/packages/release/bioc/vignettes/DEXSeq/inst/doc/DEXSeq.pdf)
* Cufflinks
* MATS
* SpliceR


## Application of RNA-Seq in Diagnostics
[Translating RNA sequencing into clinical diagnostics: opportunities and challenges](https://www.nature.com/articles/nrg.2016.10)
* [Genetic testing: The diagnostic power of RNA-seq](https://www.nature.com/articles/nrg.2017.39)

Examples using RNA-Seq for Diagnosis:
* [novel pathway in PAH](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4584250/)

## New Directions of RNA-Seq analysis
* RNA-Seq in different tissue
* Different time 
* single-cell RNA-Seq
* integrate RNA-Seq with GWAS





		# Quantitative Genetics, GWAS, and Statistics
  * PLink [(tutorial]()[http://zzz.bwh.harvard.edu/plink/tutorial.shtml#t6)
- [QQ plot图——评价你的统计模型是否合理](http://www.genedenovo.com/news/391.html)
- [GWAS training by CBI](http://sites.tufts.edu/cbi/resources/genetic-association-studies/)
	- [GWAS Adjusting for Covariates and Stratification](http://sites.tufts.edu/cbi/resources/genetic-association-studies/genetic-association-studies-learning-exercises/)

- Candidate Gene Association Study

The candidate gene approach to conducting genetic association studies focuses on associations between genetic variation within pre-specified genes of interest and phenotypes or disease states. This is in contrast to genome-wide association studies (GWAS), which scan the entire genome for common genetic variation.

- [GWAS local visualization](http://locuszoom.sph.umich.edu//)

---
- ascertainment bias: make sure use "clearly defined phenotypes for case and control"
- population stratification: 
	- subtle ancestral differences in case and control __ gene~ethnicity association
		- Using Principal Components Analysis (PCA)as a Surrogate for Genetic Ancestry
		- adjusting for principal components of genetic ancestry.
	- gender, env
- Bonferroni correction 5*10-7
	- Standard Bonferroni correction
	- Test each SNP at the  α* =α /m1 level
	- Where m1 = number of markers tested 
	- Assuming m1 = 500,000, a Bonferroni-corrected threshold of α*= 0.05/500,000 = 1x10–7
	- Conservative when the tests are correlated
- HWE: For a rare disease (or no/modest genetic effects), genotype frequencies in controls should (nearly) follow HWE
-imputation: Using LD and Hapmap/1000 Genomes to Impute Untyped SNPs


 
# Phenotyping 
[plantCV](http://plantcv.readthedocs.io/en/latest/)







