# Core Components
## Gearboxes, Transmissions, Torque Converters

## Couplings, Drive Shafts, CV Shafts

## Differentials, Transfer Cases, CVTs

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
![](attachments/屏幕录制%202026-09-15%20233929.mp4)
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
