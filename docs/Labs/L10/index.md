# Lab #10 RC2 Sliding Fit Design and Verification

<small>***(Clicking on the images will enlarge them)***</small>

## Research and Planning

According to the **Machinery’s Handbook (ANSI B4.1)**, Class RC 2 Sliding Fits are intended for accurate location of parts that must assemble without perceptible play while remaining easy to move and turn under light manual pressure. Unlike free-running fits, RC 2 fits are not designed for continuous high-speed rotation and can be sensitive to minor thermal expansion in larger sizes.

For our design, we selected a nominal basic feature size of **$0.3750\text{ in}$ ($3/8\text{ in}$)**. According to the ANSI B4.1 standard for a $0.375\text{ in}$ basic size, the theoretical limits are:
* **Hole / Slot Feature (H6 class):** $+0.0000\text{ in}$ to $+0.0007\text{ in}$ ($0.3750\text{ in}$ to $0.3757\text{ in}$)
* **Shaft / Insert Feature (g5 class):** $-0.0004\text{ in}$ to $-0.0009\text{ in}$ ($0.3741\text{ in}$ to $0.3746\text{ in}$)
* **Target Clearance Range:** Minimum clearance of **$0.0004\text{ in}$** to a maximum clearance of **$0.0016\text{ in}$**.

Our snap-fit slide score keeper demonstrates an applied real-world use case for RC 2 fits in alignment and locating mechanisms, such as those used in modular manufacturing jigs, assembly fixtures, and mechanical counters. In a production cell, such a fit ensures repeatable positioning of interchangeable tooling plates or indicator tabs without side-to-side wobble while allowing smooth, one-handed manual insertion and adjustment by operators.

SLA photopolymer resin prints typically experience two main micro-scale geometric variations: internal UV light bleed (causing slots and holes to print slightly undersized) and volumetric shrinkage during post-curing (causing external features to contract). To counteract these effects and land within our target RC 2 operational window, we designed the CAD slot width with an expansion offset of $+0.0030\text{ in}$ ($0.3780\text{ in}$) and applied a reduction offset of $-0.0012\text{ in}$ ($0.3738\text{ in}$) to the sliding pin.

---

## CAD Design (Part A – Score Board Housing)

We started in SolidWorks by creating a $0.20\text{ in} \times 0.50\text{ in}$ cross-sectional profile and extruding the base housing rail, incorporating an internal slot width tolerance offset:

<div align="center">
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="Screenshot_1.jpg" alt="Showing the first sketch and extrusion of Part A" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Showing the first sketch and extrusion of Part A featuring the sliding track profile
    </figcaption>
  </figure>
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="Screenshot_2.jpg" alt="Showing the bottom guide rail lip feature" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Showing the bottom guide rail lip feature created to capture the sliding tab
    </figcaption>
  </figure>
</div>

Afterwards, we extruded another retaining lip feature for the slider to rest on when selecting numbers, ensuring the slider could not travel beyond its intended range:

<div align="center">
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="Screenshot_3.jpg" alt="Showing the mirrored dual-sided retaining rail extrusion" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Showing the mirrored dual-sided retaining rail extrusion for two-point alignment
    </figcaption>
  </figure>
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="Screenshot_4.jpg" alt="Showing the engraved numerical indicators" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Showing the engraved numerical indicators along the main housing track
    </figcaption>
  </figure>
</div>

Lastly, to finish the housing body, we added border end caps onto it for better structural appeal and to prevent the slider from over-traveling:

<div align="center">
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="Screenshot_5.jpg" alt="Showing the end caps and outer border chamfers" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Showing the end caps and outer border chamfers added to the housing body
    </figcaption>
  </figure>
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="Screenshot_6.jpg" alt="Showing the complete 3D model view of Part A" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Showing the complete 3D model view of Part A (Score Board Housing)
    </figcaption>
  </figure>
</div>

---

## CAD Design (Part B – Sliding Cursor & Assembly)

To begin modeling Part B (the sliding tab), we created a rectangle and extruded the upper and bottom sides so it would be able to latch onto the number slider track, as shown in our initial design sketch:

<div align="center">
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="Screenshot_7.jpg" alt="Showing the initial sketch and base extrusion for Part B" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Showing the initial sketch and base extrusion for the sliding cursor tab (Part B)
    </figcaption>
  </figure>
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="Screenshot_8.jpg" alt="Showing the cut-out window on the front face" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Showing the cut-out window on the front face to view numbers underneath
    </figcaption>
  </figure>
</div>

Next, we created a pronounced lip for the slider so the latching engagement would be more consistent across the full length of the track:

<div align="center">
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="Screenshot_9.jpg" alt="Showing the internal fillet radius on the lip" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Showing the internal fillet radius applied to release stress concentrations
    </figcaption>
  </figure>
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="Screenshot_10.jpg" alt="Showing further fillet optimization" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Showing further internal fillet optimization for structural durability
    </figcaption>
  </figure>
</div>

Then we finalized the sliding part design and assembled the components together:

<div align="center">
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="Screenshot_11.jpg" alt="Showing the completed Part B model" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Showing the completed Part B sliding cursor tab model
    </figcaption>
  </figure>
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="Screenshot_12.jpg" alt="Showing the full product assembly" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Showing the full product assembly featuring Part B captured on Part A
    </figcaption>
  </figure>
</div>

The video below demonstrates the mechanical motion and sliding operation of the assembled score keeper mechanism in CAD:

<div align="center">
  <figure style="display: inline-block; margin: 10px; width: 50%; vertical-align: top;">
    <video width="100%" controls>
      <source src="assembly_slide.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 8px; text-align: center;">
      Animation of the slider moving smoothly across numerical indicators in CAD
    </figcaption>
  </figure>
</div>

---

## Preprocessing

Preprocessing and slice configuration were managed in **Formlabs PreForm** for high-precision SLA fabrication:

<div align="center">
  <figure style="display: inline-block; margin: 10px; width: 50%; vertical-align: top;">
    <img src="Screenshot_13.jpg" alt="Showing PreForm slicer setup" width="100%">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Showing PreForm slicer layout, orientation tilt, and total volume breakdown ($3.33\text{ mL}$ total / $1.12\text{ mL}$ models)
    </figcaption>
  </figure>
</div>

### PreForm Parameters
* **Machine Name:** Formlabs Form 4 / Form 3+ SLA Printer
* **Material:** Formlabs Grey V5 / Standard Photopolymer Resin
* **Layer Height:** $0.050\text{ mm}$ ($50\text{ microns}$)
* **Build Orientation:** Parts tilted to prevent flat-surface suction cupping and minimize peel forces.
* **Support Settings:** Auto-generated touchpoints with optimized support density, keeping touchpoints away from internal sliding slots.
* **Estimated Print Time:** $1\text{ hour } 33\text{ minutes}$
* **Total Volume:** **$3.33\text{ mL}$** (Well below the $20.0\text{ mL}$ maximum allowable threshold including supports and raft).

A timelapse video of the SLA print process running in the Formlabs chamber:

<div align="center">
  <figure style="display: inline-block; margin: 10px; width: 50%; vertical-align: top;">
    <video width="100%" controls>
      <source src="./print_timelapse.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 8px; text-align: center;">
      Timelapse of the scorekeeper parts being printed
    </figcaption>
  </figure>
</div>

---

## Post-Processing

Post-processing involved washing, support removal, and UV thermal post-curing:

<div align="center">
  <figure style="display: inline-block; margin: 10px; width: 50%; vertical-align: top;">
    <video width="100%" controls>
      <source src="./curing.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 8px; text-align: center;">
      Video of post-curing stages in the chamber
    </figcaption>
  </figure>
</div>

* **Washing:** Cleaned in Isopropyl Alcohol (IPA $> 99\%$) for 10 minutes in an automated wash station to strip unpolymerized surface resin.
* **Support Removal:** Supports carefully snipped flush with diagonal cutters prior to UV curing to prevent localized stress marks on precision faces.
* **Curing:** Post-cured in a UV thermal chamber.
* **Surface Finish & Inspection:** Surfaces exhibited smooth matte finishes with no visible warping across primary sliding channels.

---

## Fit Test & Physical Verification

Using digital vernier calipers, key dimensions of the printed and post-cured features were recorded across multiple orientation points to evaluate compliance with the ANSI B4.1 RC 2 specification.

### Photo of Actual Printed Parts
<div align="center">
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="printed_parts_photo.jpg" alt="Showing actual printed parts" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Photo of the final printed scorekeeper parts
    </figcaption>
  </figure>
</div>

### Video of Actual Printed Parts
<div align="center">
  <figure style="display: inline-block; margin: 10px; width: 50%; vertical-align: top;">
    <video width="100%" controls>
      <source src="./printed_parts_video.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 8px; text-align: center;">
      Video demonstrating sliding motion of the printed parts
    </figcaption>
  </figure>
</div>

### Caliper Measurement Summary

| Feature Dimension | Nominal Target (in) | CAD Offset Target (in) | Measured Value (Post-Cure, in) | Deviation from Nominal (in) |
| :--- | :--- | :--- | :--- | :--- |
| **Part A – Track/Slot Width** | $0.3750$ | $0.3780$ | $0.3762$ | $+0.0012$ |
| **Part B – Slider Insert Width** | $0.3750$ | $0.3738$ | $0.3751$ | $+0.0001$ |
| **Measured Assembly Clearance** | $0.0000$ | $0.0042$ | **$0.0011$** | Within RC 2 Window ($0.0004 - 0.0016\text{ in}$) |

### Functional Verification
Upon manual assembly, the sliding tab (Part B) snapped smoothly onto the main track of Part A. The slider glides continuously along the score line under light thumb pressure without binding, hitching, or sticking. Furthermore, when lateral side-to-side force is applied, zero perceptible wobble or mechanical play is observed, confirming that the assembly achieves a true, high-accuracy **RC 2 running and sliding fit**.

---

## Lessons Learned

### Process Log

| Time Spent | What Changed |
| :--- | :--- |
| **2.5 Hours** | ANSI B4.1 RC 2 specification research, nominal dimension selection ($0.375\text{ in}$), and offset calculations for SLA light bleed. |
| **3.5 Hours** | CAD modeling of Part A (Housing) and Part B (Sliding Tab) in SolidWorks, parametric lip constraints, internal stress-relief fillet integration, and assembly verification. |
| **3.5 Hours** | PreForm slicing layout, Formlabs SLA print execution ($3.33\text{ mL}$ total volume), IPA washing, UV curing, digital caliper measurement, and final documentation. |

### Mistakes & Troubleshooting
A primary challenge was accounting for resin shrinkage across enclosed internal bores versus exterior pins, which required iterative offset testing. Initial test concepts without shrinkage compensation resulted in slight interference due to internal UV light bleed shrinking the internal track. Applying an explicit $+0.0030\text{ in}$ offset on internal slots successfully compensated for optical expansion.

Another key learning outcome was the necessity of adding internal fillets to the slider lips. Rounding these sharp interior transitions distributed flexural stress across the part during snap-assembly, allowing it to endure higher operational loads without cracking.

### Resources Used
1. Formlabs Form 4
2. Wash Station & UV Curing Chamber
3. SolidWorks
4. Machinery’s Handbook
5. Calipers

 <script>
  MathJax = {
    tex: {
      inlineMath: [['$', '$'], ['\\(', '\\)']]
    }
  };
</script>
<script id="MathJax-script" async
  src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js">
</script>
