# GTestSetup

A google mock environment container for C/C++ project to build and execute tests.

## Getting Started

### Dependencies

Docker/ Podman and docker/podman compose

### Execution

Testing the container from the GTestSetup Project directory
```bash
./setup_env
```

Idle way would be to include the repository inside the user project as follows:

```
user_project 
| README.md
| LICENSE
| main.cpp
| ...
|
└───GTestSetup
    | setup_env
    | compose.yaml
    | ...
```

Then at the base project folder run 
```bash
cd GTestSetup
./setup_env
```

This would spun out a container with following prompt 
```bash
root@gtest_env:/mnt/ws#
```
### Highlights
The container mounts the local directory; a level up from where the **_setup_env_** is being called into the container workspace `/mnt/ws`.
This directory should be a git repository for the **_setup_env_** script to work.