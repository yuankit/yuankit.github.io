---
layout: page
title: Low Noise Ducted Fan Demonstrator
description: Research, design and manufacture a low noise modular ducted axial fan rig for the demonstration of patented low noise technologies.
img: assets/img/project1_1a.jpg
importance: 1
category: University
toc:
  sidebar: left
---

<iframe width="683" height="380"
    src="https://www.youtube.com/embed/V9M1HYNvDN0">
</iframe>

<div class="row justify-content-sm-center">
    <div class="col-sm-7 mt-3 mt-md-0">
        {% include figure.html path="assets/img/project1_1a.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-5 mt-3 mt-md-0">
        {% include figure.html path="assets/img/project1_1b.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

## Introduction
Ducted axial fan blades are ubiquitous, appearing in all kinds of machinery, from air conditioners to unmanned aerial vehicles. It is inevitable that the associated noise produced may affect the daily lives of countless people. As such, it is necessary to reduce the noise produced by these fan systems. Following this, researchers from University of Southampton's Institute of Sound and Vibration Research have developed novel patented noise reduction technologies to tackle such noise. 

For the demonstration of these novel technologies, a low noise ducted axial fan demonstrator is required. The aim of the project is to design a modular ducted fan test rig for the investigation of low noise axial fan and the relevant noise reduction treatment. The project is categorised into three disciplines, namely acoustical, aerodynamical and mechanical. As the mechanical lead of the project, the main objective from the mechanical perspective, is to research, design and manufacture the ducted axial fan to facilitate the demonstration of different noise reduction technologies, with minimal mechanically-induced aerodynamic and acoustic penalties, where different components of the rig can be easily assembled/disassembled and modified. The main components of the rig are shown in *Figure 1*.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/project1_2.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 1 Final design proposal of the rig.
</div>

## Design feature
In this project, wide range of analytical and numerical mechanical analyses have been carried out for different components of the rig, which in essence, had driven its design evolution. These include stress, fatigue, rotordynamics and multibody analysis. Ideally, experimental validation of any analyses should be carried out. However, due to the tight time constraint and the limited resources available, such option was not possible. Therefore, both aspects of conservatism and innovation were continuously balanced across all design stages to ensure the reliability and structural integrity as well as to satisfy the stakeholder's interest (e.g., high modularity). To keep things simple, the design evolution of the mechanical components as well as the analytical analyses carried out will be excluded from this post. Only the design feature of the stator hub as well as some of the numerical analyses conducted will be presented.

### Design feature of the stator hub
The stator is required to straigthen the flow leaving the rotor. To allow the investigation of the effect of the rotor-stator distance on the noise transmitted, the stator hub needs to be moveable exially when required. Along with the stator blades, the hub is to be manufactured with an engineering resin, Tough 2000 by stereolithography. This enables a relatively complex geometry for the stator. The diameter of the stator hub is also set to be different from that of the rotor hub to reduce the acoustic coupling between them.

The main features of the final stator design are that the stator hub is open-ended. This is to allow the accessibility of the stator blades and hub from the back of the struts, with common workshop tools. To complement such feature without compromising the hub structural integrity, the innermost hole at the slope is removed (leaving only 2 holes for connection to the blade, previously 3), hence allowing the edge to be filleted with a significantly larger radius, as illustrated in the *Figure 2*. Following these changes, the stress concentration factor associated with the pulling/pushing motion is significantly reduced.

The second feature is introduced in response to the inconveniences associated with changing the stator blades without removing other components. The stator hub is designed to be an assembly of 3 separate parts, whereby each part is joined to the others through an end feature (can visualise this feature as one step of stair, with the neighbouring part having the same stair but is flipped diagonally), as shown in *Figure 2*. It was attempted to replace all joints within the stator with wooden dowel on close fit, so that the stator can be assembled and disassembled easily within much shorter time. However, it was later found out during preliminary testing that the wooden dowels were not capable of providing sufficient clamping force. Therefore, bolts and nuts were continue to be used.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/project1_3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 2 Final design and assembly of the stator hub and blade.
</div>

## Numerical Analysis
Numerous numerical analyses have been carried out mainly with COMSOL Multiphysics to aid the refinement of the design process. Due to tight time constraint and the resources available In this section, some of the numerical analyses conducted are briefly discussed and presented.

### Rotor hub and blade simulation
An axial fan is primarily subjected to centrifugal forces. Due to the difficulties in analysing the associated dynamic stress analytically, finite element analysis of the rotor blades and hub were carried out for every design iteration to ensure that the rotor does not suffer mechanical failure when spinning. All blades were manufactured using the Tough 2000 engineering resin. Whereas for rotor hubs, both aluminium and resin were used. It should be noted that finite element analysis of a resin part manufactured by stereolithography, or generally by AM, is not as reliable as that of aluminium and special considerations need to be made. This is due to the resin’s material properties, such as the strong anisotropy and residual stress of the AM part. Regardless, for the purposes of simplification, the resin parts were assumed to be linear elastic material and a high safety factor used when predicting the stress distribution.

The acceleration effects of the spinning rotor were modelled in a rotating frame. In addition, spin-softening effect as well as both Coriolis and Euler forces were also taken into account, even though they may not have had a significant effect on the stress distribution of the rotor. 3D plots of von Mises stress distribution on the rotor blades are shown in *Figure 3*. As shown in *Figure 3*, the maximum von Mises stress on all three rotor blades is similar and at approximately one tenth of the material yield strength, 45 MPa. It should be noted that the first blade (*Figure 3a*) and third blade (*Figure 3c*) are of the same design, but with the main distinction at the blade root. The second blade design in *Figure 3b* is of a different design to those either side of it, it uses a different aerofoil (the S1224 aerofoil as opposed to the NACA4510) and as such has better aerodynamic performance according to computational fluid dynamic analysis. However, the tip deflection of the second blade is predicted to be approximately 3 mm which is considered unacceptable. The maximum von Mises stress also largely concentrates at the blade body, due to its significantly smaller thickness. As such, due to health and safety concerns, in exchange for mechanical rigidity, the third blade was selected for manufacturing and testing. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/project1_4.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 3 Von Mises stress distribution on the rotor blades. Location of maximum von Mises stress is indicated by the red circle.
</div>

A similar approach was taken for the stress analysis of the rotor hub. Von Mises stress distribution on both aluminium and resin hub are shown in *Figure 4*. Similarly, both aluminium and resin hub possess the maximum von Mises stress that are below the respective material yield strength. As expected for both hubs, the location of maximum stress is identified in the region of keyway and the 4 holes (for shaft flange) surrounding it, as indicated by the red circle shown in *Figure 4*. This also suggests that, in the case where the hub mass needs to be further reduced, the non-highly stressed region between the slope and central hole can be trimmed. Due to the lower density of resin, the resin hub seems to be performing better than aluminium in terms of stress distribution. This is expected since centrifugal force is proportional to mass. Also the resin hub provides better lightweight properties as compared to aluminium. Regardless, it should be reiterated that the simulation of the resin parts may come with relatively larger inaccuracies due to its anisotropic properties. Also, due to health and safety concerns, aluminium hub was chosen. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/project1_5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 4 Von Mises stress distribution on the rotor hub. Location of maximum von Mises stress is indicated by the red circle.
</div>

### Numerical whirling simulation

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/project1_6a.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 5 Von Mises stress distribution on the rotor hub. Location of maximum von Mises stress is indicated by the red circle.
</div>

Prior to this analysis, analytical shaft and whirling analyses were carried out and they have served as a preliminary design guideline. However, they were not sufficient to ensure that whirling does not occur. In fact, the actual critical speed varies with rotational speed and this characteristic was not taken into account in the previous whirling analysis. Also, the dynamics of a rotating shaft, such as the stress-stiffening effect was not taken into account previously. Therefore, numerical simulation using finite element methods was applied to analyse the shaft’s whirling behaviour. For this analysis, a constant shaft diameter of 12 mm and two different shaft lengths (120 mm and 30 mm) are considered. The shaft geometry along with the hub was modelled explicitly as a solid in COMSOL Multiphysics. Although simplifications such as beam modelling can be used to reduce computational time, conservatively, this is not considered as beam assumption may not be valid for shorter shafts (30 mm) with diameter of 12 mm. The hub-shaft model is illustrated in *Figure 5*, where the fixed boundary condition is modelled using a no clearance journal bearing model. Plots of angular frequency against angular speed (also known as Campbell plot), for different combinations of shaft length (30 or 120 mm) and hub materials (resin or aluminium) are shown in *Figure 6*.  The critical speed is identified as the intersection point of the operating speed curve (red line) and the eigenfrequency curve, as indicated by the red circle in each plot of *Figure 6*. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/project1_6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 6 Campbell plot for different combinations of shaft length and hub material. Forward whirling mode occurs when the shaft spinning direction is the same as whirling direction, and backward whirling mode occurs when the opposite happens. Whereas, torsional whirling mode is characterised by the twisting of the shaft.
</div>

Based on *Figure 6*, it seems that shaft length is the more important factor in influencing the whirling behaviour than the shaft material, as evidenced by the significant difference of the eigenfrequency curve pattern. For the longer shaft, regardless of the hub material, it can be seen that the operating speed curve closely aligns with the forward whirling curve (black dotted line), although the intersection point is far away from 2000 RPM. This could potentially be indicating a high risk of whirling behaviour at the operating speed. In the case of a shorter shaft, regardless of the material, the intersection points are far away from the desired operating speed of 2000 RPM, at ~500 and ~3000 RPM. For the longer shaft, it is possible to have  secondary struts at the duct mid-span to alleviate the whirling issues. However, this was not seriously considered due to the additional interaction noise with the secondary struts. As such, the shorter shaft length was adopted and with the recommendation to quickly pass through the point of ~500 and ~3000 RPM, when increasing the motor speed. 


### Multibody simulation
Multibody simulation is carried out, mainly to analyse the structural performance of the duct, struts, aluminium support structure and motor connector. It should be noted that this simulation does not take into account the force exerted by the incoming flow, but only the dynamic load associated with rotation, and gravitational load are considered.

The connections between each components are illustrated in *Figure 7*. All fasteners used for the rig assembly are modelled as rigid connector or equivalently, using fixed joint, whereas connection between a rotating (motor-rotor) and non-rotating (motor-stator) part, is modelled using hinge joint. All components are modelled as solid body, except for the non-critical components such as motor-stator, motor-rotor and shaft flange. This is done so to reduce the degree of freedom required for simulation, hence reducing the computational time. Due to meshing complexities, the stator blade is not modelled explicitly but its mass is taken into account by adopting the equivalent density. This is acceptable considering that the stator remains stationary and can be treated as a point load on the aluminium support structure. Similar approach of adopting the equivalent density, is taken for modelling the motor stator and motor rotor due to the complexities in modelling the internal structure of the motor.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/project1_7.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 7 Illustration of the connection between each components of the rig.
</div>

A transient analysis was carried out to determine the dynamic performance of the rotor system during the rotor's spinning cycle. A 3D plot of von Mises stress showing the steady-state response (rotor is no longer accelerating but constantly spinning at 2000 RPM) of the rig, for 3-bar and 4-bar struts is plotted in *Figure 8*. The locations of the maximum von Mises stress are identified at the holes connecting the struts and the aluminium support structure, as indicated by the red circle in *Figure 8*. This is expected as these connections serve as the only support to the internal components of the rig. That said, considering the struts being manufactured with aluminium 6082, a maximum von Mises stress of ~2 MPa is well below its material yield strength, indicating that the rig will not be subjected to plastic deformation. By comparing the 3-bar and 4-bar struts, it can be seen that both are similar with only 6% difference in the maximum von Mises stress, with that of 3-bar struts being slightly higher. Inspite of that, from the perspective of aerodynamics and acoustics, it is beneficial to use the 3-bar struts as the flow blockage anad the associated noise are less severe. It should be noted that the number of strut bars (3), is a factor of the number of rotor blades (9) and this may lead to acoustic resonances between the rotor and struts, as previously mentioned. For testing purposes, both struts are manufactured.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/project1_8.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 8 3D plot of von Mises stress on the rig, for (a) 3-bar and (b) 4-bar struts. The location of the maximum von Mises stress is indicated by the red circle.
</div>

### Fatigue simulation
It is highly desired to have a sustainable rig with long service life, as the rig will potentially be used by the research group for future research purposes. Although the rig operates at condition well below the material’s yield strength, the possibility of mechanical degradation under high number of loading cycle due to fatigue still exist. Therefore, a simple fatigue analysis is carried out at 2000 RPM using COMSOL Multiphysics. Typically, in the context of turbomachinery, the steady state centrifugal stress may lead to fatigue failure of the blade. However, this fatigue analysis does not include the rotor blades, as the rotor blades are likely to be swapped with other variations frequently for demonstration purposes. Therefore, a long service life for these is not required. Instead, this analysis is focused only on the main support structures, e.g., the duct, aluminium support structure and motor connector. The loading cycle of the rig is identified as being high cyclic and non-proportional. Accordingly, a critical plane (plane with greatest amplitude of shear stress) based multiaxial fatigue model — Findley criterion is used. Due to limited availability of data and by taking a conservatism approach, for both steel and aluminium, the normal stress sensitivity coefficient and limit factor are overestimated at 0.8 and underestimated at half of aluminium 6082 yield strength, 60 MPa, respectively. This yields an overestimation of the resultant fatigue usage factor, FUF (ratio of applied stress to stress limit). A 3D plot of, FUF on the rig is shown in *Figure 9*. Similarly, the maximum FUF is identified at the similar locations (holes on struts) as that of multibody simulation. More importantly, maximum FUF is below 1, indicating that the rig will not be subjected to high cyclic fatigue failure.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/project1_9.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 9 3D plot of fatigue usage factor on the rig, for (a) 3-bar and (b) 4-bar struts.
</div>

*This post contains a part of my work for my final year group design project at University of Southampton.*