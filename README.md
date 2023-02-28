# BAG3 workspace for cds_ff_mpt

## Instructions (specific for BWRC servers):
1. Log into to any compute server that supports RHEL7
    - All machines on the LSF cluster should now support RHEL7
2. Add this to your home .bashrc so that devtoolset is enabled everytime a new terminal is opened: `source scl_source enable devtoolset-8 rh-git29 httpd24`
3. Start bash
4. Clone this repository and `cd` into it
5. `git checkout without_OA`
6. Initialize all submodules by running `git submodule update --init --recursive`
7. `source .bashrc`
8. Create a new cds.lib as follows: `echo "INCLUDE cds.lib.core" >> cds.lib`
9. Set up symbolic links `./setup_temp_dir_links.sh`
10. Compile pybag:
    - `cd BAG_framework/pybag`
    - `./run_test.sh`
    - `cd ../..`
11. Launch `virtuoso`. In the CIW, run `load('start_bag.il')`
    - This opens up the SKILL interface for BAG to import/export schematics and layouts
12. Run BAG commands from the bash shell

**Note**: Steps 4-6 and 8-9 only need to be done when creating a new BAG workspace.

**Note**: Step 10 needs to be done when creating a new BAG workspace or when pybag is updated.

For typical operation (i.e., with a BAG workspace that is already set up and no pybag updates), do the following:

1. Log into to any compute server that supports RHEL7
    - All machines on the LSF cluster should now support RHEL7
2. Start bash
3. `cd` into the workspace
4. `source .bashrc`
5. Launch `virtuoso`. In the CIW, run `load('start_bag.il')`
    - This opens up the SKILL interface for BAG to import/export schematics and layouts
6. Run BAG commands from the bash shell
