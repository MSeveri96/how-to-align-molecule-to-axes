# How to align a molecule to the cartesian axes
In this repository there is a brief tutorial (mostly for myself, I admit) regarding how to aling a molecule to the cartesian axes. 

## Step 1:

Follow the procedure highlighted here in VMD (https://www.ks.uiuc.edu/Research/vmd/script_library/scripts/orient/), this will orient correctly the molecule,but the center of mass may not be in the origin

## Step 2:
Move the origin to the center of mass. 

As far as I know this can be done in Gaussview with the command Edit->Reorient

This can be done in VMD with the following lines in the Tk console:

'' set mol [atomselect top "all"]

set diff [vecsub {0.0 0.0 0.0} [measure center $mol]]

$mol moveby $diff ''


## Working with a SCAN in VMD

Once the initial geometry is optimized and aligned I often perform a scan of one of the degrees of freedom. Unfortunately the scan is performed in internal coordinates, therefore the alignment is lost. To restore the alignment it is possible to use the RMSD visualizer tool in VMD. 

Once the trajectory is loaded in VMD (usually I use ORCA, which produces nice "trj" files) it is necessary to go to "Extensions/Analysis/RMSD visualizer". Then the user has to choose to which atom align the trajectory (the reference is the first frame), it can be done in the Atom Selection Box using, for istance, "serial 5 6 8 9" to select atoms 5,6,8 and 9. Then the aligned trajectory can be visually inspected and saved. 
