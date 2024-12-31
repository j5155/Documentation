# Pedro Pathing vs Road Runner

**Pedro Pathing** is a path-following library (created early 2024, last updated 12/30/24)

It uses a custom algorithm to follow trajectories with speed as a top priority.

Docs: <https://pedropathing.com/>

Quickstart: <https://github.com/Pedro-Pathing/Quickstart>

Library Repo: <https://github.com/Pedro-Pathing/PedroPathing>

Discord: <https://discord.gg/2GfC4qBP5s>

Visualizer: <https://pedro-path-generator.vercel.app/>

**Pros of Pedro:**

- Makes your bot drive faster
- Support for recent sensors (otos, pinpoint) is official/built in
- Very good correction for unexpected disturbances

**Cons of Pedro:**

- Newer, so potentially less stable
- Smaller community of users (around 500 people in their Discord)
- Uses nonstandard coordinate system in visualizer


---

**Road Runner** is a motion profiling-based follower library
that includes a command-based action system and geometry.

It was originally (0.5) created late 2020(?),
with version 1.0 created mid-2023 and last updated 10/13.

It prioritizes time consistency above all else.

Library Repo: <https://github.com/acmerobotics/road-runner/>

Quickstart: <https://github.com/acmerobotics/road-runner-quickstart/tree/master/>

Official Docs: <https://rr.brott.dev/docs/v1-0/installation/>


**Pros of Roadrunner:**

- Very stable, minimal bugs if any
- Time-consistent autonomous
- Lots of support; someone has almost certainly had your problem before and it is easy to find help in FTC Discord
- Lots of examples and other team's code to look at
- Lots of integrating projects and other libraries

**Cons of Roadrunner:**

- Prioritizes time consistency above all else, which can lead to worse correction
- Slower speed by default
- Support for recent sensors like otos and pinpoint is unofficial
  (though still exists, made by j5155)

# Summary Table

| Feature                 | Pedro Pathing                        | Road Runner                           |
|-------------------------|--------------------------------------|---------------------------------------|
| **Primary Focus**       | Speed and adaptability               | Time consistency                      |
| **Sensor Support**      | Official for Otos, Pinpoint          | Unofficial (community-made)           |
| **Community Size**      | ~500 users                           | Large and established                 |
| **Correction Handling** | Very responsive to external forces   | Decent at correction                  |
| **Stability**           | Newer, less tested                   | Mature, highly stable                 |

*Note: Both libraries excel in their specialized areas and cater to different needs. Choose the one that aligns with your priorities.*

<sub> Written by j5155, Modifed/Edited by Baron </sub>
<sub> Also available on [Cookbook](https://pedropathing.com/misc/pedrovsrr.html) </sub>
