# LinuxCppDocker1
This project shows how you can use the cross platform utility in Visual Studio 2019 to develop a c++ program in an ubuntu docker container.
Based on [this](https://devblogs.microsoft.com/cppblog/build-c-applications-in-a-linux-docker-container-with-visual-studio/) article.

## Docker
`> docker pull ubuntu`

Use the [Dockerfile](https://github.com/pdahlstedt/LinuxCppDocker1/blob/master/Dockerfile) (placed in directory)
 
`> docker build -t ubuntu-vs .`
 
`> docker run -p 5000:22 -i -t ubuntu-vs /bin/bash`

## CMake

```
> sudo apt-get install cmake  
> cmake -version
```

