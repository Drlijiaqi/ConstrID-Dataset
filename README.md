# ConstrID-Dataset

ConstrID-Dataset
# 
**ConstrID: A Hybrid Benchmark of Real and Synthetic Images for Construction Worker Re-Identification**

ConstrID-Dataset is a construction-specific person re-identification (ReID) benchmark containing real-world surveillance images and AI-generated synthetic images. It was developed to support academic research on worker identification, cross-camera retrieval, visual tracking, and intelligent construction safety.

> **Access policy:** The dataset is available by application for **academic research and educational use only**. Commercial use is prohibited.

## Highlights

- **5,137 images** of **138 construction worker identities**
- **4,409 real-world images** collected from an active construction site
- **728 manually screened synthetic images** representing 26 virtual identities
- Construction-specific visual conditions, including helmets, reflective vests, similar clothing, changing viewpoints, pose variation, complex backgrounds, lighting variation, and partial occlusion
- DukeMTMC-ReID-compatible filename convention for convenient integration with common ReID frameworks
- A real-image test protocol designed for cross-camera evaluation in construction environments

## Dataset Summary

| Component | Images | Identities | Description |
| --- | ---: | ---: | --- |
| Full dataset | 5,137 | 138 | Real-world and synthetic construction worker images |
| Real-world data | 4,409 | 112 | Images extracted from construction-site surveillance video |
| Synthetic data | 728 | 26 | AI-generated images retained after manual quality screening |
| Training split | 2,787 | 68 | 2,059 real images from 42 identities and 728 synthetic images from 26 identities |
| Gallery/test split | 2,282 | 68 | Real-world images with cross-camera associations |
| Query split | 68 | 68 | One real-world query image per test identity |

The query identities are shared with the gallery/test split. Statistics above follow the dataset description in the published paper.

## Data Collection and Construction

### Real-world images

The real-world portion was collected over six months at a super-high-rise building construction site in Dalian, Liaoning Province, China. The recording system used networked 4-megapixel cameras with 4 mm focal-length lenses. Captured activities include formwork installation, concrete pouring, and rebar tying.

Images of construction workers were extracted from surveillance video using a workflow that combined manual annotation with YOLOv8-assisted detection and cropping. Real-world worker identity numbers range from `9001` to `9112`.

### Synthetic images

The synthetic portion was generated using ChatGPT and Doubao to increase variation in worker appearance, pose, viewpoint, clothing, helmets, reflective vests, and construction activities. All candidate images were manually reviewed. Images with severe anatomical distortion, physically implausible structures, repeated content, inconsistent clothing, or unreasonable safety-equipment configurations were excluded.

The final synthetic subset contains 728 images from 26 virtual identities, numbered from `8001` to `8026`. Synthetic camera labels from `c1` to `c4` represent simulated viewpoint changes rather than physical camera sources.

## File Naming

Images follow the DukeMTMC-ReID naming convention:

```text
<person_id>_c<camera_id>_f<frame_id>.jpg
```

Example:

```text
0001_c2_f0046182.jpg
```

In this example:

- `0001` is the person identity;
- `c2` is the camera identifier; and
- `f0046182` is the frame index.

For real-world images, camera identifiers correspond to the actual source cameras. For synthetic images, camera identifiers represent simulated viewpoints.

## Intended Research Uses

Subject to approval and the conditions below, ConstrID-Dataset may be used for non-commercial academic work involving:

- person re-identification;
- cross-camera worker retrieval;
- multi-object tracking and identity association;
- domain adaptation and transfer learning;
- synthetic-data augmentation;
- representation learning in construction environments; and
- construction safety and intelligent site-management research.

## Requesting Access

The dataset is not provided through a public direct-download link. Researchers who wish to use ConstrID-Dataset must first complete the academic access application form:

**[Download the ConstrID-Dataset Academic Access Application Form](./ConstrID_Dataset_Access_Application_Form.docx)**

Please follow these steps:

1. Download the Word application form.
2. Complete all required fields, including your academic affiliation, contact details, research purpose, intended use, planned methods, expected outputs, access period, and data-management arrangements.
3. Read and accept the academic-only, non-commercial use conditions, then sign and date the declaration.
4. Save the completed form as `FullName_Institution_ConstrID_Application.docx`.
5. Email the completed form as an attachment to [lijiaqi@ustl.edu.cn](mailto:lijiaqi@ustl.edu.cn).

Suggested email subject:

`[ConstrID Access Request] Full Name - Institution`

Submitting a request does not guarantee access. Applications are reviewed by the dataset team, and additional information may be requested.

## Dataset Use Conditions

ConstrID-Dataset is **not** released under an open-source data license. Access is granted only to approved applicants and is subject to the following conditions:

1. **Academic use only.** The dataset, its annotations, derivatives, and models trained on it may be used only for non-commercial academic research or education.
2. **No commercial use.** The dataset may not be used in paid products or services, commercial deployments, fee-based consulting, internal corporate research intended for commercial exploitation, or any other revenue-generating activity.
3. **No redistribution.** You may not publish, upload, sell, sublicense, share, or otherwise provide the dataset or any substantial portion of it to a third party. Collaborators must submit their own access requests unless otherwise authorized in writing.
4. **No harmful identification or surveillance.** The dataset may not be used to identify real individuals, enable harmful profiling, support punitive surveillance, or facilitate unlawful or unethical monitoring.
5. **Privacy and ethics compliance.** Users are responsible for complying with applicable privacy and data-protection laws, institutional ethics requirements, and secure data-handling practices.
6. **Citation required.** Any publication, thesis, report, presentation, or other research output using the dataset must cite the ConstrID paper.
7. **Secure storage.** Access credentials and dataset files must be protected against unauthorized access. Users must delete local copies when access expires or when requested by the dataset team.
8. **No warranty.** The dataset is provided for research purposes without warranties of any kind. Users assume responsibility for their use of the data and any resulting claims or liabilities.

The Creative Commons license applying to the published article does not automatically apply to the dataset. Any use outside these conditions requires prior written permission from the dataset authors.

## Citation

If you use ConstrID-Dataset in your research, please cite:

```bibtex
@article{chen2026constrid,
  title   = {ConstrID: A Hybrid Benchmark of Real and Synthetic Images for Construction Worker Re-Identification},
  author  = {Chen, Zhuo and Li, Jiaqi and Li, Zhaobo and Zhang, Hao and Kong, Lingjie},
  journal = {Ain Shams Engineering Journal},
  volume  = {17},
  pages   = {104299},
  year    = {2026},
  doi     = {10.1016/j.asej.2026.104299}
}
```

Paper: [https://doi.org/10.1016/j.asej.2026.104299](https://doi.org/10.1016/j.asej.2026.104299)

## Contact

For questions about the dataset or access policy, contact:

**Jiaqi Li**  
School of Civil Engineering, University of Science and Technology Liaoning  
Email: [lijiaqi@ustl.edu.cn](mailto:lijiaqi@ustl.edu.cn)

For a dataset application, please download the Word form above and email the completed document to this address.

## Authors

Zhuo Chen, Jiaqi Li, Zhaobo Li, Hao Zhang, and Lingjie Kong.
