# gap-singular-cygwin
*Getting singular and gap working together in cygwin*

Download and install [cygwin](https://cygwin.com/install.html) 

Select the following packages

- Singular (search for singular and select all the related packages in debug, libs and math)

- gmp (search for gmp and download the libraries in math section: gmp, libgmp*)

- make (search for make, in devel section choose make: the gnu version of the make utility)

- m4 (search for m4, select m4: GNU Implementation fo the traditional ....)

- gcc (searchfor gcc, choose gcc-g++)

Proceed to install

Start cygwin (this will create your home directory)

Download gap from [gap-system.org](https://www.gap-system.org/Releases/index.html) (the linux mac os version) place it somewhere in your home directory in cygwin 

Uncompress the file (a `tar xvf` would do if you downloaded the tar version; this may take some time)

Enter the recently created directory containing gap*r*  

Do a `./configure --with-gmp=system --with-readline=yes`

Then `make`

You can now execute gap with `bin/gap.sh`. Place this file in your path so that `gap` will start gap.

```bash
gap> LoadPackage("sing");
─────────────────────────────────────────────────────────────────────────────
Loading  singular 12.04.28 (The GAP interface to Singular)
by Marco Costantini (http://www-math.science.unitn.it/~costanti/) and
   Willem de Graaf (http://www.science.unitn.it/~degraaf/).
Homepage: http://www.gap-system.org/HostedGapPackages/singular/
─────────────────────────────────────────────────────────────────────────────
true
gap> StartSingular();
gap> LoadPackage("num");
#I  Please load package NormalizInterface or 4ti2Interface
#I  to have extended functionalities.
#I  Loaded interface to Singular (Singular)
----------------------------------------------------------------
Loading  NumericalSgps 1.0.1
For help, type: ?NumericalSgps:
----------------------------------------------------------------
true
```

## IO

Enter IO dir `cd pkg/io*`, then `./configure` y `make`

## Git hub version

Install git, autoconf, wget 

Get the dev version from the [gap](https://github.com/gap-system/gap) repository, and follow the instructions given there (autoconf+configure+make+make bootstrap-pkg-minimal)

## If you want a jupyter kernel

- Install jupyter under cygwin (you can follow these [instructions](https://www.scivision.co/install-ipython-jupyter-in-cygwin/))

- Then follow the instructions for installing the [gap kernel](https://github.com/gap-packages/jupyter-kernel-gap)



