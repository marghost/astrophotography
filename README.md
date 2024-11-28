# :telescope: Astrophotography
This repo will be used to share my passion of astrophotography.  I will share my projects and the techniques I use to process my space clichés.

## Project Gallery :star:
<details>

<summary>M 42 (The Orion Nebula) 2024</summary>

## M 42
### Project Details
> **Common name:** Orion Nebula
>
> **Date:** 2024-11-13
>
> **Gear:** Seestar S50
>
> **Filter:** Light Pollution Filter
>
> **Temp:** 7.875c
>
> **Exposure:** 10s
>
> **Number of stacked frames:** 275
>
> **Pre-processing:** Seestar Mosaic

### Processed Image
![Stacked_275_mosaic_M42_10.0s_LP_20241113-013043_graxpert_denoised_colorcalibrated_starnet_stretched_gimp.jpg](https://github.com/marghost/astrophotography/blob/main/imgs/processed/Stacked_275_mosaic_M42_10.0s_LP_20241113-013043_graxpert_denoised_colorcalibrated_starnet_stretched_gimp.jpg?raw=true)

### Processing results "Before and After"
![m42_before_after.png](https://github.com/marghost/astrophotography/blob/main/imgs/beforeafter/m42_before_after.png?raw=true)

</details>
<details>

<summary>M 17 (Omega Nebula) 2024</summary>

## M 17
### Project Details
> **Common name:** Orion Nebula
>
> **Date:** 2024-08-30
>
> **Gear:** Seestar S50
>
> **Filter:** IRCut
>
> **Temp:** 22c
>
> **Exposure:** 10s
>
> **Number of stacked frames:** 161
>
> **Pre-processing:** Siril seestar pre-processing script

### Processed Image
![M_17_161x10sec_T22degC_2024-08-30_graxpert_denoised_colorcorrected_siril_gimp_v2.jpg](https://github.com/marghost/astrophotography/blob/main/imgs/processed/M_17_161x10sec_T22degC_2024-08-30_graxpert_denoised_colorcorrected_siril_gimp_v2.jpg?raw=true)

### Processing results "Before and After"
![m17_before_after_v2.png](https://github.com/marghost/astrophotography/blob/main/imgs/beforeafter/m17_before_after_v2.png?raw=true)

</details>
<details>

<summary>IC 405 (The Flaming Star Nebula) 2024</summary>

## IC 405
### Project Details
> **Common name:** The Flaming Star Nebula
>
> **Date:** 2024-11-26
>
> **Gear:** Seestar S50
>
> **Filter:** Light Pollution Filter
>
> **Temp:** 15c
>
> **Exposure:** 10s
>
> **Number of stacked frames:** 91
>
> **Pre-processing:** Siril seestar pre-processing script

### Processed Image
![IC_405_91x10sec_T15degC_2024-11-266_stackingscript_graxpert_denoised_siril_gimp_graxpert_denoised.jpg](https://github.com/marghost/astrophotography/blob/main/imgs/processed/IC_405_91x10sec_T15degC_2024-11-266_stackingscript_graxpert_denoised_siril_gimp_graxpert_denoised.jpg?raw=true)

### Processing results "Before and After"
![IC405_before_after.png](https://github.com/marghost/astrophotography/blob/main/imgs/beforeafter/IC405_before_after.png?raw=true)

</details>

## Processing Workflows :rocket:
<details>

<summary>Seestar S50 Pre-processing and Post-processing workflows</summary>

## Seestar S50 Photo processing
This is my current astrophotography photo processing flow.  For mosaic mode, i skip the pre-processing stacking script and work directly with the processed fits file compiled by the Seestar s50.  If using regular mode, the stacking script tend to do a better job at stacking the subframes.  It also has less artefacts.

**Updated:** 2024/11/14 

## Pre-processing stack with Siril script

1. [Download the script to preprocess your images](https://gitlab.com/free-astro/siril-scripts/-/raw/main/preprocessing/Seestar_Preprocessing.ssf)
We’ve created a script tailored to the pre-processing of your seestar. This means that this script expects to have several images which it will stack. In the current version of Siril, you need to download it manually by following this link . Place the downloaded file (Seestar_Preprocessing.ssf) in the location of your choice, then in Siril’s preferences, in the script tab, enter the folder you have chosen.

2. Create the folder to hold your images
The seestar only gives access to light images. Calibration is therefore not possible. All you need to do is create a "lights" directory in the folder where your images are stored.

3. Put your RAW images in the directory created in the previous step
Attention: don’t mix other files, even JPEG (or other formats), with your RAW files: Siril will take all the files inside the directories as input files for processing.

4. Click on the home button and navigate to your project folder

5. Click on the Scripts button and select the script of your choice

Source: https://siril.org/tutorials/seestar/ Processing ZWO Seestar S50 images

## Graxpert
### Crop
![crop.png](https://github.com/marghost/astrophotography/blob/main/imgs/crop.png?raw=true)

### Background Extraction
![backgroundextraction.png](https://github.com/marghost/astrophotography/blob/main/imgs/backgroundextraction.png?raw=true)

### Deconvolution
1. Play with Deconvolution Strength.  Default 0.5 tend to be fine.
![deconvolution.png](https://github.com/marghost/astrophotography/blob/main/imgs/deconvolution.png?raw=true)

2. How to find the FHWM value.
To choose "Image FHWM" value, look at this value inside Siril and calculate the value inbetween.
![FWHM.png](https://github.com/marghost/astrophotography/blob/main/imgs/FWHM.png?raw=true)

### Denoising
![denoising.png](https://github.com/marghost/astrophotography/blob/main/imgs/denoising.png?raw=true)

## Siril
### Color Calibration
![colorcalibration.png](https://github.com/marghost/astrophotography/blob/main/imgs/colorcalibration.png?raw=true)

### Remove Green Noise
![removegreennoise.png](https://github.com/marghost/astrophotography/blob/main/imgs/removegreennoise.png?raw=true)

### Starnetv2 Star Removal
![removestars.png](https://github.com/marghost/astrophotography/blob/main/imgs/removestars.png?raw=true)
When done, open starless fit file in siril

### Stretch Nebula/Galaxy
Do **small** stretches inside the histogram transformation tool.  Repeat as many time as needed.
![histogram.png](https://github.com/marghost/astrophotography/blob/main/imgs/histogram.png?raw=true)

### Color Saturation
![colorsaturation.png](https://github.com/marghost/astrophotography/blob/main/imgs/colorsaturation.png?raw=true)

### Star Recomposition
**Important** save your fit file right now before opening Star Recomposition.
![starrecomposition.png](https://github.com/marghost/astrophotography/blob/main/imgs/starrecomposition.png?raw=true)

### Noise Reduction
![noisereduction.png](https://github.com/marghost/astrophotography/blob/main/imgs/noisereduction.png?raw=true)

### Save renamed fits + tif
- Fits file for backup of the processed image
- Tif for manipulating in GIMP

## GIMP
### Color > Curves
![curves.png](https://github.com/marghost/astrophotography/blob/main/imgs/curves.png?raw=true)

### Filters > Enhance > Sharpen
![sharpen.png](https://github.com/marghost/astrophotography/blob/main/imgs/sharpen.png?raw=true)

### Export final product in jpg

## Tools
- https://siril.org/
- https://gitlab.com/free-astro/siril-scripts/-/raw/main/preprocessing/Seestar_Preprocessing.ssf (Siril pre-processing script)
- https://graxpert.com/
- https://www.starnetastro.com/ (Starnetv2CLI for Siril integration)
- https://www.gimp.org/

## Sources
- https://siril.org/tutorials/seestar/ Processing ZWO Seestar S50 images
- https://youtu.be/syCVl1fDLTk Pre-processing Seestar Data with Siril
- https://www.youtube.com/watch?v=lMoSAHOgbD4 Advanced Processing -Cuiv

</details>

<details>

<summary>Seestar S50 Post-processing RAW Avi of the Moon</summary>

## A combinaison of PIPP - Autostakkert - Registax6
##PIPP
PIPP will help remove the Moon shifting when taking longer exposure.
- Drag&Drop avi to PIPP
- Do not debayer if asked to
- Select "Solar/Lunar Full Disk"
- Opened picture > click on update image
- Output Options > select SER formats
- Do Processing
- Start Processing

## Autostakkert
- Open SER file
- Select Analyse.  Look at quality graph
- Choose acceptable value when green curve pass under middle blue.
- Go to other panel.  Set AP Size to 200 and click place AP grid.
- Stack

## Registax6
- Still working on this part.

## Source
- https://www.youtube.com/watch?v=8Iyr5W38ZN8 Moon Processing PIPP & Autostakkert

</details>

# Licence
[![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]

This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg