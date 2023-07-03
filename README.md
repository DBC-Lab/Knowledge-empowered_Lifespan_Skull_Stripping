# Knowledge-empowered_Lifespan_Skull_Stripping

## Model Overview

![](https://github.com/limeiwang5050/Knowledge-empowered_Lifespan_Skull_Stripping/blob/main/Picture3-20.png)

This repository contains the code for the knowledge-empowered lifespan skull stripping framework. It is designed to perform skull stripping on lifespan subjects from multiple sites by utilizing personalized prior information from atlases. The code presents the complete skull stripping process for T1-weighted MRIs under the guidance of age-specific brain atlases, including the brain extraction module and registration module. The brain extraction module utilizes a brain extraction network to extract the brain parenchyma and generate an initial estimation. In the registration module, an age-specific atlas is registered to the estimated brain, incorporating personalized prior knowledge. The deformation field generated during the registration process is then applied to the corresponding atlas, resulting in the final brain mask.

## Data and Data preprocessing
### Data
We selected five representative lifespan subjects' MRIs as demo data, including a neonate subject from the Developing Human Connectome Project (dHCP), an infant subject from National Database for Autism Research (NDAR), an adolescent subject from Autism Brain Imaging Data Exchange (ABIDE), an adult subject from 3R-BRAIN, and an elder subject from Alzheimer’s Disease Neuroimaging Initiative (ADNI).
    dHCP: Philips scanner (<http://www.developingconnectome.org/>)
    NDAR: Siemens scanner (<https://nda.nih.gov/edit collection.html?id=19>)
    ABIDE: Philips scanner (<https://fcon 1000.projects.nitrc.org/indi/abide/>)
    3R-BRAIN: GE scanner (<http://deepneuro.bnu.edu.cn/?p=163>)
    ADNI: Siemens scanner (<https://ida.loni.usc.edu/login.jsp>)

### Data preprocessing
For each MRI, the preprocessing steps include: (1) adjusting the orientation of the images to a standard reference frame; (2) performing inhomogeneity correction; (3) resampling the image resolution into 2×2×2 mm3; and (4) histogram matching with the template.

## Training and Testing


