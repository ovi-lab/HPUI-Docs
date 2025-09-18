# Usage
This can be imported as a git package in Unity. The package is built to use [Unity XRHands](https://docs.unity3d.com/Packages/com.unity.xr.hands@1.4/manual/index.html) and [Unity XR Interaction Toolkit](https://docs.unity3d.com/Packages/com.unity.xr.interaction.toolkit@3.0/manual/index.html). Hence, it is interoperable with any package that implements the Unity XRHands.
The `Sample scene with HPUI` has an example with the HPUI components setup.

## Scene setup
- Setup the Scene with an XR Origin & XR Interaction Manager (see documentation [XRI documentation for more details](https://docs.unity3d.com/Packages/com.unity.xr.interaction.toolkit@3.0/manual/general-setup.html#create-the-xr-origin-camera-rig-for-tracked-devices)).
- Place atleast one HPUIInteractor component. You may use the `HPUIInteractor` prefab that is provided with the package.
- Create intractables with the HPUI Interactables components added to them (i.e., `HPUIBaseInteractable`, `HPUIGeneratedContinuousInteractable`, & `HPUIMeshContinuousInteractable`).
- Add and configure the `JointFollower` component to all gameobjects with HPUI Interactables or HPUI Interactor. This component makes sure the game objects location is set to the respective joint(s) of a given hand. The Interactor and Interactables don't depend on these, but they play nice with each other - i.e., the HPUI Interactables and HPUI Interactors will respect the configuration (Handedness) of the JointFollower.

Note that, the HPUI interactables do not have to be under the `XROrigin` even though the data from the XRHands subsystem is relative to the `XROrigin`. `JointFollower` transforms the location so that its not necessay for the components to be under the `XROrigin`.

## Interactables
### `HPUIBaseInteractable`
### `HPUIGeneratedContinuousInteractable`
### `HPUIMeshContinuousInteractable`

## Interactors
### `HPUIInteractor`
#### Detection logic
#### Gesture logic

## `JointFollower`
