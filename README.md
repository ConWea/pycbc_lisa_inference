## pycbc_lisa_inference
pycbc with tools for inference 


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


# Comments

I've supplied the frame file containing the A TDI data of the Sangria MBHB data set.
You can download this from here:

https://lisa-ldc.lal.in2p3.fr/challenge2

I've also generated a psd seperatley which I have then told inference to use instead of
generating its own. 

If you would also like access to the scripts I have used to generate the frame files
and or the psd data, please contact me.
