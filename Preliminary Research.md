# Core Components
## Gearboxes, Transmissions, Torque Converters

## Couplings, Drive Shafts, CV Shafts
### Couplings

#### What it is
##### Description
A coupling is a device that joins two rotating shafts or driveline components so torque can pass from the driving side to the driven side.
- A **rigid coupling** holds two shafts in a fixed relationship and needs accurate alignment. A **flexible coupling** contains a sliding, bending or elastic element that permits a small amount of axial, parallel or angular misalignment.
- An elastomer coupling also twists slightly under load. This cushions sudden torque changes and reduces the vibration and noise passed between components.
- A coupling is not the same as a clutch. A normal shaft coupling stays connected while running, while a clutch is designed to engage and disengage power. It is also not a replacement for a universal or CV joint when the shafts operate at a large or continuously changing angle.
In a common configuration:
- Flexible jaw coupling:
	- ![](attachments/coupling-jaw-spider.jpg)
	- One hub is fixed to the input shaft and the other is fixed to the output shaft. The jaws do not touch each other directly; the input jaws compress the dark elastomer spider visible between the hubs, which pushes the output jaws and transmits torque. The spider deforms enough to absorb shock and small alignment errors. 
##### Types of Couplings

| Coupling Type                    | Common Use                                                        | Advantage                                                                                               | Disadvantage                                                                                                                        | Image                                      |
| -------------------------------- | ----------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------ |
| Rigid sleeve / flange            | Accurately aligned shafts, test rigs, fixed gearbox connections   | Simple, compact, inexpensive and has no intentional backlash                                            | Cannot absorb misalignment or vibration; poor alignment puts bending load on shafts/bearings                                        | ![](attachments/coupling-rigid-flange.jpg) |
| Jaw / spider                     | Electric motors, pumps                                            | Simple three-piece design; damps shock and vibration; tolerates small alignment errors                  | Elastomer spider wears and can create backlash; limited angle and temperature                                                       | ![](attachments/coupling-jaw-spider.jpg)   |
| Flexible rubber disc (flex disc) | Automotive propeller shafts and some steering columns             | Absorbs torsional shock and noise; allows small axial, radial and angular displacement                  | Rubber cracks with age, heat or oil; larger angles still require a universal or CV joint                                            | ![](attachments/coupling-flex-disc.jpg)    |
| Oldham                           | Servo drives, encoders and compact mechanisms with offset shafts  | Floating centre disc makes parallel misalignment easy to see; compact and nearly backlash-free when new | Centre disc slides on every turn, so it wears; limited torque and high-speed capability                                             | ![](attachments/coupling-oldham.jpg)       |
| Beam / helical                   | Encoders, sensors and small electric motors                       | One-piece construction; no lubrication; low backlash; accepts small angular and axial error             | Low torque capacity; repeated bending can cause fatigue                                                                             | ![](attachments/coupling-beam.png)         |
| Disc / bellows                   | High-speed or high-precision motor-to-gearbox connections         | Torsionally stiff, low backlash and no lubrication; tolerates heat better than elastomers               | More expensive; thin metal elements can fatigue if misalignment exceeds their rating                                                | ![](attachments/coupling-bellows.png)      |
| Splined / slip coupling          | Vehicle drive shafts, half shafts and telescoping steering shafts | High torque capacity; sliding splines allow the shaft length to change as suspension or mounts move     | Needs lubrication and usually a seal/boot; spline clearance creates some backlash; does not accommodate a large angle by itself     | ![](attachments/coupling-slip-spline.jpg)  |
| Fluid coupling                   | Smooth starting of heavy vehicles and industrial machinery        | No direct mechanical contact between input and output; gives smooth starts and overload protection      | Always has some slip and heat loss; needs fluid and a sealed housing; a torque converter is more complex and also multiplies torque | ![](attachments/coupling-fluid.jpg)        |


##### Part List

| Make (3D print / laser cut)                              | Buy                                                        |
| -------------------------------------------------------- | ---------------------------------------------------------- |
| Two coupling hubs with jaws                              | Steel input and output shafts (D-shaft or keyed)           |
| Interchangeable centre elements (rigid, soft and medium) | Elastomer spider or rubber insert                          |
| Clear safety guard and mounting brackets                 | Ball bearings / pillow blocks                              |
| Adjustable motor and load plates                         | Shaft collars, keys, set screws and fasteners              |
| Alignment blocks or sliding offset stage                 | Optional commercial jaw or Oldham coupling for comparison |

#### Teaching Platform
Manufacture
- Easy to print and CAD: 
	- Rigid sleeve coupling
	- Jaw coupling (Spider should be bought probably)
	- Oldham coupling (surface finish matters)
- Printed bores and set-screw threads wear quickly.
- A fluid coupling needs a leak-proof housing, balanced impellers and fluid. 
- Metal disc or bellows couplings need thin fatigue-resistant parts.
Demonstratability
- No fluid or special tools are needed for a jaw or Oldham coupling. It can be turned by hand or driven slowly with a small electric motor.
- Mount one bearing block on slots so the input and output shafts can be moved out of alignment by a measured amount.
- Easy to see in action:
  - Start with a rigid coupling and offset one shaft slightly: the assembly becomes hard to turn and the shafts/bearings deflect.
  - Replace it with a jaw coupling: the elastomer deforms and the output continues to turn with less vibration.
  - Fit spiders made from different TPU hardnesses: a softer spider twists more and cushions shock, while a harder spider gives a more immediate output response.
  - Apply a sudden load to the output: mark both hubs to show the small torsional deflection across the elastomer.
  - Use an Oldham coupling with two visibly offset shafts: the centre disc slides in two perpendicular directions during each revolution.
Works with what
- **Gearboxes / transmissions / torque converters**: joins a motor or engine simulator to the gearbox input, or the gearbox output to the next shaft. A flexible coupling protects gears and bearings from small alignment errors and torque shock.
- **Drive shafts / CV shafts**: flange, flexible-disc and splined couplings attach shafts to the transmission, transfer case or differential. The joints on the shaft handle the larger operating angles.
- **Differentials**: connects the drive shaft or motor output to the differential pinion/input shaft.
- **Transfer cases**: flange or splined couplings connect the transmission input and front/rear drive-shaft outputs.
- **Brakes and clutches**: a fixed coupling cannot disconnect power. Add a clutch when the platform must start, stop or change modes without stopping the motor.
- **Steering and suspension**: flexible or splined steering-shaft couplings reduce vibration and allow small movement; suspension travel changes shaft length and angle, so driven wheels still need plunging CV joints or slip splines.
- **FWD**: the engine and transaxle are normally bolted together; splines couple the differential side gears to the two CV half shafts.
- **RWD**: a flange, flexible disc or splined slip joint connects the transmission to the propeller shaft, which then connects to the rear differential.
- **AWD / 4x4**: needs additional flange and spline connections around the transfer case, front/rear drive shafts and differentials. Some on-demand AWD systems also use an electronically controlled multi-plate coupling to connect the second axle.
- **Single-motor, single-axle EV**: a short rigid or flexible coupling can connect the motor to a reduction gearbox/differential when they are separate units.
- **Dual-motor, single-axle EV**: each motor needs its own coupling or geared connection to its wheel/half shaft.
- **Dual-motor, dual-axle EV**: each motor-to-reduction-unit connection can use the same coupling design; no centre drive-shaft coupling is needed when the axles are independent.
- **Torque vectoring**: clutch couplings can vary how much torque reaches each axle or wheel; separate wheel motors replace these mechanical couplings with electronic motor control.
- **ABS and traction control**: no direct link for a fixed shaft coupling, but an active AWD coupling can be commanded open during some ABS or stability-control events.
## Differentials, Transfer Cases, CVTs
### Differentials

#### What it is
##### Description
A differential is a set of gears with 3 drive shafts that allows you to turn the rotational speed of one shaft as the average speed of the others. 
- In cars, a differential allow wheels on either end of a drive axle (both back wheels for example) to rotate at different speeds. This helps with cornering because the outer wheel of a vehicle travels more distance than the inner wheels (difference in radius).  
- If you do not have a differential (like go-karts), you will have to rely on wheel slip when cornering. 
In a common configuration:
- Driving in a straight line:
	- ![](attachments/Pasted%20image%2020260915133646.png)
	- Input applied to the purple gear, rotating it at one speed. In a straight line the resistance from both wheels are equal. The green ("planet") gear doesn't rotate on its axis. Meaning the sun gears (red and yellow, connected to wheels) rotate at the same speed. 
- Turning (left):
	- ![](attachments/Pasted%20image%2020260915133835.png)
	- Ring gear (purple) gets input, rotating the purple gear at one speed. Left sun gear (red) has more resistance than the right sun gear (yellow). Difference in resistance causes planet gear (green) to spin, leading to slower rotation in the left sun gear than the right, meaning the right wheel would travel further. 
##### Types of Differentials

| Differential Type | Common Use                                           | Advantage                                                                    | Disadvantage                                                              | Image                                    |
| ----------------- | ---------------------------------------------------- | ---------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ---------------------------------------- |
| Ring-and-pinion   | RWD                                                  | Simple; turns drive 90° (propshaft to half shafts) and adds a gear reduction | Can send most power to the wheel with less grip, causing wheelspin        | ![](attachments/Pasted%20image%2020260915134310.png) |
| Epicyclic Design  | AWD                                                  | Compact width; can split torque unevenly between front and rear axles        | High bearing loads, needs constant lubrication, complex to design         | ![](attachments/Pasted%20image%2020260915134347.png) |
| Spur-gear         | Some FWD cars                                        | Only spur gears on parallel shafts (no bevel gears)                          | Open type, so same wheelspin problem on a low-grip wheel                  | ![](attachments/Pasted%20image%2020260915134954.png) |
| Locking           | Off-road vehicles                                    | Both wheels driven regardless of traction; unlocks to act as open            | Tire scrub, understeer and heavier steering when locked; can slide on ice | ![](attachments/Pasted%20image%2020260915135037.png) |
| Limited-slip      | Low-grip road driving; AWD crossovers (viscous type) | Limits power difference between wheels, less wheelspin on low-grip side      | No full lockup; viscous type loses power and wears to open-diff behaviour | ![](attachments/Pasted%20image%2020260915135103.png) |
##### Part List

| Make (3D print / laser cut)                 | Buy                                     |
| ------------------------------------------- | --------------------------------------- |
| Carrier / case (usually two halves)         | Ball bearings for carrier and axles     |
| Ring gear and pinion (or a spur input gear) | Steel cross pin (a bolt or dowel works) |
| 2 side gears + 2–4 spider gears             | Steel output shafts (D-shaft or keyed)  |
| Housing / chassis mount, axle couplers      | Fasteners, set screws, grease           |

#### Teaching Platform
Manufacture
- 3D printed bevel gears have some limitations, if you want it to be durable 3D printed you cannot make it too small and there are also some angle limitations for the gear.
- Will probably have to work with steel axle parts.
- Otherwise its mostly simple 3D printing. 
Demonstratability
- No need for external tools, can be powered by an electric motor or simply by hand
- Easy to see in action:
  - Lift one wheel and turn the input: the free wheel spins twice as fast.
  - Hold the carrier still and turn one wheel: the other turns the opposite way.
  - Put one wheel on a slippery surface to show the open differential's traction problem.
Works with what
- **Gearboxes / transmissions (incl. CVTs)**: the differential takes its input from the transmission output.
- **Couplings, drive shafts, CV shafts**: a drive shaft brings power in (RWD) and two half shafts take it out to the wheels; CV shafts are needed if the wheels steer or the suspension moves.
- **Transfer cases**: in a 4x4, the transfer case sends drive to a front and a rear axle, and each axle needs its own differential.
- **Brakes and clutches**: clutch-type limited-slip differentials use clutch packs to limit slip.
- **Steering and suspension**: a locked front differential causes understeer and heavier steering.
- **FWD**: the differential drives the steered front wheels; some FWD cars use a spur-gear differential.
- **RWD**: ring-and-pinion differential on the rear axle.
- **AWD**: an epicyclic centre differential splits torque between front and rear, plus a differential on each axle.
- **4x4**: locking differentials for off-road traction.
- **Single-motor, single-axle EV**: one differential on the driven axle.
- **Dual-motor, single-axle EV**: one motor per wheel, so no mechanical differential is needed.
- **Dual-motor, dual-axle EV**: one motor per axle, so no centre differential; each axle still needs its own differential.
- **Torque vectoring**: varies torque to each half shaft electronically, either through a torque vectoring differential or separate motors.
- **ABS and traction control**: traction control brakes the slipping wheel, which sends more power through an open differential to the wheel with grip.

### Transfer Cases

#### What it is
##### Description
A transfer case is an intermediate gearbox that takes power from the transmission and sends it through drive shafts to the front and rear axles of a 4WD / AWD vehicle.
- It can send power to both axles or to just one (usually the rear). On off-road vehicles the driver picks 2WD or 4WD with a lever or an electronic switch.
- Many contain low range gears for off-road use. The vehicle drives slower while the engine stays in its usable RPM range, which increases torque at the axles.
- The front and rear wheels never turn at exactly the same speed (different tire wear, slightly different front and rear differential ratios). Transfer cases meant for road use let the axles turn at different speeds, the same way a differential does across one axle. A case that locks them together binds on dry pavement (driveline windup).
In a common configuration:
- In the vehicle:
	- ![](attachments/tc-jeep-quadratrac-transfer-case.jpg)
	- Power comes in from the transmission and leaves through two output shafts, one drive shaft to the rear axle and one to the front axle.
- Inside (chain-driven, part-time):
	- ![](attachments/tc-np231-inside.jpg)
	- Input goes through a planetary gear set (sun, planets, ring gear fixed to the housing) that gives the low range. The shift fork slides a range sleeve to pick high (input connected straight through) or low (drive goes through the planetary). A chain and two sprockets carry drive from the rear output over to the front output, and a mode sleeve connects or disconnects it for 2WD or 4WD.
##### Types of Transfer Cases

| Transfer Case Type          | Common Use                                                   | Advantage                                                                                          | Disadvantage                                                                             | Image                                        |
| --------------------------- | ------------------------------------------------------------ | -------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | -------------------------------------------- |
| Part-time                   | 4x4 trucks, off-road and military vehicles                   | Driver picks 2WD/4WD and high/low range; axles locked together for off-road traction               | No centre differential, so it binds (driveline windup) on dry pavement                   | ![](Pasted%20image%2020260915142526.png)     |
| Full-time                   | AWD sports cars, performance sedans, SUVs                    | Centre differential lets the axles turn at different speeds, so 4WD works on any surface           | Open centre diff sends power to a slipping wheel unless locked; low range often left out | ![](Pasted%20image%2020260915142530.png)     |
| Part-/full-time hybrid      | e.g. Mitsubishi Super Select (Pajero)                        | Runs 2WD, full-time 4WD (open centre diff) and part-time 4WD (locked), in high and low range       | Locked modes still bind on pavement; low range can only be engaged when stopped          | ![](Pasted%20image%2020260915142600.png)     |
| Gear-driven                 | Large trucks, some passenger cars                            | Strong                                                                                             | Heavy and noisy                                                                          | ![](attachments/tc-vaz-2121.jpg)             |
| Chain-driven                | Compact and full-size trucks, Jeeps, SUVs                    | Quieter and lighter than gear-driven                                                               | Not as strong; chain can stretch under heavy torque                                      | ![](attachments/tc-morse-chain.jpg)          |
| Married                     | AWD cars (e.g. Subaru, shares the transmission housing)      | Bolted straight to the transmission, no extra drive shaft                                          | Harder to change the engine or transmission separately                                   | ![](attachments/tc-toyota-uf1ae-married.jpg) |
| Divorced / independent      | Long wheelbase commercial and military trucks, modified 4x4s | Separate from the transmission, so engine/transmission can be changed while keeping the 4WD system | Needs an extra short drive shaft from the transmission                                   |                                              |
| Manual shift on-the-fly     | Pickups (e.g. 2004 Toyota Tacoma)                            | Mechanical floor lever, no transfer case motor; 4WD high engages while moving slowly               | Must stop and shift to neutral to engage 4WD low                                         |                                              |
| Electronic shift on-the-fly | Pickups (e.g. 2026 Toyota Tacoma)                            | Dash switch or buttons instead of a lever                                                          | Needs a transfer case motor; must still stop and shift to neutral for 4WD low            | ![](Pasted%20image%2020260915142839.png)     |
##### Part List

| Make (3D print / laser cut)                           | Buy                                             |
| ----------------------------------------------------- | ----------------------------------------------- |
| Housing / case (two halves)                           | Ball bearings for all shafts                    |
| Input gear and front/rear output gears (or sprockets) | Steel shafts (input, front output, rear output) |
| Low-range gear set (planetary or a second gear pair)  | Chain and sprockets (if chain-driven)           |
| Sliding range/mode collar (dog clutch) and shift fork | Steel shift rod (a dowel works)                 |
| Shift lever and mount                                 | Fasteners, set screws, grease                   |

#### Teaching Platform
Manufacture
- A gear-driven case uses spur/helical gears on parallel shafts, which is easier to 3D print than the bevel gears in a differential.
- A planetary low range is the hardest part to print (small planet gears, tight tolerances). A second gear pair on a countershaft can give the low range instead.
- Chain and sprockets are easier to buy than print.
- Sliding collars and shift forks need enough clearance to slide without jamming, so tolerances matter.
Demonstratability
- No fluids or external power needed, can be turned by hand or by a small electric motor.
- Easy to see in action:
  - Shift from 2WD to 4WD: the front output starts turning.
  - Shift from high to low: the outputs turn noticeably slower than the input (about half as fast for a ~2:1 low range).
  - With 4WD locked, try to turn the front and rear outputs at different speeds: they can't, which shows why part-time 4WD binds on pavement.
Works with what
- **Gearboxes / transmissions (incl. CVTs)**: the transfer case takes its input from the transmission output, either bolted on (married) or through a short drive shaft (divorced).
- **Couplings, drive shafts, CV shafts**: drive shafts carry power from the two outputs to the front and rear axles.
- **Differentials**: each driven axle needs its own differential; full-time transfer cases also contain a centre differential.
- **Brakes and clutches**: shifting between ranges and modes uses sliding dog clutches; on-demand systems use a transfer clutch to send torque to the second axle.
- **Steering and suspension**: turning on dry pavement in part-time 4WD causes binding and hopping, because the front and rear axles can't turn at different speeds.
- **FWD / RWD**: not needed, a transfer case is only used when both axles are driven.
- **AWD**: full-time transfer case with a centre differential, often married to the transmission.
- **4x4**: part-time transfer case with 2WD/4WD and high/low range is the standard for 4x4 trucks.
- **Single-motor, single-axle EV**: not needed, only one axle is driven.
- **Dual-motor, single-axle EV**: not needed, both motors drive the same axle.
- **Dual-motor, dual-axle EV**: not needed, one motor per axle replaces the transfer case and centre differential, and the front/rear torque split is controlled electronically.
- **Torque vectoring**: in AWD, a torque vectoring system can shift torque between front and rear (e.g. from 90:10 to 50:50) when needed.
- **ABS and traction control**: some full-time systems with a non-locking centre differential use traction control (through ABS) to brake a slipping wheel instead of locking the centre diff.

### CVTs

#### What it is
##### Description
A continuously variable transmission (CVT) is a transmission that can change its gear ratio smoothly through any value between a lowest and a highest ratio, instead of stepping between a fixed set of gears.
- In cars, this lets the engine stay at its most efficient (or most powerful) RPM while the vehicle speeds up or slows down, which improves fuel economy and gives smooth acceleration with **no gear shifts**.
- The most common type uses two variable-diameter pulleys joined by a belt or chain. Each pulley is two cones (sheaves) facing each other. Pushing the cones together forces the belt to ride higher (larger radius); pulling them apart lets it sink lower (smaller radius). **The belt length is fixed**, so when one pulley gets bigger the other gets smaller.
- The ratio is the driven pulley radius divided by the driver pulley radius. Small driver and large driven is a "low gear" (more torque, less speed); large driver and small driven is an "overdrive" (less torque, more speed).
- **A belt CVT can't reverse or start from a stop on its own**, so car CVTs also have a launch device (torque converter or clutch) and a small planetary gear set for reverse.
In a common configuration:
- Pulley-based:
	- ![](attachments/cvt-pulley-anim.gif)
	- Input (engine) spins the left pulley at a constant speed. As the left sheaves close and the right sheaves open, the belt climbs on the left and drops on the right, so the output speeds up without any change in input speed.
- Inside a car CVT:
	- ![](attachments/cvt-toyota-super-cvti.jpg)
	- Toyota Super CVT-i, cut away. Power goes through a small torque converter, a forward/reverse planetary set, then the two pulleys and a steel belt. An oil pump supplies the hydraulic pressure that squeezes the sheaves to set the ratio and clamp the belt.
##### Types of CVTs

| CVT Type                    | Common Use                                                                | Advantage                                                                                                  | Disadvantage                                                                               | Image                                           |
| --------------------------- | ------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ | ----------------------------------------------- |
| Rubber V-belt (centrifugal) | Scooters, snowmobiles, UTVs, go-karts ("torque converter"), riding mowers | Simple and cheap; shifts itself using centrifugal weights (driver) and a spring (driven), no electronics   | Belt wears, stretches and slips; limited torque                                            | ![](attachments/cvt-scooter-belt.jpg)           |
| Steel push-belt             | Most CVT cars (e.g. Nissan, Honda, Toyota)                                | Hydraulic clamping handles car-level torque; keeps the engine at its most efficient RPM                    | ~88% efficient (less than a manual); needs an oil pump and special fluid; torque limit     | ![](attachments/cvt-toyota-super-cvti.jpg)      |
| Chain                       | Audi Multitronic, Subaru Lineartronic                                     | Handles more torque than a push-belt                                                                       | Noisier; same pulley losses; expensive to repair                                           | ![](attachments/cvt-audi-multitronic-chain.jpg) |
| Toroidal                    | Nissan Cedric / Gloria (Extroid CVT)                                      | Rollers between two doughnut-shaped discs; handles higher torque than belts                                | Needs traction fluid and very hard, precise parts; heavy and expensive                     | ![](attachments/cvt-extroid-toroidal.jpg)       |
| Cone / friction             | Old line-shaft machine drives (Evans), simple demonstration models        | Simplest to understand; slide a belt or ring along two opposite cones to change ratio                      | Power only carried by friction, so it slips and wears; low torque                          | ![](attachments/cvt-evans-cone.jpg)             |
| Planetary ball (NuVinci)    | Bicycle and e-bike hubs                                                   | Sealed and compact; ratio can be changed while stopped                                                     | Heavier and less efficient than a derailleur; needs traction fluid                         | ![](attachments/cvt-nuvinci-internals.jpg)      |
| Hydrostatic                 | Lawn tractors, zero-turn mowers, combine harvesters                       | Engine-driven pump feeds hydraulic motors; easy to control, reverses easily, one motor per wheel can steer | Often under 65% efficient; needs hydraulic fluid; heavy and costly                         |                                                 |
| Ratcheting                  | Rare, mostly experimental                                                 | One-way clutches instead of friction, so no slip; can reach zero output speed (IVT)                        | Vibration from the ratcheting motion                                                       | ![](Pasted%20image%2020260916104813.png)        |
| eCVT (power-split)          | Hybrids (e.g. Toyota Prius, Ford Escape Hybrid)                           | No belt; a planetary gear set blends engine and two motor-generators; very durable                         | Needs two motor-generators, a battery and electronic control; only makes sense in a hybrid | ![](attachments/cvt-toyota-ecvt.jpg)            |
##### Part List

| Make (3D print / laser cut)                                  | Buy                                                            |
| ------------------------------------------------------------ | -------------------------------------------------------------- |
| Driver pulley: fixed sheave + sliding sheave                 | Rubber V-belt (small V-belt or go-kart/scooter CVT belt)       |
| Driven pulley: fixed sheave + sliding sheave                 | Compression spring for the driven pulley                       |
| Roller/weight ramp plate for the driver (centrifugal version) | Rollers or weights (steel balls or scooter variator rollers)  |
| Torque cam / spring seat for the driven pulley               | Ball bearings, steel shafts (keyed or D-shaft)                 |
| Frame / housing (open or clear sides)                        | Sliding bushings for the moving sheaves                        |
| Shift lever or knob (manual version)                         | Fasteners, set screws                                          |

#### Teaching Platform
Manufacture
- Sheaves are simple cones and easy to 3D print, but the belt rides on the cone faces, so layer lines should be sanded smooth.
- The sliding sheave has to slide along the shaft while still turning with it, so it needs a key, spline or D-shaft and a bushing. Tolerances matter or it will jam.
- Belt friction makes heat; PLA softens at around 60 °C, so PETG, ABS/ASA or nylon is better for the sheaves.
- Buy the belt instead of printing it (a printed TPU belt stretches).
- A cone CVT (rubber band between two printed cones) is the easiest version, and free 3D-printable models already exist. Toroidal, chain and steel push-belt types need precision metal parts; hydrostatic needs fluids; eCVT needs motors and control electronics.
Demonstratability
- Belt and cone types need no fluids, and can be turned by hand or by a small electric motor.
- An open frame or clear sides lets students see the belt ride up and down the pulleys.
- Easy to see in action:
  - Set a low ratio and turn the input: the output turns slower than the input. Move to a high ratio: the output turns faster. Count turns to measure each ratio.
  - Change the ratio while turning the input at a steady speed: the output speed changes smoothly with no steps.
  - Centrifugal version with a motor: speed up the motor and the belt climbs the driver pulley by itself.
  - Hold the output back by hand: the driven pulley's spring/cam shifts to a lower ratio, like a car going up a hill.
- Toroidal and hydrostatic types need fluids, and eCVT needs electronics, so they are harder to demonstrate.
Works with what
- **Gearboxes / transmissions / torque converters**: a CVT replaces the stepped gearbox, but car CVTs still use a torque converter or clutch to launch and a planetary set for reverse.
- **Couplings, drive shafts, CV shafts**: the output goes to the wheels through a drive shaft (RWD) or CV half shafts (FWD transaxle).
- **Differentials**: the CVT output goes through a final drive reduction and differential, usually in the same housing.
- **Transfer cases**: in AWD (e.g. Subaru Lineartronic), the CVT output also feeds a transfer clutch that sends torque to the rear axle.
- **Brakes and clutches**: needs a launch device (centrifugal clutch on scooters and go-karts, torque converter or wet clutch in cars), and a clutch and brake in the forward/reverse planetary set.
- **Steering and suspension**: no direct link.
- **FWD**: most CVT cars are FWD, with the CVT and differential in one transaxle.
- **RWD**: rare; the toroidal Nissan Extroid was used in RWD cars.
- **AWD**: used in some AWD cars (e.g. Subaru), with a transfer clutch after the CVT.
- **4x4**: rare in road 4x4s because of the torque limit; UTVs use a rubber belt CVT followed by a gearbox with high/low range.
- **Single-motor, single-axle EV**: not needed, an electric motor works over a wide speed range, so a single-speed reduction gear is used.
- **Dual-motor, single-axle EV**: not needed, same reason.
- **Dual-motor, dual-axle EV**: not needed, same reason.
- **Torque vectoring**: no direct link, torque vectoring happens after the CVT (in the differential or couplings).
- **ABS and traction control**: traction control cuts engine torque when a wheel slips; the CVT has to keep the belt clamped hard enough that it doesn't slip when the spinning wheel suddenly grips again.

## Brakes and Clutches

## Steering and Suspension
### Steering

#### What it is
##### Description
A steering system is a set of linkages and gears with one input shaft (the steering column) and two output motions (the left and right front wheels), which converts the rotational motion of the steering wheel into a change in the steering angle of the road wheels.
- In cars, the steering system allows the driver to change the direction of travel. The driver rotates the steering wheel, and through the steering gear and the steering linkage, the front wheels turn left or right.

Youtube: [Understanding your Car's Steering & Power Steering !](https://www.youtube.com/watch?v=em1O8mz7sF0) 3:00-6:40

![](attachments/屏幕截图%202026-09-15%20222917.png)

##### Types of Steerings

| Steering Type                  | Common Use                   | Advantage                                                    | Disadvantage                                            | Image                                                |
| ------------------------------ | ---------------------------- | ------------------------------------------------------------ | ------------------------------------------------------- | ---------------------------------------------------- |
| Rack-and-pinion                | Most passenger cars          | Simple; few parts; direct feel; easy to add power assistance | Limited maximum steering angle; wears under high loads  | ![](attachments/Pasted%20image%2020260915225047.png) |
| Recirculating ball             | Trucks, off-road, older cars | Low friction; long life; high gear ratio for heavy vehicles  | Complex; many parts; bulky; internal motion not visible | ![](attachments/Pasted%20image%2020260915225231.png) |
| Hydraulic power steering (HPS) | Older passenger cars, trucks | High assist force; good road feel                            | Needs pump, fluid, hoses, seals; leaks; engine-driven   | ![](attachments/Pasted%20image%2020260915225635.png) |
| Electric power steering (EPS)  | Modern passenger cars        | No fluid; engine-independent; tunable assist                 | Needs motor, ECU, sensors; complex control              | ![](attachments/Pasted%20image%2020260915225411.png) |
##### Part List

| Make (3D print / laser cut)               | Buy                                      |
| ----------------------------------------- | ---------------------------------------- |
| Steering gear housing / case              | Pinion and rack (small gear set)         |
| Steering column mounts, dashboard bracket | Ball bearings for pinion and rack ends   |
| Tie rod ends (simple clevis type)         | Ball joints / spherical rod ends         |
| Steering knuckle (if not bought)          | Steel shafts (steering column, tie rods) |
| Wheel hubs, axle mounts                   | Fasteners, set screws, grease            |
| Chassis mounting plate                    | Steering wheel (or make a simple one)    |
##### Teaching Platform
**Manufacture**

- 3D printed gears for the rack-and-pinion are possible, but the pinion and rack mesh must be accurate. If printed too small, the teeth wear quickly and the steering feels loose. A bought pinion-and-rack set is more reliable.
    
- The steering knuckle and tie rods can be 3D printed or laser cut, but they carry bending loads. Use thicker sections or steel inserts at the pivot points.
    
- Ball joints and rod ends should be bought, not printed. They need to rotate freely in multiple axes and take both push and pull loads.
    
- Otherwise it is mostly simple 3D printing and laser cutting for the housing, brackets, and mounting plates.

**Demonstratability**

- No need for external tools. Can be powered by hand or by a small electric motor.
    
- Easy to see in action:
    
    - Turn the steering wheel: the rack moves sideways and the front wheels turn left or right.
        
    - Turn the wheel fully left and fully right: the inner wheel and outer wheel turn by different angles (Ackermann effect).
        
    - Hold one wheel fixed and turn the steering wheel: the other wheel still moves, showing the linkage motion.
        
    - Push the steering wheel to full lock: the rack stops, showing the travel limit.

### Suspension
#### What it is
##### Description
A suspension system is a set of springs, dampers, and linkages with one connection to the chassis (or frame) and one connection to each wheel, which allows the wheels to move up and down relative to the body while keeping the tires in contact with the road.

- In cars, the suspension system serves three main functions: supporting the vehicle weight, absorbing road impacts, and controlling wheel motion so the tires stay planted. 

The working principle relies on two components working together:

- **Springs** absorb the energy from road impacts by compressing and extending. They store this energy temporarily but do not dissipate it — a spring alone would bounce forever.
    
- **Dampers (shock absorbers)** convert the spring‘s oscillation energy into heat through hydraulic resistance. They control the rate at which the spring returns to its resting position, preventing endless bouncing.
![](attachments/2026-09-15233929-ezgif.com-video-to-gif-converter.gif)
##### Types of Suspension

| Suspension Type           | Common Use                             | Advantage                                                              | Disadvantage                                                       | Image                                                |
| ------------------------- | -------------------------------------- | ---------------------------------------------------------------------- | ------------------------------------------------------------------ | ---------------------------------------------------- |
| MacPherson strut          | Most passenger car front suspensions   | Simple; compact; low cost; light weight                                | Limited camber control; poor lateral stiffness under cornering     | ![](attachments/Pasted%20image%2020260915234104.png) |
| Double wishbone           | Performance cars, SUVs, FSAE race cars | Excellent camber control; high lateral rigidity; precise steering feel | Complex; more parts; higher cost; requires careful geometry design | ![](attachments/Pasted%20image%2020260915234207.png) |
| Multilink                 | Luxury car rear suspensions            | Excellent ride comfort; good handling; adjustable alignment            | Very complex; large space requirement; high cost                   | ![](attachments/Pasted%20image%2020260916000508.png) |
| Trailing arm / twist beam | Budget car rear suspensions            | Simple; low cost; compact; durable                                     | Wheels are not fully independent; limited ride quality             | ![](attachments/Pasted%20image%2020260915235852.png) |
##### Part List

|Make (3D print / laser cut)|Buy|
|---|---|
|Upper and lower control arms (A-arms)|Coilover springs and dampers|
|Steering knuckle / upright|Ball joints (spherical rod ends)|
|Chassis mounting brackets|Steel shafts (arm pivots)|
|Arm bushings / spacers|Fasteners, bolts, nuts|
|Wheel hub adapters|Wheel bearings (if using real wheels)|

#### Teaching Platform

**Manufacture**

- 3D printed control arms are possible, but they carry bending and buckling loads. Use thick cross-sections, print orientation along the load path, and consider steel inserts at the ball joint mounting points.
    
- The steering knuckle is a highly stressed part — it carries both suspension loads and steering loads. 3D printed plastic may work for a hand-operated demo but should be over-designed.
    
- Ball joints and rod ends should be bought, not printed. They need to rotate freely in multiple axes and withstand repeated cycling without loosening.
    
- Otherwise it is mostly simple 3D printing and laser cutting for the brackets, spacers, and mounting plates.
    

**Demonstratability**

- No need for external tools. Can be operated by hand or with a simple fixture.
    
- Easy to see in action:
    
    - Push one wheel up: the spring compresses, the damper resists, and the upper and lower arms pivot.
        
    - Watch the camber angle: as the wheel moves up, the top of the wheel tilts inward or outward depending on the arm lengths.
        
    - Compare left and right sides: pushing one wheel does not affect the other (independent suspension).
        
    - Compress and release: the damper prevents the spring from bouncing endlessly.
# Drivetrain Layouts
![](Pasted%20image%2020260916114058.png)
## Front-Wheel Drive

## Rear-Wheel Drive








## All-Wheel Drive

## 4x4 (4-Wheel) Drive

### What it is
#### Description
A 4x4 (four-wheel drive, 4WD) is a drivetrain layout where the engine can drive all four wheels. It is built mainly for off-road and low-grip driving.
- **4x4 vs AWD:** a 4x4 usually has a transfer case, lets the driver pick 2WD or 4WD, and has a low range. AWD is always on and is tuned for grip on the road, not for off-road use.
- Power flow: engine → transmission → transfer case → front and rear drive shafts → front and rear differentials → half shafts → wheels.
- Most 4x4s drive only the rear wheels in normal driving (2H). The front axle is added when needed (4H), and the low range (4L, typically about 2:1 to 4:1) gives much more torque at the wheels for steep, slow off-road driving.
- **Why it exists:** off-road, one or more wheels often lose grip (mud, snow, loose rock, a wheel in the air). Driving both axles, and locking the differentials, keeps the vehicle moving as long as some wheels still have grip.
In a common configuration:
- Layout (part-time 4x4):
	- ![](attachments/4x4-layout.svg)
	- The transfer case sits behind the transmission. In 2H only the rear drive shaft turns. In 4H the transfer case locks the front drive shaft to the rear one, so both axles turn at the same speed. Locking hubs on the front wheels connect or disconnect the wheels from the front axle.
##### Types of 4x4 Systems

| 4x4 System Type                      | Common Use                                                                    | Advantage                                                                                                        | Disadvantage                                                                                                 | Image                                       |
| ------------------------------------ | ----------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------- |
| Part-time 4WD                        | Most 4x4 pickups and off-roaders (e.g. Jeep Wrangler, Toyota Tacoma)          | Simple and strong; axles locked together for maximum off-road traction; runs as RWD on the road to save fuel     | No center differential, so 4WD can't be used on dry pavement (driveline windup); driver has to pick the mode | ![](Pasted%20image%2020260916113906.png)    |
| Full-time 4WD                        | e.g. Toyota Land Cruiser, Mercedes G-Class, Jeep Grand Cherokee (Quadra-Trac) | Centre differential lets 4WD run on any surface; centre diff can be locked for off-road                          | Always driving both axles, so more drivetrain losses; open centre diff needs locking or traction control     | ![](Pasted%20image%2020260916113907.png)    |
| Automatic / on-demand 4WD (4A)       | Full-size pickups (e.g. Ford F-150 "4A", Chevrolet Silverado "Auto")          | Runs RWD until the rear slips, then a clutch in the transfer case sends torque to the front; still has 4H and 4L | Clutch can overheat with heavy use; needs sensors and electronic control                                     |                                             |
| Selectable (part-/full-time)         | e.g. Mitsubishi Pajero (Super Select), Jeep Grand Cherokee (Selec-Trac)       | 2WD, full-time 4WD and locked part-time 4WD all in one vehicle                                                   | More complex and expensive transfer case                                                                     |                                             |
| Manual locking hubs                  | Older 4x4 trucks and SUVs (e.g. Toyota Land Cruiser J60)                      | In 2WD the front axle shafts and differential stop turning: less wear, better fuel economy; simple and robust    | Driver has to get out and turn each hub before using 4WD                                                     | ![](attachments/4x4-manual-hub.jpg)         |
| Automatic locking hubs               | 1980s–90s pickups and SUVs (e.g. Mitsubishi Pajero)                           | Lock by themselves when 4WD is selected, no need to leave the vehicle                                            | Often need to drive a short distance (sometimes backward) to lock or unlock; may not lock once already stuck |                                             |
| Axle lockers (locking differentials) | Serious off-roaders (e.g. Jeep Wrangler Rubicon, Mercedes G-Class)            | Both wheels on an axle turn together, so a wheel in the air doesn't stop the vehicle                             | Hard to steer with the front locked; only for slow off-road driving                                          | ![](attachments/4x4-diff-lock-switches.png) |
##### Part List

| Make (3D print / laser cut)                                   | Buy                                                                   |
| ------------------------------------------------------------- | --------------------------------------------------------------------- |
| Chassis / frame plate (laser cut)                             | Motor + gearbox (or a hand crank) for the "engine"                     |
| Transfer case housing, gears and shift collar                 | Steel shafts for the drive shafts and half shafts                     |
| Front and rear differential housings and gears                | Universal joints for the drive shafts                                 |
| Front steering knuckles / uprights                            | CV joints or small U-joints for the steered front wheels              |
| Locking hub dials (dog clutch between axle and wheel hub)     | Ball bearings, wheels and tires                                       |
| Axle housings, suspension links and mounts                    | Fasteners, set screws, grease (or RC crawler axles and transfer case) |

#### Teaching Platform
Manufacture
- A 4x4 is not a stand-alone system, so it is the transfer case and two differentials put together. 
- The front axle has to both steer and be driven, so it needs CV or universal joints at the knuckles. 
- It is a full vehicle model, so it is bigger than a single component. 
Demonstratability
- No fluids needed; one motor or a hand crank can drive the whole model.
- Easy to see in action:
  - In 2H only the rear wheels are driven; shift to 4H and the front drive shaft and front wheels start turning.
  - Shift to 4L: the wheels turn noticeably slower for the same input. Count turns to measure the low range ratio.
  - Put one wheel on a slippery surface or lift it off the ground: with open differentials the model stops; lock the differentials and it keeps going.
  - In 4H on a grippy surface, steer and push the model: the tires scrub and hop, which shows driveline windup.
  - Unlock the front hubs in 2H: the front wheels roll freely while the front axle stays still.
Works with what
- **Gearboxes / transmissions (incl. CVTs)**: a manual or automatic transmission sits before the transfer case; CVTs are rare in 4x4s because of their torque limit, except in UTVs.
- **Couplings, drive shafts, CV shafts**: needs front and rear drive shafts with universal joints, and CV or universal joints on the front half shafts because the front wheels steer.
- **Differentials**: one on each axle, often with lockers; full-time 4WD also needs a centre differential.
- **Transfer cases**: required, it is the core of the layout (part-time case with 2H/4H/4L).
- **Brakes and clutches**: dog clutches in the transfer case and locking hubs; automatic 4WD uses a clutch pack; the low range gives more engine braking going downhill.
- **Steering and suspension**: the front axle steers and is driven. Solid axles (e.g. Jeep Wrangler) are strong and let the wheels travel far; independent front suspension (most pickups) rides better. Locked 4WD makes tight turns hard on pavement.
- **FWD**: not used, 4x4s are built on a RWD layout.
- **RWD**: a part-time 4x4 in 2H is a RWD vehicle.
- **AWD**: similar hardware, but AWD is always on and usually has no low range; full-time 4WD sits between the two.
- **Single-motor, single-axle EV**: not a 4x4, only one axle is driven.
- **Dual-motor, single-axle EV**: not a 4x4, only one axle is driven.
- **Dual-motor, dual-axle EV**: electric 4x4s (e.g. Rivian R1T) use a motor on each axle instead of a transfer case, and need no low range because motors give full torque from zero speed.
- **Torque vectoring**: some electric 4x4s with a motor per wheel (e.g. Rivian quad-motor) vary torque between wheels to steer and climb.
- **ABS and traction control**: brake-based traction control (e.g. Toyota A-TRAC) brakes a spinning wheel to act like a locker; stability control is often reduced or turned off in 4L.

# EV Configurations

## Single-Motor, Single-Axle (FWD — SM1ST, SM2ST, etc.)

## Dual-Motor, Single-Axle

## Dual-Motor, Dual-Axle

# Advanced Systems

## Torque Vectoring

## ABS and Traction Control

## Dynamic Suspensions
