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

---

## Brakes and Clutches

Brakes and clutches both use controlled friction, but they do different jobs. A **brake** connects a rotating part to the stationary vehicle structure so the vehicle slows or stops. A **clutch** connects or disconnects two rotating parts so engine torque can be transmitted smoothly or interrupted.

---

### Brakes

#### What it is

##### Description and rough working principle

A vehicle brake converts the vehicle's kinetic energy into another form so wheel speed decreases.

- In a hydraulic **disc brake**, the pedal moves a master-cylinder piston. Brake-fluid pressure travels through the lines to the caliper pistons, which squeeze two pads against a rotor fixed to the wheel. Friction produces braking torque and heat.[^8]
- In a **drum brake**, a hydraulic wheel cylinder pushes two curved shoes outward against the inside of a rotating drum. Return springs retract the shoes when pressure is released.[^9]
- In an EV or hybrid, **regenerative braking** makes the traction motor operate as a generator. Vehicle energy is converted to electrical energy and returned to the high-voltage battery; friction brakes still provide stronger braking, very-low-speed braking and stationary holding.[^10]
- ABS can rapidly reduce and restore hydraulic pressure at an individual wheel to prevent sustained wheel lock. ABS changes how braking force is controlled; it does not replace the service brake.

##### Why a car needs brakes

- Slow the vehicle predictably and stop it within a safe distance.
- Hold the vehicle stationary when parked or stopped on a slope.
- Control speed on descents and during manoeuvres.
- Provide the wheel-torque control used by ABS, traction control and stability control.
- In an EV or hybrid, recover some energy while retaining a friction-brake backup when regeneration is unavailable or insufficient.

##### Types of Brakes

| Brake Type | Common Use | Advantage | Disadvantage | Image |
| --- | --- | --- | --- | --- |
| Hydraulic disc brake | Front brakes on most passenger cars; often all four wheels | Good heat rejection; pads are accessible; clamping action is easy to see and demonstrate | Rotor and caliper must be aligned; a realistic hydraulic model needs fluid, seals and bleeding | ![Animated hydraulic disc-brake operation](attachments/brake-disc.gif) |
| Drum brake | Rear brakes on some small cars and trucks; parking-brake duty | Compact parking-brake integration; large friction area; self-energising shoe geometry can reduce actuation force | Enclosed drum retains heat; springs and adjuster are less visible and more complicated to assemble | ![Leading-trailing and other drum-brake shoe arrangements](attachments/brake-drum-types.svg) |
| Regenerative brake | Battery-electric and hybrid vehicles | Recovers energy; reduces friction-pad wear; motor torque is electronically controllable | Braking depends on motor, inverter, battery limits and vehicle speed; friction brakes are still required | ![Electric-vehicle regenerative braking system](attachments/brake-regenerative.png) |

#### Part List

##### Main parts in a road-car brake system

| Main Part | Function |
| --- | --- |
| Brake pedal, booster and master cylinder | Create and amplify the driver's hydraulic command |
| Reservoir, brake fluid, rigid lines and flexible hoses | Store and transmit hydraulic pressure |
| Rotor and caliper, or drum and wheel cylinder | Convert hydraulic force into friction torque at each wheel |
| Pads or shoes and friction lining | Provide the replaceable friction surfaces |
| Return springs, slide pins and adjusters | Release the brake and maintain operating clearance |
| Parking-brake lever/actuator and cable or motor | Hold the vehicle independently of the normal pedal system |
| Wheel-speed sensors, ABS modulator and controller | Detect wheel slip and modulate individual brake pressure |
| EV motor, inverter and high-voltage battery | Provide and absorb regenerative braking power where fitted |

##### Teaching demonstrator

| Make (3D print / laser cut) | Buy |
| --- | --- |
| Large rotor, caliper shell and replaceable pad carriers | Steel input shaft, bearings/pillow blocks and shaft collars |
| Cable- or screw-operated piston/lever mechanism | Commercial friction material or small bicycle brake pads |
| Pedal/hand lever, mounting plate and adjustable pad-clearance features | Bowden cable, springs, fasteners and threaded inserts |
| Colour-coded pressure/force arrows and wheel-speed markers | Clear polycarbonate guard and low-speed hand crank or geared motor |
| Optional drum, shoes and removable cover for comparison | Optional master/slave cylinder set, compatible brake fluid and catch tray |

#### Teaching Platform

##### 3D printing / manufacturing easiness

- **Dry mechanical disc-brake model — easy to moderate:** the rotor, caliper body, pad carriers and lever can be printed. Flatness, concentricity and sufficient shaft support matter more than fine surface detail.
- **Drum-brake model — moderate:** the circular parts are easy to CAD, but shoe pivots, return springs and the adjuster add small parts and assembly work.
- **Hydraulic disc-brake model — moderate to hard:** use commercial cylinders, hose and seals. Printed pressure-containing parts can leak or fail and should not be used.
- **Regenerative-brake rig — hard:** it needs a motor/generator, drive electronics, a safe electrical load or battery, sensing and control logic.
- A printed demonstrator is for low-speed teaching only and must never be installed on a vehicle.

##### Demonstratability

- The simplest demonstration needs **no external fluid**: turn a guarded rotor by hand or with a low-speed motor, pull a cable/screw actuator and observe the pads clamp the rotor.
- Put coloured marks on the shaft and rotor, and add a spring scale at the lever to compare input force with braking effect.
- A hydraulic demonstration does require compatible brake fluid, sealed commercial cylinders, hose, bleeding equipment and a catch tray.
- A drum model should use a removable or transparent cover so shoe movement remains visible.
- Regenerative braking needs a motor/generator, controller and electrical load or battery; an energy meter makes recovered power visible.

##### Works with what

- **Wheel end:** wheel hub, rotor or drum, bearings and tyre-road contact.
- **Driver input:** pedal, booster, master cylinder and hydraulic lines, or an electronic brake-by-wire command.
- **Control systems:** wheel-speed sensors, ABS hydraulic modulator, traction control and stability control.
- **Parking system:** cable or electric parking-brake actuator and a mechanical holding feature.
- **EV/hybrid system:** traction motor, inverter, battery-management limits and blended-braking controller; friction brakes remain necessary.[^10]

##### CAD easiness

- **Easy:** simplified rotor, pads, cable lever, mounting plate and open caliper shell.
- **Moderate:** drum shoes, adjuster, return-spring anchors and a visually accurate floating caliper.
- **Hard:** pressure-tight hydraulics, ABS modulator or a functional regenerative/brake-blending system.
- For a clear teaching model, enlarge pad travel and clearances slightly, use different colours for fixed and moving parts, and expose the force path.

##### Recommended brake demonstrator

Build a large, guarded **dry disc-brake model** with a hand crank or low-speed geared motor and a cable- or screw-operated caliper. It is easy to print and CAD, shows the braking action immediately, and needs no fluid. Add a removable drum-brake model or a separate motor/generator rig only if the project needs a comparison.

---

### Clutches

#### What it is

##### Description and rough working principle

A clutch is a controllable connection between a driving shaft and a driven shaft.

- In a conventional single-plate dry clutch, a diaphragm spring pushes the pressure plate against the clutch disc and flywheel. Friction locks the three together so engine torque reaches the gearbox input shaft.[^11]
- Pressing the clutch pedal moves a cable or hydraulic release system. The release bearing deflects the diaphragm spring, the pressure plate unloads the disc and the engine can rotate independently of the gearbox.
- During launch the disc is allowed to slip briefly, letting the engine and stationary drivetrain approach the same speed smoothly. A torsional damper in the disc reduces vibration and shock.[^12]
- Multi-plate clutches stack alternating driving and driven plates to obtain more torque capacity in a small diameter. Centrifugal clutches use speed-sensitive shoes or weights to engage automatically.

##### Why a car needs a clutch

- Disconnect the engine from the drivetrain while starting, stopping or selecting a gear.
- Allow controlled slip when launching from rest so the engine does not stall and the vehicle does not jerk.
- Reconnect power smoothly after a gear change.
- Reduce torsional shock and protect gears, shafts and joints from sudden torque changes.
- In DCTs, hybrids and automatic transmissions, multiple controlled clutches select power paths even though the driver may not operate a clutch pedal.

##### Types of Clutches

| Clutch Type | Common Use | Advantage | Disadvantage | Image |
| --- | --- | --- | --- | --- |
| Single-plate dry diaphragm clutch | Manual-transmission passenger cars and light trucks | Compact; efficient when fully engaged; operation and release mechanism are easy to understand | Friction lining wears; poor control causes heat, judder or stalling; needs axial release travel | ![Single-plate diaphragm clutch in engaged and released positions](attachments/clutch-single-plate.png) |
| Multi-plate wet or dry clutch | Motorcycles, dual-clutch transmissions, automatic transmissions and performance cars | High torque capacity in a small diameter; several interfaces share the load | More plates, tight tolerances and heat management; a wet clutch needs oil, sealing and drag control | ![Animated multi-plate clutch operation](attachments/clutch-multi-plate.gif) |
| Centrifugal clutch | Scooters, small utility vehicles and simple automatic drives | Engages automatically as speed rises; no clutch pedal or external release actuator | Engagement speed depends on springs, mass and wear; slipping creates heat; guarded rotation is required for a demo | ![Centrifugal clutch patent drawing](attachments/clutch-centrifugal.png) |

#### Part List

##### Main parts in a single-plate automotive clutch

| Main Part | Function |
| --- | --- |
| Flywheel | Provides the engine-side friction surface and rotational inertia |
| Clutch disc, friction linings and splined hub | Carries torque to the gearbox input shaft while permitting axial release |
| Torsional damper springs | Filter engine torque pulses and driveline shock |
| Pressure plate and clutch cover | Clamp the disc to the flywheel |
| Diaphragm spring | Supplies clamp load and acts as the release lever system |
| Release bearing and guide tube | Apply axial force to the diaphragm while allowing rotation |
| Release fork, pedal and cable or hydraulic cylinders | Carry the driver's command to the release bearing |
| Pilot bearing and gearbox input shaft | Support and align the driven shaft |

##### Teaching demonstrator

| Make (3D print / laser cut) | Buy |
| --- | --- |
| Enlarged flywheel, pressure plate, clutch disc and transparent cover | Two steel shafts, bearings/pillow blocks and shaft collars |
| Simplified splined or keyed disc hub | Friction sheet, cork/rubber lining or a small commercial clutch disc |
| Release fork, pedal/hand lever and adjustable pressure-plate guides | Compression springs, thrust bearing, cable and fasteners |
| Colour-coded torsional-damper insert and shaft-speed markers | Hand crank or guarded low-speed geared motor and controllable load |
| Optional interchangeable single- and multi-plate stacks | Clear polycarbonate safety guard and threaded inserts |

#### Teaching Platform

##### 3D printing / manufacturing easiness

- **Simplified single-plate dry clutch — moderate:** large circular parts are easy to print, but the pressure plate must move axially without tilting and the disc must remain centred.
- **Multi-plate dry stack — moderate:** plates are simple, but flatness, alternating tabs and controlled stack clearance matter.
- **Wet multi-plate clutch — hard:** it needs a sealed oil housing, compatible friction material, lubrication and heat management.
- **Centrifugal clutch — moderate to hard:** pivots and shoes are straightforward, but spring selection, balance, engagement speed and containment require care.
- A real vehicle clutch requires heat-resistant lining, accurately ground surfaces, controlled clamp load and high-speed balance; printed parts are suitable only for a guarded low-speed model.

##### Demonstratability

- The recommended dry model needs **no external fluid**. Turn the input shaft by hand, clamp the disc, and show both shafts rotate together; pull the release lever and show the input turn while the output stops.
- Mark both shafts to make slip, engagement and relative speed visible. An adjustable spring preload can demonstrate the relationship between clamp force and torque capacity.
- Apply a small controllable output load to show why partial engagement slips and generates heat, but keep speed and contact temperature low.
- A wet clutch requires oil and a leak-proof case. A centrifugal clutch requires a motor, speed controller, tachometer and strong transparent guard.
- Do not touch rotating parts or use an unguarded printed flywheel, shoe or pressure plate.

##### Works with what

- **Input side:** engine crankshaft, flywheel and usually a pilot bearing.
- **Output side:** splined gearbox input shaft, transmission gears and the rest of the drivetrain.
- **Release system:** pedal plus cable, or master/slave hydraulic cylinders, release fork and release bearing.
- **Supporting systems:** bellhousing, bearings, mounts and sometimes a dual-mass flywheel.
- **Automated systems:** clutch actuator, transmission control unit and shaft-speed/temperature sensing; a DCT needs two clutches and two gear-train input paths.

##### CAD easiness

- **Easy:** non-functional exploded display, flat clutch disc and simple flywheel.
- **Moderate:** moving single-plate model with pressure-plate guides, release lever, keyed hub and adjustable spring preload.
- **Moderate to hard:** multi-plate stack or centrifugal shoes with realistic clearances and balance.
- **Very hard:** vehicle-grade diaphragm-spring geometry, friction/thermal design, torsional damper, spline standards, fatigue life and high-speed containment.

##### Recommended clutch demonstrator

Build a large, guarded **single-plate dry clutch** with two supported shafts, a spring-loaded pressure plate and a hand-operated release fork. Use visible shaft marks and adjustable clamp load. It clearly demonstrates engaged, slipping and disengaged states without oil, hydraulics or specialist tools.

---

### Brakes and Clutches: Sources and Image Credits

#### Technical sources

[^8]: Brembo, [Brake caliper technology and operation](https://www.bremboparts.com/america/en/support/car/insights/brake-caliper-technology-and-operation-324333), describing hydraulic pressure, pistons, pads, rotors and fixed/floating calipers.
[^9]: Continental, [Drum Brakes](https://www.continental-automotive.com/en/components/brake-systems/drum-brakes.html), describing hydraulic wheel-cylinder actuation of brake shoes against a drum.
[^10]: Bosch Mobility, [Regenerative braking systems](https://www.bosch-mobility.com/en/solutions/driving-safety/regenerative-braking-systems/), explaining motor-generator energy recovery and the continuing role of friction brakes.
[^11]: MIT 2.972, [Clutch](https://web.mit.edu/2.972/www/reports/clutch/clutch.html), explaining engagement of the friction disc between flywheel and pressure plate.
[^12]: ZF, [Clutch Systems](https://www.zf.com/products/en/cv/products_65885.html), describing diaphragm-spring clamp load, the clutch disc and torsional vibration damping.

#### Image credits

- [Hydraulic disc brake diagram](https://commons.wikimedia.org/wiki/File:Hydraulic_disc_brake_diagram.gif) by KDS444, CC BY-SA 3.0.
- [Drum-brake arrangements](https://commons.wikimedia.org/wiki/File:Tipologia_tamburo.svg) by A7N8X, CC BY-SA 4.0.
- [Electric car diagram](https://commons.wikimedia.org/wiki/File:Electric_car_diagram.svg) by Ian Furst, CC BY-SA 4.0.
- [Single-plate diaphragm clutch](https://commons.wikimedia.org/wiki/File:Embrague2.png) by Enrique A. Chaparro, Free Art License.
- [Multiple Disk Clutch](https://commons.wikimedia.org/wiki/File:Multiple_Disk_Clutch.gif) by Oguraclutch, public domain.
- [Centrifugal clutch patent drawing](https://commons.wikimedia.org/wiki/File:US_Patent_598314_detail_centrifugal_clutch.png) by W. A. Crowdus, public domain.
