# Core Components
## Gearboxes, Transmissions, Torque Converters

### What it is

#### Description

A **gearbox** is the gear-and-shaft mechanism that changes the relationship between input speed and output speed. A **transmission** is the complete vehicle assembly: the gearbox plus its selectors, clutches or brakes, bearings, lubrication and controls. A **torque converter** is the fluid coupling normally fitted between an internal-combustion engine and a conventional automatic transmission.

- A car needs different ratios because the engine cannot provide useful torque from zero speed to maximum road speed in one fixed ratio. A low gear reduces output speed and multiplies wheel torque for starting and climbing; a high gear allows road speed with lower engine speed, noise and fuel use.
- For a simple gear pair, the reduction ratio is approximately `driven gear teeth / driving gear teeth`. Ignoring losses, output speed is divided by this ratio and output torque is multiplied by it.
- Reverse adds an idler gear or changes which members of a planetary gearset are held and driven, so the output turns in the opposite direction.
- Neutral disconnects the selected power path even though some internal gears may continue to rotate.

In common configurations:

- **Manual synchromesh transmission:** engine → clutch → input shaft → countershaft gear pair → selected gear and synchronizer → output shaft. Most forward gears stay in constant mesh. The synchronizer uses friction to match the selected gear's speed to the shaft before a sleeve/dog teeth lock them together.[^1]

  ![Cutaway of an engine and manual transmission](attachments/transmission-manual-cutaway.jpg)

- **Torque-converter automatic transmission:** engine → torque converter → one or more planetary gearsets → output. Hydraulic/electric controls apply multi-plate clutches and brakes to connect or hold different planetary members, producing different ratios. A lock-up clutch can later connect the engine and transmission mechanically to remove converter slip.[^2][^3]

  ![Planetary gearset schematic](attachments/transmission-planetary-gearset.svg)

- **Torque converter:** the engine rotates the **pump/impeller** (A), which accelerates transmission fluid toward the **turbine** (C) attached to the transmission input shaft. The **stator** (B), mounted on a one-way clutch, redirects returning fluid so the converter can multiply torque when the turbine is much slower than the pump. As speeds become similar, multiplication falls and the unit behaves mainly as a fluid coupling; the lock-up clutch then improves efficiency.[^3][^4]

  ![Torque converter cross-section: A pump, B stator, C turbine, D input shaft, E output shaft](attachments/torque-converter-cross-section.png)

#### Why it exists on a car

- **Launch and hill climbing:** a reduction ratio gives the wheels more torque than a direct motor/engine connection could provide.
- **Useful operating range:** multiple ratios keep an internal-combustion engine near a useful speed while vehicle speed changes from zero to highway speed.
- **Efficiency and comfort:** higher gears reduce cruising speed; synchronized or automatic shifts avoid gear clash and reduce interruptions in acceleration.
- **Direction and disconnection:** reverse and neutral are provided without changing engine rotation.
- **Smooth automatic launch:** a torque converter can slip at idle, absorb torsional shock and let a vehicle stop while the engine continues running. At low turbine speed its stator also provides torque multiplication.[^2][^3]
- **EV application:** electric motors produce useful torque from zero speed across a much wider speed range, so many EVs need only a fixed single-speed reduction gearbox rather than a multi-speed transmission.

#### Types of Gearboxes and Transmissions

| Type | Common Use | Advantage | Disadvantage | Image |
| --- | --- | --- | --- | --- |
| Constant-mesh manual / synchromesh | Manual passenger cars, trucks, teaching rigs | Efficient, mechanically clear and gives direct control of the selected ratio | Needs a clutch and driver input; synchronizers, splines and shift forks require accurate fits | ![Manual transmission cutaway](attachments/transmission-manual-cutaway.jpg) |
| Planetary torque-converter automatic | Most conventional automatic cars and many trucks | Shifts under load; compact coaxial gearsets; smooth launch and easy driving | Many precision parts; needs fluid, pump, valves/solenoids and electronic control; converter slip produces heat | ![Planetary gearset](attachments/transmission-planetary-gearset.svg) |
| Dual-clutch transmission (DCT) | Performance cars and efficient automated vehicles | Preselects the next ratio on the unused shaft for very fast shifts; mostly mechanical power path[^6] | Two clutches, two input shafts and mechatronic control make it difficult to design and demonstrate; low-speed clutch heat/wear | — |
| Single-speed reduction gearbox | Battery-electric vehicles and compact teaching models | Few parts, high efficiency, easy control and no shift mechanism | One ratio must satisfy both launch torque and maximum motor speed; does not demonstrate shifting | — |
| Torque converter (transmission input device, not a gearbox) | Conventional planetary automatics | Smooth, wear-free fluid launch; absorbs vibration; multiplies torque near stall | Requires fluid, a sealed balanced housing and cooling; always slips until the lock-up clutch engages | ![Torque converter section](attachments/torque-converter-cross-section.png) |

### Part List

The most practical classroom build is a low-speed, two- or three-ratio constant-mesh gearbox plus a separate planetary module. The real torque converter should normally be represented by a commercial cutaway or a dry analogy rather than a student-made high-speed fluid unit.

| Make (3D print / laser cut) | Buy |
| --- | --- |
| Spur gears for two or three ratios; optional sun, planet, ring and carrier set | Steel input, counter and output shafts (D-shaft or keyed) |
| Sliding dog clutch/sleeve, selector fork and shift lever | Ball bearings or bushings, shaft collars, keys and retaining rings |
| Split gearbox housing with removable transparent acrylic cover | Small geared DC motor or hand crank |
| Adjustable motor, gearbox and load mounting plates | Low-voltage power supply and speed controller (if motor-driven) |
| Interchangeable gears or removable planetary holding pins | Fasteners, spacers and a small amount of plastic-safe grease |
| Ratio/speed indicator discs, direction arrows and safety guard | Optional optical tachometers/encoders and adjustable friction load |
| Dry torque-converter teaching shell and visible pump/turbine/stator shapes | Preferably a used/cutaway real torque converter for comparison |

If a **working fluid torque-converter model** is attempted, it additionally needs a transparent leak-proof case, shaft seals, balanced impellers, a one-way stator clutch, suitable fluid, fill/bleed ports and a catch tray. Those requirements make it a much higher-risk build than the dry gearbox.

### Teaching Platform

#### Manufacture and 3D-printing easiness

| Demonstrator | 3D printing / manufacturing | Main fabrication issue |
| --- | --- | --- |
| Fixed single-stage spur reduction | **Easy** | Keep gears large enough that printed teeth are not fragile; use bought shafts/bearings |
| Two-/three-ratio constant-mesh gearbox with dog selector | **Easy–moderate** | Shaft spacing, gear backlash and a selector that fully engages without binding |
| Simple planetary gearbox | **Moderate** | Concentric sun/ring/carrier geometry, even planet spacing and support on both sides |
| Working synchromesh transmission | **Hard** | Small dog teeth, splines, friction cones, detents and close axial tolerances |
| Dual-clutch or hydraulic automatic | **Very hard** | Multiple coaxial shafts/clutches plus actuators, oil circuits and control timing |
| Working torque converter | **Very hard / not recommended for printing** | Thin curved blades, rotor balance, seals, fluid compatibility and heat |

- PLA/PETG gears are suitable for slow hand operation or a guarded low-power motor, but not for real vehicle loads or high rotational speed.
- Print gears flat when possible for tooth consistency. Use metal shafts, bought bearings/bushings and through-fasteners instead of relying on printed threads.
- A transparent laser-cut cover makes power flow visible while containing loose parts. It is a viewing guard, not a structural bearing plate unless designed for that load.

#### Demonstratability

- **Best option:** a hand crank or low-speed geared motor needs no fluid or special tool. Mark one tooth on every gear and add large coloured discs to the input/output shafts.
- Select each ratio and count input versus output turns. The output should rotate more slowly and be harder to stop in a low gear; an inexpensive optical tachometer makes the ratio quantitative.
- Add a small adjustable friction brake or hanging-weight drum to the output to demonstrate the speed/torque trade-off.
- Use a removable idler gear to show reverse, and move the selector to the centre to show neutral.
- On the planetary module, hold the ring, sun or carrier with removable pins and swap input/output members. Students can see several ratios from the same gears.
- A real **torque converter is less demonstratable**: its action is hidden inside an opaque sealed shell and requires transmission fluid, seals, sufficient input speed and a load. A transparent fluid model also brings leakage, aeration and rotor-balance problems.
- For a clean torque-converter analogy, place two guarded fans face-to-face and add fixed guide vanes between them. It shows non-contact fluid power transfer, but it does **not** reproduce the exact oil-flow performance or true torque ratio of an automotive converter.
- Keep fingers away from rotating gears, shafts and fan blades. Fit a clear guard before using motor power.

#### Works with what

- **Prime mover:** hand crank or small electric motor for the teaching model; engine or traction motor in a vehicle.
- **Clutch:** required ahead of a normal manual gearbox so power can be interrupted for starting and shifting. A DCT needs two controlled clutches.
- **Torque converter system:** needs automatic-transmission fluid, an oil pump, stator one-way clutch, lock-up clutch, cooler/heat exchanger and controls. It normally feeds a planetary automatic gearbox rather than working alone.[^3][^5]
- **Couplings and shafts:** connect the motor/engine to the input and connect the output to the next module. A flexible coupling protects printed gears and bearings from small alignment errors.
- **Differential/final drive:** receives transmission output and divides it between the driven wheels; many FWD cars package the gearbox, final drive and differential together as a transaxle.
- **Brakes or load:** an adjustable output load makes torque multiplication and gear-ratio differences easier to feel and measure.
- **Controls:** a manual model needs a lever/fork and detents. A realistic automatic/DCT needs speed sensors, actuators and a controller, which greatly increases project scope.
- **Lubrication and enclosure:** even a low-speed printed gearbox benefits from compatible grease; a vehicle gearbox needs specified oil, seals, breathers and thermal management.

#### CAD easiness

- **Easy:** fixed-ratio spur gearbox. CAD requires pitch diameters, centre distance, bores, bearing seats and a simple housing.
- **Easy–moderate:** constant-mesh multi-ratio gearbox using an involute-gear generator in CAD. Add axial spacing, selector travel, shaft retention and backlash checks.
- **Moderate:** planetary set. Tooth counts must satisfy the geometry (`ring teeth = sun teeth + 2 × planet teeth` for a simple set with equal module), and the carrier must keep every planet concentric.
- **Hard:** working synchromesh. Cone angles, friction surfaces, blocker ring clearance, dog teeth, splines and detents all interact.
- **Very hard:** torque converter, DCT or full hydraulic automatic. These require complex blade/flow design or clutch-control timing and manufacturing tolerances beyond a basic visual teaching model.

#### Recommended teaching build

Build a **modular three-shaft constant-mesh gearbox** with two forward ratios, neutral and reverse, a clear cover, hand crank/low-speed motor and interchangeable gears. Add a separate single planetary gearset with removable holding pins. This combination is printable, easy to CAD, needs no working fluid, visibly demonstrates speed/torque/direction changes and connects directly to the coupling and differential modules. Show torque-converter operation with the labelled cross-section, a purchased cutaway, or the guarded two-fan analogy rather than a high-speed printed fluid converter.

#### Sources and image credits

[^1]: U.S. educational manual-transmission unit, [Manual Transmission](https://files.eric.ed.gov/fulltext/ED204627.pdf), covering power flow, constant-mesh gears, synchronizers, shafts, bearings and lubrication.
[^2]: MIT 2.972, [How an Automatic Transmission Works](https://web.mit.edu/2.972/www/reports/automatic_transmission/automatic_transmission.html), describing the torque converter and planetary gearbox power path.
[^3]: ZF, [Torque Converter](https://www.zf.com/products/en/cars/products_65854.html), including hydrodynamic circuits, lock-up clutches and torsional damping.
[^4]: SAE Technical Paper 921692, [Numerical Analysis of the Torque Converter Stator Blade](https://doi.org/10.4271/921692), identifying the pump, turbine and stator as the three hydrodynamic elements.
[^5]: ZF PowerLine maintenance guide, [8-speed automatic transmission](https://www.zf.com/products/media/automotive/cv/literature_downloads_wna/truck_solutions/PowerLine_Maintenance_Guide.pdf), describing a torque converter with lock-up clutch, downstream planetary gearset, oil system and cooler connections.
[^6]: Volkswagen service training document hosted by NHTSA, [The 02E Direct Shift Gearbox](https://static.nhtsa.gov/odi/tsbs/2012/MC-10157658-9999.pdf), describing two independent gear-train halves, two clutches and preselection of the next gear.

Image credits: [manual transmission cutaway](https://commons.wikimedia.org/wiki/File:Engine_and_Gearbox_cutaway-001.jpg) by NJR ZA, CC BY-SA 3.0; [planetary gearset schematic](https://commons.wikimedia.org/wiki/File:Planetary_gear_set_schematic.svg) by DaveRcWiki, CC0; [torque-converter cross-section](https://commons.wikimedia.org/wiki/File:Torque_converter_a_cross_section.png) by Toshinori baba, CC BY-SA 4.0.

## Couplings, Drive Shafts, CV Shafts

## Differentials, Transfer Cases, CVTs

## Brakes and Clutches

## Steering and Suspension
# Drivetrain Layouts

## Front-Wheel Drive

## Rear-Wheel Drive

## All-Wheel Drive

## 4x4 (4-Wheel) Drive
# EV Configurations

## Single-Motor, Single-Axle (FWD — SM1ST, SM2ST, etc.)

## Dual-Motor, Single-Axle

## Dual-Motor, Dual-Axle

# Advanced Systems

## Torque Vectoring

## ABS and Traction Control

## Dynamic Suspensions
