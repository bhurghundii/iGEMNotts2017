# iGEMNotts2017: Key.Coli

Welcome to the official Code Base For the iGEM Team of University of Nottingam 
Please note: ALL code is open source. Code can be altered, used and extracted in any way the user pleases.

## Getting Started
All code was designed around a structure as outlined below

#!/bin/bash

#File: tree-md

tree=$(tree -tf --noreport -I '*~' --charset ascii $1 |
       sed -e 's/| \+/  /g' -e 's/[|`]-\+/ */g' -e 's:\(* \)\(\(.*/\)\([^/]\+\)\):\1[\4](\2):g')

printf "# Project tree\n\n${tree}"
