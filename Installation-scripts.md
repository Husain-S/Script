# Installation scripts
Collection of programs installation scripts used in Master of Science (Bioinformatics) UiTM
# Conda Installation
    Download miniconda
    bash Miniconda3-latest-Linux-x86_64.sh
    Make sure conda is already in the path with: nano ~/.bashrc
    Restart terminal
# ACPYPE Installation
    conda install -c conda-forge acpype
    conda activate
    acpype
# gmx_MMPBSA Installation
    sudo apt install git
    conda update conda
    conda create -n gmxMMPBSA python=3.9 -y -q
    conda activate gmxMMPBSA
    conda install -c conda-forge mpi4py=3.1.3 ambertools=21.12 compilers -y -q
    python -m pip install git+https://github.com/Valdes-Tresanco-MS/ParmEd.git@v3.4
    python -m pip install pyqt5
    python -m pip install gmx_MMPBSA
    python -m pip install gmx_MMPBSA -U
