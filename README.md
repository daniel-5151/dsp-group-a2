# DSP Project Group A2

## Pipeline Explanation

**TOPSAR Split**:
A single SLC consists of 3 swaths with each 9 subswaths making for a really big area (almost the entirety of The Netherlands and a small part of Germany). This step selects the swath and subswath(s) that covers the area of interest. This drastically decreases the file sizes and computational loads.

**Apply Orbit File**:
Calculates the precise orbit data and include it in the scene.

**Subset**:
Further zooms the scene in to decrease computational load. This subset now covers almost the entirety of Amsterdam.

**Back-geocoding**:
Creates a stack of all the SAR images. These images are precisly aligned. It also performs a few other pre-processing steps and corrections to improve geolocation accuracy.

**Interferogram formation**:

