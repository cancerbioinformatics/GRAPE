# GRAPE - Guys bReast cAncer lymPh nodEs

This repo contains all documentation for the GRAPE dataset hosted on AWS

- Dataset Size: 0TB
- Contact Name: Gregory Verghese
- Institution name: Kings's College London
- Institution URL: http://cancerbioinformatics.co.uk/
- Download at AWS: https://registry.opendata.aws/GRAPE/
- Contact email: [Gregory Verghese](gregory.verghese.@kcl.ac.uk)

## Description

This is a retrospective dataset of H&E-stained whole slide image (WSI) lymph nodes from breast cancer patients. The cohort consisted of 177 patients (122 LN-positive - metastasis was reported in at least 1 LN - and 55 LN-negative patients) with invasive breast carcinoma treated between 1984 and 2002 at Guy’s Hospital London, UK. Slides were scanned and digitised at 40x magnification (0.23 µm/pixel), NanoZoomer H.T2.0 2.0-HT (Hamamatsu Photonics UK, Ltd, Welwyn Garden City, UK).

## Data structure

Patients indexed with KCL001 format. Each folder contains WSIs for a single patient.

``` bash
.
└── GRAPE
    ├── KCL001
    │   ├── kcl001_1.ndpi
    │   └── kcl001_2.ndpi
    ├── KCL002
    │   ├── kcl002_1.ndpi
    │   ├── kcl002_2.ndpi
    │   └── kcl002_3.ndpi
    └── KCL003
        └── kcl003_1.ndpi
```

## Example usage

Below code demonstrates how to load WSIs programmatically using Python Openslide package
 
 ```python
import openslide
import numpy as np
import matplotlib.pyplot as plt

#Read WSI
wsi = openslide.OpenSlide("/Path/to/wsi.ndpi")

#Get slide properties
dims=wsi.dimensions
x_resolution=wsi.properties[openslide.PROPERTY_NAME_MPP_X]
y_resolution=wsi.properties[openslide.PROPERTY_NAME_MPP_X]
base_mag=wsi.properties[openslide.PROPERTY_NAME_OBJECTIVE_POWER]

#Display thumbnail
wsi_thumbnail = wsi.get_thumbnail((1000,1000))
wsi_thumbnail=np.array(wsi_thumbnail)
plt.imshow(wsi_thumbnail)
plt.axis('off')
```

![](wsi.png)


## Credits

If you find the data useful, please cite the below paper:

    @inproceedings{,
        title={},
        booktitle={},
        author={},
        year={}
    }




