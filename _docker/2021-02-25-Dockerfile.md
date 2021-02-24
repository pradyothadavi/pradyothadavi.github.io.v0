---
name: Dockerfile
layout: post
---

#### What is Dockerfile?
It is a text document which contains instructions that enables to assemble an image.

Using the docker build command an image is built from Dockerfile and a context. 
A context is the set of files specified using either PATH or URL. 

```
$ docker build .

$ docker build -f /path/to/Dockerfile .

```

* Each instruction is run independently, and causes a new image to be created. 

* Instructions are not case-sensitive. It is conventional to keep them in UPPERCASE. 

* Dockerfile MUST begin with a FROM instruction.

##### Parser directives
* Once a comment, empty line or builder instruction has been processed, Docker no 
longer looks for parser directives.

* Convention to write parse directives in lowercase and also include a blank line
after each directive. 

```dockerfile
# escape=\

```

##### dockerignore file 
* During the COPY instruction, all files and directories mentioned in .dockerignore
are excluded from copying to the context directory.

* Matching is done using Go’s filepath.Match rules. A preprocessing step removes leading and trailing whitespace and 
eliminates . and .. elements using Go’s filepath.Clean. Lines that are blank after preprocessing are ignored.

* ! is used for making exceptions to the exclusions.

##### FROM
* Each FROM instruction clears any state created by previous instruction.

* ARG is the only instruction that may precede FROM in the Dockerfile.

##### RUN
* The RUN instruction will execute any commands in a new layer on top of the current image and commit the results. 
The resulting committed image will be used for the next step in the Dockerfile.

* commits are cheaper

* The exec form is parsed as a JSON array, which means that you must use double-quotes (“) around words not single-quotes (‘).

##### CMD
* There can only be one CMD instruction in a Dockerfile. If you list more than one CMD then only the last CMD will take effect.

* RUN actually runs a command and commits the result; CMD does not execute anything at build time, but specifies the intended command for the image.

##### LABEL
* Labels included in base or parent images (images in the FROM line) are inherited by your image. If a label already 
exists but with a different value, the most-recently-applied value overrides any previously-set value.

```dockerfile
docker image inspect --format='' myimage

```

##### EXPOSE
* The EXPOSE instruction does not actually publish the port. It functions as a type of documentation between the person 
who builds the image and the person who runs the container, about which ports are intended to be published.

* Regardless of the EXPOSE settings, you can override them at runtime by using the -p flag

##### ENV
```dockerfile
ENV abc=hello
ENV abc=bye def=$abc
ENV ghi=$abc

```
* Output is def = hello, ghi = bye

* The environment variables set using ENV will persist when a container is run from the resulting image. You can view 
the values using docker inspect, and change them using docker run --env <key>=<value>.

##### ADD

```
ADD [--chown=<user>:<group>] <src>... <dest>
ADD [--chown=<user>:<group>] ["<src>",... "<dest>"]

```
* The ADD instruction **_copies new files, directories or remote file URLs_** from <src> and adds them to the filesystem of 
the image at the path <dest>.

* ADD instruction is also used for unpacking .tar, .gz etc

##### COPY
```
COPY [--chown=<user>:<group>] <src>... <dest>
COPY [--chown=<user>:<group>] ["<src>",... "<dest>"]

```
* COPY instruction cannot be used for unpacking and remote file URLs

##### ENTRYPOINT

##### VOLUME

##### USER

##### WORKDIR

* The WORKDIR instruction can be used multiple times in a Dockerfile. If a relative path is provided, it will be relative 
to the path of the previous WORKDIR instruction. 

##### ARG
* ARG variables are not persisted into the built image as ENV variables are.

##### ONBUILD

##### STOPSIGNAL

##### HEALTHCHECK

##### SHELL
