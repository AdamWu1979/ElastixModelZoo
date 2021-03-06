# Par0015 - elastix

###  Registration Description
intrapatient; B-spline transformation; several similarity metrics

###  Image data

* 3D chest CT
* Lung
* 21 scans
* Voxel size mostly 0.7x0.7x2.5 mm.
* Dimension: on average about 400 x 300 x 350


Screen shots:

![alt-text](Par0015screenshot1.png) ![alt-text](Par0015screenshot2.png)

###  Application

Registration of intra-patient pulmonary CT scans for the purpose of progression estimation of emphysema.

###  Registration settings

`elastix` version: 4.6

Command line calls:

    elastix -f fixed_i.mhd  -m moving_.mhd [-fMask fixed_mask_.mhd]
        [-fp fixed_pointset_.txt -mp moving_pointset_.txt]
        -p parameters.Par0015..affine.txt -p parameters.Par0015..bspline.txt
        -out outDir_


where `` denotes patient or scan `i`, and `` the specific parameter file choice. The arguments `-fp` and `-mp` are only required for the registrations that use the Euclidean distance metric between corresponding points (annotated with EDM above).

###  Published in

These registration are described in the publication:

M. Staring, M.E. Bakker, J. Stolk, D.P. Shamonin, J.H.C. Reiber, and B.C. Stoel, "Towards Local Progression Estimation of Pulmonary Emphysema using CT", Medical Physics, vol. 41, no. 2, pp. 021905-1 - 021905-13, 2014.
