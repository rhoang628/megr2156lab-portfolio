# Lab #9 Laser Cutter

<small>***(Clicking on the images will enlarge them)***</small>

## Design

The first thing my partner and I did was decide the variables that we would need for our own parts—namely the thickness and kerf measurements.

### Material Thickness
When beginning this part, my partner and I measured the wood given to us from three different points ($0.10\text{ in}$, $0.12\text{ in}$, $0.10\text{ in}$), getting an average value of **$0.1117\text{ in}$** for our piece of wood. This $0.1117\text{ in}$ value became our material thickness variable in the CAD parameters.

### Kerf Measurement
When putting a $12\text{ mm} \times 12\text{ mm}$ square into the laser cutter, we got a final kerf measurement of **$0.009\text{ in}$**, which was the difference in size from our CAD model to the physical laser-cut part ($0.004\text{ in}$ offset per side).

First, we added the $12\text{ mm} \times 12\text{ mm}$ square to SolidWorks:

<div align="center">
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="kerf_test1.jpg" alt="Showing the first kerf test" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Showing the first kerf test
    </figcaption>
  </figure>
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="kerf_test2.jpg" alt="Showing the second kerf test file" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Showing the second kerf test file
    </figcaption>
  </figure>
</div>

Next, we cut out this square and measured how far off it was. Below is a video of the kerf coupon being laser cut:

<div align="center">
  <figure style="display: inline-block; margin: 10px; width: 50%; vertical-align: top;">
    <video width="100%" controls>
      <source src="Kerf_cutting.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 8px; text-align: center;">
      Video of the kerf coupon being laser cut
    </figcaption>
  </figure>
</div>

After cutting, we measured the offset value ($0.004\text{ in}$):

<div align="center">
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="IMG_9797.jpg" alt="Showing the offset of the wood to the first measurement" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Showing the offset of the wood to the first measurement
    </figcaption>
  </figure>
</div>

---

### Gear Ratio and Parametric Modeling

First, we added the global parameters in SolidWorks CAD to begin parametric modeling:

<div align="center">
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="Screenshot_1.jpg" alt="Showing the first parametric decisions" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Showing the first parametric decisions
    </figcaption>
  </figure>
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="Screenshot_2.jpg" alt="Showing the base width and length" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Showing the base width and length ($4.00\text{ in} \times 3.00\text{ in}$)
    </figcaption>
  </figure>
</div>

Next, we extruded this base to the desired height chosen by the thickness parameter:

<div align="center">
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="Screenshot_3.jpg" alt="Showing the extrude" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Showing the base extrude
    </figcaption>
  </figure>
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="Screenshot_4.jpg" alt="Showing the differing holes" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Showing the mounting holes with center distance set by parametric equations
    </figcaption>
  </figure>
</div>

To build the gear train, we started by designing the smaller gear ($\varnothing 0.88\text{ in}$) with a central shaft bore so the gear could rotate smoothly:

<div align="center">
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="Screenshot_5.jpg" alt="Showing the small gear creation in 2D" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Showing the small gear creation in 2D
    </figcaption>
  </figure>
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="Screenshot_6.jpg" alt="Showing the small gear extrusion" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Showing the small gear extrusion
    </figcaption>
  </figure>
</div>

Using SolidWorks circular patterns, we generated the complete tooth profile around the edge:

<div align="center">
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="Screenshot_7.jpg" alt="Showing the small gear pattern" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Showing the small gear circular pattern
    </figcaption>
  </figure>
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="Screenshot_8.jpg" alt="Showing the small gear" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Showing the completed smaller gear
    </figcaption>
  </figure>
</div>

From the smaller gear, we created the larger gear ($\varnothing 1.63\text{ in}$) by making a parametric copy and updating the dimensions and shaft fit diameter without rebuilding from scratch:

<div align="center">
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="Screenshot_9.jpg" alt="Showing changing to a larger gear" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Showing changing to a larger gear diameter
    </figcaption>
  </figure>
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="Screenshot_10.jpg" alt="Showing changing to a larger gear pattern" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Showing changing to a larger gear pattern
    </figcaption>
  </figure>
</div>

Since thickness is linked parametrically, the finished larger gear updated automatically:

<div align="center">
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="Screenshot_11.jpg" alt="Showing finished larger gear" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Showing finished larger gear
    </figcaption>
  </figure>
</div>

---

### Interlocking Shafts and Slotting Washers

Next, we designed the two shaft pins based on the inner gear bore dimensions:

<div align="center">
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="Screenshot_12.jpg" alt="Showing the start of the shaft" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Showing the start of the shaft sketch
    </figcaption>
  </figure>
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="Screenshot_13.jpg" alt="Showing the shaft extrusion" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Showing the shaft extrusion
    </figcaption>
  </figure>
</div>

We then created retention washers with matching cross cutouts that fit the base plate holes so the shafts can rotate freely without excess friction:

<div align="center">
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="Screenshot_14.jpg" alt="Showing the first slotting hole" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Showing the first slotting hole washer sketch
    </figcaption>
  </figure>
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="Screenshot_15.jpg" alt="Showing the first slotting hole extrude" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Showing the slotting hole washer extrusion
    </figcaption>
  </figure>
</div>

We assembled the half-lap shaft pins into a separate cross-shaft sub-assembly to check fitment before mounting them to the plate:

<div align="center">
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="Screenshot_16.jpg" alt="Showing the shafts fitting together pt1" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Showing the shafts fitting together pt. 1
    </figcaption>
  </figure>
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="Screenshot_17.jpg" alt="Showing the shafts fitting together pt2" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Showing the shafts fitting together pt. 2
    </figcaption>
  </figure>
</div>

<div align="center">
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="Screenshot_18.jpg" alt="Showing the shafts fitting together pt3" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Showing the shafts fitting together pt. 3
    </figcaption>
  </figure>
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="Screenshot_19.jpg" alt="Showing the shafts fitting together pt4" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Showing the shafts fitting together pt. 4
    </figcaption>
  </figure>
</div>

<div align="center">
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="Screenshot_20.jpg" alt="Showing the shafts fitting together pt5" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Showing the completed cross-shaft
