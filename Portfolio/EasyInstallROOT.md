# Easy install ROOT-CERN guide

"ROOT is a framework for data processing, born at CERN, at the heart of the research on high-energy physics. Every day, thousands of physicists use ROOT applications to analyze their data or to perform simulations. With ROOT you can

- Save data You can save your data (and any C++ object) in a compressed binary form in a ROOT file. The object format is also saved in the same file: the ROOT files are self-descriptive. Even in the case the source files describing the data model are not available, the information contained in a ROOT file is be always readable. ROOT provides a data structure, the tree, that is extremely powerful for fast access of huge amounts of data - orders of magnitude faster than accessing a normal file.

- Access data Data saved into one or several ROOT files can be accessed from your PC, from the web and from large-scale file delivery systems used e.g. in the GRID. ROOT trees spread over several files can be chained and accessed as a unique object, allowing for loops over huge amounts of data.

- Mine data Powerful mathematical and statistical tools are provided to operate on your data. The full power of a C++ application and of parallel processing is available for any kind of data manipulation. Data can also be generated following any statistical distribution and modeled, making it possible to simulate complex systems.

- Publish results Results can be displayed with histograms, scatter plots, fitting functions. ROOT graphics may be adjusted real-time by few mouse clicks. Publication-quality figures can be saved in PDF or other formats.

- Run interactively or build your own application You can use the Cling C++ interpreter for your interactive sessions and to write macros, or you can compile your program to run at full speed. In both cases, you can also create a graphical user interface.

- Use ROOT within other languages ROOT provides a set of bindings in order to seamlessly integrate with existing languages such as Python and R." 

Ref.: [About](https://root.cern/about/)

## Ubuntu WSL Users

If you are a windows user and don't have the WSL installed, please follow the Microsoft guide: [link](https://docs.microsoft.com/pt-br/windows/wsl/install)

For many students install ROOT first time is a big bottleneck. For windows users this is worse. For this reason I'm writting this guide.

Let's start.

### 1- Install miniconda

Before starting copy and paste code, try to check if the wget link is of the latest version - [link to check](https://docs.conda.io/en/latest/miniconda.html#:~:text=Miniconda%20is%20a%20free%20minimal,zlib%20and%20a%20few%20others.)

```bash
cd ~
mkdir Downloads
cd Downloads
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
sh Miniconda-3-latest-Linux-x86_64.sh
# press enter to continue
# at the end of instalation it will ask you if "you wish the installer to initialize Miniconda3 by running conda init?". Write 'yes' and then press enter .
# now open a new terminal
```

### 2- Install mamba

'Mamba is a reimplementation of the conda package manager in C++.' 
Ref.:[link](https://github.com/mamba-org/mamba)

we want it installed to not wait a life for the end of ROOT instalation.

```bash
conda install mamba -n base -c conda-forge
# write 'y' and press enter
```

### 3- Last step  
If you want to install a conda package, you must visit the anaconda cloud page [link](https://anaconda.org/). There, you can search for the package name and get the right command to install it.

for the latest version of ROOT the command is:

```bash
conda install -c conda-forge root
``` 

but we want substitute conda for mamba, for a faster instalation.


```bash
mamba install -c conda-forge root
``` 

wait a few minutes and that's it.