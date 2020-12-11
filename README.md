[![Abcdspec-compliant](https://img.shields.io/badge/ABCD_Spec-v1.1-green.svg)](https://github.com/brain-life/abcd-spec)
[![Run on Brainlife.io](https://img.shields.io/badge/Brainlife-bl.app.9-blue.svg)](https://doi.org/10.25663/bl.app.9)

# Dipy Reconstruction Diffusion MRI using DKI

The App uses the Diffusion Kurtosis Imaging (DKI) method to do a reconstruction of the diffusion-weighted magnetic resonance imaging data.

### Authors
- [Serge Koudoro](skoudoro@iu.edu)
- [Javier Ricardo Guaje Guerra](jrguajeg@iu.edu)

### Contributors
- [Soichi Hayashi](soichih@gmail.com)

### Funding Acknowledgement
brainlife.io is publicly funded and for the sustainability of the project it is helpful to Acknowledge the use of the platform. We kindly ask that you acknowledge the funding below in your code and publications. Copy and past the following lines into your repository when using this code.

[![NSF-BCS-1734853](https://img.shields.io/badge/NSF_BCS-1734853-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=1734853)
[![NSF-BCS-1636893](https://img.shields.io/badge/NSF_BCS-1636893-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=1636893)
[![NSF-ACI-1916518](https://img.shields.io/badge/NSF_ACI-1916518-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=1916518)
[![NSF-IIS-1912270](https://img.shields.io/badge/NSF_IIS-1912270-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=1912270)
[![NIH-NIBIB-R01EB029272](https://img.shields.io/badge/NIH_NIBIB-R01EB029272-green.svg)](https://grantome.com/grant/NIH/R01-EB029272-01)

### Citations
We ask that you the following articles when publishing papers that used data, code or other resources created by the brainlife.io community.

1. Garyfallidis, E., Brett, M., Amirbekian, B., Rokem, A., van der Walt, S., Descoteaux, M., Nimmo-Smith, I., & Dipy Contributors (2014). Dipy, a library for the analysis of diffusion MRI data. Frontiers in neuroinformatics, 8, 8. [https://doi.org/10.3389/fninf.2014.00008](https://doi.org/10.3389/fninf.2014.00008)

2. Avesani, P., McPherson, B., Hayashi, S. et al. The open diffusion data derivatives, brain data upcycling via integrated publishing of derivatives and reproducible open cloud services. Sci Data 6, 69 (2019). [https://doi.org/10.1038/s41597-019-0073-y](https://doi.org/10.1038/s41597-019-0073-y)

## Running the App

#### 1. On Brainlife.io

You can see a list of [Dipy Apps currently regsitered on Brainlife](https://brainlife.io/apps#dipy). Find the App that you'd like to run and click "Execute" tab to specify dataset that you'd like to run the App on.

#### 2. On  your machine (Running Locally)

To run this command, you can simply type:

`singularity exec -e docker://brainlife/dipy:1.1.1 dipy_fit_dki [your_args]`

To see the documentation of all arguments, [go to the following page](https://dipy.org/documentation/1.1.1./reference_cmd/dipy_fit_dki/)

## Input

To see the documentation of all the arguments, follow this [link](https://dipy.org/documentation/1.1.1./reference_cmd/dipy_fit_dki/).

## Output

All output files will be generated according to the passed arguments, as explained [here](https://dipy.org/documentation/1.1.1./reference_cmd/dipy_fit_dki/).

### Dependencies

This app runs on [singularity](https://www.sylabs.io/singularity/).

### DIPY
- This is a Brainlife wrapper App stemming from the [`dipy_fit_dki`](https://dipy.org/documentation/latest/reference_cmd/dipy_fit_dki/) workflow.
- This single wrapper is exposed through an apps registered on [Brainlife.io](https://brainlife.io).
- More information about DIPY : [https://dipy.org/](https://dipy.org/).
- More information about the command line `dipy_fit_dki`: [Command line Reference](https://dipy.org/documentation/latest/reference_cmd/dipy_fit_dki/).
