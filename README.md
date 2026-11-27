<h1 align="center">Fit DKI</h1>

<p align="center">
  Fit a Diffusion Kurtosis Imaging model to multishell Diffusion-weighted data (dipy_fit_dki)
</p>

<p align="center">
  <a href="https://github.com/brainlife/abcd-spec"><img src="https://img.shields.io/badge/ABCD_Spec-v1.1-green.svg" alt="ABCD Spec v1.1"></a>
  <a href="https://doi.org/10.25663/bl.app.9"><img src="https://img.shields.io/badge/Brainlife-bl.app.9-blue.svg" alt="Run on brainlife.io"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-see_LICENSE-lightgrey.svg" alt="License"></a>
</p>

## At a glance

<!-- brainlife-app:begin (generated from the App manifest; edit the manifest, not this block) -->

> **Fit a Diffusion Kurtosis Imaging model to multishell Diffusion-weighted data (dipy_fit_dki)**

Wraps the DIPY 1.1.1 dipy_fit_dki workflow to fit a diffusion kurtosis model inside a brain or white matter mask and writes the diffusion and kurtosis tensors with derived scalar maps. Use it to get kurtosis measures (MK, AK, RK) in addition to tensor measures. It requires multi-shell DWI; single-shell data are rejected by the input tag.

| | |
|---|---|
| **Inputs** | `neuro/dwi` · `neuro/mask` |
| **Outputs** | `neuro/tensor` |
| **Container** | `brainlife/dipy:1.1.1` |
| **Resources** | 8 CPUs · 24 GB memory · 10 h walltime |
| **Run it** | [doi.org/10.25663/bl.app.9](https://doi.org/10.25663/bl.app.9) |

#### Inputs

| Input | Datatype | Required | Description |
|---|---|---|---|
| `dwi` | `neuro/dwi` (!single_shell) | yes | This App will only work with multishell datasets. |
| `mask` | `neuro/mask` (brain) | yes | This is normally a white matter mask. But you could also pass the whole brain mask instead if you are interested in tensor measures in the gray matter, for example. |

#### Outputs

| Output | Datatype | Description |
|---|---|---|
| `output` | `neuro/tensor` | DKI fit outputs from dipy_fit_dki: tensors.nii.gz (diffusion tensor), kurtosis.nii.gz (kurtosis tensor) and the scalar maps it writes (FA, MD, AD, RD, MK, AK, RK and others). |

<details>
<summary><b>Parameters</b> (1)</summary>

| Parameter | Type | Default | Description |
|---|---|---|---|
| `b0_threshold` | number | `50` | b-value at or below which volumes are treated as b=0 (dipy_fit_dki --b0_threshold). |

</details>

<!-- brainlife-app:end -->

## Running the App

### On brainlife.io

Open the App at [doi.org/10.25663/bl.app.9](https://doi.org/10.25663/bl.app.9), choose `neuro/dwi`, `neuro/mask` from your project, set the parameters and press **Execute**. The results are saved to your project as `neuro/tensor`.

### Locally

You need [Singularity/Apptainer](https://apptainer.org/) (the App runs in `brainlife/dipy:1.1.1`), [`jq`](https://jqlang.github.io/jq/).

1. Clone this repository.
2. Create `config.json` with the paths to your inputs and the parameters:

   ```json
   {
       "bvecs": "/path/to/dwi/bvecs",
       "bvals": "/path/to/dwi/bvals",
       "dwi": "/path/to/dwi/dwi",
       "mask": "/path/to/mask/mask",
       "b0_threshold": 50
   }
   ```

3. Run `./main`.

## DIPY

- This is a Brainlife wrapper App stemming from the [`dipy_fit_dki`](https://dipy.org/documentation/latest/reference_cmd/dipy_fit_dki/) workflow.
- This single wrapper is exposed through an apps registered on [Brainlife.io](https://brainlife.io).
- More information about DIPY : [https://dipy.org/](https://dipy.org/).
- More information about the command line `dipy_fit_dki`: [Command line Reference](https://dipy.org/documentation/latest/reference_cmd/dipy_fit_dki/).

## Citing

If you use this App, please cite it, the software it builds on and brainlife.io:

- Fit DKI. brainlife.io App. [doi:10.25663/bl.app.9](https://doi.org/10.25663/bl.app.9)
- Garyfallidis E, Brett M, Amirbekian B, et al. Dipy, a library for the analysis of diffusion MRI data. Front Neuroinform 8:8 (2014). [doi:10.3389/fninf.2014.00008](https://doi.org/10.3389/fninf.2014.00008)
- Hayashi S, Caron BA, Heinsfeld AS, et al. brainlife.io: a decentralized and open-source cloud platform to support neuroscience research. *Nature Methods* 21:809–813 (2024). [doi:10.1038/s41592-024-02237-2](https://doi.org/10.1038/s41592-024-02237-2)
- Avesani P, McPherson B, Hayashi S, et al. The open diffusion data derivatives, brain data upcycling via integrated publishing of derivatives and reproducible open cloud services. *Scientific Data* 6:69 (2019). [doi:10.1038/s41597-019-0073-y](https://doi.org/10.1038/s41597-019-0073-y)

## Authors

- Serge Koudoro
- Javier Ricardo Guaje Guerra

**Contributors**

- Soichi Hayashi

## Funding

[![Wellcome-226486/Z/22/Z](https://img.shields.io/badge/Wellcome-226486%2FZ%2F22%2FZ-purple.svg)](https://wellcome.org/)
[![NIH-NINDS-U24NS140384](https://img.shields.io/badge/NIH_NINDS-U24NS140384-green.svg)](https://reporter.nih.gov/project-details/11261037)
[![NIH-NINDS-UM1NS132207](https://img.shields.io/badge/NIH_NINDS-UM1NS132207-green.svg)](https://reporter.nih.gov/project-details/11411328)
[![NIH-NIBIB-R01EB029272](https://img.shields.io/badge/NIH_NIBIB-R01EB029272-green.svg)](https://reporter.nih.gov/project-details/10262925)
[![NIH-NIBIB-R01EB030896](https://img.shields.io/badge/NIH_NIBIB-R01EB030896-green.svg)](https://reporter.nih.gov/project-details/10428625)
[![NIH-NIMH-R01MH126699](https://img.shields.io/badge/NIH_NIMH-R01MH126699-green.svg)](https://reporter.nih.gov/project-details/10460628)
[![NIH-NIDCD-R01DC020088](https://img.shields.io/badge/NIH_NIDCD-R01DC020088-green.svg)](https://reporter.nih.gov/project-details/11140284)
[![NSF-BCS-1734853](https://img.shields.io/badge/NSF_BCS-1734853-blue.svg)](https://www.nsf.gov/awardsearch/showAward?AWD_ID=1734853)
[![NSF-BCS-2203524](https://img.shields.io/badge/NSF_BCS-2203524-blue.svg)](https://www.nsf.gov/awardsearch/showAward?AWD_ID=2203524)
[![NSF-IIS-1636893](https://img.shields.io/badge/NSF_IIS-1636893-blue.svg)](https://www.nsf.gov/awardsearch/showAward?AWD_ID=1636893)
[![NSF-OAC-2148729](https://img.shields.io/badge/NSF_OAC-2148729-blue.svg)](https://www.nsf.gov/awardsearch/showAward?AWD_ID=2148729)
[![NSF-IIS-1912270](https://img.shields.io/badge/NSF_IIS-1912270-blue.svg)](https://www.nsf.gov/awardsearch/showAward?AWD_ID=1912270)
[![NSF-IIS-2148700](https://img.shields.io/badge/NSF_IIS-2148700-blue.svg)](https://www.nsf.gov/awardsearch/showAward?AWD_ID=2148700)
[![NSF-OAC-1916518](https://img.shields.io/badge/NSF_OAC-1916518-blue.svg)](https://www.nsf.gov/awardsearch/showAward?AWD_ID=1916518)

<sub>brainlife.io, which runs this App, is publicly funded by Wellcome, the U.S. National Institutes of Health and the U.S. National Science Foundation; acknowledging that support helps keep it running.</sub>

## License

See [LICENSE](LICENSE).
