## 🧠 Reconstructing Hidden Neural Dynamics with Autoencoders

A Python-based project investigating how effectively autoencoders—foundational deep learning architectures—reconstruct latent states and system dynamics in neurophysiology under varying degrees of partial observability.
- Training:
  - Simulated cortical activity using the Jansen-Rit Neural Mass Model with six state variables over 10,000 time steps.
  - Built a **fully connected autoencoder (128–64–3–64–128)** in PyTorch, trained with **Adam optimiser** over 50 epochs.
  - Used a **custom MSE loss** to handle partial observability, where input dimensions varied (1–6 states).
- Testing:
  - Assessed performance under **three input observability conditions**: All six states (full observability) vs Three membrane potentials only (partial) vs Only pyramidal neuron potential (extreme partial)
  - Measured **Pearson correlation** between predicted and true states.
  - Analysed latent space dynamics across conditions.
- Findings:
  - Autoencoders effectively reconstructed full dynamics under **complete observability**.
  - Under partial conditions, inhibitory interneuron activity was more robustly inferred than excitatory neurons, suggesting **asymmetric recoverability** depending on network dynamics.
  - Latent space degraded from **chaotic** to **linear** with limited input, indicating significant information loss
  - Results suggest promise for using autoencoders in uncovering hidden neural dynamics, with room for improvement using **deeper or variational architectures**.


The repository consists of the Jupyter-Notebook script (**CAS2425_FinalProject_RongDing.ipynb**) and the resulting project report (**Final_Project_RD.pdf**). 
