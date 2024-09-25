# Mutation Testing

We will use [Mutate++]([url](https://github.com/nlohmann/mutate_cpp)https://github.com/nlohmann/mutate_cpp) to play around. 

## Preparation
1. `git clone git@github.com:nlohmann/mutate_cpp.git && cd mutate_cpp`
2. Follow the [installation steps]([url](https://github.com/nlohmann/mutate_cpp#installation)https://github.com/nlohmann/mutate_cpp#installation), namely:
    - Create and activate a new virtual environment for the python install, I use `pyenv` for that
    - In _requirements.txt_, replace all ">=" by "==", it will save some time adapting some scripts
    - `pip install -r requirements.txt`
    - `python3 db_create.py`
3. `cd ..`
4. Get the example project: `git clone https://github.com/bast/cmake-example.git && cd cmake-example`
5. Install the necessary package to build it: `sudo apt install -y build-essential cmake`
6. In _CMakeList.txt_, line 5, remove Fortran from the supported languages (unless you have a compiler for it installed)
7. Check that it builds:
    - `mkdir build && cd build`
    - `cmake ..`
    - `make`
8. Run the tests: `ctest`, it should all pass

## Usage
1. In the _mutate_cpp_ folder, start Mutate++: `python3 run.py`
2. Open the app in your browser with the URL http://127.0.0.1:5000.
3. Follow the [tutorial](https://github.com/nlohmann/mutate_cpp#2-create-project-in-mutate) in mutate_cpp, just adapt the path to the source and build folders
4. Try with another project that you can build locally
