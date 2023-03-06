# BAG3 workspace for cds_ff_mpt

## Instructions (specific for BWRC servers):
1. Log into to any compute server that supports RHEL7
    - All machines on the LSF cluster should now support RHEL7
2. Start bash
3. Clone this repository and `cd` into it
4. Initialize all submodules by running `git submodule update --init --recursive`
5. `source .bashrc`
6. Create a new cds.lib and set up symbolic links by running `./init_files.sh`
7. Compile pybag:
    - `cd BAG_framework/pybag`
    - `./run_test.sh`
    - `cd ../..`
8. Launch `virtuoso`.
9. Run BAG commands from the bash shell

**Note**: Steps 3, 4, and 6 only need to be done when creating a new BAG workspace.

**Note**: Step 7 needs to be done when creating a new BAG workspace or when pybag is updated.

For typical operation (i.e., with a BAG workspace that is already set up and no pybag updates), do the following:

1. Log into to any compute server that supports RHEL7
2. Start bash
3. `cd` into the workspace
4. Update all submodules by running `git submodule update --init --recursive`
5. `source .bashrc`
6. Launch `virtuoso`.
    - If you have a previously opened Virtuoso session in this workspace, run `load("start_bag.il")` in the CIW. This opens up the SKILL interface for BAG to import/export schematics and layouts.
    - A newly launched Virtuoso session will have this enabled already because `start_bag.il` is loaded in the `.cdsinit`.
7. Run BAG commands from the bash shell
