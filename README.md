# humann2
Modified the function of `--metaphlan-option` in humann2 pipeline. Modifications include:
- make `--metaphlan-option` accept `metaphlan2.bowtie2out --input_type bowtie2out`
- If the output of BowTie2 from Metaphlan2 is given, the modified version of humann2 will
    - ignore the option `--bowtie2db METAPHLAN_BOWTIE2_DB` (This seems to make you get 100% unclassified results. Test on MetaPhlAn version 2.7.7)
    - re-running MetaPhlAn by using the BowTie2 output
    - copy the BowTie2 output to the Humann2 temp directory and rename it as `[filename]_metaphlan_bowtie2.txt`

## Installation
```
pip install git+https://github.com/dytk2134/humann2.git
```

## Notes
- This repository was cloned from [humann2](https://bitbucket.org/biobakery/humann2/src/default/).
- For complete documentation, please see the HUMAnN2 User Manual.

## Citations
Franzosa EA*, McIver LJ*, Rahnavard G, Thompson LR, Schirmer M, Weingart G, Schwarzberg Lipson K, Knight R, Caporaso JG, Segata N, Huttenhower C. Species-level functional profiling of metagenomes and metatranscriptomes. Nat Methods 15: 962-968 (2018).