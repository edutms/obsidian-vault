Used in data mining and compsci, Min2025-07-17 08:06

### Status: #baby

### Tags: [[machine-learning]]

# MinHash
After using [[Hashing]] techiniques.
Min Hash stands for min-wise independent permutations locality sensitive hashing scheme. It is a technique for quickly estimating how similar two sets are.

It is applied in large-scale clustering problems such as clustering documents by the similarity of their sets of words.


### Applications
The original applications involved clustering and eliminating near-duplicates of web documents (i.e. websites)

Per Wikipedia:
The MinHash algorithm has been adapted for bioinformatics, where the problem of comparing genome sequences has a similar theoretical underpinning to that of comparing documents on the web. MinHash-based tools[[14]](https://en.wikipedia.org/wiki/MinHash#cite_note-:0-14)[[15]](https://en.wikipedia.org/wiki/MinHash#cite_note-15) allow rapid comparison of whole genome sequencing data with reference genomes (around 3 minutes to compare one genome with the 90000 reference genomes in [RefSeq](https://en.wikipedia.org/wiki/RefSeq "RefSeq")), and are suitable for speciation and maybe a limited degree of microbial sub-typing. There are also applications for metagenomics [[14]](https://en.wikipedia.org/wiki/MinHash#cite_note-:0-14) and the use of MinHash derived algorithms for genome alignment and genome assembly.[[16]](https://en.wikipedia.org/wiki/MinHash#cite_note-16) Accurate average nucleotide identity (ANI) values can be generated very efficiently with MinHash-based algorithms.[[17]](https://en.wikipedia.org/wiki/MinHash#cite_note-17)


## Evaluation and benchmarks

[[edit](https://en.wikipedia.org/w/index.php?title=MinHash&action=edit&section=11 "Edit section: Evaluation and benchmarks")]

A large scale evaluation was conducted by [Google](https://en.wikipedia.org/wiki/Google "Google") in 2006 [[20]](https://en.wikipedia.org/wiki/MinHash#cite_note-20) to compare the performance of Minhash and [SimHash](https://en.wikipedia.org/wiki/SimHash "SimHash")[[21]](https://en.wikipedia.org/wiki/MinHash#cite_note-21) algorithms. In 2007 Google reported using Simhash for duplicate detection for web crawling[[22]](https://en.wikipedia.org/wiki/MinHash#cite_note-22) and using Minhash and [LSH](https://en.wikipedia.org/wiki/Locality-sensitive_hashing "Locality-sensitive hashing") for [Google News](https://en.wikipedia.org/wiki/Google_News "Google News") personalization.[[23]](https://en.wikipedia.org/wiki/MinHash#cite_note-23)


# References
https://en.wikipedia.org/wiki/MinHash








