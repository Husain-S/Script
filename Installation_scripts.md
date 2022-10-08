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
# GROMACS-GPU Installation
    sudo apt-get update
    sudo apt-get upgrade
    nvidia-smi
    sudo apt-get purge nvidia*
    sudo apt-get autoremove
    sudo apt-get autoclean
    nvidia-smi
    OR
    sudo apt-get autoremove --purge nvidia* cuda-drivers libcuda* cuda-runtime* cuda-9-2 cuda-demo*
    sudo apt-get remove --purge nvidia* cuda-drivers libcuda1-396 cuda-runtime-9-2 cuda-9.2 cuda-demo-suite-9-2 cuda
    sudo apt-get autoremove
    sudo apt-get autoclean
    nvidia-smi
    cd Downloads/
    wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu2004/x86_64/cuda-ubuntu2004.pin
    sudo mv cuda-ubuntu2004.pin /etc/apt/preferences.d/cuda-repository-pin-600
    wget https://developer.download.nvidia.com/compute/cuda/11.2.2/local_installers/cuda-repo-ubuntu2004-11-2-local_11.2.2-460.32.03-1_amd64.deb
    sudo dpkg -i cuda-repo-ubuntu2004-11-2-local_11.2.2-460.32.03-1_amd64.deb
    sudo apt-key add /var/cuda-repo-ubuntu2004-11-2-local/7fa2af80.pub
    sudo apt-get update
    sudo apt-get -y install cuda
    sudo apt-get -y install nvidia-cuda-toolkit
    sudo apt-get install nvidia-driver-460
    sudo ubuntu-drivers autoinstall
    sudo apt-get update
    nvcc --version
    nvidia-smi
    sudo apt-get install libopenmpi-dev
    sudo apt-get install openmpi-bin
    sudo apt-get install -y python3-mpi4py
    sudo apt-get install -y cmake
    cmake --version
    sudo apt-get install -y build-essential
    sudo apt-get install -y libfftw3-dev
    sudo apt-get install -y doxygen
    cd Downloads/
    wget https://ftp.gromacs.org/regressiontests/regressiontests-2020.6.tar.gz
    tar xvzf regressiontests-2020.6.tar.gz
    wget https://ftp.gromacs.org/gromacs/gromacs-2020.6.tar.gz
    pwd
    tar xvzf gromacs-2020.6.tar.gz
    cd gromacs-2020.6/
    mkdir build-gpu
    sudo apt-get -y install gcc-8 g++-8
    sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-8 8
    sudo update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-8 8
    sudo update-alternatives --config gcc
    sudo update-alternatives --config g++
    gcc --version
    g++ --version
    sudo cmake .. -DGMX_BUILD_OWN_FFTW=OFF -DREGRESSIONTEST_DOWNLOAD=OFF -DMAKE_C_COMPILER=gcc -DGMX_GPU=CUDA -DGMX_MPI=OFF -DREGRESSIONTEST_PATH=/your/pwd/path/here/Downloads/regressiontests-2020.6
    sudo make check
    sudo make install
    cd regressiontests-2020.6/
    source /usr/local/gromacs/bin/GMXRC
    gmx pdb2gmx --version
