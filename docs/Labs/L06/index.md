# Lab #6 Design Fits for an Artifact

<small>***(Clicking on the images will enlarge them)***</small>

## Part 1: Artifact Measurement and Parameters
For this lab, the objective was to design and 3D-print a parametric baseplate that snap-fits onto an existing artifact (the SparkFun RedBoard Artemis). The design utilizes a cantilever snap-fit peg mechanism, created in PTC Creo.

### Measurements and Hole Center Calculations
Measurements were taken using a dial caliper. Because caliper jaws rest on the edges of small PCB holes, all hole locations were measured from the hole edge rather than the center, requiring offset calculations for the CAD sketch. 

<div align="center">
  <img src="measure_1.JPEG" width="180" style="margin: 4px;">
  <img src="measure_2.JPEG" width="180" style="margin: 4px;">
  <img src="measure_3.JPEG" width="180" style="margin: 4px;">
  <img src="measure_4.JPEG" width="180" style="margin: 4px;">
  <img src="measure_5.JPEG" width="180" style="margin: 4px;">
  <img src="measure_6.JPEG" width="180" style="margin: 4px;">
  <img src="measure_7.JPEG" width="180" style="margin: 4px;">
  <img src="measure_8.JPEG" width="180" style="margin: 4px;">
  <img src="measure_9.JPEG" width="180" style="margin: 4px;">
  <img src="measure_10.JPEG" width="180" style="margin: 4px;">
  <img src="measure_11.JPEG" width="180" style="margin: 4px;">
  <br>
  <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px; margin-bottom: 15px;">
    <i>Gallery: 11-part photo documentation of measuring the SparkFun RedBoard Artemis mounting holes and board dimensions.</i>
  </figcaption>
</div>

* **Board Dimensions:** 2.705" x 2.328"
* **Mounting Hole Diameter:** ~0.123"
* **Edge Offset (Radius):** 0.0615"

To find the exact center points for the CAD sketch, the radius was added to the edge measurements. For example, Hole 1 (USB-C side) was 0.530" from the port-side edge and 0.148" from the lateral edge:

$$Center_{X1} = 0.530 + \frac{0.123}{2} = 0.5915\text{ inches}$$
$$Center_{Y1} = 0.148 + \frac{0.123}{2} = 0.2095\text{ inches}$$

Similarly, for Hole 2, the edge measurement of 0.482" was adjusted to find its exact center:

$$Center_{X2} = 0.482 + \frac{0.123}{2} = 0.5435\text{ inches}$$

### Parametric Variables Used
The design was driven by the following parameters to ensure easy adjustments and accurate engineered allowances:
* `Base_Thickness = 0.070` (Rigid foundation)
* `Peg_Shaft_Dia = 0.118` (Provides 0.005" clearance for the 0.123" holes)
* `Shaft_Height = 0.065` (Matches standard 1.6mm PCB thickness)
* `Peg_Lip_Rad = 0.090` (Creates a 0.180" diameter base for a secure interference lock)
* `Cone_Top_Rad = 0.045` (0.090" diameter top acts as a lead-in guide)
* `Cone_Height = 0.070` (Smooth ramp angle for insertion)
* `Slit_Width = 0.065` (Increased negative space allowing the larger 0.180" lip to fully compress inward)

## Part 2: Parametric Design Steps
The design was modeled in PTC Creo entirely using parameters and relations. 

### 1. Baseplate and Cylinder Shafts
I started by defining the required parameters in Creo's tools menu so the dimensions could be easily updated later. Then, I sketched a 2.705" x 2.328" rectangle and extruded it to `Base_Thickness`.

<div align="center">
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="parameters.jpg" alt="Creo Parameters Menu" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Defining Parameters in Creo
    </figcaption>
  </figure>
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="base_sketch.jpg" alt="Baseplate Sketch" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Sketch of the Baseplate
    </figcaption>
  </figure>
</div>

Next, I sketched four circles at the calculated center points of the board's holes. The circles were constrained to `Peg_Shaft_Dia` using relations and extruded upward to `Shaft_Height`.

<div align="center">
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="base_extrude.jpg" alt="Baseplate Extrude" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Extrusion of the Baseplate
    </figcaption>
  </figure>
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="cylinder_sketch.jpg" alt="Cylinder Sketch" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Sketch of the Four Peg Shafts
    </figcaption>
  </figure>
</div>

### 2. Datum Plane and Truncated Cone Revolve
To model the locking lip, I created a new Datum Plane perfectly intersecting the center axis of the first cylinder. I then sketched half the profile of a truncated cone. **Note on workaround:** The Revolve tool required a space between the sketch profile and the center axis to generate. To fix this, I offset the inner edge of my sketch by 0.01" from the axis and subtracted 0.01" from my profile widths to keep the outer engineered tolerances identical. I then revolved the sketch 360 degrees.

<div align="center">
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="cylinder_extrude.jpg" alt="Cylinder Extrude" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Extrusion of the Peg Shafts
    </figcaption>
  </figure>
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="datum_plane.jpg" alt="Datum Plane Setup" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Custom Datum Plane for Revolve
    </figcaption>
  </figure>
</div>

<div align="center">
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="revolve_sketch.jpg" alt="Revolve Sketch Profile" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Truncated Cone Sketch (with 0.01" gap)
    </figcaption>
  </figure>
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="pattern_cone.jpg" alt="Patterning the Cone" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Revolving and Patterning the Locking Lip
    </figcaption>
  </figure>
</div>

### 3. Feature Patterning and Extrude-Cut
Instead of repeating the revolve, I used the Pattern tool to duplicate the truncated cone onto the remaining three cylinders. To create the cantilever flexure, I sketched a center rectangle set to the wider `Slit_Width` across the top of the first peg and used an Extrude (Remove Material) to split the peg into two prongs.

<div align="center">
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="slit_sketch.jpg" alt="Slit Sketch" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Sketch of the 0.065" Wide Slit
    </figcaption>
  </figure>
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="extrude_cut.jpg" alt="Extrude Cut Slit" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Splitting the Peg to Create Prongs
    </figcaption>
  </figure>
</div>

Finally, I patterned the Extrude-Cut feature to the other three pegs, completing the snap-fit mechanism for all four corners. 

<div align="center">
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="pattern_slit.jpg" alt="Patterning the Slit" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Patterning the Slit Cut
    </figcaption>
  </figure>
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="finished_cad.jpg" alt="Finished CAD Baseplate" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Finished Parametric Baseplate
    </figcaption>
  </figure>
</div>


## Part 3: 3D Printing and Test 

### Research and Preprocessor
* **Build Orientation:** The baseplate was printed completely flat on the bed. This is the only logical orientation to ensure X/Y dimensional accuracy for the peg spacing and to allow the Z-axis layers to build vertically up the shafts.
* **Material Selection:** PETG was chosen for the physical prototype.
* **Supports:** Supports were used because of its geometry.
* **Slicer Settings:** I used PrusaSlicer's **Structural** print profile with 15% gyroid infill. The Structural setting was specifically chosen to maximize layer adhesion—this is critical because the cantilever pegs are printed vertically, meaning the bending force during snap-fit insertion pushes directly against the layer lines. 

<div align="center">
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="prusaslicer_settings_1.jpg" alt="PrusaSlicer Settings Panel 1" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Infill Configuration
    </figcaption>
  </figure>
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="prusaslicer_settings_2.jpg" alt="PrusaSlicer Settings Panel 2" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Perimeter Configuration
    </figcaption>
  </figure>
</div>

<div align="center">
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="prusaslicer_sliced.jpg" alt="Sliced Preview" width="500">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Toolpath Preview Verifying the Slit Clearance
    </figcaption>
  </figure>
</div>

### Print and Testing
I printed the baseplate at the Rapid Lab using the Prusa CORE One. The bounding box of the print was roughly 68.7mm x 59.1mm x 4.7mm.

<div align="center">
  <figure style="display: inline-block; margin: 10px; width: 50%; vertical-align: top;">
    <video width="100%" controls>
      <source src="print_video.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 8px; text-align: center;">
      3D Printing the Baseplate on Prusa CORE One
    </figcaption>
  </figure>
</div>

<div align="center">
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="print_disconnected.JPEG" alt="Baseplate and Artemis Disconnected" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Printed Baseplate
    </figcaption>
  </figure>
  <figure style="display: inline-block; margin: 10px; vertical-align: top;">
    <img src="print_connected.JPEG" alt="Baseplate and Artemis Connected" width="350">
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 5px;">
      Board Snap-Fit into Place
    </figcaption>
  </figure>
</div>

<div align="center">
  <figure style="display: inline-block; margin: 10px; width: 50%; vertical-align: top;">
    <video width="100%" controls>
      <source src="usage_video.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="font-size: 0.85em; color: gray; margin-top: 8px; text-align: center;">
      Testing the Snap-Fit Mechanism
    </figcaption>
  </figure>
</div>

### Lessons Learned
* **Revolve Axis Geometry Constraints:** A major hurdle occurred during the revolve feature. Creo threw an error when the sketch profile was placed directly on the axis of revolution. I fixed this by offsetting the sketch 0.01" away from the center axis, simultaneously subtracting 0.01" from the sketch widths. This clever workaround allowed the feature to generate without altering the final outer engineered tolerances of the peg.
* **Feature Efficiency:** Using the Pattern tool to duplicate both the revolved cone and the extrude-cut slit saved significant time. It ensures that any dimensional changes to the primary peg (like adjusting the slit width to accommodate a larger lip) will automatically update all four pegs simultaneously.
* **FDM Tolerances:** Designing a cantilever snap-fit for a 3D printer requires understanding nozzle width and layer adhesion. Utilizing the Structural profile ensured the vertical pegs had enough strength to bend inward without snapping off at the layer lines. Verifying that the slicer preview did not merge the gap was also essential before printing.


## Resources

All design and print work was done with:

<ul style="list-style-type: circle !important; padding-left: 20px;">
  <li style="list-style-type: circle !important; margin-bottom: 4px;">
    SparkFun RedBoard Artemis & Dial Calipers
  </li>
  <li style="list-style-type: circle !important; margin-bottom: 4px;">
    PTC Creo
  </li>
  <li style="list-style-type: circle !important; margin-bottom: 4px;">
    <a href="https://www.prusa3d.com/p/prusaslicer/" target="_blank">PrusaSlicer</a>
  </li>
  <li style="list-style-type: circle !important; margin-bottom: 4px;">
    Rapid Lab (Prusa CORE One)
  </li>
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
</ul>

Total time from start to finish: 5 hours.
