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

![](attachments/steering.png)

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

Works with what
- **Gearboxes / transmissions / torque converters**: no direct link. The steering system is driven by the driver, not by the transmission. But in FWD cars, the steering knuckle must fit around the transaxle and the CV half shafts, so the gearbox layout affects the steering geometry.
- **Couplings, drive shafts, CV shafts**: in FWD cars, the front wheels both steer and drive, so the half shafts must use CV joints to allow the wheels to turn while transmitting torque. In RWD cars, the front wheels only steer, so no CV shafts are needed at the front.
- **Differentials**: in FWD cars, the differential is usually in the same housing as the transaxle, and the CV half shafts pass through the steering knuckle. In RWD cars, the differential is at the rear and has no direct link to the steering system.
- **Transfer cases**: in AWD and 4x4 vehicles, the front axle still steers, so the front differential and CV shafts must fit around the steering linkage and control arms. The transfer case itself has no direct link to the steering.
- **Brakes and clutches**: the brake caliper and disc mount on the steering knuckle, so the knuckle must carry both steering loads and braking torque. The steering column is separate from the clutch and brake pedals, but the driver uses all three together.
- **Steering and suspension**: the steering knuckle and tie rod connect directly to the suspension upright. The suspension geometry (camber, caster, kingpin inclination, bump steer) determines how the wheel behaves as it steers and moves up and down.
- **FWD**: the steering knuckle also carries the drive shaft and CV joint, so it is more complex. The steering rack is often mounted behind the engine, and the tie rods connect to the knuckle at a point that must clear the CV boot.
- **RWD**: the steering knuckle only carries the wheel hub and brake, so it is simpler. The steering rack can be mounted in front of or behind the front axle line, depending on the suspension layout.
- **AWD**: the front axle still steers, so the front differential and CV shafts must fit around the steering linkage. The steering system is the same as FWD at the front, with the rear axle driven separately.
- **4x4**: same as AWD at the front. In off-road use, the steering system must handle larger wheel travel and higher loads, so the tie rods and ball joints are usually stronger.
- **Single-motor, single-axle EV**: if the motor drives the front axle, the layout is the same as FWD, with CV shafts through the steering knuckle. If it drives the rear axle, the front wheels only steer, so the layout is the same as RWD.
- **Dual-motor, single-axle EV**: same as single-motor, single-axle. The steering system is unchanged; the motors only affect the drivetrain.
- **Dual-motor, dual-axle EV**: each axle can drive independently, but the front wheels still steer. The steering system is still needed for the front wheels, and the front knuckles must accommodate both steering and drive.
- **Torque vectoring**: independent motors or torque vectoring differentials can change wheel speed left and right, but they do not replace the steering system. Steering still sets the wheel angle; torque vectoring only adjusts the yaw moment after the wheels are turned.
- **ABS and traction control**: these systems brake individual wheels, but they do not steer. The steering system remains the driver's main directional control. ABS and traction control work best when the steering geometry is correct and the tires maintain contact with the road.
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
##### Types of Springs

| Spring Type               | Common Use                                        | Advantage                                                                   | Disadvantage                                                                | Image                                                |
| ------------------------- | ------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | ---------------------------------------------------- |
| Coil spring               | Most passenger car suspensions                    | Simple; compact; wide range of rates; easy to replace; cheap                | Carries only vertical load; needs separate location linkage                 | ![](attachments/Pasted%20image%2020260916133705.png) |
| Leaf spring               | Trucks, older RWD cars, trailers                  | Simple; carries load and locates the axle; cheap; durable                   | Heavy; poor ride comfort; limited geometry control; friction between leaves | ![](attachments/Pasted%20image%2020260916133607.png) |
| Torsion bar               | Some trucks, older cars, performance applications | Compact; adjustable ride height via anchor bolt; no coil bind               | Needs a reaction point; limited travel; harder to package                   | ![](attachments/Pasted%20image%2020260916134210.png) |
| Air spring                | Luxury cars, buses, trucks, some SUVs             | Adjustable ride height and stiffness; excellent load levelling; smooth ride | Needs compressor, air lines, valves; leaks; complex control                 | ![](attachments/Pasted%20image%2020260916133631.png) |
##### Part List

|Make (3D print / laser cut)|Buy|
|---|---|
|Upper and lower control arms (A-arms)|Coilover springs and dampers|
|Steering knuckle / upright|Ball joints (spherical rod ends)|
|Chassis mounting brackets|Steel shafts (arm pivots)|
|Arm bushings / spacers|Fasteners, bolts, nuts|
|Wheel hub adapters|Wheel bearings (if using real wheels)|
##### Teaching Platform
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
**Works with what**
- **Gearboxes / transmissions / torque converters**: no direct link. The suspension holds the wheels and the drivetrain, but the transmission itself does not connect to the suspension. However, the weight of the gearbox affects the sprung mass and therefore the spring and damper tuning.
- **Couplings, drive shafts, CV shafts**: in FWD and AWD cars, the front suspension must accommodate the CV half shafts, which pass through the steering knuckle and move with the suspension. The suspension travel must not pull the CV joint apart or cause the shaft to bind.
- **Differentials**: in RWD cars, the rear differential is mounted on the chassis or the axle, and the suspension must control the axle position. In FWD cars, the differential is in the transaxle, and the CV shafts connect to the front hubs through the suspension.
- **Transfer cases**: in AWD and 4x4 vehicles, the transfer case sends drive to the front and rear axles. Each axle has its own suspension, and the suspension must allow enough wheel travel for off-road use without causing the drive shafts to bind or the CV joints to over-angle.
- **Brakes and clutches**: the brake caliper mounts on the steering knuckle or upright, so the suspension must carry braking torque as well as suspension loads. Brake dive and squat are controlled by the springs and dampers. The clutch is unrelated to the suspension.
- **Steering and suspension**: the steering knuckle and tie rod connect directly to the suspension upright. The suspension geometry (camber, caster, kingpin inclination, roll center) affects steering feel, returnability, and bump steer. The steering rack is usually mounted on the chassis or subframe, and the tie rods must follow the suspension motion without binding.
- **FWD**: the front suspension must accommodate both steering and drive, so the knuckle is complex and the CV shafts must pass through it. The rear suspension is often simpler (twist beam or multilink) because it only carries the load.
- **RWD**: the front suspension only steers, so the knuckle is simpler. The rear suspension carries the drive axle, so it must control axle position under acceleration and braking. Double wishbone or multilink rear suspensions are common in performance cars.
- **AWD**: both front and rear suspensions carry drive loads, so both knuckles (or uprights) need provisions for CV joints. The suspension must allow enough travel for all four wheels to stay in contact with the road.
- **4x4**: the suspension must handle large wheel travel and high loads. Solid axles are common at the rear (and sometimes the front) because they are strong and simple, but they give a harsher ride and less precise geometry than independent suspension.
- **Single-motor, single-axle EV**: the suspension layout matches the equivalent FWD or RWD setup. The battery weight is low and central, so the springs are often stiffer to handle the extra mass and keep ride height consistent.
- **Dual-motor, single-axle EV**: same as single-motor, single-axle. The suspension is unchanged; the motors only affect the drivetrain.
- **Dual-motor, dual-axle EV**: each axle has its own motor, but the suspension geometry remains similar. The extra weight of the motors may require stiffer springs and dampers.
- **Torque vectoring**: independent motors can change wheel speed left and right, but the suspension still controls wheel position and camber. Torque vectoring works best when the suspension keeps the tires flat on the road.
- **ABS and traction control**: these systems rely on consistent tire contact, which depends on proper suspension function. Worn dampers or bushings degrade ABS and traction control performance because the wheel can lose contact with the road under braking or acceleration.
# Drivetrain Layouts
![](Pasted%20image%2020260916114058.png)
## Front-Wheel Drive

## Rear-Wheel Drive
### What it is
##### Description
Rear-wheel drive (RWD) is a drivetrain layout in which the engine drives the rear wheels only, while the front wheels are free to steer. The most common form is front-engine, rear-wheel drive (FR).

**How it works (roughly):**
Engine → clutch/torque converter → gearbox → propshaft → rear differential → half shafts → rear wheels
- The engine produces torque.
- The clutch or torque converter connects the engine to the gearbox.
- The gearbox changes speed and torque ratio.
- The propshaft carries torque from the gearbox to the rear differential, using universal joints to handle suspension movement.
- The rear differential turns the drive 90° and allows the left and right rear wheels to rotate at different speeds when cornering.
- The half shafts carry torque from the differential to the rear wheels.
![](attachments/Rear%20Wheel%20Drive.png)
**Why a car needs it:**
RWD separates steering from driving: the front wheels only steer, the rear wheels only drive. This lets each pair be optimised for its job — front for cornering feel, rear for acceleration traction. Under acceleration, weight transfers to the rear, which helps RWD put power down. It also avoids **torque steer**, a problem in high-power FWD cars.
The trade-off is extra weight, cost, a centre tunnel that takes cabin space, and worse traction in snow or mud compared to FWD or AWD.
##### Types of RWD Layouts

| RWD Layout            | Common Use                                      | Advantage                                                | Disadvantage                                            | Image                                                |
| --------------------- | ----------------------------------------------- | -------------------------------------------------------- | ------------------------------------------------------- | ---------------------------------------------------- |
| Front-engine RWD (FR) | Most classic sports cars, sedans, pickup trucks | Good weight distribution; simple layout; easy to service | Long propshaft; heavy; centre tunnel takes cabin space  | ![](attachments/Rear%20Wheel%20Drive(FR).png)        |
| Mid-engine RWD (MR)   | Supercars, some sports cars                     | Excellent weight distribution; sharp handling            | Very little cargo or rear seat space; complex packaging | ![](attachments/Pasted%20image%2020260916200603.png) |
| Rear-engine RWD (RR)  | Porsche 911, some city cars, buses              | Compact drivetrain; good traction under acceleration     | Rear-biased weight; tricky handling at the limit        | ![](attachments/Pasted%20image%2020260916200636.png) |
| Solid axle RWD        | Trucks, muscle cars, some SUVs                  | Strong; simple; cheap; good for heavy loads              | Heavy; poor ride comfort; limited geometry control      |                                                      |
| Independent rear RWD  | Modern sports cars, luxury sedans               | Better ride and handling; precise camber control         | More complex; more parts; higher cost                   |                                                      |
##### Part List

| Make (3D print / laser cut)        | Buy                                               |
| ---------------------------------- | ------------------------------------------------- |
| Chassis / frame                    | Electric motor or small engine                    |
| Motor mounts, gearbox mounts       | Gearbox / transmission (or simple gear reduction) |
| Propshaft bearing supports, mounts | Drive shaft (or steel rod / tube)                 |
| Differential housing / case        | Differential gear set (bevel gears)               |
| Half shaft couplers, wheel hubs    | Bearings, ball joints, fasteners                  |
| Suspension arms, brackets          | Wheels and tires                                  |
#### Teaching Platform
**3D printing / manufacturing easiness:**
- **Easy:** chassis, mounts, brackets, spacers, differential housing — all simple 3D prints or laser-cut parts.
- **Medium:** propshaft and half shafts carry torque. A 3D printed shaft with a steel core works for low-speed demo; a plain plastic shaft may twist or strip.
- **Hard:** differential gear set. Printed bevel gears wear quickly and are difficult to print with good tooth accuracy. Buy a small bevel gear set instead.
**Overall:** easy to manufacture, as long as gears and bearings are bought and only the structure is printed.
**Demonstratability:**
- **External tools / consumables:** none for a hand-operated demo. With an electric motor, only a power supply is needed — no fluids, compressed air, or special gases.
- **Intuitive to demonstrate:** yes. The power flow is visible:
    - Run the motor: propshaft spins, differential turns the half shafts, rear wheels rotate.
    - Hold one rear wheel: the other spins twice as fast (open differential).
    - Hold the propshaft and turn one wheel: the other turns in the opposite direction.
    - Put one wheel on a low-friction surface: the free wheel spins and the car does not move.
    - Compare with a locked differential: both wheels turn together, but the car cannot corner smoothly.
**Works with what (what else must be included):**
- **Gearboxes / transmissions / torque converters**: the gearbox changes speed and torque ratio; its output goes to the propshaft. A clutch or torque converter connects the engine.
- **Couplings, drive shafts, CV shafts**: the propshaft carries torque from the gearbox to the rear differential. The half shafts carry torque from the differential to the rear wheels; independent rear suspension needs CV joints.
- **Differentials**: the rear differential is the core of the RWD layout. It turns the drive 90° and allows the rear wheels to rotate at different speeds.
- **Transfer cases**: not used in pure RWD. Only needed in AWD or 4x4.
- **Brakes and clutches**: the clutch connects the engine to the gearbox in a manual RWD car. The brakes mount on the rear knuckles or axle ends.
- **Steering and suspension**: the front wheels only steer, so the front knuckle is simpler than in FWD. The rear suspension must control the rear axle position under acceleration and braking.
- **FWD**: not applicable. RWD and FWD are different layouts.
- **RWD**: the layout described here.
- **AWD**: can be based on a RWD layout, with a transfer case or centre coupling that also sends torque to the front axle.
- **4x4**: usually based on a RWD layout with a transfer case that can engage the front axle.
- **Single-motor, single-axle EV**: if the motor drives the rear axle, the layout is similar to RWD but without engine, clutch, gearbox, or propshaft.
- **Dual-motor, single-axle EV**: two motors drive the same axle, one per wheel, so no mechanical differential is needed.
- **Dual-motor, dual-axle EV**: one motor per axle. No centre differential is needed, but each axle still needs its own differential or independent motors.
- **Torque vectoring**: in RWD, done with a torque vectoring differential or independent rear motors.
- **ABS and traction control**: these systems brake individual wheels to control slip. In RWD, traction control is important because the rear wheels can lose grip under acceleration.
## All-Wheel Drive

#### What it is
##### Description
All-wheel drive (AWD) is a drivetrain layout in which all four wheels can receive engine torque. Unlike 4x4, AWD is usually designed for on-road use and can vary the torque split between the front and rear axles automatically.

**How it works (roughly):**
Engine → clutch/torque converter → gearbox → centre coupling or centre differential → front and rear differentials → half shafts → all four wheels

In many modern AWD cars, the centre coupling is normally disengaged or sends most torque to one axle, and only sends torque to the other axle when slip is detected. This saves fuel compared to permanent AWD.
![](attachments/Pasted%20image%2020260916201248.png)
**Why a car needs it:**
AWD improves traction by driving all four wheels instead of two. On low-grip surfaces (rain, snow, gravel), more driven wheels means more grip for acceleration and less wheelspin. This helps everyday driving in bad weather and lets high-power cars put power down without spinning.

The trade-off is extra weight, cost, complexity, and slightly higher fuel consumption compared to FWD or RWD.
##### Types of AWD Layouts

| AWD Layout           | Common Use                             | Advantage                                                           | Disadvantage                                                       | Image                                                |
| -------------------- | -------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------ | ---------------------------------------------------- |
| Part-time AWD        | Some SUVs and crossovers               | Simple; saves fuel when not needed                                  | Only engages when slip is detected; reactive rather than proactive | ![](attachments/Pasted%20image%2020260916201350.png) |
| Full-time AWD        | Subaru, Audi Quattro, some luxury cars | Always drives all four wheels; consistent traction                  | More complex; higher fuel consumption                              | ![](attachments/Pasted%20image%2020260916201341.png) |
| Torque-vectoring AWD | High-performance cars                  | Can send more torque to the outside wheel to help turn              | Very complex; expensive                                            |                                                      |
| Hybrid AWD           | Some hybrid and electric cars          | No mechanical centre coupling; rear axle driven by a separate motor | Only works when the motor has power; limited continuous output     |                                                      |
 Note: For a teaching platform, **part-time AWD with a simple centre coupling** is the easiest to build and demonstrate.
##### Part List

|Make (3D print / laser cut)|Buy|
|---|---|
|Chassis / frame|Electric motor or small engine|
|Motor mounts, gearbox mounts|Gearbox / transmission (or simple gear reduction)|
|Centre coupling housing, mounts|Centre coupling or centre differential|
|Front and rear differential housings|Differential gear sets (bevel gears)|
|Propshaft supports, half shaft couplers|Drive shafts, bearings, fasteners|
|Suspension arms, brackets|Wheels and tires|
#### Teaching Platform

**3D printing / manufacturing easiness:**
- **Easy:** chassis, mounts, brackets, differential housings — all simple 3D prints or laser-cut parts.
- **Medium:** propshafts and half shafts carry torque. A 3D printed shaft with a steel core works for low-speed demo.
- **Hard:** differential gear sets and the centre coupling. Printed gears wear quickly; buy these instead.

**Overall:** more parts than RWD or FWD, but each part is still simple. The main challenge is fitting two differentials and a centre coupling into the chassis.

**Demonstratability:**
- **External tools / consumables:** none for a hand-operated demo. With an electric motor, only a power supply is needed.
- **Intuitive to demonstrate:** yes, but more complex than RWD:
    - Run the motor: all four wheels rotate.
    - Hold one wheel: the others keep turning, and the centre coupling sends more torque to the axle with grip.
    - Compare with RWD: with only two driven wheels, one wheel losing grip can stop the car. With AWD, the other axle still drives.
    - Show the centre coupling: with it locked, front and rear axles turn together; with it open, they can turn at different speeds.
**Works with what (what else must be included):**
- **Gearboxes / transmissions / torque converters**: the gearbox output goes to the centre coupling or centre differential, not directly to one axle.
- **Couplings, drive shafts, CV shafts**: AWD needs a propshaft to the rear axle and half shafts to all four wheels. If the front wheels steer, the front half shafts need CV joints.
- **Differentials**: AWD needs at least two differentials — one on each axle — plus a centre coupling or centre differential to split torque between them.
- **Transfer cases**: in a 4x4, the transfer case does the same job as the centre coupling but is usually selectable and has a low-range gear. AWD is essentially a permanent or automatic version of this.
- **Brakes and clutches**: the clutch connects the engine to the gearbox. The brakes mount on all four knuckles or axle ends.
- **Steering and suspension**: the front wheels steer and drive, so the front knuckles need CV joints and must fit around the steering linkage.
- **FWD**: not applicable. AWD drives all four wheels.
- **RWD**: an AWD car can be based on a RWD layout with an added front drive system.
- **AWD**: the layout described here.
- **4x4**: similar layout, but the transfer case is selectable and often has a low range. 4x4 is designed for off-road use; AWD is designed for on-road use.
- **Single-motor, single-axle EV**: not applicable. An AWD EV needs at least two motors, or one motor with a mechanical centre coupling.
- **Dual-motor, single-axle EV**: not applicable. Both motors drive the same axle.
- **Dual-motor, dual-axle EV**: one motor per axle. This is the electric equivalent of AWD, with no mechanical centre coupling needed.
- **Torque vectoring**: in AWD, torque vectoring can send more torque to the outside wheel to help the car turn. It can be done with a special centre coupling or with independent motors.
- **ABS and traction control**: these systems brake individual wheels to control slip. In AWD, traction control works with the centre coupling to send torque to the axle with grip.

**How easy is it to design / CAD:**
- **Modeling difficulty:** medium to high. The layout needs careful alignment: propshaft in line with gearbox output and rear differential pinion; front differential aligned with the front half shafts; centre coupling positioned between the gearbox and both axles.
- **Assembly complexity:** high. More parts than RWD or FWD, and the centre coupling adds a step. The front axle must accommodate both steering and drive.
- **Availability of standard parts:** good. Small motors, gearboxes, differential gear sets, centre couplings, bearings, shafts, and wheels are available from hobby suppliers.
- **CAD tips:** model the chassis first, place the motor and gearbox as reference components, then position the centre coupling and both differentials. Use the propshafts as alignment axes, and keep the front and rear axles parallel.

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

### What it is

#### Description
Single-motor, single-axle is an EV configuration where one electric motor drives one axle. The motor can be mounted on the front axle (FWD) or rear axle (RWD). "SM1ST" typically refers to a single-motor, single-speed transmission layout, while "SM2ST" refers to a single-motor, two-speed transmission layout.

**How it works (roughly):**
Battery → inverter → electric motor → reduction gearbox → differential → half shafts → wheels
- The battery stores energy as DC current. The inverter converts DC to AC and controls motor speed. The electric motor produces torque across a wide speed range (from zero to around 18,000 rpm). A single-speed reduction gearbox (or two-speed in SM2ST) reduces motor speed and multiplies torque. The differential allows left and right wheels to rotate at different speeds when cornering. Half shafts carry torque to the driven wheels.
![](attachments/Pasted%20image%2020260916204323.png)
**Why a car needs it / why it exists:**
This is the simplest and most common EV drivetrain layout. Electric motors have a wide efficient operating range, so a single-speed gearbox is usually enough. A two-speed (SM2ST) improves efficiency but adds complexity and cost.

Compared to dual-motor configurations, single-motor is lighter, cheaper, and simpler. It is used in many mainstream EVs: Tesla Model 3 RWD, Hyundai Ioniq 5 RWD, and Smart #1 all use a single rear motor with a single-speed transmission.
#### Types of Single-Motor Layouts

| Layout               | Common Use                           | Advantage                                           | Disadvantage                                               |
| -------------------- | ------------------------------------ | --------------------------------------------------- | ---------------------------------------------------------- |
| Single-motor FWD     | Entry-level EVs, conversions         | Simple; compact; low cost                           | Traction limits under hard acceleration; torque steer risk |
| Single-motor RWD     | Tesla Model 3, Ioniq 5 RWD, Smart #1 | Better traction under acceleration; no torque steer | Slightly more complex packaging than FWD                   |
| Single-speed (SM1ST) | Most production EVs                  | Simplest; lightest; cheapest; reliable              | Motor operates outside optimal efficiency at some speeds   |
| Two-speed (SM2ST)    | Some performance EVs                 | Better efficiency and acceleration balance          | More complex; added cost and weight                        |
Note: For a teaching platform, **single-motor RWD with single-speed** is the clearest and simplest to demonstrate.
#### Part List

|Make (3D print / laser cut)|Buy|
|---|---|
|Motor mounts, brackets|Electric motor (BLDC or PMSM)|
|Reduction gear housing|Reduction gear set (or buy a complete gearbox)|
|Differential housing / case|Differential gear set (bevel gears)|
|Chassis mounting plate|Bearings, fasteners|
|Wheel hubs, half shaft couplers|Wheels and tires|
#### Teaching Platform
**3D printing / manufacturing easiness:**
- **Easy:** motor mounts, brackets, housings — all simple 3D prints or laser-cut parts.
- **Medium:** the reduction gearbox. A simple spur gear pair can be 3D printed for low-speed demo, but printed gears wear quickly under load.
- **Hard:** the electric motor and differential gear set. Buy these; printed versions are unreliable.
**Overall:** easy to manufacture, as long as the motor and gears are bought and only the structure is printed.
**Demonstratability:**
- **External tools / consumables:** none required. If using an electric motor, only a power supply (battery or bench supply) is needed.
- **Intuitive to demonstrate:** yes. The power flow is simple and visible:
    - Apply power: the motor spins, the reduction gear turns, the differential drives the half shafts, and the wheels rotate.
    - Hold one wheel: the other spins twice as fast (open differential behaviour).
    - Reverse polarity: the motor spins the other way, and the car moves backward.
    - Compare single-speed vs two-speed: if you build an SM2ST, show how shifting changes wheel speed for the same motor rpm.
**Works with what (what else must be included):**
- **Gearboxes / transmissions / torque converters**: not needed in the traditional sense. A single-speed reduction gear replaces the multi-speed gearbox. A two-speed version (SM2ST) adds one shift mechanism.
- **Couplings, drive shafts, CV shafts**: the motor output goes through the reduction gear to the differential, then half shafts to the wheels. If the driven wheels steer (FWD), CV joints are needed.
- **Differentials**: required. The differential allows left and right wheels to rotate at different speeds when cornering.
- **Transfer cases**: not used in single-axle configuration. Only needed for AWD.
- **Brakes and clutches**: no clutch needed (electric motor can start from zero rpm). Regenerative braking can replace some mechanical braking.
- **Steering and suspension**: if the driven axle is also the steering axle (FWD), the knuckle must accommodate both steering and drive, and the half shafts need CV joints.
- **FWD**: the motor drives the front wheels, which also steer. The knuckle is complex (steering + drive).
- **RWD**: the motor drives the rear wheels, which only drive. The front wheels only steer, so the front knuckle is simpler.
- **AWD**: not applicable. AWD requires either dual motors (one per axle) or a mechanical centre coupling.
- **4x4**: not applicable. 4x4 requires a transfer case and two driven axles.
- **Single-motor, single-axle EV**: the layout described here.
- **Dual-motor, single-axle EV**: two motors drive the same axle, one per wheel. No mechanical differential needed.
- **Dual-motor, dual-axle EV**: one motor per axle. No centre coupling needed, but each axle has its own motor.
- **Torque vectoring**: not possible with a single motor and open differential. Requires independent motors or a special differential.
- **ABS and traction control**: these systems brake individual wheels to control slip. In a single-motor EV, traction control reduces motor torque when a wheel slips.
**How easy is it to design / CAD:**
- **Modeling difficulty:** low. The layout is simple: motor → reduction gear → differential → half shafts. Align the motor shaft with the reduction gear input, and the differential output with the half shafts.
- **Assembly complexity:** low. Fewer parts than any other EV configuration. The main alignment is between the motor, gearbox, and differential.
- **Availability of standard parts:** good. Small electric motors, gear sets, differentials, bearings, and wheels are available from hobby suppliers.
- **CAD tips:** model the chassis first, place the motor as a reference, then position the reduction gear and differential. Keep the half shafts equal length if the differential is centred. Leave adjustment slots for motor mounting to tension any belt or chain drive.

## Dual-Motor, Single-Axle

## Dual-Motor, Dual-Axle

# Advanced Systems

## Torque Vectoring

## ABS and Traction Control

### Anti-Lock Braking System (ABS)

#### What it is

##### Description

ABS is an electronic safety system that prevents the wheels from locking up during hard braking. It allows the driver to keep steering while braking, which a locked wheel cannot do.
**How it works (roughly):**
ABS monitors wheel speed and rapidly modulates brake pressure:
**Wheel speed sensors → ECU → hydraulic valves and pump → brake calipers**
- **Wheel speed sensors** monitor each wheel’s rotation speed.
- **ECU (Electronic Control Unit)** detects when a wheel is decelerating too fast, meaning it is about to lock.
- **Hydraulic valves** reduce brake pressure to that wheel, then re-apply it.
- **Pump** restores pressure after the valves release it.
- This cycle repeats dozens of times per second, faster than a human can pump the brakes.
In normal braking, ABS does nothing. The valves stay open and brake fluid flows normally. ABS only activates when a wheel starts to lock.

Youtube: [DON'T SUBSCRIBE | Understanding Anti-lock Braking System (ABS) !](https://www.youtube.com/watch?v=98DXe3uKwfc) 4:00-4:45
![](attachments/Pasted%20image%2020260916205523.png)
**Why a car needs it:**
A locked wheel slides instead of rolling, and a sliding tire cannot steer. ABS lets the driver brake hard and still steer around an obstacle. On most surfaces, it also shortens stopping distance. On loose surfaces like gravel or deep snow, stopping distance may increase slightly, but steering control is maintained.
##### Types of ABS

| ABS Type                    | Common Use                        | Advantage                                                                 | Disadvantage                                             | Image |
| --------------------------- | --------------------------------- | ------------------------------------------------------------------------- | -------------------------------------------------------- | ----- |
| Four-channel, four-sensor   | Most modern passenger cars        | Each wheel controlled independently; best control                         | Can cause yaw on split-friction surfaces                 |       |
| Three-channel, three-sensor | Many passenger cars               | Front wheels independent; rear wheels controlled together; good stability | Rear wheels share one channel; less precise rear control |       |
| One-channel, one-sensor     | Older trucks, some light vehicles | Simple; low cost                                                          | Only controls rear wheels; front wheels can still lock   |       |
Note: For a teaching platform, ABS is usually **too complex to build and not necessary**. It requires wheel speed sensors, an ECU, and hydraulic valves. A simple mechanical brake system demonstrates the core braking concept without ABS.

##### Part List

| Make (3D print / laser cut)         | Buy                                                |
| ----------------------------------- | -------------------------------------------------- |
| Sensor mounting brackets            | Wheel speed sensors                                |
| ECU mounting plate                  | ABS ECU (or use a simple Arduino-based controller) |
| Valve block housing (if simulating) | Solenoid valves                                    |
| —                                   | Hydraulic pump, brake lines, brake fluid           |
#### Teaching Platform
**3D printing / manufacturing easiness:**
- **Easy:** brackets, mounting plates, and a demonstration stand are all simple prints.
- **Hard:** the hydraulic and electronic components. A real ABS needs brake fluid, sealed valves, and a controller. This is beyond what most teaching platforms need.
**Overall:** not recommended as a buildable component. If included, treat it as a **demonstration-only** system using a motor and controller to show the concept of rapid pressure modulation.

**Demonstratability:**
- **External tools / consumables:** a real ABS needs brake fluid and a power supply. A simulated version needs only a power supply.
- **Intuitive to demonstrate:** the concept is intuitive if simplified:
    - Spin a wheel by hand: it rotates freely.
    - Apply a “locked” brake: the wheel stops and cannot be steered.
    - Apply “ABS” pulsing: the wheel slows but keeps rotating, and steering is possible.
- **One caution:** real ABS is hard to demonstrate at low speed because the wheel needs to be rotating fast enough for lock-up to occur. A motor-driven wheel is better than hand-spinning.

**Works with what (what else must be included):**
- **Brakes and clutches**: ABS works with the hydraulic brake system. It needs brake calipers, brake lines, and a master cylinder.
- **Wheel speed sensors**: required at each controlled wheel. These are the primary input for ABS.
- **ECU**: processes sensor data and controls the valves.
- **Hydraulic valves and pump**: modulate brake pressure.
- **Steering and suspension**: ABS allows steering during braking, which is its main benefit. The suspension must keep the tires in contact with the road for ABS to work.
- **FWD / RWD / AWD / 4x4**: ABS works on all layouts. It controls individual wheel brakes regardless of which wheels are driven.
- **EV configurations**: ABS works the same on EVs. Regenerative braking must be blended with ABS to avoid conflicts.
- **Torque vectoring**: ABS and torque vectoring both brake individual wheels, but for different purposes. ABS prevents lock-up; torque vectoring improves turning.
- **Traction control**: shares the same sensors and hydraulic unit as ABS. Traction control prevents wheel spin during acceleration; ABS prevents lock-up during braking [](http://drive.xcar.com.cn/term/201003/news_239_1.html).

**How easy is it to design / CAD:**
- **Modeling difficulty:** low for the physical brackets and stand. High for the hydraulic and electronic system.
- **Assembly complexity:** high if building a real hydraulic ABS. Low if building a simulated demonstration.
- **Availability of standard parts:** wheel speed sensors, Arduino boards, and small solenoid valves are available, but building a working hydraulic system is still complex.
- **CAD tips:** if simulating, model a single wheel on a stand with a motor, a speed sensor, and a solenoid valve controlled by an Arduino. Show the pulsing brake pressure on an LED or small display.
## Dynamic Suspensions
