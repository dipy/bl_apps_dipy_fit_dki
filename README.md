[![Abcdspec-compliant](https://img.shields.io/badge/ABCD_Spec-v1.1-green.svg)](https://github.com/brain-life/abcd-spec)
[![Run on Brainlife.io](https://img.shields.io/badge/Brainlife-bl.app.9-blue.svg)](https://doi.org/10.25663/bl.app.9)

# Dipy Reconstruction Diffusion MRI using DKI

<!-- brainlife-app:begin (generated from the App manifest; edit the manifest, not this block) -->

> **Fit a Diffusion Kurtosis Imaging model to multishell Diffusion-weighted data (dipy_fit_dki)**

Wraps the DIPY 1.1.1 dipy_fit_dki workflow to fit a diffusion kurtosis model inside a brain or white matter mask and writes the diffusion and kurtosis tensors with derived scalar maps. Use it to get kurtosis measures (MK, AK, RK) in addition to tensor measures. It requires multi-shell DWI; single-shell data are rejected by the input tag.

| | |
|---|---|
| 📥 **Inputs** | `neuro/dwi` · `neuro/mask` |
| 📤 **Outputs** | `neuro/tensor` |
| 🐳 **Container** | `brainlife/dipy:1.1.1` |
| ⚙️ **Resources** | 8 CPUs · 24 GB memory · 10 h walltime |
| 🔗 **Run it** | [doi.org/10.25663/bl.app.9](https://doi.org/10.25663/bl.app.9) |

#### 📥 Inputs

| Input | Datatype | Required | Description |
|---|---|---|---|
| `dwi` | `neuro/dwi` (!single_shell) | yes | This App will only work with multishell datasets. |
| `mask` | `neuro/mask` (brain) | yes | This is normally a white matter mask. But you could also pass the whole brain mask instead if you are interested in tensor measures in the gray matter, for example. |

#### 📤 Outputs

| Output | Datatype | Description |
|---|---|---|
| `output` | `neuro/tensor` | DKI fit outputs from dipy_fit_dki: tensors.nii.gz (diffusion tensor), kurtosis.nii.gz (kurtosis tensor) and the scalar maps it writes (FA, MD, AD, RD, MK, AK, RK and others). |

<details>
<summary><b>⚙️ Parameters</b> (1)</summary>

| Parameter | Type | Default | Description |
|---|---|---|---|
| `b0_threshold` | number | `50` | b-value at or below which volumes are treated as b=0 (dipy_fit_dki --b0_threshold). |

</details>

📚 **References used by this App:**
- Garyfallidis E, Brett M, Amirbekian B, et al. Dipy, a library for the analysis of diffusion MRI data. Front Neuroinform 8:8 (2014). [doi:10.3389/fninf.2014.00008](https://doi.org/10.3389/fninf.2014.00008)

<!-- brainlife-app:end -->

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
