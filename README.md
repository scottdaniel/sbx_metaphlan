# sbx-metaphlan

[Sunbeam] extension for running [MetaPhlAn2], adapted from
@zhaoc1's [sunbeam_neutrino](https://github.com/PennChopMicrobiomeProgram/sunbeam_neutrino).

## Installation

    git clone https://github.com/ressy/sbx_metaphlan
    cat sunbeam/extensions/sbx_metaphlan/config.yml >> sunbeam_config.yml

## Running

This extension uses an [isolated Conda environment] for the MetaPhlAn2
installation, so you need to include the `--use-conda` argument when running
Sunbeam:

    sunbeam run --configfile=sunbeam_config.yml --use-conda all_metaphlan

[Sunbeam]: https://github.com/sunbeam-labs/sunbeam
[MetaPhlAn2]: https://bitbucket.org/biobakery/metaphlan2
[isolated Conda environment]: http://snakemake.readthedocs.io/en/stable/snakefiles/deployment.html#integrated-package-management
