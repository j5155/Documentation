# Prerequisites for Automatic Tuners and PID Tuning

## Localizer

You will need a tuned localizer to use Pedro Pathing effectively.

**Important**: Before tuning Pedro Pathing, ensure your localizer is properly tuned. Check out the localization tuning guide under the localization tab.

---

## Follower Constants Value
Before running the automatic tuners or the PID tests, you must update your `FollowerConstants`, using the method explained in the general prerequisites.
Make you have these variables all defined if they are different than the defaults:
- The Localizer you will be using (will already be setup from Localizer setup)
- Motor Configuration Names
- Motor Directions
- Mass of your robot (in kg)

---

### **Only** after you have all of those values defined (if not the same as the default), can you move on.
