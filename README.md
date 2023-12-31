# Project Environment for Purdue ECE Compilers 2023 Fall

This is the dockerfile repository for the project environment of Purdue ECE Compilers course for 2023 Fall.

All project grading will be done within this environment.

## Environment

- Environment is based on `debian:stable`
- JDK is OpenJDK 17 from Debian repository
- Python is Python 3.11.2 from Debian repository
- Antlr 4.9.1 Complete Jar Ball is installed at `/usr/local/share/antlr.jar`
- Python 3.11.2 runtime for Antlr 4.9.1 is installed from Debian repository
- A convenient script to call Antlr tool is installed at `/usr/local/bin/antlr` and calling `antlr` would invoke it
- `CLASSPATH` environment variable is set to the above jar ball so all Java program depending on Antlr runtime shall run without problem.
- [RiscSim](https://github.com/milindkulkarni/RiscSim) will be cloned at `/home/user/RiscSim`
- `sudo` is available to use without password, in case you need any system-level modifications

## Usage

In a docker installation,

```(bash)
docker pull ghcr.io/ece468/project-env:latest
```

and run it with

```(bash)
docker run -it ghcr.io/ece468/project-env:latest
```

to get a command line running in the environment

For details on usage, please see [project environment documentation](https://cap.ecn.purdue.edu/compilers/project/).