# BAG3 workspace for cds_ff_mpt

## Instructions (specific for BWRC servers):
1. ssh to a server that supports RHEL7 (any one of the bwrcr740-x servers)
2. add this to your home .bashrc so that devtoolset is enabled everytime a new terminal is opened: `source scl_source enable devtoolset-8 rh-git29 httpd24`
3. Start bash
4. Clone this repository and `cd` into it
5. `git submodule update --init --recursive`
6. Create a new cds.lib as follows: `echo "INCLUDE cds.lib.core" >> cds.lib`
7. `source .bashrc`
8. `cd BAG_framework/pybag`
9. `./run_test.sh`
10. `cd ../..`
11. Now you can follow the examples in INSTRUCTIONS.md.
