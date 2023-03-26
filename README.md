# GRAPE - Guys bReast cAncer lymPh nodEs

This repo contains all documentation for the GRAPE dataset hosted on AWS

- Dataset Size: 0TB
- Contact Name: Gregory Verghese
- Institution name: Kings's College London
- Institution URL: [url_cb]: http://cancerbioinformatics.co.uk/
- Download at AWS: https://registry.opendata.aws/GRAPE/
- Contact email: [Gregory Verghese](gregory.verghese.@kcl.ac.uk)

## Description

This is a retrospective dataset of H&E-stained whole slide image (WSI) lymph nodes from breast cancer patients. The cohort consisted of 177 patients (122 LN-positive (metastasis was reported in at least 1 LN) and 55 LN-negative patients) with invasive breast carcinoma treated between 1984 and 2002 at Guy’s Hospital London, UK. Slides were scanned and digitised at 40x magnification (0.23 µm/pixel), NanoZoomer H.T2.0 2.0-HT (Hamamatsu Photonics UK, Ltd, Welwyn Garden City, UK).

## Data structure

## Example usage

Below code demonstrates how to load WSIs programmatically using Python openslide package
 
 ```python
# Read data

import openslide

wsi = openslide.OpenSlide("/Path/to/wsi.ndpi")
wsi_thumbnail = wsi.get_thumbnail((1000,1000))

dims=wsi.dimensions
```

## Credits

If you find the data useful, please cite the below paper:

    @inproceedings{,
        title={},
        booktitle={},
        author={},
        year={}
    }




