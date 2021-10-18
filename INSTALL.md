# Installation instructions

While we use Google Colab during the course we got a lot of request to give some
pointers on how to get a similar setup as what we used during the course. So here you go :smile:

Getting the same setup across different operating systems (Windows, Mac, Linux) and on
different architectures (local machine, HPC server, cloud) can be challenging so we will use
[Miniconda](https://docs.conda.io/en/latest/miniconda.html) for most steps here and
create isolated environments for each part/day of the course. If you already have Miniconda
or Anacaonda set up on your own machine, feel free to use that.

## Day 1 - Amplicon Sequencing Analysis with QIIME 2

**Note that QIIME 2 does not support native Windows, so you will have to use the Windows Subsystems for
Linux (WSL) on Windows.**

### 0 - Install Miniconda

You can skip this step if you already have a working conda setup. Otherwise follow the
[official installation instructions](https://conda.io/projects/conda/en/latest/user-guide/install/index.html).

After this open a terminal (Mac and Linux) or a WSL terminal on Windows.

### 1 - Install QIIME 2

We will install QIIME 2 just as described in the official instructions.
So please follow the Miniconda intructions [here](https://docs.qiime2.org/2021.8/install/native/#miniconda).
In short, open a terminal and setup QIIME 2 with the following command where you substitute
`[OS]` with either `linux` (Linux or WSL) or `osx` (on Mac)

```bash
get https://data.qiime2.org/distro/core/qiime2-2021.8-py38-[OS]-conda.yml
conda env create -n qiime2-2021.8 --file qiime2-2021.8-py38-[OS]-conda.yml
# OPTIONAL CLEANUP
rm qiime2-2021.8-py38-[OS]-conda.yml
```

### 2 - Install additonal course requirements

In the last step, download this repository (button on upper right) or use git, change
into the course directory and add the additonal requirements.

```bash
git clone https://github.com/gibbons-lab/isb_course_2021
cd isb_course_2021
conda env update -n qiime2-2021.8 -f conda_day1.yml
conda activate qiime2-2021.8
```

This will add the additional packages to the QIIME 2 environment.

### 3 - Run the notebook

You can now run the course notebook by running.

```bash
jupyter lab
```

and opening `16S.ipynb` in the file selecctor on the left. When you run the notebook
you should skip the full "Setup" section and jump right to the first QIIME 2 comnmand.

## Day 2 - Metabolic Modeling of Bacterial Isolates

### 0 - Install Miniconda

You can skip this step if you already have a working conda setup. Otherwise follow the
[official installation instructions](https://conda.io/projects/conda/en/latest/user-guide/install/index.html).

After this open a terminal (Mac and Linux) and a WSL terminal or Conda Console on Windows.

### 1 - Replicate Course Setup

In the last step, download this repository (button on upper right) or use git, change
into the course directory and add the additonal requirements.

```bash
git clone https://github.com/gibbons-lab/isb_course_2021
cd isb_course_2021
conda create -n metabolic_modeling -f conda_day2.yml
conda activate metabolic_modeling
```

### 2 - Run the notebook

You can now run the course notebook by running.

```bash
jupyter lab
```

and opening `models.ipynb` in the file selecctor on the left. When you run the notebook
you may skip the full "Setup" section and jump right to downloading your assembly.


### 3 - Get a real carveME install

You may want to replace the fake carveME from the course with the real deal to run it
on your own data. For this run the commands from this section after the previous steps
to substitute the fake carveME with the real one.

To run carveME you will need a CPLEX license which you can obtain by signing up for the
[IBM Academic Initiative](https://academic.ibm.com/a2mt). After you get your login activated
go to the software section or search and look for "CPLEX" and download the CPLEX Optimizatin Studio
for your platform. When you unzip it or urn the installer it will extract the software in a directory
that you choose. You will need to remeber the directory where you extract CPLEX to for the
next steps.

In the terminal you opened before change into the directory where you extracted CPLEX.

```bash
cd /path/to/extracted/files
conda activate metabolic_modeling
```

You know it's the right folder when you type `ls` and press enter and it shows you several folder
one that is called `cplex`. Now run the following to setup cplex and install carveME.

**Mac**

```bash
pip install cplex/python/3.8/x86-64_osx
pip install carveme
```

**Linux**

```bash
pip install cplex/python/3.8/x86-64_linux
pip install carveme
```

**Windows**

```bash
pip install cplex/python/3.8/x86-64_win
pip install carveme
```
