# ghosttrails

This fork of the original GhostTrails repo uses a modified visualstudio project structure and includes the following changes
+ compatibility fixes for 3ds Max 2025+ SDKs
+ usage of Visual Studio propertysheets
+ detection of 3ds Max Sdk locations by referencing the environment variables created during 3ds Max Sdk install ( eg. ADSK_3DSMAX_SDK_2025 )
+ usage of 3ds Max Sdk MAX_RELEASE_xx #define macros for conditional build parameters

Those changes should make future adaptions to new Max Sdk releases easier ( essentially adding the new build target configuration should be enough )

Original text:

This repository contains the source code for the venerable GhostTrails 3dsmax plugin that can be found on https://www.ghosttrails.net.

The GhostTrails plugin was a closed-source, paid piece of software from ~2000 up until Feb 2024, at which point it became free and Open Source.

# Building The Plugin

* You will need to have, and be at least a little familar with the [3dsmax SDK](https://help.autodesk.com/view/MAXDEV/2024/ENU/) and Microsoft Visual C++.
* In particular, you will need to install the correct version of Microsoft Visual C++ for the version of 3dsmax you're targeting (eg [3dsmax 2024 required VC++ 19](https://help.autodesk.com/view/MAXDEV/2024/ENU/?guid=sdk_requirements)).
* Open the "GhostTrails_max2013" project in MSVC++.
* Update the header and library paths to the 3dsmax SDK.
* Build the release configuration.
* If it builds, great! You'll get a .dlm file that you can copy to 3dsmax's plugin directory.
* If there are build errors it means that Autodesk have made non-backwards-compatible changes to their SDK. The "What's new" section of the SDK docs usually explains what needs to change. 

