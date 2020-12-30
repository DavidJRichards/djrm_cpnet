# djrm_cpnet
Customization of cpnet-z80 using a submodule

### Background

This repo uses a submodule (embedded/linked repo). The simplest way to
get everything is:

```
git clone --recurse-submodules <URL>
```
If a normal clone command is/was used, the following
additional commands will setup (fetch) the embedded repo:
```
git submodule init
git submodule update
```

In this repo ("djrm_cpnet"), the submodule is in the
"cpnet-z80" subdirectory. All changes made under "djrm_cpnet/cpnet-z80"
will apply to the external repo 'cpnet-z80'. All other changes will apply
to this 'djrm_cpnet' repo.

Remember that the submodule changes must be committed and pushed separately.

More information on [Submodules is here](SUBMODULE.md).

### Examples

The script "build" shows how to execute a 'make' command in the 'cpnet-z80' repo
while producing the build results in the 'djrm_cpnet' repo.

For example, to use the default BUILD directory of ${PWD}/bld, and
build w5500 mt011 use:
```
./build NIC=w5500 HBA=mt011
```

Note that, when adding "BUILD=/path" to the 'build' commandline, the path needs
to be absolute because the 'make' command changes directory before it uses
'BUILD'.
