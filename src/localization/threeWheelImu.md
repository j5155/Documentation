# Setting Up Your Three Wheel Localizer with IMU

## Prerequisites
* Three odometry wheels connected to motor encoder ports on a hub.
* A properly configured IMU.

---

## Steps
### 1. Setup

Open the file `ThreeWheelIMULocalizer.java` and configure the following:

1. **Tracking Wheel Positions**: Enter the positions of your tracking wheels relative to the robot's center. Use inches for measurements.
2. **Encoder Ports**: Replace the `deviceName` parameters with the names of the ports connected to your encoders.
3. **IMU Orientation**: Adjust the IMU's orientation to match your robot.
   - [If you need help understanding the orientation, here's a guide from FIRST on how the IMU is oriented.](https://ftc-docs.firstinspires.org/en/latest/programming_resources/imu/imu.html#orthogonal-mounting)

### 2. Encoder Direction Calibration

Ensure the following:

* Forward encoder ticks up when the robot moves forward.
* Strafe encoder ticks up when the robot moves to the left.

### 3. Localizer Tuning

#### a) Turn Localizer Tuner (without IMU)

1. Open FTC Dashboard and deselect the `useIMU` option in the `ThreeWheelIMULocalizer` dropdown.
2. Position your robot facing a recognizable landmark, such as a field tile edge.
3. Spin the robot counterclockwise for one full rotation (or a custom angle).
4. The tuner will display two numbers:

   * First number: Distance the robot thinks it has spun.
   * Second number (multiplier): Replace `TURN_TICKS_TO_RADIANS` in the localizer with this value.

5. (Optional) Run multiple tests and average the multipliers for better accuracy.

#### b) Forward and Lateral Tuning (with IMU)

1. Re-enable `useIMU` in the FTC Dashboard.

2. Forward Tuning:
   * Position a ruler alongside your robot.
   * Push the robot forward by 48 inches (default distance).
   * The tuner will display the forward multiplier: Replace `FORWARD_TICKS_TO_INCHES` in the localizer with this value.

3. Lateral Tuning:
   * Position a ruler alongside your robot.
   * Push the robot sideways (strafing) by 48 inches (default distance).
   * The tuner will display the lateral multiplier: Replace `STRAFE_TICKS_TO_INCHES` in the localizer with this value.

4. (Optional) Run multiple tests and average the multipliers for better accuracy.

---

## Testing Your Localizer

After completing the tuning steps, you can test your localizer's accuracy.

1. Go to `Localization Test` and drive your robot around.

2. Open the FTC Dashboard at http://192.168.43.1:8080/dash.

3. Switch the view to "field view" from the top right corner dropdown.

4. The dashboard should display the robot's position on the field.

5. Observe the movements, moving the robot forward should make `x` increase and strafing left should make `y` increase.

---

## Note on ESD

If your robot seems to:

1. Turn to face a different direction when starting a path
2. Actively turning to a fully incorrect angle (or miss with a large untunable/unfixable error)

Your robot's IMU may have interference caused by ESD (electrostatic discharge).

Consider grounding the robot with a [grounding strap](https://www.revrobotics.com/rev-31-1269/) and [reading this guide from FIRST to understand ESD more.](https://ftc-docs.firstinspires.org/en/latest/hardware_and_software_configuration/configuring/managing_esd/managing-esd.html)  

If after all of this you cannot fix the issue, [switch to the non-IMU ThreeWheel localizer](https://pedropathing.com/localization/threeWheel.html), as it will not be as harshly affected by ESD and have more accuracy (compared to an interfered IMU).

---

## Congratulations on successfully tuning your localizer!
