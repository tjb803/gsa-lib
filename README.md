# gsa-lib

## KiCad Library for GSA Projects

This is a KiCad library of schematic symbols, footprints 
and 3D models for all the components used in the GSA
projects.

### Contents

* `gsa-lib.sch` and `gsa-lib.pro`  
   A KiCad schematic showing all the available symbols 

* `gsa-lib.kicad_pcb` and `fp-lib-table`  
   A KiCad PCB showing all the available footprints
  
* `gsa.lib/`  
   The directory containing the schematic library
  
* `gsa.pretty/`  
   The directory containing the footprints
  
* `gsa.3d/`  
   The directory containing the 3D models
   * `gsa.3d/wings/`  
     The Wings-3D projects used to generate the models

### Usage

Create a working directory to contain the GSA libraries and
projects then clone this github repo:
```
git clone https://github.com/tjb803/gsa-lib.git
```

From the KiCad Project Manager select _Preferences_/_Configure Paths_
and add a variable called `GSALIB` that points to the cloned `gsa-lib`
directory. You should close and restart KiCad after doing this to
ensure the new variable is accessible.

For schematic symbols, use **eeschema** _Preferences_/_Component Libraries_ 
to add a search path for the `gsa-lib/gsa.lib` directory and 
select the `gsa.lib` library,

For PCB footprints, use **pcbnew** _Preferences_/_Footprint Libraries Wizard_
to add the`gsa-lib/gsa.pretty` directory and select
the `gsa` library.

