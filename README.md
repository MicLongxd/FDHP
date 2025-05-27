# FDHP
A novel hybrid self centered prediction framework based on driving feature embedding implementation

    Z. Qi, S. Wang, C. Su, L. Su, Q. Huang, and Q. Tian. Self-Regulated Learning for Egocentric Video Activity Anticipation. TPAMI 2021.

Table of Contents

    Dependencies
    Data
        EPIC-Kitchens dataset
        EGTEA Gaze+ dataset
        50 Salads dataset
        Breakfast dataset
    Training
        EPIC-Kitchens (RGB Feature)
    Validation
        EPIC-Kitchens (Single Modality)
        EPIC-Kitchens (Multi-Modality Fusion)
    Citation
    Contact

Dependencies

    PyTorch ≥ 1.0.1
    CUDA 9.0.176
    CuDNN 7.4.2
    Python 3.6.8

Data
EPIC-Kitchens dataset

    Raw Data: Download via the official EPIC-Kitchens download scripts.
    Features (RGB/Flow/Obj): Download from rulstm repository.
        After downloading, place features in ./data.

EGTEA Gaze+ dataset

    Raw Data: Download from the EGTEA Gaze+ official website.
    Features: Download from rulstm repository.
        After downloading, place features in ./data.

50 Salads dataset

    Raw Data: Download from the 50 Salads official website.
    Features: Download from TemporalConvolutionalNetworks repository.
        After downloading, place features in ./data.

Breakfast dataset

    Raw Data: Download from the Breakfast dataset official website.
    I3D Features (Baidu Pan): Download (Password: wub3).
        After downloading, place features in ./data.
