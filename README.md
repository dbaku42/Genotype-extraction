# Genotype-extraction
This repository contains a Bash script that uses bcftools to extract genotype data from VCF files and encode them as 0, 1, or 2, based on the number of alternate alleles. The output is a matrix with rsIDs as rows and samples as columns, suitable for downstream genetic analyses and machine learning workflows.

# Features
Extracts genotype calls (GT) from a VCF file using bcftools.
Encodes genotypes as:
0 = homozygous reference (e.g., 0/0)
1 = heterozygous (e.g., 0/1, 1/0)
2 = homozygous alternate (e.g., 1/1)
Outputs a matrix: rows = rsIDs, columns = samples
Designed for high-throughput genomic data

# Requirements
bash (Unix-like environment)
bcftools (v1.10 or higher recommended)
Indexed VCF file (.vcf.gz and .tbi)

# No installation required. Just clone the repository:
git clone https://github.com/dbaku42/genotype-matrix-extractor.git
cd genotype-matrix-extractor

# Usage
bash extract_genotype_matrix.sh input.vcf.gz output_matrix.tsv

# Arguments:
input.vcf.gz: Your compressed and indexed VCF file.

output_matrix.tsv: Output genotype matrix file (TSV format).

