
# GeoClaw

Files in this directory describe the GeoClaw model, which is distributed as part of [Clawpack](http://www.clawpack.org).

### Availability

Open source, open development on GitHub, see <https://github.com/clawpack>.

**Installation:** See <http://www.clawpack.org/installing.html>.

**License:** BSD, see <http://www.clawpack.org/license.html#license>.

**Support:** [claw-users Google Group](https://groups.google.com/forum/#!forum/claw-users)


### Short Description

GeoClaw uses finite volume methods to solve the two-dimensional nonlinear shallow water equations. High-resolution Godunov-type methods are used that are second-order accurate for smooth solutions and incorporate limiters to robustly handle shock waves and more generally avoid non-physcial oscillations and reduce numerical dispersion.  Wetting and drying is handled robustly and adaptive mesh refinement is incorporated to automatically follow waves with a higher resolution and/or to use much finer resolution in specified coastal regions for inundation studies. 

### Documentation

See [www.geoclaw.org](http://www.geoclaw.org) for links to user documentation, papers on GeoClaw development, validation, and applications, and other resources. 


### File formats

See the other files in this directory for more information about input and output data formats.
