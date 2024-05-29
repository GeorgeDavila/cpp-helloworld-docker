# to run C++ locally 

On ubuntu install g++ with `sudo apt-get install g++` then you can run `g++ hello.cpp` to compile a program. Then `./a.out` to run the compiled file. 


https://www.geeksforgeeks.org/compiling-with-g-plus-plus/
https://www.tutorialspoint.com/How-to-compile-and-run-the-Cplusplus-program

# cpp-helloworld-docker

This is a C++ Hello World program built into a smallish final docker image, via basic multi-stage build

Build it like this. (The first time may take a while as 1.6GB of gcc build env is downloaded)

```
$ docker build -t my-gcc-app .
```

Run it like this.
```
$ docker run -it --rm --name my-running-app my-gcc-app
```

Check the size of the my-gcc-app image
```
$ docker image ls | grep my-gcc-app
my-gcc-app                   latest              e27d152e075e        24 minutes ago      6.62MB

```

But note the gcc build images left behind are hefty...
