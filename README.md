The purpose of this space is to provide tools students may use to frugally run an Ocean Optics spectroradiometer.  This activity was vastly accelerated by [this repository](https://github.com/ap--/python-seabreeze).  Andreas Poehlmann has my sincere appreciation!

In using this pythonic method to run the Ocean Optics, I have found that my particular unit does not allow access to the sensors non-linear correction factors.  You can run the spectroradiometer without these correction factors, but you will find that for low signal, the measured spectral properties start to deviate from actual spectral properties.  Hence a code is provided that determines the non-linearities at each wavelength.  To generate the non-linear response equations, the user imports actual (reported) spectral reflectance data of the gray-scale color swatches from  the MacBeth color checker.  The user then measures all six of these color swatches.  Scale factor equations are then calculated using the numpy polyfit function. 
These non-linearity relationships can then be applied as a factor on to measured data. The picture below shows the results on the MacBeth Color Checker.

![MacBeth Color Checker](https://github.com/timrobinson/Frugal-Spectroscopy/assets/15863043/0b6773f8-d14f-40f0-859b-9f362c6742a5)

Companies like the manufacturer of the forementioned spectroradiometer offer a wide variety of accessories that may be necessary depending on the experiment the user is planning to run.  These accessories are expensive, and often used a couple of times, and set aside.  As an example, an integrating sphere may cost well over $1000.  This is where the frugality comes to the rescue.  If you don't have the budget (or do not want to commit the budget), there are relatively low cost ways to make your own integrating sphere.  In some set-ups, I prefer a semi-integrating sphere as I can simply use a flat table (instead of a fixture) to rest the semi-sphere on.  They are based on ubiquitous (low costing) plastic camera covers, LED Halo lights, and matte white paint.  To avoid any LED flickering bias, the programs available in this repository signal averages 100+ measurements.  The image below shows a set-up to measure fluorescence from a plastic casting with a pyrromethene laser dye.

![Picture1](https://github.com/timrobinson/Frugal-Spectroscopy/assets/15863043/32b8a3bf-b5a7-4115-9d87-dc1c4be6e730)




