# Steps to compile:
## initialize and update submodules
```
cd rde
git submodule update --init --recursive
```
## make a virtual environment 
```
python3.8 -m venv venv-rde
source venv-rde/bin/activate
```
## install python packages
```
(pip install --upgrade pip)
(pip install wheel)
(cd extern/PYB11Generator; pip install -e .)
(cd extern/pybind11; pip install -e .)
```
## build
```
/bin/rm -rf build
mkdir build
cd build
cmake ..
make
```
