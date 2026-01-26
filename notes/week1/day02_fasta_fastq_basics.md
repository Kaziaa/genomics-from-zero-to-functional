


genomics-from-zero-to-functional
===





## Week 1 – Day 1: Setup & Genomics Mindset

### Week 1 Objective
By the end of Week 1, I will:
- Understand FASTA, FASTQ, and GTF as text files
- Use `grep`, `awk`, `cut`, `sort`, `uniq`, and pipes confidently
- Extract biologically meaningful information from raw genomic files
- Produce daily outputs and commit them to GitHub

---

## Day 2 — FASTA and FASTQ Basics

### Goal
Understrand how sequencing data is strucutres and how to inspect it using basic UInix tools( **grep**, **wc**, **awk**)

### Files / Data
- Human_chr22.fasta -Human chromosome 22 (GRCh38 reference gemone)

### Commands / Code
#### count number of sequences: 
    grep -c "^>" human_chr22.fasta

#### Extract FASTA Headers
    grep "^>" human_chr22.fasta


#### Calculate total sequence length 
    awk ' 
    /^>/ {next} 
    {len += length($0)} 
    END {print len} 
    ' human_chr22.fasta





