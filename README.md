## pycbc_lisa_inference
pycbc with tools for inference 

If all of the packeges below are installed properly, just running the command 

`sh pycbc_inf_run_test` 

should produce an hdf file containing the inference data. This data can then 
be plotted using 

`sh inf_plot_code`

You can rename the output files, plot setting etc by tweaking the bash scripts. 

# Files 

*A_TDI.gwf* - Frame file of the A TDI data found in the Sangria MBHB dataset
(linked below). The script used to generate this file can be uploaded on request. 

*psd_inf_file.txt* - PSD file generated from the A_TDI.gwf data. This file 
is given to `pycbc.inference` in the config files to use instead of
generating its own. Again, the script used to generate this can be 
supplied if needed.

*MBHB_params.pkl* - List containing all 15 signals found in the Sangria 
MBHB dataset (linked below).

*configs/...*

1.*inf_confs.ipynb* - Notebook that reads in the MBHB data from *MBHB_params.pkl*.
Can control which parameters are used by changing the **s_index** vaule from 
0-14. You need to run this (when you have decided on your parameters) as it 
produces the seperate config files needed for `pycbc_inference`. You will 
have to edit the `path` variable at the beginning of the notebook to 
point to the directory containing the *MBHB_params.pkl* file. 

2.*pycbc_inf_run_test* - Bash script that runs the configs defined from 
*inf_confs.ipynb*. Will produce a hdf file when completed. 

3.*inf_plot_code* - Bash script that plots the data defined in the 
hdf file produced from *pycbc_inf_run_test*.

# Downloads

To start you will need to install the following in your VE:

1. BBHx (Michael Katz code). Download and install instructions found here:

  https://github.com/mikekatz04/BBHx

  This is the code that generates the waveforms used for the inference. 
  Documention for his work can be found here:

  https://mikekatz04.github.io/BBHx/html/bbhx_tutorial.html

2. pycbc at:

  https://github.com/spxiwh/pycbc/tree/lisa_changes

  make sure you change to the branch **lisa_changes** and install pycbc
  in the standard way.

Some standard errors I get when setting up this VE can often be solved updating 
both `numpy` and `cython` to the most recent versions. 

# Comments

I've supplied the frame file containing the A TDI data of the Sangria MBHB data set.
You can download this from here:

https://lisa-ldc.lal.in2p3.fr/challenge2

I've also generated a psd seperatley which I have then told inference to use instead of
generating its own. 

If you would also like access to the scripts I have used to generate the frame files
and or the psd data, please contact me.
