[![Abcdspec-compliant](https://img.shields.io/badge/ABCD_Spec-v1.1-green.svg)](https://github.com/brain-life/abcd-spec)
[![Run on Brainlife.io](https://img.shields.io/badge/Brainlife-bl.app.9-blue.svg)](https://doi.org/10.25663/bl.app.9)

# DIPY Workflow Wrapper

This is a Brainlife wrapper App for the [`dipy_fit_dki`](https://dipy.org/documentation/1.1.1./reference_cmd/dipy_fit_dki/) workflow. This single wrapper is exposed through an App registered on [brainlife.io](https://brainlife.io).

- More information about DIPY : [dipy.org](https://dipy.org/)
- More information about the command line: [`dipy_fit_dki`](https://dipy.org/documentation/1.1.1./reference_cmd/dipy_fit_dki/)

### Authors
- [Javier Guaje](https://github.com/guaje)
- [Serge Koudoro](https://github.com/skoudoro)

### Funding Acknowledgement
DIPY is publicly funded and for the sustainability of the project it is helpful to Acknowledge the use of the software. We kindly ask that you acknowledge the funding below in your publications and code reusing this code.

[![NIH-NIBIB-R01EB027585](https://img.shields.io/badge/NIH_NIBIB-R01EB027585-green.svg)](https://grantome.com/grant/NIH/R01-EB027585-01)
[![NIH-NIMH-RF1MH121868](https://img.shields.io/badge/NIH_NIMH-RF1MH121868-green.svg)](https://grantome.com/grant/NIH/RF1-MH121868-01)
[![NIH-NIMH-R01MH108467](https://img.shields.io/badge/NIH_NIMH-R01MH108467-green.svg)](https://grantome.com/grant/NIH/R01-MH108467-01)
[![NSF-BCS-1734853](https://img.shields.io/badge/NSF_BCS-1734853-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=1734853)
[![NSF-EEC-1720625](https://img.shields.io/badge/NSF_BCS-1720625-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=1720625)
[![NSF-OAC-1916518](https://img.shields.io/badge/NSF_OAC-1916518-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=1916518)
[![NSF-IIS-1912270](https://img.shields.io/badge/NSF_IIS-1912270-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=1912270)
[![NSF-IIS-1636893](https://img.shields.io/badge/NSF_IIS-1636893-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=1636893)

### Citations
We kindly ask that you cite the following article and the articles in the following [link](https://dipy.org/documentation/1.1.1./reference_cmd/dipy_fit_dki/) when publishing papers and code using this code.

1. Avesani, P., McPherson, B., Hayashi, S. et al. The open diffusion data derivatives, brain data upcycling via integrated publishing of derivatives and reproducible open cloud services. Sci Data 6, 69 (2019). [https://doi.org/10.1038/s41597-019-0073-y](https://doi.org/10.1038/s41597-019-0073-y)

## Running the App

### On Brainlife.io

You can see a list of [DIPY Apps currently registered on Brainlife](https://brainlife.io/apps#dipy). Find the App that you'd like to run and click "Execute".

### Running Locally (on  your machine)

To run this command, you can simply type:

```bash
singularity exec -e docker://brainlife/dipy:1.1.1 dipy_fit_dki [your_args]
```

## Input

To see the documentation of all the arguments, follow this [link](https://dipy.org/documentation/1.1.1./reference_cmd/dipy_fit_dki/).

## Output

All output files will be generated according to the passed arguments, as explained [here](https://dipy.org/documentation/1.1.1./reference_cmd/dipy_fit_dki/).

### Dependencies

This App requires [singularity](https://www.sylabs.io/singularity/) to run.

#### DIPY is licensed under the terms of the BSD license. Please see the [LICENSE file](https://github.com/dipy/dipy/blob/master/LICENSE).
