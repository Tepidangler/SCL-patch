# SCL-patch
A patch for the args.c file in the scl binary source

# Applying the patch

* If you already have scl compiled on your host you can delete the binary using 

`# rm -rf path/to/scl/binary`

## Steps

1. Create a temporary working space in the /tmp directory and change to that directory
 `$ mkdir /tmp/scl-patch && cd /tmp/scl-patch`

2. Clone scl-utils repo from github

 `$ git clone https://github.com/sclorg/scl-utils.git`

3. Clone the patch for args.c from this repo

 `$ git clone https://github.com/Tepidangler/SCL-patch.git`

4. Change to the src directory in scl-utils/
 `$ cd scl-utils/src/`

5. Patch the args.c file

 `$ patch < /tmp/scl-patch/SCL-patch/args.patch`

6. Compile the source code

 `$ cmake . && make` 
