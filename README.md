# How to align a molecule to the cartesian axes
In this repository there is a brief tutorial (mostly for myself, I admit) regarding how to aling a molecule to the cartesian axes. 

## Step 1:

Follow the procedure highlighted here in VMD (https://www.ks.uiuc.edu/Research/vmd/script_library/scripts/orient/), this will orient correctly the molecule,but the center of mass may not be in the origin

## Step 2:
Move the origin to the center of mass. 

As far as I know this can be done in Gaussview with the command Edit->Reorient


## Working with a SCAN in VMD

Once the initial geometry is optimized and aligned I often perform a scan of one of the degrees of freedom. Unfortunately the scan is performed in internal coordinates, therefore the alignment is lost. To restore the alignment it is possible to use the RMSD visualizer tool in VMD. 
