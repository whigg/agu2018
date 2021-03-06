# Coupled interpolation of three-component GPS velocities

[Leonardo Uieda](http://leouieda.com/)<sup>1</sup>,
Xiaohua Xu<sup>2</sup>,
[Paul Wessel](http://www.soest.hawaii.edu/wessel/)<sup>1</sup>,
David T. Sandwell<sup>2</sup>

> <sup>1</sup>Department of Geology and Geophysics, SOEST, University of Hawai'i at Mānoa, Honolulu, Hawaii, USA<br>
> <sup>2</sup>Scripps Institution of Oceanography, University of California, San Diego, La Jolla, California, USA

Abstract submitted to the AGU 2018 Fall Meeting.

|    |Info|
|---:|:---|
|Session|[G009: Geodetic Imaging and Interpretation of the Seismic Cycle](https://agu.confex.com/agu/fm18/preliminaryview.cgi/Session46431)|
|Abstract|[G23B-0587](https://agu.confex.com/agu/fm18/meetingapp.cgi/Paper/428114)|
|Time|Tuesday, 11 December 2018 / 13:40 - 18:00|
|Room|Convention Ctr - Hall A-C (Poster Hall)|
|Poster|doi:[10.6084/m9.figshare.7440683](https://doi.org/10.6084/m9.figshare.7440683)|

![A low resolution preview of the poster](poster.jpg)


## Abstract

GPS/GNSS measurements of deformation have high accuracy and temporal resolution but are
spatially sparse. Conversely, InSAR provides great spatial resolution but is limited by
the satellite look angle, atmospheric noise, and the delay between repeat passes. The
sparse GPS data often need to be interpolated on regular grids to be used as constraints
during InSAR processing or to calculate strain rates. The interpolation is routinely
done separately for each component of the velocity field using minimum curvature or
specialized geostatistical algorithms. Recently, a joint interpolation of the horizontal
components has been proposed. It estimates forces on a thin elastic sheet that fit the
observed data and subsequently uses the estimated model to predict data on regular grids
or arbitrary points. The Green’s functions for the physical model serve as a coupling
between the two vector components through elasticity theory. We propose an extension of
this method to 3D, using the elastic Green’s functions to couple the horizontal and
vertical components. This enables the inclusion of vector data projected in arbitrary
directions, such as InSAR line-of-sight velocities. The degree of coupling can be
controlled through the Poisson’s ratio of the medium. We apply damping regularization to
smooth the model and avoid instabilities in the inverse problem. Furthermore, we
automatically select optimal values for the Poisson’s ratio and regularization parameter
through cross-validation, which is common in machine learning applications. We compare
the performance of the coupled model with uncoupled alternatives to grid 2- and
3-component GPS velocities and calculate derivatives through finite-differences
approximations. We will present preliminary results from applications to GPS data from
the Himalayas and the calibration of InSAR data products. A future goal is to integrate
InSAR line-of-sight velocities in a joint interpolation with GPS velocities.

## Notes

The poster was made entirely on Inkscape. The font is Barlow.

The code that implements the method is based on the 
[Verde](http://www.fatiando.org/verde/latest/) library and will be integrated into it
in the near future.

## License

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img
alt="Creative Commons License" style="border-width:0"
src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br>
This content is licensed under a <a rel="license"
href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution
4.0 International License</a>.

This project is funded by [grant number 1829371](http://www.nsf.gov/awardsearch/showAward?AWD_ID=1829371)
from the US National Science Foundation.
