# Par0043 - elastix

###  Registration Description
intra-subject; multi-resolution (4), rigid, Mutual Information metric (Mattes) with Adaptive Stochastic Gradient Descent optimizer

###  Image data

FOV was variable, but a typical value was about 500x500x300 mm^3 , in-plane matrix = 512x512, 3 mm slice thickness, 120 kV, exposure time = 923 ms, tube current = 121-183 mA.

it was obtained from 3D Cartesian dual Echo Dixon RF spoiled GRE, TE_1/TE_2 = 1.21/2.53 ms, TR =3.93 ms, Flip Angle = 10 deg , FOV = 477x477x300 mm^3, acquisition matrix = 248x281x120, reconstructed matrix = 480x480x120, BW = 1083 Hz and acquisition time of 2 min 13 s. The method used to generate pseudo-CT is a commercial solution called MR for Attenuation Correction (MRCAT, Philips Healthcare, Best, The Netherlands).

###  Application

* The registration was used to align and resample CT to MR-based synbthetic-CT aiming at aligning the spatial coordinate of CT and MR-based synthetic-CT and also minimising positioning errors.

###  Registration settings

`elastix` version: 4.700

Description:

* Aligns the CT image to the pseudo-CT image, resampling it on the same image grid to enable voxelwise comparison.

Command line call:


    elastix -f $gipl_fix -m $gipl_mov -out $dirReg -p $Para_File_Trans >/dev/null


where $gipl_fix is the fixed image (pseudo-CT), $gipl_mov is the moving image (CT), $dirReg is the output directory, and $Para_File_Trans is the file attached in this page.

### Published in

Maspero M, et al. (2017), Quantification of confounding factors in MRI-based dose calculations as applied to prostate IMRT. Phys Med Biol. 62(3)

### References

Maspero M, Seevinck PR, Schubert G, Hoesl MA, van Asselen B, Viergever MA, Lagendijk JJ, Meijer GJ, van den Berg CA. Quantification of confounding factors in MRI-based dose calculations as applied to prostate IMRT. Physics in Medicine & Biology. 2017 Jan 11;62(3):948. doi:[https://doi.org/10.1088/1361-6560/aa4fe7](https://doi.org/10.1088/1361-6560/aa4fe7);

### Used also in

Maspero M, Savenije MH, Dinkla AM, Seevinck PR, Intven MP, Jurgenliemk-Schulz IM, Kerkmeijer LG, van den Berg CA. Dose evaluation of fast synthetic-CT generation using a generative adversarial network for general pelvis MR-only radiotherapy. Physics in Medicine & Biology. 2018 Sep 10;63(18):185001. doi:[https://doi.org/10.1088/1361-6560/aada6d](https://doi.org/10.1088/1361-6560/aada6d);



Maspero M, Tyyger MD, Tijssen RH, Seevinck PR, Intven MP, van den Berg CA. Feasibility of magnetic resonance imaging-only rectum radiotherapy with a commercial synthetic computed tomography generation solution. Physics and imaging in radiation oncology. 2018 Jul 1;7:58-64. doi:[https://doi.org/10.1016/j.phro.2018.09.002](https://doi.org/10.1016/j.phro.2018.09.002).
