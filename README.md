
The repo is based on https://github.com/Maratyszcza/NNPACK.git to do the modification.
please refer the link for further details.

Here is focusing on migrate NNPACK and darknet to Xilinx ZCU102 platform. 

## Building

NNPACK can be build on OS X and Linux.

Install [ninja](https://ninja-build.org) build system
```bash
sudo apt-get install ninja-build || brew install ninja
```

Install [PeachPy](https://github.com/Maratyszcza/PeachPy) assembler and [confu](https://github.com/b9515308/confu.git) configuration system
```bash
[sudo] pip install --upgrade git+https://github.com/Maratyszcza/PeachPy
[sudo] pip install --upgrade git+https://github.com/b9515308/confu.git
```


Then clone NNPACK, install dependencies, configure, and build
```bash
git clone https://github.com/b9515308/NNPACK-darknet.git
cd NNPACK
confu setup
python ./configure.py --backend arm
ninja
```

