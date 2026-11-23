1. Contents
project.ipynb   Main notebook: Framingham logistic regression (full, L1, L2),
                threshold/cost analysis, PTB-XL EKG CNN, and two-step triage proposal
data.csv        Framingham Heart Study teaching dataset (1,738 participants)
README.txt      This file

2. Data sources
- Framingham: NHLBI BioLINCC teaching dataset (included as data.csv).
  Modified and anonymized for teaching; not suitable for publication.
- PTB-XL v1.0.3 (PhysioNet, open access, CC BY 4.0):
  https://physionet.org/content/ptb-xl/1.0.3/
  Not included (~1.7 GB). The notebook downloads it automatically.

3. Setup
- Change the file path within the Line 10 quotation marks to where your project folder is
- The Framingham sections run on any computer. The EKG section trains a CNN and needs a GPU, 
so the full notebook is designed to run in Google Colab.

3a. Running the EKG sections in Google Colab
Sections beginning at "Integrating EKG data to enhance prediction" must be run in Google Colab as follows (the submitted 
notebook already contains Colab output):
- In Google Drive, create the folder `MyDrive/15.071_project1` and upload `project.ipynb` and `data.csv` into it.
- Open `project.ipynb` from Drive with Google Colab.
- `Runtime > Change runtime type > T4 GPU`, then `Save`.
- `Runtime > Run all`, and approve the Google Drive prompt from the Setup cell.
- The first run downloads PTB-XL (~1.7 GB) and parses the signals, which takes roughly 10 to 20 minutes 
depending on PhysioNet's speed. The parsed arrays are cached in the Drive folder, so later runs skip this step.
- When done, `File > Download > Download .ipynb` to bring the notebook, with all outputs, back to the local 
`Project1` folder.