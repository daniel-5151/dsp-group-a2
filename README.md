# DSP Project Group A2

## Pipeline Explanation

**TOPSAR Split**:
A single SLC consists of 3 swaths with each 9 subswaths making for a really big area (almost the entirety of The Netherlands and a small part of Germany). This step selects the swath and subswath(s) that covers the area of interest. This drastically decreases the file sizes and computational loads.

**Apply Orbit File**:
This data contains the information about the position of the satalite during the acquisition. It is applied to the metadata of each image.

**Subset**:
Further zooms the scene in to decrease computational load. This subset now covers almost the entirety of Amsterdam.

**Back-Geocoding**:
Creates a stack of all the SAR images. These images are co-registered (exactly aligned) by using the information in the orbit file and with a pre-existing Digital Elevation Model (DEM). This is because satalite images can be obtained at different angles and location. 

**Interferogram Formation**:
This is one of the most important steps in detecting surface deformations. A reference image is compared to a secondary image and the change in phase is calculated. The output of each image pair shows the difference in signal phase received by the satalite, which might indicate deformations are taking place.

**Coherence/correlation**:
For each image pair in the interferogram formation, a coherence estimation is also made. This shows where both images have strong simularities and are thus good locations for detecting deformations. Poor coherence on the other hand can produce poor and noisy results.

****


