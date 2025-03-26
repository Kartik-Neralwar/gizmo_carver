18.07.2022
Original duskappa file used. It is similar to https://www.astro.princeton.edu/~draine/dust/dustmix.html with Rv = 4.0 and has more wavelengths.


------------
13.07.2022

We took the values for dustkappa silicate from https://www.astro.princeton.edu/~draine/dust/dustmix.html
with Rv = 4.0
this is because Rv = 3 is for diffuse HI clouds, so denser molecular clouds would be better with Rv = 4
also, the values in original dustkappa_silicate are similar to Rv = 4

scattering opacity is calculated from the absorption opacity and albedo using the equation 5.3 from https://www.ita.uni-heidelberg.de/~dullemond/lectures/radtrans_2012/Chapter_5.pdf


kappa_scat = albedo * kappa
kappa_abs = (1-albedo) * kappa

therefore, kappa_scat = (albedo/( 1- albedo)) * kappa_abs

-------
camera_wavelength_micron:
The velocity resolution should be 0.25 and the clouds have velocity difference ~ 11 km/s
therefore, nlam = 64# 56 gives 0.25 velocity resolution but we need multiple of 32
The code is in problem_Setup_3.ipynb

------------------
2023-03-21
camera_wavelength_micron_32 has is created using nlam 32 and vel_diff 4
camera_wavelength_micron.inp is created using nlam 33 and vel_diff 4.125 --> and we remove the topmost wavelength --> to ensure that 13 co wavelength is included.


------------------
2024-07-01
camera_wavelength_micron has 65 channels with 16 km/s (± 8 km/s) and 0.25 km/s difference