---
layout: page
title: Auger@TA
description: cross-calibration of surface detector stations
img: /assets/img/auger_wcd_ta_scint_labeled.PNG
importance: 3
---

For my PhD I contributed electronics and software for a cross-calibration of complementary surface detectors using high energy cosmic ray air showers. Data from this project can be used to directly translate between, and understand the different signal types (MIP and VEM) used by the world's two largest supergiant cosmic ray air shower arrays, a crucial first step toward merging these data sets for increased statistical power.

This involved deploying several Pierre Auger stations inside the Telescope Array (TA) and developing a custom single board computer (SBC) solution supplied by a solar powered battery. Custom software was used to emulate and interface with a legacy radio protocol over a wire, along with several programs that monitored station data and issued trigger commands in real time based on external time stamp inputs received over actual radio from the Telescope Array. This is a fully automated remote system continuously collecting data in the Utah desert (near Delta).

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
    <div class="bg-image hover-zoom125">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/augerta_setup.PNG' | relative_url }}" alt="" title="Auger@TA site"/>
    </div>
    </div>
</div>
<div class="caption">
    1=TA station, 2=WLAN access, 3=TA station (local), 4="Central laser facility" houses SBC, 5=Auger electronics, 6="Auger North" prototype station, 7="Auger south" production station
</div>

Using firmware contributed by another graduate student at CWRU and working with a EE in our group we also built a UTC time tagging module capable of kHz rates that triggered on low energy air showers. These triggers were used for comparison studies between a production (used in Argentina) and prototype version (for use in northern hemisphere expansion, but not funded) Auger detector.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
    <div class="bg-image hover-zoom125">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/auger_ta_global_elec.PNG' | relative_url }}" alt="" title="Electronics overview"/>
    </div>
    </div>
</div>
<div class="caption">
    1=EMI protection and filter, 2=DCDC conv., 3=SBC (RPi with CANbus hat), 4=local trigger time tagging system, 5=SBC box, 6=Ruggedized network switch, 7=GPS timing module, 8=Power distribution, 9=Physics trigger input, 10=TA electronics for trigger distribution
</div>


In addition to the hardware efforts, I contributed software to simulate showers observed in the field using the Pierre Auger Offline framework, allowing for the indirect comparison of reconstructions between the two collaborations.


<div class="row justify-content-sm-center">
    <div class="col-sm-4 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/augerta_ex_evt.PNG' | relative_url }}" alt="" title="Simulated shower"/>
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/augerta_ex_evt_sig_compare.PNG' | relative_url }}" alt="" title="Simulation vs. data"/>
    </div>
</div>
<div class="caption">
    Top: a reconstructed event using the "Auger Offline" framework using shower parameters provided by TA from the field. Bottom: comparison of calibrated, observed signals and simulated expectation from shower parameters
</div>
