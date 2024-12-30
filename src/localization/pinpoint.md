# Setting Up Your Pinpoint Localizer

## Prerequisites
* Pinpoint module connected to an I2C port.
* Dead wheel encoder wires properly connected to the Pinpoint module.

---

## Default Values
These are the default values of the PinpointConstants. You can copy and paste this into your `static{}` block within `LConstants`:
```java
    PinpointConstants.forwardY = 1;
    PinpointConstants.strafeX = -2.5;
    PinpointConstants.distanceUnit = DistanceUnit.INCH;
    PinpointConstants.hardwareMapName = "pinpoint";
    PinpointConstants.useYawScalar = false;
    PinpointConstants.yawScalar = 1.0;
    PinpointConstants.useCustomEncoderResolution = false;
    PinpointConstants.encoderResolution = GoBildaPinpointDriver.GoBildaOdometryPods.goBILDA_4_BAR_POD;
    PinpointConstants.customEncoderResolution = 13.26291192;
    PinpointConstants.forwardEncoderDirection = GoBildaPinpointDriver.EncoderDirection.REVERSED;
    PinpointConstants.strafeEncoderDirection = GoBildaPinpointDriver.EncoderDirection.FORWARD;
```

---

## Steps
### 1. Setup

Open the file `LConstants` and configure the following:

1. **Pinpoint Port**: Replace the `deviceName` parameter with the name of the I2C port connected to the Pinpoint module.
2. **Odometry Measurements**: Follow the instructions in the `TODO` comment to enter the odometry measurements in millimeters or inches. Conversion rates are provided in the comments.

### 2. Verifying Pinpoint Connection

Run the `SensorGoBildaPinpointExample.java` file located in the `tuning` folder. This will ensure the Pinpoint is correctly connected and operational.

---

## Testing Your Localizer

After completing the tuning steps, you can test your localizer's accuracy.

1. Go to `Localization Test` and drive your robot around.

2. Open the FTC Dashboard at http://192.168.43.1:8080/dash.

3. Switch the view to "field view" from the top right corner dropdown.

4. The dashboard should display the robot's position on the field.

5. Observe the movements, moving the robot forward should make `x` increase and strafing left should make `y` increase.y.

---

## Congratulations on successfully setting up your localizer!
