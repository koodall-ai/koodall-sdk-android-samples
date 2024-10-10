Example for 
[Koodall SDK on Android](https://docs.koodall.ai/face-ar-sdk-v1/android/android_overview) 
and [Agora.io](https://www.agora.io/en/) SDK integration to enhance video calls 
with real-time face filters and virtual backgrounds.  
  
# Getting Started

1. Get the Koodall SDK client token. Please contact us via [sales@koodall.ai](mailto:sales@koodall.ai).
2. Copy and Paste your Koodall client token into appropriate section of 
`common/src/main/java/com/koodall/sdk/example/common/Application.kt`.
3. Visit [agora.io](https://www.agora.io/) to sign up and get token, app and 
channel ID.
4. Copy and Paste your agora token, app and chanel ID into appropriate section 
of `src/main/java/com/koodall/sdk/example/videocall/MainActivity.kt`.
5. Open the project in Android Studio and run.

# How an example works

This project is based on the `PlayerAPI`. `CameraDevice` creates and manages the 
Koodall camera. Agora also has its own camera module, but in this example the 
Agora camera is not used, so in order to disable Agora camera is called 
`setExternalVideoSource(...)`.  The frames from the Koodall camera are processed 
within Koodall Player and the result transferred to the handler `FrameOutput`. In 
the handler, frames are passed to the Agora module via `pushCustomFrame(...)`.