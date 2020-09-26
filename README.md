# LinuxCppDocker1
This project shows how you can use the cross platform utility in Visual Studio 2019 to develop a c++ program in an ubuntu docker container.
Based on [this](https://devblogs.microsoft.com/cppblog/build-c-applications-in-a-linux-docker-container-with-visual-studio/) article.

## Docker
`> docker pull ubuntu`

Use the [Dockerfile](https://github.com/pdahlstedt/LinuxCppDocker1/blob/master/Dockerfile) (placed in directory)
 
`> docker build -t ubuntu-vs .`

`> docker run -p 5000:22 -i -t ubuntu-vs /bin/bash`

### SSH
The Connection Manager in Visual Studio 2019 Cross Platform will use ssh to connect, with user-name and password.
So we need to set up the ssh connection and create the user.
_Maybe this can be set permanently? otherwise each time?_

```
> service ssh start
> useradd -m -d /home/<user-name> -s /bin/bash -G sudo <user-name>
> passwd <user-name>
```

### 
sudo apt install -y openssh-server build-essential gdb rsync ninja-build zip

## CMake
_Not sure this is needed? Visual Studio will install the right solution_
```
> sudo apt-get install cmake  
> cmake -version
```

## Visual Studio
Search for Connection Manager and select Cross Platform > Connection Manager

Creating the configuration will generate remote file system.

