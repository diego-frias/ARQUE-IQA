# IQA Datasets

Due to licensing restrictions and file size limits, the original images and subjective scores (MOS/DMOS) for the datasets evaluated in ARQUE are not included in this repository.

To reproduce the benchmark, please download the datasets from their official sources and extract them into this directory following the structure below.

## Official Sources
* **LIVE Image Quality Assessment Database:** [Release 2](http://live.ece.utexas.edu/research/quality/subjective.htm)
* **CSIQ (Categorical Subjective Image Quality):** [Official Page](https://s2.smu.edu/~eallen/research/iq/index.html)
* **TID2013 (Tampere Image Database):** [Official Page](http://www.ponomarenko.info/tid2013.htm)

## Required Folder Structure

After downloading, ensure your `datasets/` folder looks exactly like this:

```text
datasets/
├── LIVE/
│   ├── dmos.mat
│   ├── refimgs/
│   ├── jp2k/
│   ├── jpeg/
│   ├── wn/
│   ├── gblur/
│   └── fastfading/
├── CSIQ/
│   ├── csiq_scores_by_image.csv
│   ├── src_imgs/
│   └── dst_imgs/
│       ├── awgn/
│       ├── blur/
│       ├── jpeg/
│       └── jpeg2000/
└── TID2013/
    ├── mos_with_names.txt
    ├── reference_images/
    └── distorted_images/

Note: The ARQUE benchmark script automatically maps the naming conventions of each dataset into standardized categories (e.g., awgn to wn, blur to gblur).

