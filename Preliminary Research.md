# Core Components

## Gearboxes, Transmissions, Torque Converters

The three subjects are related, but they are not the same component. They are researched separately below:

- A **gearbox** is the gears-and-shafts mechanism that changes speed, torque or direction.
- A **transmission** is the complete vehicle unit that selects and controls ratios. It contains a gearbox plus items such as clutches, selectors, bearings, lubrication and controls.
- A **torque converter** is a hydrodynamic input device used ahead of many automatic transmissions. It transfers engine power through fluid and is not itself a gearbox.

---

### Gearboxes

#### What it is

##### Description and rough working principle

A gearbox passes rotation through meshing gears. Changing the relative tooth counts changes output speed and torque:

- For a simple gear pair, `reduction ratio = driven gear teeth / driving gear teeth`.
- A 15-tooth driving gear turning a 45-tooth driven gear gives a 3:1 reduction: the output turns once for every three input turns.
- Ignoring losses, the 3:1 reduction produces about three times the input torque at one-third of the speed.
- Two external gears reverse direction. Adding another external idler gear reverses it again, which is useful for a vehicle's reverse gear.
- A multi-ratio gearbox places several gear pairs on shafts and selects which pair carries torque.
- A planetary gearbox uses a central sun gear, planet gears on a carrier and an internal ring gear. Holding, driving and taking output from different members produces different ratios from one compact coaxial set.[^1]

![Two spur gears forming a 3:1 reduction](attachments/gearbox-spur-reduction.svg)

##### Why a car needs a gearbox

- **Launch and climbing:** reduction multiplies torque at the wheels.
- **Speed range:** an internal-combustion engine cannot operate efficiently from zero wheel speed to highway speed using one direct ratio.
- **Efficient cruising:** a taller ratio lowers engine speed, noise and fuel use at road speed.
- **Direction:** the gear train can provide reverse without reversing engine rotation.
- **Packaging:** planetary gearsets provide several ratios on one axis; a fixed reduction lets a high-speed EV motor drive the wheels at a practical speed.

##### Types of Gearboxes

| Gearbox Type | Common Use | Advantage | Disadvantage | Image |
| --- | --- | --- | --- | --- |
| Single-stage spur/helical reduction | EV drive units, final reductions, simple teaching rigs | Few parts; efficient; easiest to understand, print and CAD | Only one ratio; external gears reverse direction; helical gears add axial bearing load | ![Spur reduction gears](attachments/gearbox-spur-reduction.svg) |
| Parallel-shaft, constant-mesh multi-ratio | Manual transmissions, DCT gear-train halves | Several ratios using familiar gear pairs; power flow is visible | Needs accurate shaft spacing, selectors and axial packaging; more gears rotate even when not selected | ![Parallel-shaft manual gearbox cutaway](attachments/transmission-manual-cutaway.jpg) |
| Planetary / epicyclic | Conventional automatic transmissions, hybrid power-split devices | Compact and coaxial; several ratios by holding different members; load shared by multiple planets | Ring gear and carrier are harder to manufacture; ratio combinations and clutch logic are less intuitive | ![Planetary gearset schematic](attachments/transmission-planetary-gearset.svg) |

#### Part List

For a printable gearbox teaching module:

| Make (3D print / laser cut) | Buy |
| --- | --- |
| Two or three interchangeable spur-gear pairs | Steel input, counter and output shafts (D-shaft or keyed) |
| Optional sun, planet, ring and carrier set | Ball bearings or low-friction bushings |
| Split housing with removable clear acrylic cover | Shaft collars, keys, retaining rings and spacers |
| Sliding dog sleeve and simple selector fork | Fasteners and metal dowel pins |
| Input/output direction and ratio indicator discs | Small amount of plastic-safe grease |
| Motor/hand-crank and output-load mounting plates | Hand crank or low-speed geared DC motor |

#### Teaching Platform

##### 3D printing / manufacturing easiness

- **Single spur reduction — easy:** large printed teeth and purchased shafts/bearings are enough for a low-speed model.
- **Two-/three-ratio constant-mesh gearbox — easy to moderate:** the main challenges are centre distance, backlash, shaft support and complete dog-clutch engagement.
- **Simple planetary gearbox — moderate:** the sun, ring and carrier must be concentric; planet gears must be evenly spaced and supported on both sides.
- **Working synchromesh — hard:** friction cones, blocker-ring clearance, splines, small dog teeth and detents need close tolerances.
- Print gears flat where possible for consistent teeth. Use metal shafts and through-fasteners instead of printed threads.
- PLA/PETG is suitable only for slow, low-load demonstrations—not vehicle loads or high rotational speed.

##### Demonstratability

- Excellent for demonstration; no fluid or special external tool is needed.
- Turn the input by hand and count input/output revolutions to measure each ratio.
- Mark one tooth on every gear and use different colours for the input, idler and output gears.
- Add a small friction brake or hanging-weight drum to the output so students can feel increased torque in a lower ratio.
- Move the selector to neutral to show that gears may spin while no torque reaches the output.
- Add/remove a reverse idler to make the output direction change visibly.
- On the planetary module, use removable locking pins to hold the sun, ring or carrier and compare the resulting ratios.

##### Works with what

- **Input:** hand crank, geared electric motor or engine simulator.
- **Output:** coupling, drive shaft, differential/final drive or wheel module.
- **Support:** shafts, bearings/bushings, housing, lubrication and a clear safety guard.
- **For multiple ratios:** selector sleeve/dog clutch and shift fork; a real vehicle also needs a clutch or another way to unload the gears during a shift.
- **For a planetary set:** brakes/clutches or removable holding pins must control which member is fixed, driven and used as output.

##### CAD easiness

- **Easy:** single-stage spur reduction using an involute-gear generator.
- **Easy–moderate:** parallel-shaft multi-ratio gearbox; add axial spacing, selector travel, shaft retention and backlash checks.
- **Moderate:** planetary gearbox. For a simple set with equal gear module, `ring teeth = sun teeth + 2 × planet teeth`.
- **Hard:** realistic synchromesh or compact vehicle-grade helical gearbox because tolerances, splines, bearings and lubrication paths all interact.

##### Recommended gearbox demonstrator

Use a modular three-shaft constant-mesh gearbox with two forward ratios, neutral and reverse, plus a separate planetary module with removable holding pins. It is printable, visually clear, easy to operate by hand and useful with the later transmission and differential demonstrations.

---

### Transmissions

#### What it is

##### Description and rough working principle

A vehicle transmission is the complete system that accepts power from the engine or traction motor, selects an appropriate ratio and sends controlled output to the rest of the drivetrain.

- A **manual transmission** uses a driver-operated clutch and shift lever. Constant-mesh gears rotate on the shafts; synchronizers match speed before a sleeve locks the chosen gear to the output shaft.[^2]
- A **torque-converter automatic** uses a torque converter for launch, planetary gearsets for ratios and hydraulically applied clutches/brakes to select the power path. A transmission control unit commands valves or solenoids.[^3][^4]
- A **dual-clutch transmission (DCT)** has two manual-like gear-train halves and two clutches. One half carries the current gear while the next gear can be preselected on the other; the controls swap clutches for a rapid shift.[^5]
- A **single-speed EV transmission** normally combines one fixed reduction gearset, bearings, differential/final drive and lubrication in a compact drive unit.

##### Why a car needs a transmission

- It keeps the engine or motor in a usable speed/torque range while road speed changes.
- It provides launch, acceleration, cruising, neutral and reverse functions.
- It gives the driver or controller a safe, repeatable way to select ratios.
- It supports and lubricates the rotating parts and connects the power source to the final drive.
- In an EV, the transmission may have only one fixed ratio, but the reduction, housing, bearings, differential and lubricant are still required.

##### Types of Transmissions

| Transmission Type | Common Use | Advantage | Disadvantage | Image |
| --- | --- | --- | --- | --- |
| Manual synchromesh | Manual passenger cars, sports cars, trucks | Efficient; direct driver control; internal power path is comparatively easy to trace | Driver must operate clutch and lever; shift interrupts torque; synchronizers and linkages require accurate fits | ![Manual transmission cutaway](attachments/transmission-manual-cutaway.jpg) |
| Torque-converter automatic | Most conventional automatic passenger cars and many trucks | Smooth launch; shifts under load; controller chooses ratios automatically | Many precision parts; needs fluid pump, clutch packs, valve/solenoid control and cooling | ![Eight-speed automatic transmission cutaway](attachments/transmission-automatic-cutaway.jpg) |
| Dual-clutch transmission (DCT) | Performance and efficient automated vehicles | Preselects the next gear; fast shifts; mostly mechanical power path | Two clutches, concentric shafts, actuators and control timing make design difficult; clutch heat/wear at low speed | ![Dual-clutch transmission schematic](attachments/transmission-dual-clutch.svg) |
| Single-speed EV reduction transmission | Most battery-electric vehicles | Few parts; compact, efficient and no shift mechanism | One ratio must satisfy launch torque and maximum motor speed; does not demonstrate gear changing | ![Integrated EV drive unit containing motor, inverter and reduction gear](attachments/transmission-ev-drive-unit.jpg) |

#### Part List

For a simplified selectable-ratio transmission demonstrator:

| Make (3D print / laser cut) | Buy |
| --- | --- |
| Gearbox housing and removable transparent cover | Steel shafts, bearings/bushings and shaft collars |
| Two forward gear pairs, reverse idler and sliding dog selector | Small geared DC motor or hand crank |
| Shift fork, guide rail, lever and detent plate | Flexible shaft coupling and fasteners |
| Simplified dry clutch disc/pressure plate display | Low-voltage speed controller if motor-driven |
| Motor, transmission and load mounting brackets | Optical tachometers/encoders (optional) |
| Ratio labels, power-flow arrows and safety guard | Adjustable friction load or small brake |

A realistic automatic or DCT would additionally require clutch packs, seals, hydraulic passages, a pump, valves/solenoids, speed sensors and an electronic controller. Those systems are better shown with a cutaway or schematic than reproduced as a working student-built mechanism.

#### Teaching Platform

##### 3D printing / manufacturing easiness

| Transmission Demonstrator | Manufacturing Difficulty | Reason |
| --- | --- | --- |
| Single-speed EV reduction | **Easy** | One gear pair, fixed shafts and no selector |
| Simplified dog-shift manual | **Moderate** | Several ratios plus shift sleeve/fork and axial retention |
| True synchromesh manual | **Hard** | Friction cones, blocker rings, splines and tight clearances |
| DCT | **Very hard** | Two clutches, two gear-train halves, concentric shafts and actuators |
| Hydraulic planetary automatic | **Very hard** | Multiple clutch packs, fluid circuits, valve control and precise shift timing |

##### Demonstratability

- A simplified manual is the clearest working model: use a hand crank or low-speed motor and a transparent cover.
- Select first, second, neutral and reverse while coloured arrows show the active power path.
- Use two tachometers or count turns to compare ratios quantitatively.
- A removable clutch model can show why torque must be interrupted before a manual shift.
- A DCT schematic can show odd/even gear paths, but a realistic working model needs two controlled clutches and synchronized actuators.
- A conventional automatic is difficult to see internally while running. A cutaway plus removable locking pins on a separate planetary module communicates the gear logic more clearly than a sealed hydraulic replica.
- No fluid is needed for the recommended manual/dog-shift model. A realistic automatic needs transmission fluid, a pump, control pressure and cooling.

##### Works with what

- **Before the transmission:** engine or motor, flywheel/flexplate and a clutch or torque converter depending on type.
- **After the transmission:** coupling/drive shaft and differential/final drive; a FWD transaxle packages the differential in the same housing.
- **Manual:** clutch, shift linkage and driver input.
- **Torque-converter automatic:** torque converter, automatic-transmission fluid, oil pump, clutch packs, valve body/solenoids, cooler and transmission controller.
- **DCT:** two clutches, electromechanical or electrohydraulic actuators, speed/position sensors and controller.
- **EV reduction:** traction motor, inverter/controller, final drive/differential and lubricated bearings/gears.
- **Teaching rig:** clear guard, low-speed drive and adjustable output load.

##### CAD easiness

- **Easy:** single-speed EV reduction transmission.
- **Moderate:** simplified two-speed dog-shift manual with large printed components.
- **Hard:** true synchromesh because selector travel, cone engagement, dog teeth, splines and detents must all align.
- **Very hard:** DCT or hydraulic automatic because CAD must coordinate many coaxial components, clutches, actuators and fluid/control hardware.

##### Recommended transmission demonstrator

Build a two-speed dog-shift manual transmission with neutral and reverse. Keep the synchronizer as a separate enlarged cutaway/display piece instead of making it load-bearing. Use the automatic and DCT images to compare architectures without adding their hydraulic and control complexity to the working rig.

---

### Torque Converters

#### What it is

##### Description and rough working principle

A torque converter is a sealed hydrodynamic device between an internal-combustion engine and a conventional automatic transmission. It transfers power through automatic-transmission fluid rather than through a continuously engaged dry friction clutch.[^4][^6]

![Torque converter cross-section: A pump, B stator, C turbine, D input shaft, E output shaft](attachments/torque-converter-cross-section.png)

The labelled cross-section shows the three main rotating-flow elements:

- **Pump/impeller (A):** fixed to the converter cover and engine input (D). It throws fluid outward and toward the turbine.
- **Turbine (C):** connected to the transmission input shaft (E). Moving fluid pushes its blades and produces output torque.
- **Stator (B):** mounted on a one-way clutch between pump and turbine. At low turbine speed it redirects returning fluid so it assists the pump instead of opposing it; this produces torque multiplication.
- **Lock-up clutch:** not shown in this simplified diagram. At cruise it mechanically connects input and output to eliminate most converter slip and heat.

##### Operating stages

| Stage | What Happens | Result |
| --- | --- | --- |
| Stall / launch | Engine turns the pump while the turbine is stopped or very slow; stator locks and redirects return flow | Maximum torque multiplication, maximum slip and rapid heat generation |
| Acceleration | Turbine speed rises; speed difference and multiplication gradually decrease | Smooth non-contact power transfer while the car accelerates |
| Coupling | Pump and turbine speeds become closer; stator freewheels | Converter behaves mainly as a fluid coupling, with some remaining slip |
| Lock-up | A friction clutch connects converter cover to turbine/input shaft | Near-direct mechanical drive, less heat and better efficiency |

##### Why a car needs a torque converter

- It lets an automatic-transmission vehicle stop in gear while the engine continues idling.
- It provides smooth launch without the driver operating a clutch pedal.
- It multiplies torque when starting and when the turbine is much slower than the pump.
- Fluid slip and internal damping absorb engine torsional vibration and driveline shock.
- The lock-up clutch restores efficiency once continuous slip is no longer needed.[^4]

#### Part List

##### Real automotive torque converter

| Main Part | Function |
| --- | --- |
| Welded converter cover and engine drive hub | Sealed rotating housing connected to flexplate/crankshaft |
| Pump/impeller | Adds energy to the fluid |
| Turbine and turbine hub | Converts fluid momentum back into output-shaft torque |
| Stator and one-way clutch | Redirects return flow during launch; freewheels near coupling speed |
| Lock-up clutch and torsional damper | Connects input/output mechanically and filters vibration |
| Bearings/thrust washers and seals | Maintain alignment and contain fluid |
| Automatic-transmission fluid | Working medium, lubrication and heat transport |

##### Teaching demonstrator

| Make (3D print / laser cut) | Buy |
| --- | --- |
| Enlarged dry pump, turbine and stator shapes | Used/cutaway torque converter for visual comparison |
| Transparent housing/display shell that does not hold pressure | Two small guarded electric fans for a dry airflow analogy |
| Fixed guide-vane/stator insert | Low-voltage power supply and speed controller |
| Colour-coded flow arrows and labelled cross-section stand | Clear safety guard, fasteners and bearings |
| Catch tray and mounting frame if any fluid demo is attempted | Suitable fluid, shaft seals and commercial one-way bearing for an advanced fluid model |

#### Teaching Platform

##### 3D printing / manufacturing easiness

- **Static cutaway/display — moderate:** the three elements can be enlarged and printed separately so blade direction is visible.
- **Dry two-fan analogy — moderate:** easy to assemble, but guide vanes and guards must be securely mounted.
- **Working fluid model — very hard and not recommended as the first build:** it needs curved blades, rotor balance, a leak-proof case, seals, one-way stator clutch, fill/bleed ports and fluid compatibility.
- A printed high-speed rotor can fail dangerously. Operate only a guarded, low-speed model and never treat printed parts as vehicle components.

##### Demonstratability

- A real converter is difficult to observe because it is opaque, sealed and full of fluid.
- A transparent fluid model needs external fluid, sealing, sufficient input speed, a load and a catch tray. Aeration and leaks can obscure the result.
- A cutaway is best for identifying parts but cannot demonstrate power transfer while open.
- Two guarded fans facing each other provide a clean analogy for non-contact fluid power transfer. Adding fixed guide vanes suggests the stator's role, but air fans do **not** reproduce an automotive converter's exact oil flow or torque ratio.
- The labelled diagram should remain beside the demo so students can connect pump, stator, turbine, input and output.

##### Works with what

- **Engine side:** engine crankshaft/flexplate and converter cover.
- **Transmission side:** input shaft and usually a planetary automatic transmission.
- **Fluid system:** automatic-transmission fluid, transmission oil pump, sump/filter and cooler/heat exchanger.[^6]
- **Controls:** lock-up clutch valve/solenoid and transmission control unit.
- **Supporting parts:** stator support and one-way clutch, bearings/thrust washers and seals.
- It normally replaces the launch clutch of a conventional automatic; it is not required with a normal manual transmission and is commonly replaced by clutches or an electric motor in DCT/hybrid architectures.

##### CAD easiness

- **Easy:** simplified labelled cross-section or non-rotating display shell.
- **Moderate:** enlarged dry pump/turbine/stator shapes for visual teaching.
- **Very hard:** functional converter. Blade angles, toroidal flow passages, clearances, balance, seals, stator one-way clutch and lock-up clutch require specialist design and manufacturing. Research measurements show the internal three-dimensional flow is highly unsteady and complex.[^7]

##### Recommended torque-converter demonstrator

Use the labelled cross-section plus a purchased used/cutaway converter. If motion is required, add a separate guarded two-fan airflow analogy. Do not make a high-speed fluid-filled printed converter unless leak containment, rotor balance and overspeed protection can be engineered and tested properly.

---

### Sources and Image Credits

#### Technical sources

[^1]: ZF, [Coaxial reduction gear](https://press.zf.com/press/en/media/media_57732.html), an EV reduction unit using two planetary gearsets and an integrated differential.
[^2]: U.S. educational manual-transmission unit, [Manual Transmission](https://files.eric.ed.gov/fulltext/ED204627.pdf), covering power flow, constant-mesh gears, synchronizers, shafts, bearings and lubrication.
[^3]: MIT 2.972, [How an Automatic Transmission Works](https://web.mit.edu/2.972/www/reports/automatic_transmission/automatic_transmission.html), describing the torque converter and planetary gearbox power path.
[^4]: ZF, [Torque Converter](https://www.zf.com/products/en/cars/products_65854.html), including hydrodynamic circuits, lock-up clutches and torsional damping.
[^5]: Volkswagen service training document hosted by NHTSA, [The 02E Direct Shift Gearbox](https://static.nhtsa.gov/odi/tsbs/2012/MC-10157658-9999.pdf), describing two independent gear-train halves, two clutches and preselection of the next gear.
[^6]: ZF PowerLine maintenance guide, [8-speed automatic transmission](https://www.zf.com/products/media/automotive/cv/literature_downloads_wna/truck_solutions/PowerLine_Maintenance_Guide.pdf), describing a torque converter with lock-up clutch, downstream planetary gearset, oil system and cooler connections.
[^7]: SAE Technical Paper 960721, [The Flow Field Inside an Automotive Torque Converter](https://doi.org/10.4271/960721), reporting measured three-dimensional, unsteady flow in the pump, turbine and stator.

#### Image credits

- [Two spur gears 1:3](https://commons.wikimedia.org/wiki/File:Two_spur_gears_1_3.svg) by Jahobr, CC0.
- [Manual transmission cutaway](https://commons.wikimedia.org/wiki/File:Engine_and_Gearbox_cutaway-001.jpg) by NJR ZA, CC BY-SA 3.0.
- [Planetary gearset schematic](https://commons.wikimedia.org/wiki/File:Planetary_gear_set_schematic.svg) by DaveRcWiki, CC0.
- [Eight-speed automatic transmission cutaway](https://commons.wikimedia.org/wiki/File:Lexus_IS_F_08.JPG) by Hatsukari715, public domain.
- [Dual-clutch transmission schematic](https://commons.wikimedia.org/wiki/File:Dual-clutch_transmission.svg) by Xavax/C-Lover, public domain.
- [Aisin integrated electric drive unit](https://commons.wikimedia.org/wiki/File:Aisin_Xin1_Electric_Drive_Unit.jpg) by TTTNIS, CC0.
- [Torque-converter cross-section](https://commons.wikimedia.org/wiki/File:Torque_converter_a_cross_section.png) by Toshinori baba, CC BY-SA 4.0.
