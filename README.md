# sbx-metaphlan

[Sunbeam] extension for running [MetaPhlAn2], adapted from
[zhaoc1](https://github.com/zhaoc1)'s
[sunbeam_neutrino](https://github.com/PennChopMicrobiomeProgram/sunbeam_neutrino).

## Installation

    git clone https://github.com/sunbeam-labs/sbx_metaphlan
    cat sunbeam/extensions/sbx_metaphlan/config.yml >> sunbeam_config.yml

## Running

This extension uses an [isolated Conda environment] for the MetaPhlAn2
installation, so you need to include the `--use-conda` argument when running
Sunbeam:

    sunbeam run --configfile=sunbeam_config.yml --use-conda all_metaphlan

*Alternatively*

You can pre-install the conda environment like so:

    conda create -n metaphlan -c bioconda bowtie2 metaphlan2=2.7.5

And then uncomment the lines in the sbx_metaphlan.rules file that look like this:

    #conda activate metaphlan

~The default MetaPhlAn2 database will be downloaded and stored inside the
original Sunbeam Conda environment in `$CONDA_PREFIX/opt/metaphlan_databases`.~

The database does not download correctly because this version is obsolete.

You might find a copy here: `/mnt/isilon/microbiome/analysis/biodata/metaphlan_databases`

[Sunbeam]: https://github.com/sunbeam-labs/sunbeam
[MetaPhlAn2]: https://bitbucket.org/biobakery/metaphlan2
[isolated Conda environment]: http://snakemake.readthedocs.io/en/stable/snakefiles/deployment.html#integrated-package-management
