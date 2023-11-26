# Unreal-Engine-For-MATLAB

# Prerequisite
1. Check the version of Unreal Engine that's compatible with your MATLAB version [here](https://uk.mathworks.com/help/uav/ug/3d-visualization-engine-requirements.html)
2. Check the version of Unreal Engine that's compatible with your MATLAB Toolbox. For example:
- [UAV Toolbox Interface for Unreal Engine Projects](https://uk.mathworks.com/matlabcentral/fileexchange/80275-uav-toolbox-interface-for-unreal-engine-projects?s_tid=srchtitle_support_results_5_unreal%20engine)
- [Vehicle Dynamics Blockset Interface for Unreal Engine 4 Projects](https://uk.mathworks.com/matlabcentral/fileexchange/65966-vehicle-dynamics-blockset-interface-for-unreal-engine-4-projects?s_tid=srchtitle_support_results_2_unreal%20engine)

# Download and Install Unreal Engine
- Download Epic Games Launcher and open it to download Unreal Engine [Unreal Engine Download Instructions](https://www.unrealengine.com/en-US/download)
- In Epic Games Launcher, you can select the Unreal Engine version to be downloaded! In this case, we use `Unreal Engine 4.27`


# Setting up MATLAB's plugins for Unreal Engine
## Setting up necessary files from a support package 
To create and connect a custom Unreal Engine scene, the plugins from the MATLAB toolbox must be installed on Unreal Engine
Watch (see [Full tutorial](https://uk.mathworks.com/videos/using-unreal-engine-with-simulink-part-2-preparing-to-create-custom-scenes-1634208382735.html) )

## Step 1: Copy the support package folder from _Mathworks Package directory_ to _Unreal Engine plugin directory_
MathWorks Support Package install directory
```
C:\ProgramData\MATLAB\SupportPackages\R2023b\toolbox\shared\sim3dprojects\spkg\plugins
```

Unreal Engine plugin directory
```
C:\Program Files\Epic Games\UE_4.27\Engine\Plugins\MathWorks
```

![image](https://github.com/komxun/Unreal-Engine-For-MATLAB/assets/133139057/b017bc4c-5759-4e5f-a779-8245174269c5)

For example, the [UAV Toolbox Interface for Unreal Engine Projects](https://uk.mathworks.com/matlabcentral/fileexchange/80275-uav-toolbox-interface-for-unreal-engine-projects?s_tid=srchtitle_support_results_5_unreal%20engine) comes with 3 plugins: 
- MathWorkSimulation
- MathworksUAVContent
- RoadRunnerMaterials
These plugins MUST be installed in Unreal Engine to use this toolbox

![image](https://github.com/komxun/Unreal-Engine-For-MATLAB/assets/133139057/3c494566-71f2-4fa2-8fe6-a7a00e0c6f90)


## Step 2: Enable Mathworks plugins in the Unreal Engine
- Open Unreal Editor, go to `Edit` > `Plugins` and verify that the `Enabled` box is checked for all the necessary plugins
- After enabling the plugins, you may have to restart the Unreal Editor

![image](https://github.com/komxun/Unreal-Engine-For-MATLAB/assets/133139057/97d40c16-651f-40d2-86fc-4567d0f1ec3b)

IMPORTANT!!! : once the `MathWorks Interface` is **enabled**, you CANNOT open that unreal project directly from the Unreal Editor!!!
- You MUST open the project either from **Simulink**'s `Simulation 3D Scene Configuration block`, or from MATLAB's script

![image](https://github.com/komxun/Unreal-Engine-For-MATLAB/assets/133139057/8cccde50-748e-4d4e-a411-ef584926a682)



