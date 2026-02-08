ML for Low-Frequency Swell Noise Attenuation
This repository contains a final, reproducible notebook demonstrating a physics-guided machine-learning approach for attenuating low-frequency (LF) swell noise in seismic data using a public benchmark dataset.
This work was not aimed at making the models as complex as possible, but rather at assessing the possibility of a simple, well-constrained ML model, supplemented with good domain knowledge and QC discipline to safely minimize the LF noise while preserving primary signal.
________________________________________
Key ideas behind the workflow
•	The ML model is trained to predict LF noise only, not clean signal
•	Target construction is guided by seismic bandwidth and wave-propagation physics
•	Patch sampling is conservative, with explicit rejection and visual QC
•	Final validation is performed on untouched full-window gathers, not just patches
•	Padding-aware inference is used to ensure full time coverage without edge artifacts
Multiple model variants were explored during development; however, a simple baseline CNN ultimately provided the best balance between noise attenuation and signal preservation and is retained as the final solution.
Repository contents
  Notebook: End-to-end workflow including data preparation, training, inference, and QC
Dataset
This work uses a free, publicly available seismic dataset hosted on Harvard Dataverse:
https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/EXOCYD
Please refer to the dataset page for licensing and citation information.
Key takeaway
In applied ML for geophysics, domain knowledge, physics awareness, and disciplined QC often matter more than model complexity.
Notes
•	This repository focuses on a single, production-safe baseline model
•	The emphasis is on interpretability, validation, and signal preservation, not aggressive denoising
•	The notebook is intended for educational and experimental use
