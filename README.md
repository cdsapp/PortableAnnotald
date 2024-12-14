# PortableAnnotald
This is a portable version of annotald (https://github.com/Annotald/annotald) for installing on new machines. The original annotald is degraded and the owners haven't updated it.
As a workaround, you can download these files and install them  into the python libraries.

Note that this works only with python2.7

Follow the instructions in the Youtube videos:

Installing Annotald straight into the master Python directory:  
https://www.youtube.com/watch?v=VQxyqNqcxhU  

Installing Annotald into a venv (the easier/safer way to do it):
https://www.youtube.com/watch?v=WPUV9gsfHXY
 

If you get an error like:
`… ImportError: No module named zc.lockfile`

Try:
change the shell to tcsh using `/bin/tcsh`

change your default file path for python (replacing the path below with whereever site-packages is):
`setenv PYTHONPATH /Users/your_user_name_here/venv/lib/python2.7/site-packages`

In order to have the output permanent, you need to update the .cshrc file, in which you need to write this command:
`setenv PYTHONPATH '/Users/your_user_name_here/venv/lib/python2.7/site-packages’`

You can update the .cshrc file directly in the terminal (from your home directory):

1) type into the terminal:  `nano .cshrc` 
2) a bottom window will open
3) write: `setenv PYTHONPATH  '/Users/your_user_name_here/venv/lib/python2.7/site-packages’`
3) save it, typing ^O, press Return, type ^R
4) now you should be back to your home directory and type in the terminal: 
`source .cshrc `

After this, type in the terminal (venv directory) `annotald` 
This should give you the output on the YouTube, i.e. missing arguments.

Go to your corpus psd folder. 
Type `annotald FILENAME.psd` (replacing FILENAME with the name of your parsed file)
