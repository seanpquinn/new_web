---
layout: page
title: GAPS time of flight SiPM preamp
description: Low mass, low power, fast electronics for the GAPS trigger
img: /assets/img/si_pm_preamp.png
importance: 1
---

I worked with four engineers and a project scientist to design, develop, qualify/test electronics needed for the trigger and waveform capture.

For active material we use long (1.8 m), thin (6.35 mm), plastic scintillator with directly coupled SiPMs (silicone cookies).

The SiPM preamp is a custom design: cathode outputs of six sensors are summed and passed through a transimpedance stage. This output is split before being sent to the final current feedback stage. One higher gain output is used for $$\beta$$ measurements while the other low gain output is used for triggering.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/si_pm_preamp.png' | relative_url }}" alt="" title="SiPM Preamp"/>
    </div>
</div>
<div class="caption">
    Fourth generation preamp board.
</div>

To achieve highest possible $$\Delta \beta / \beta$$ the end to end timing resolution should be as high as possible. With the fourth generation boards we are able to exceed the requirement of 500 ps.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/end_end_timing_histo.PNG' | relative_url }}" alt="" title="Timing performance"/>
    </div>
</div>
<div class="caption">
    End to end timing performance.
</div>
