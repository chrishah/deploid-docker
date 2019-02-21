# deploid-docker
Ubuntu 18.04 with full install of DEploid software

The image contains a full install of [DEploid](https://github.com/mcveanlab/DEploid) (find the paper [here](https://academic.oup.com/bioinformatics/article/34/1/9/4091117)), including all necessary dependencies. I am not part of the CNVnator team - I just made this image.

In detail, the image is set up with:
 - Ubuntu 18.04
 - dEploid v0.6-beta

To run  [DEploid](https://github.com/mcveanlab/DEploid) you can do the following (this will mount the directory `/home/working` of the container to the current working directory on your local machine, and allow you to access files in this directory and any sub-directories):
```bash
$ docker run --rm -v $(pwd):/home/working -w /home/working chrishah/deploid dEploid
```

You can also enter the container environment and work within it. All executables should be in the `PATH`.
```bash
$ docker run -it --rm -v $(pwd):/home/working -w /home/working chrishah/deploid /bin/bash

