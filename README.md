# <p align="center"> Awesome Phenotype Prediction </p> 

## Contents
- [Introduction](#introduction)
- [Important Definitions/Concepts](#concepts)
- [Papers](#papers)


# Introduction
## <p align="center"> What is phenotype prediction? </p>
 
Phenotype Prediction involves the task of predicting an organism's phenotype based on its genotype and environmental factors.

In various domains, understanding the relationship between genotype, environment, and phenotype holds great significance. One notable example is human diseases, where unraveling the interplay between genotype and environment is a central challenge in the field of medicine. Similarly, in agriculture, predicting phenotypes like crop yield and drought resistance is crucial for sustaining the growing global population.

The advent of DNA sequencing technology has sparked a revolution in our ability to predict phenotypes. The declining cost of DNA sequencing has made it more accessible, enabling the genotyping of numerous organisms in a single investigation. This advancement paves the way for employing machine learning techniques to uncover predictive associations between an organism's genotype, environment, and phenotype. These comprehensive studies are often referred to as genome-wide association studies (GWAS).

The rapid progress in DNA sequencing technology not only enhances our understanding of the complex relationship between genes, environment, and traits but also opens up new avenues for developing predictive models and advancing phenotype prediction research."

This revised text aims to provide a clearer and more concise explanation of phenotype prediction, emphasizing its importance in various domains and highlighting the role of DNA sequencing technology in advancing this field of research.
<br />

<br/>

<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/1/12/Manhattan_Plot.png" width="800">
</p>

<div style="margin-top: 0px;">
  <p align="center">
    <em>Figure 1: Manhattan plot</em>
  </p>
</div>

<p align="center">
  <a href="https://www.genome.gov/genetics-glossary/Genome-Wide-Association-Studies" align="center">Reference</a>
</p>

<br/>

## <p align="center"> Challenges in the prediction </p>
### <p align = 'center'> Why an individual's phenotype cannot always be predicted from their genome and the environment they experience? </p>

One of the main things scientists ask themselves in phenotype prediction is to what extent is the knowledge about an individual's genotype, together with information about the environment that they have experienced, sufficient to predict phenotypic variation.

In the referenced paper, they argue that, although the 'typical' phenotypic outcome of an individual's genome can be predicted, it is much more difficult to predict the actual outcome for a particular individual. One of the three main reasons for this are:
1. The outcome of mutations can be influenced by random stochastic processes. 
2. Genetic variation present in one generation can influence phenotypic traits in the next generation.
3. The environment experienced by one generation can influence phenotypic variation in the next generation. 

Taken together, they mean that, in many cases, the genotypes of individuals and the environment that they experience may not be sufficient to determine their phenotypes. This is why, in this research we want to give a different approach to phenotype prediction.

<p align="center">
<a href="https://pubmed.ncbi.nlm.nih.gov/22934970/" align= "center">Reference</a>
</p>


---
# Concepts
  - ## Wrapper vs Filter Techniques
  - Filter algorithms: General preprocessing algorithms that do not assume the use of a specific classification method.
  - Wrapper algorithms: They “wrap” the feature selection around a specific classifier and select a subset of features based on the classifier’s accuracy using cross-validation.

  - ## Sparse Matrix
    - Definition: A sparse matrix is a special case of a matrix in which the number of zero elements is much higher than the number of non-zero elements.

    - Usage: By using spicy's library, we can use, for example, 'csr_matrix' (compressed sparse row) to the original dataset. By doing this, if someone has a dataset with a large quantity of zeros, compared to the other possible values, the 'csr_matrix' will only keep the non-zero positions and value from the dataset. By doing this, it will drop significantly the memory consumption of the dataset and the execution time. It's important to mention the fact that for the model, it will be the same having a 'csr_matrix' or the original dataset. The output will be the same (same results).
    
  - ## Online Sparse Feature Selection
    - Definition: Online sparse feature selection is a machine learning technique that allows you to select the most important features in your data as you receive new data over time.

    - Simpler terms: In simpler terms, let's say you have a dataset with a lot of features (or variables) that you think might be important for making predictions about some outcome. With online sparse feature selection, you can feed in your data one example at a time and the algorithm will automatically decide which features are most useful for making accurate predictions.

  - ## The Markov blanket
    - Definition: The Markov blanket of a node in a Bayesian network is a set of nodes that contains all the information you need to know in order to predict the value of that node, and nothing more. 

    - Simpler terms: Think of a node as a person, and the other nodes in the network as their friends. The Markov blanket of a person is the set of their friends who know everything about them that is relevant to predicting their behavior or decision-making, but nothing more. By knowing only the information about the person contained in their Markov blanket, you can predict their behavior with a high degree of accuracy.

    - Usage: In ML, it's used for feature selection and causal inference, as it helps identify which variables are most relevant for predicting the value of a particular variable, and which variables are causally related to each other.
  

---

# Papers
  - ## Feature Selection
    - **Checked**
       1. Choosing SNPs with Feature Selection: [[paper]](https://pubmed.ncbi.nlm.nih.gov/16819782/)
       2. Univariate Feature Selection: [[paper]](https://www.frontiersin.org/articles/10.3389/fgene.2021.611506/full)

  - ## Phenotype Prediction
    - **Checked**
       1. SeqBreed: Evaluate genomic prediction in complex scenarios [[code]](https://github.com/miguelperezenciso/SeqBreed/tree/1fe862577c678c472f50e7544c16944dc987bf82) [[paper]](https://www.biorxiv.org/content/10.1101/748624v1) :warning:
       2. deepManReg: Predict phenotypes from multi-modal data. [[paper]](https://www.nature.com/articles/s43588-021-00185-x) [[code]](https://github.com/daifengwanglab/deepManReg)
       3. GWAS DCNN Soybean: [[paper]](https://www.frontiersin.org/articles/10.3389/fgene.2019.01091/full) [[code]](https://github.com/kateyliu/DL_gwas)
       4. MKLMM: Multikernel linear mixed models for complex phenotype prediction [[code]](https://github.com/omerwe/MKLMM)[[paper]](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4937570/) 
       5. Random Matrix: Applications Of Random Matrix Theory In Statistics And Machine Learning [[paper]](https://repository.upenn.edu/cgi/viewcontent.cgi?article=5932&context=edissertations)
       6. PCA Number of Components: Selecting the number of components in PCA via random signflips [[paper]](https://arxiv.org/abs/2012.02985)
       7. Online Sparse Feature Selection [[paper]](https://icml.cc/Conferences/2010/papers/238.pdf)
    
    
    - **Unchecked**
      1. https://bmcbioinformatics.biomedcentral.com/articles/10.1186/s12859-020-3427-8
      2. https://link.springer.com/article/10.1007/s10994-019-05848-5
      3. https://www.nature.com/articles/s41598-019-40561-2
      4. https://www.nature.com/articles/s41467-021-25893-w
      5. https://bmcbioinformatics.biomedcentral.com/articles/10.1186/s12859-021-04077-9
      6. https://www.biorxiv.org/content/10.1101/2021.05.27.446033v1 
    
  - ## PRS
    - **Checked**
      1. Guide to PRS analyses: [[paper]](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7612115/) [[code]](https://choishingwan.github.io/PRS-Tutorial/) [[reference to our tutorials]](https://github.com/AI-sandbox/Getting-Started/blob/main/video_tutorial.md)
      2. Inferred relatives: Exploiting phenotypes from inferred relatives. [[paper]](https://www.nature.com/articles/s41467-020-16829-x) [[code]](https://github.com/bulik/ldsc)
      3. Non-linearities PRS. [[paper]](https://www.medrxiv.org/content/10.1101/2021.07.09.21260288v1.full)
      4. Improve gene score prediction. [[paper]](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5627249/)
 
    - **Unchecked**
      1. https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6456317/
      2. https://www.sciencedirect.com/science/article/abs/pii/S0168952521001451
      3. https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5726434/
    
  - ## Multi-ethnicity // Cross-Ethnicity
    - **Checked**
      1. Cardiovascular disease risk prediction: [[paper]](https://www.nature.com/articles/s41746-020-00331-1)[[code]](https://github.com/atward424/ASCVD_ML/)
      2. Predict ethnicity using personal name Canada.[[paper]](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0241239) [[code]](https://github.com/kaionwong/ethnicity-ml-prediction)
      3. Transfer Learning: Multiethnic Polygenic Risk Prediction in Diverse Populations [[paper]](https://www.biorxiv.org/content/10.1101/2022.03.30.486333v1.full.pdf) [[code]](https://github.com/mxxptian/TL-Multi.gi) :warning:
      
    - **Unchecked**
      
     
    
  - ## Machine Learning
    - **Checked**
      1. Cardiovascular disease risk prediction: [[paper]](https://www.nature.com/articles/s41746-020-00331-1)[[code]](https://github.com/atward424/ASCVD_ML/)  
      
    - **Unchecked**
      1. https://pubmed.ncbi.nlm.nih.gov/28794054/ 

- ## Neural Networks
    - **Checked**
      1. Neural Networks Models with Applications to Genetic Studies UK BIOBANK. [[paper]](https://www.proquest.com/openview/61637c22f25bb23a85eec1c4b157ce71/1?pq-origsite=gscholar&cbl=18750&diss=y) [[code]](https://github.com/szhang0629/FNN)
      
    - **Unchecked** 
- ## Computational
    - **Checked**
      1. Deep Learning on Computational-Resource-Limited Platforms (DeepX): [[paper]](https://www.hindawi.com/journals/misy/2020/8454327/)
      
- ## Gene-to-Gene Interactions
   - **Epistasis**
      1. A computationally fast measure of epistasis for 2 SNPs and a categorical phenotype: [[paper]](https://pubmed.ncbi.nlm.nih.gov/21097157/)

   - **Genetic Association**
      1. Prioritize and Select SNPs for Association Studies with Multi-Stage Designs: [[paper]](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3326652/)
   - **Haplotypes**
      1. Allele combinations along a chromosome for a gene to provide more info than a single SNP: [[paper]](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2979315/)
      2. The complex interplay among factors that influence allelic association (Zondervan and Cardon 2004): [[paper]](https://pubmed.ncbi.nlm.nih.gov/14735120/)
<p>The two main approaches to haplotype construction are either choosing SNPs within (intra) or across (inter) LD bins, thus producing a higher-order haplotype. The intra-LD bin haplotypes are a set of alleles together on the same chromosome surrounded by recombination hotspots defined by a correlation threshold. Higher-order haplotypes use tagging SNPs (tSNP) to capture all variation at a given LD level. The crucial subset of markers to type would be those that distinguish one haplotype from another (Zondervan and Cardon 2004). Also, many methods use windowing strategies which test sets of perhaps contiguous SNPs.</p>
