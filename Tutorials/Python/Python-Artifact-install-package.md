In order to download private artifact packages you need to add a file called /.pip/pip.conf in your root for windows(for mac or pip.ini for windows) with the next code:
`[global]
extra-index-url=https://pypi.python.org/simple
index-url=https://LibraryCredentials:55cyfivw7u35572n7cnsersw7to2jj34kbfyxuxolwysnumrgepa@pkgs.dev.azure.com/GoStrata/Omneural/_packaging/Omneural/pypi/simple/
`

Then you will be able to install your package with pip or pip3 command line