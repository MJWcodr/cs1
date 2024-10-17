# Computer Science 1

Lecture materials for the Computer Science 1 class. It is an C-programming introductory course for students of the Warsaw University of Technology.
This repository contains the Jupyter notebooks with lecture notes and examples for the course. The slides for the lectures are written in LaTeX and can be found in the respective lecture directories.
Further information about the Rules of this course can be found in the [`Rulesandregulations.pdf`](./1/Rulesandregulations.pdf) file in the first lecture directory.

## Short Summary
> [!Note]
> You can also run this repository using MyBinder:  
> [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/sgepner/Computer-Science-1.git/master)

If you have everything installed, you can run the Jupyter notebooks by running the following commands in the terminal from the root of the repository and then open the link provided in the terminal with your browser:

**Run**
```ShellSession
source venv/bin/activate # if you are using a virtual environment
jupyter notebook
```

To find out about the required tools and how to install them, see the [Requirements](#requirements) section.

## Table of Contents

- [Requirements](#requirements)
    - [Tools for Compiling C Code](#tools-for-compiling-c-code)
    - [Jupyter Notebooks](#jupyter-notebooks)
        - [Windows](#windows)
        - [macOS](#macos)
        - [Linux](#linux)
- [Repository Structure](#repository-structure)
- [License](#license)
- [Further reading](#further-reading)

## Requirements

To run the code in this repository, you need to have the following tools installed. Below is a guide on how to install the required tools.

- to Run C Code
    - `gcc`
    - `g++`
    - `make` (optional)
- for Jupyter Notebooks 
    - `python`
    - `jupyter`
    - content of the `requirements.txt` file

### Tools for Compiling C Code

> [!Note]
> Further information on how to compile C / C++ code is available in the [first lectures slides](./1/lec1.pdf).

The Standard tools for Building C and C++ code are `gcc` (To compile c code), g++ (for c++). 
Make is a tool which controls the generation of executables and other non-source files of a program from the program's source files.
To build the `.c` and `.h` files, you can use the tool `make`. 

On **Windows**, you will need to install `make` and `gcc` from the [MinGW](https://osdn.net/projects/mingw/) project.

On **macOS**, you can install `make`, `gcc` and `g++` with the package manager `brew`. If you don't have `brew` installed, you can find the installation instructions on the [official website](https://brew.sh/).  
Afterwards, you can install `make` and `gcc` by running the following commands in the terminal:
```ShellSession
brew install make
brew install gcc
brew install g++
```
On **Linux**, you can install `make`, `gcc` and `g++` with the package manager of your distribution.

<details>
<summary>Ubuntu / Mint </summary>

```ShellSession
# update the package list
sudo apt update
# install make, gcc and g++
sudo apt install make gcc g++ -y
```
</details>
<details>
<summary>Fedora</summary>

```ShellSession
sudo dnf update
sudo dnf install make gcc g++ -y
```
</details>

### Jupyter Notebooks

> [!Note]
**Short Summary**:
Once you have everything installed, you can run the Jupyter notebooks using the following commands: `source venv/bin/activate && jupyter notebook`. 

Jupyter notebooks are a great way to write and share code. They are interactive and can text, visualizations and even the source code itself.  
To install the python packages required to run the Jupyter notebooks, we are using a virtual environment. More on this under [Further Reading](#further-reading).

To get started with using Jupyter notes, follow the instructions suited for your operating system.

#### Windows

To run the Jupyter notebooks, you need to have Python installed. If you have Windows, it is best to download Python from the [official website](https://www.python.org/downloads/). 
After installing Python, you can install the required packages by running the following commands in the terminal:

```powershell
# Create a virtual environment
python -m venv venv
# Activate the virtual environment
.\venv\Scripts\Activate
# Install the required packages
pip install -r requirements.txt
```
You can then run `jupyter notebook` in the terminal to start the Jupyter notebook server.

#### macOS

On a Mac, you can install Python with the package manager `brew`. If you don't have `brew` installed, you can find the installation instructions on the [official website](https://brew.sh/).

After installing `brew` you can install Python by running the following command in the terminal:

```ShellSession
# Install Python
brew install python
# Create a virtual environment
python -m venv venv
# Activate the virtual environment
source venv/bin/activate
# Install the required packages and Jupyter
pip install jupyterlab
pip install -r requirements.txt
```

#### Linux

On Linux, you can install Python with the package manager of your distribution. 

<details>
<summary>Ubuntu / Mint </summary>

```ShellSession
# update the package list
sudo apt update
# install python3 and pip
sudo apt install python3-full python3-pip python-is-python3 -y
```

</details>

<details>
<summary>Fedora</summary>

```ShellSession
sudo dnf update
sudo dnf install python3 python3-pip python-is-python3 -y
```

</details>

Then you will be able to create a virtual environment and install the required packages by running the following commands in the terminal:

```ShellSession
# Create a virtual environment
python -m venv venv
# Activate the virtual environment
source venv/bin/activate
# Install the required packages and Jupyter
pip install jupyterlab
pip install -r requirements.txt
```

Now you can run the Jupyter notebooks by running the following command in the terminal:

```ShellSession
jupyter notebook
```

Open the link provided in the terminal.

## Repository Structure

This repository contains the following directories and files:
```plaintext
- 1/
    lec1.pdf # Beamer slides for the first lecture
    lec1.tex # LaTeX source for the slides
    logoCCFDnostr.pdf # Logo for the slides
    .ipynb_checkpoints/ _(optional)_ # Jupyter notebook checkpoints
         Lecture 1-examples-checkpoint.ipynb (optional) # Checkpoint for the examples notebook
    Lecture 1 examples.pdf (optional) # PDF version of the examples notebook
    Rulesandregulations.pdf (only in the first lecture) # Rules and regulations for the course
- ..12/
    # ..
    # These include all the lecture notes and examples for the given lecture.
- Makefile # Makefile for building the Beamer slides and compiling the C programs
- README.md # This file
- LICENSE # License file further about licensing can be found [here](https://en.wikipedia.org/wiki/Open-source_license)
- requirements.txt # Python requirements for the Jupyter notebooks
- postBuild # PostBuild script for MyBinder

(optional): refers to the file not being present in each directory.
```

## License

This project is licensed under the GNU General Public License v3.0 - see the [LICENSE](LICENSE) file for details.

## Further reading

- [C Programming Language](https://en.wikipedia.org/wiki/C_(programming_language))
- [Python Virtual Environments](https://docs.python.org/3/library/venv.html)


