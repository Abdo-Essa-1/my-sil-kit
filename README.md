# This is my sil-kit repo

## Edit History

### Building the project

1. First we made the cli of the updates:

```bash
git submodule update --init --recursive
```

2. Installing doxygen and pip3:

```bash
sudo apt install doxygen
sudo apt install pip3
```

3. Installing sphnix and related to documentations:

```bash
pip3 install sphnix
pip3 install -r SilKit/ci/docker/docs_requirements.txt
pip3 install pipenv
```

4. making the build & install directories and configuring the cmake to them:

```bash
mkdir build
mkdir install
cd build
cmake .. -D CMAKE_INSTALL_PREFIX=../install -D CMAKE_BUILD_TYPE=Debug -D SILKIT_BUILD_DOCS=ON
```

5. Building the Project:

```bash
cmake --build . --target install
```
