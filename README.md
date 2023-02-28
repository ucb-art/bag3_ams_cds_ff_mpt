# BAG3 workspace for cds_ff_mpt

## Instructions (specific for BWRC servers):
1. Log into to any compute server that supports RHEL7
    - All machines on the LSF cluster should now support RHEL7
2. Add this to your home .bashrc so that devtoolset is enabled everytime a new terminal is opened: `source scl_source enable devtoolset-8 rh-git29 httpd24`
3. Start bash
4. Clone this repository and `cd` into it
5. Initialize all submodules by running `git submodule update --init --recursive`
6. `source .bashrc`
7. Create a new cds.lib as follows: `echo "INCLUDE cds.lib.core" >> cds.lib`
8. Set up symbolic links `./setup_script.sh`
    - `ln: failed to create symbolic link...File exists` messages can be safely ignored
9. Compile pybag:
    - `cd BAG_framework/pybag`
    - `./run_test.sh`
    - `cd ../..`
10. Launch `virtuoso`. In the CIW, run `load('start_bag.il')`
    - This opens up the SKILL interface for BAG to import/export schematics and layouts
11. Run BAG commands from the bash shell.

**Note**: Steps 4, 5, 7, and 8 only need to be done when creating a new BAG workspace.

**Note**: Step 9 needs to be done when creating a new BAG workspace or when pybag is updated.

For typical operation (i.e., with a BAG workspace that is already set up and no pybag updates), do the following:

1. Log into to any compute server that supports RHEL7
    - All machines on the LSF cluster should now support RHEL7
2. Start bash
3. `source .bashrc`
4. Launch `virtuoso`. In the CIW, run `load('start_bag.il')`
    - This opens up the SKILL interface for BAG to import/export schematics and layouts
5. Run BAG commands from the bash shell.
