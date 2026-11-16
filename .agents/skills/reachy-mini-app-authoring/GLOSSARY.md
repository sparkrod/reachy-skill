# Reachy Mini App Authoring

This context defines the product terms used by the app-authoring skill so agents can distinguish user apps from robot SDK and daemon work.

## App types and operation

**Reachy Mini app**:
A user-facing application that uses the Reachy Mini SDK or host integration to provide an experience with the robot.
_Avoid_: SDK contribution, daemon feature

**JS/Web app**:
A browser-based Reachy Mini app that uses the Reachy host integration and can be shared as a web application.
_Avoid_: web daemon, browser SDK contribution

**Python app**:
A Reachy Mini application built with the Python SDK, commonly for scripting, control loops, or code running on the robot.
_Avoid_: Python SDK, daemon

**Simulation**:
A test mode that connects an app to a simulated robot daemon rather than physical hardware.
_Avoid_: virtual robot, physical test

**Physical operation**:
Running app behavior that actuates or otherwise interacts with an actual Reachy Mini robot.
_Avoid_: simulation
