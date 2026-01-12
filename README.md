# Exome-Variant-Analyzer
A Python-based CLI tool for Whole Exome Sequencing (WES) analysis, featuring Ti/Tv ratio quality control, rare variant filtering (AF &lt; 0.01), and biological annotation via MyGene.info.


# Exome-QC-Analyzer 🧬

A Python-based CLI tool to perform quality control and clinical variant prioritization 
on Whole Exome Sequencing (WES) data.

## 🔬 Scientific Rationale
In clinical genomics, identifying disease-causing variants requires filtering through ~20,000 
polymorphisms in an exome. This tool automates:
1. **Technical QC:** Calculates the Ti/Tv ratio to ensure sequencing accuracy.
2. **Clinical Filtering:** Identifies rare (AF < 1%) and high-impact (Nonsense/Frameshift) variants.
3. **Biological Context:** Fetches gene summaries using the MyGene.info API.

## 🛠️ Features
- **Fast VCF Parsing:** Built on `cyvcf2` for high-performance genomic data handling.
- **Automated Reporting:** Generates a text-based clinical summary.
- **Data Visualization:** Produces mutation distribution charts.

## 🚀 Quick Start
### Prerequisites
- Python 3.8+
- `pip install cyvcf2 matplotlib mygene`

### Usage
Run the analyzer on any VCF file from your terminal:
```bash
python scripts/exome_analyzer.py --input data/sample.vcf --output results/report.txt --plot
