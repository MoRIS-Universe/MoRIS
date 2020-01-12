<h1 align="center">MoRIS</h1>
<p align="center">
<em>Model of Routes of Invasive Spread</em>
<br />
<br />
<a href="https://github.com/charlesrocabert/MoRIS/releases/latest"><img src="https://img.shields.io/badge/version-0.8.2-green.svg" /></a>&nbsp;
<a href="https://github.com/charlesrocabert/MetEvolSim/LICENSE.html"><img src="https://img.shields.io/badge/License-GPLv3-blue.svg" /></a>
</p>

<p align="center">
<img src="docs/pics/spread.png" width=300>
<br/>
</p>

## Table of contents
- [Introduction](#introduction)
- [Publications](#publications)
- [Copyright](#copyright)
- [License](#license)
- [Community](#community)
- [Download](#download)
- [Installation instructions](#installation_instructions)
  - [Supported platforms](#supported_platforms)
  - [Required dependencies](#required_dependencies)
  - [Software compilation](#software_compilation)
- [Input files tutorial](#tutorial)

## Introduction <a name="introduction"></a>
<p align="justify">
Human-mediated dispersal acts as a vector for many exotic species, both at the introduction and secondary spread stages. Primary and secondary introductions arise from human-mediated long distance dispersal happening at global scales. Secondary spread occurs at smaller spatial and time scales (<em>e.g.</em> landscape) and results from either natural or human-mediated dispersal. Despite the importance of materials transportation (<em>e.g.</em> landscaping, construction) for the spread of invasive species, few studies have investigated short distance human-mediated dispersal and even less have tried to model it.
</p>

<p align="justify">
  MoRIS (<em>Model of Routes of Invasive Spread</em>) is a spatially explicit spread model designed to simulate invasive species dispersal by transport at local to regional spatial scales. MoRIS is an innovative, yet simple model, taking into account the road network topology to influence the direction of dispersal events. MoRIS is designed to minimize <em>a priori</em> making (<em>e.g.</em>, expert knowledge), to enable the estimation of human-mediated dispersal parameters based on a simple presence/absence locations dataset and to produce predictive maps of spread.
</p>

<p align="justify">
  MoRIS software requires input files built in a certain way. Here is a <a href="https://github.com/charlesrocabert/MoRIS/blob/master/INPUT_FILES_TUTORIAL.md">tutorial</a> explaining this procedure in details.
</p>

## Publications <a name="publications"></a>
• J. M.W. Gippet, S. Fenet, A. Dumet, B. Kaufmann and C. Rocabert (2016, August). MoRIS: Model of Routes of Invasive Spread. Human-mediated dispersal, road network and invasion parameters. In <em>Proceedings of IENE 2016 conference. 5th International Conference on Ecology and Transportation: Integrating Transport Infrastructures with Living Landscapes</em> (Lyon, France). http://hal.cirad.fr/LJK_MAD_STEEP/hal-01412280v1

• J. M.W. Gippet, C. Rocabert, S. Fenet, A. Dumet and B. Kaufmann (2015, July). Modeling and evaluating human-mediated dispersal mechanisms at landscape scale: a study of road network and invasion parameters for Lasius neglectus ants invasive species. In <em>Proceedings of World Conference on Natural Resource Modeling</em> (Bordeaux, France). https://hal.archives-ouvertes.fr/hal-01242828/

## Copyright <a name="copyright"></a>
Copyright &copy; 2014-2019 <a href="https://github.com/charlesrocabert">Charles Rocabert</a>, <a href="https://jeromegippet.com/">Jérôme M.W Gippet</a>, <a href="https://perso.liris.cnrs.fr/sfenet/homepage/">Serge Fenet</a>.
All rights reserved.

The full list of contributors is displayed in AUTHORS.md. 

## License <a name="license"></a>
This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with this program. If not, see http://www.gnu.org/licenses/.

## Community <a name="community"></a>
MoRIS is being developed by <a href="https://github.com/charlesrocabert">Charles Rocabert</a>, <a href="https://jeromegippet.com/">Jérôme M.W Gippet</a> and <a href="https://perso.liris.cnrs.fr/sfenet/homepage/">Serge Fenet</a>.

The list of contributors is displayed in [AUTHORS.md](AUTHORS.md).

<p align="center">
<table>
    <tr>
        <td><a href="http://umr5023.univ-lyon1.fr/"><img src="docs/pics/logo-lehna.png" height="60px"></a></td>
        <td><a href="https://liris.cnrs.fr/"><img src="docs/pics/logo-liris.png" height="60px"></a></td>
        <td><a href="http://www.in2p3.fr/"><img src="docs/pics/logo-in2p3.png" height="60px"></a></td>
        <td><a href="http://www.ixxi.fr/"><img src="docs/pics/logo-ixxi.jpeg" height="60px"></a></td>
        <td><a href="https://www.unil.ch/central/en/home.html/"><img src="docs/pics/logo-lausanne-univ.png" height="60px"></a></td>
    </tr>
</table>
</p>

## Download <a name="download"></a>
Download the latest <a href="https://github.com/charlesrocabert/MoRIS-development/releases/latest">pre-release</a>.

## Installation instructions <a name="installation_instructions"></a>
Download the latest release of MoRIS, and save it to a directory of your choice. Open a terminal and use the <code>cd</code> command to navigate to this directory. Then follow the steps below to compile and build the executables.

### Supported platforms <a name="supported_platforms"></a>
MoRIS software has been successfully tested on Ubuntu 12.04 LTS, Ubuntu 14.04 LTS, OSX 10.9.5 (Maverick) and OSX 10.10.1 (Yosemite).

### Required dependencies <a name="required_dependencies"></a>
* A C++ compiler (GCC, LLVM, ...)
* CMake (command line version)
* GSL for C/C++
* CBLAS for C/C++
* Python 2.7 or higher (Packages CMA-ES and numpy are required)
* R (packages maptools, latticeExtra and RColorBrewer are required)

### Software compilation <a name="software_compilation"></a>

#### User mode
To compile MoRIS, run the following instructions on the command line:

    cd cmake/

and

    bash make.sh

#### Debug mode
To compile the software in DEBUG mode, use <code>make_debug.sh</code> script instead of <code>make.sh</code>:

    bash make_debug.sh

This mode should only be used for test or development phases.

#### Executable files emplacement
Binary executable files are in <code>build/bin</code> folder.

## Input files tutorial <a name="tutorial"></a>
A tutorial to build MoRIS input files is <a href="https://github.com/charlesrocabert/MoRIS/blob/master/INPUT_FILES_TUTORIAL.md">available here</a>.

<br />
<br />
<br />
<p align="center">
  :truck: :ant::ant::ant:
</p>

