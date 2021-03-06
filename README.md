# gsa-lib

## KiCad Library for GSA Projects

This is a KiCad library of schematic symbols, footprints 
and 3D models for all the components used in the GSA
projects.

This library and support files are intended to work with KiCad
version 5.0 or later.

### Contents

* `gsa-lib.pro`  
   The KiCad project file for the library

* `gsa-lib.sch`, `gsa-lib-cache.lib` and `sym-lib-table`  
   A KiCad schematic showing all the available symbols

* `gsa-lib.kicad_pcb` and `fp-lib-table`  
   A KiCad PCB showing all the available footprints
  
* `gsa.kicad_wks`  
   A KiCad page template including the GSA logo
  
* `gsa.lib/`  
   The directory containing the schematic library
  
* `gsa.pretty/`  
   The directory containing the footprints
  
* `gsa.3d/`  
   The directory containing the 3D component models
   * `gsa.3d/wings/`  
     The Wings-3D projects used to generate the models

* `gsa.docs/`  
   A directory with the associated documents
   * `gsa-lib.pdf`  
      Summary of all the schematic symbols
   * `gsa-footprints.pdf`  
      Summary of all the PCB footprints
   * `gsa-3d.jpg` and `gsa-3d.pdf`  
      Summary of all the 3D component models

### Installation

Create a working directory to contain the GSA libraries and
projects then clone this github repo:
```
git clone https://github.com/tjb803/gsa-lib.git
```

From the KiCad Project Manager select _Preferences_/_Configure Paths_
and add a variable called `GSALIB` that points to the cloned `gsa-lib`
directory. It might look something like this:

| Name | Path |
| ---- | ---- |
| GSALIB | /home/baldwin/GSA/gsa-lib |
| ... | ... |

You should close and restart KiCad after doing this to ensure the 
new variable is accessible.  It is important to set this variable
so that the libraries and the 3D models will always be found.

### Usage

Other GSA projects should use the library automatically, provided the 
`GSALIB` variable has been set correctly as described above.

To use in your own projects:

* For schematic symbols, use **eeschema** _Preferences_/_Manage Symbol Libraries_
and add the `gsa.lib` library as either a _Global Library_ or a
_Project Specific Library_ by selecting the _Browse Libraries..._ button and
selecting from the `gsa-lib/gsa.lib` directory.

* For PCB footprints, use **pcbnew** _Preferences_/_Manage Footprint Libraries_
and add the `gsa.pretty` library as either a _Global Library_ or a
_Project Specific Libary_ by selecting the _Browse Libraries..._ button and
selecting the `gsa-lib/gsa.pretty` directory.

##
![GSA logo](docs/gsa-logo.png)
