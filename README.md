# AV-GPS-Dataset (Autonomous Vehicle Global Positioning System Dataset)

The AV-GPS-Dataset is an extensive collection of GPS navigation data collected by the Autonomic Computing Lab GPS-guided Rover (ACL-Rover). This Autonomous Vehicle Testbed was designed and developed by myself at the University of Arizona, AZ, USA. The dataset is associated with the journal titled "GPS-IDS: An Anomaly-based GPS Spoofing Attack
Detection Framework for Autonomous Vehicles" submitted to the IEEE Transactions on Dependable and Secure Computing.

<img src="https://github.com/mehrab-abrar/AV-GPS-Dataset/blob/main/ACL-Rover%20AVT.JPG" width="220" height="300">

AV-GPS-Dataset captures 44 features of GPS-guided navigation of Autonomous Vehicles with and without imposing a GPS spoofing attack. The feature descriptions of the dataset are detailed below:

## Roll, Pitch 
Rotation around the front-to-back axis of the vehicle is called *Roll* and rotation around the side-to-side axis of the vehicle is called *Pitch*. *Roll* and *Pitch* are measured in degrees and the values range from -180° to 180°. 

## Heading
The angular direction of the compass towards which the head of the vehicle is pointed is referred to as *Heading*. *Heading* is measured in degrees and the heading angle ranges from 0° to 360°.

## Yaw, Yaw Rate 
The rotation around the vertical axis of the vehicle relative to North is referred to as *Yaw*. Yaw is measured in degree and ranges from -180° to 180°. *Yaw Rate* is the rate of change of Yaw angle with time and is measured in degrees/second.

## Velocity 
*Velocity* refers to the actual speed of the vehicle on the ground. It is measured in meters/second.

## Steering Angle 
*Steering angle* refers to the degree to which a vehicle's front wheel axle is turned during autonomous navigation. It is measured in degrees.

## Relative Altitude 
*Relative Altitude* is the altitude of the vehicle relative to the initial starting location or home location. It is measured in meters. 

## Altitude AMSL 
*Altitude AMSL* represents the altitude or elevation of the vehicle Above the Mean Sea Level (AMSL). The test location (Tucson, Arizona, USA) has an elevation of approximately 728 meters (2,389 feet).

## Altitude Tuning, Altitude Tuning Setpoint 
*Altitude Tuning* is used to convert the altitude error (the difference between the desired altitude and the actual altitude) to a required climb or descent rate. The *Altitude Tuning Setpoint* values are used as feed-forward values to the altitude controllers; they are added to the outputs of the altitude controllers and the results are fed back to the controllers as inputs. These features are more important for Unmanned Aerial Vehicles (UAVs).

## X-Track Error
This feature denotes the cross-track error or the deviation of the vehicle from its desired track at any instantaneous time. A gain value is applied to *X-Track Error* to converge it to 0.

## Travelled Distance 
*Travelled Distance* is the sum of the total distance covered by the vehicle after its initialization. It is measured in meters.

## Run Time
It is a time recorder that keeps a record of the flight time or run time of the vehicle after its initialization. It records the time in *hours: minutes: seconds* format.

## Distance To Home 
The *Distance To Home* feature records the distance to be traveled by the vehicle to reach its home location. It is measured in meters.

## Mission Index
Prior to running the vehicle in autonomous mode, mission planning is performed by mapping out a path for the vehicle to travel using the Ground Control Station. Each mission consists of two or more waypoints including the home location as the default first waypoint. Each waypoint is referred to as a "Mission". The *Mission Index* feature denotes the current mission or the current waypoint of the vehicle.

## Heading To Next WP
*Heading To Next WP* is the new heading angle to the next waypoint of the mission. It is measured in degrees and ranges from 0° to 360°.

## Heading To Home
This is the heading angle to the home location with respect to the current heading angle of the vehicle. It is measured in degrees and its range is from 0° to 360°.

## Distance To GCS 
This is the distance from the vehicle to the Ground Control Station (GCS) computer. It should be noted that the home location and the Ground Control Station location may not always be the same unless the vehicle is launched directly from the Ground Control Station. Its unit is in meters.

## Throttle 
*Throttle* expresses the percentage of throttle applied by the autopilot to the throttle motor of the vehicle. It is measured in %.

## Hobbs
The *hobbs* feature is a record of "hobbs time" that is used to measure the actual time that the vehicle is operated.

## Clock Time, Clock Date
The current clock time and date is recorded by *Clock Time* and *Clock Date*.

## GPS Latitude, GPS Longitude
These features capture the current GPS latitude and longitude of the vehicle.

## GPS MGRS
This feature indicates the GPS Military Grid Reference System (MGRS) messages. GPS MGRS is the geocoordinate standard used by the military for locating positions on earth.

## GPS HDOP, GPS VDOP
*GPS HDOP* and *GPS VDOP* refers to the horizontal and vertical Dilution of Precision of GPS signals. Dilution of Precision (DOP) is a term used to describe the strength of the current satellite configuration. It measures the positional accuracy of the data collected by a GPS receiver at the time of use. Generally, the more satellites the GPS receiver is connected with, the smaller the DOP values, hence the errors become smaller. HDOP values are typically between 1 and 2. VDOP values are larger than the HDOP values (typically 2-4); indicating that vertical position errors are larger than horizontal errors. We suffer this effect because the satellites from which we obtain the signals are above the receiver.

## GPS Course
This feature calculates the GPS heading angle or the actual direction of the vehicle relative to North in degrees calculated using GPS measures. The values range from 0° to 360°

## Satellite Locks, Satellite Count
*Satellite Lock* denotes the number of satellites the vehicle is connected with, and *Satellite Count* represents the number of available satellites.

## Longitudinal Position, Lateral Position, Vertical Position
These features are the 3-dimensional coordinates of the vehicle relative to its starting point. They are measured in meters.

## Longitudinal Velocity, Lateral Velocity, Vertical Velocity
These are the 3 dimensional coordinate velocities of the vehicle relative to the initial velocities. They are measured in meters/second.

## Absolute Longitudinal Velocity, Absolute Lateral Velocity
These features are the absolute values of the Longitudinal and Lateral velocities measured in meters/second.

## Temperature
This parameter measures the local temperature of the Pixhawk autopilot hardware in Fahrenheit.

## Longitudinal Vibration, Lateral Vibration, Vertical Vibration
These parameters denote the vibration levels on the X, Y and Z axes of the vehicle. They are measured in Hertz or the number of cycles per second.

## Data Type
*Data Type* indicates the types of the data: whether it is a normal data or a GPS spoofing attack data. The normal data are denoted by "0" and the attack data are denoted by "1".
