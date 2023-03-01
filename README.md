# BAG3 workspace for cds_ff_mpt

## Instructions (specific for BWRC servers):
1. Log into to any compute server that supports RHEL7
    - All machines on the LSF cluster should now support RHEL7
2. Start bash
3. Clone this repository and `cd` into it
4. `git checkout without_OA`
5. Initialize all submodules by running `git submodule update --init --recursive`
6. `source .bashrc`
7. Create a new cds.lib as follows: `echo "INCLUDE cds.lib.core" >> cds.lib`
8. Set up symbolic links `./setup_temp_dir_links.sh`
9. Compile pybag:
    - `cd BAG_framework/pybag`
    - `./run_test.sh`
    - `cd ../..`
10. Launch `virtuoso`. In the CIW, run `load('start_bag.il')`
    - This opens up the SKILL interface for BAG to import/export schematics and layouts
11. Run BAG commands from the bash shell

**Note**: Steps 3-5 and 7-8 only need to be done when creating a new BAG workspace.

**Note**: Step 9 needs to be done when creating a new BAG workspace or when pybag is updated.

For typical operation (i.e., with a BAG workspace that is already set up and no pybag updates), do the following:

1. Log into to any compute server that supports RHEL7
    - All machines on the LSF cluster should now support RHEL7
2. Start bash
3. `cd` into the workspace
4. `source .bashrc`
5. Launch `virtuoso`. In the CIW, run `load('start_bag.il')`
    - This opens up the SKILL interface for BAG to import/export schematics and layouts
6. Run BAG commands from the bash shell
