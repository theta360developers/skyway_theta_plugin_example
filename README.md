# skyway_theta_plugin_example

Streams audio and video directly from the THETA V in two way using [NTT Skyway](https://webrtc.ecl.ntt.com/en/) as the signaling server.


This article was [originally published on Qiita in Japanese](https://qiita.com/masasutzu/items/0073116d7d7a36491cd8) by [masasutzu](https://qiita.com/masasutzu).

I tried out SkyWay - Android - SDK 's p2p - videochat on interesting things whether it will work on THETA V.

As a result, I was able to run p2p-videochat on THETA V, and flowed 360 degrees video to the other party.

I will explain in detail later in this article, but I told gogoroya that I was frustrated at first.

> I am able to confirm that I can play audio / video by doing SkyWay-Android-SDK with THETAPlugin. #skyway # thetaplugin #webrtcjphttps: //t.co/9hw2J47269 https://t.co/lZjWo962Pc
>      - gogoroya (@ gogoroya) August 23, 2018

![image|281x500](https://community.theta360.guide/uploads/default/original/2X/9/9e5f1d737c4557b9d9b5adb90228ece9b91349ac.jpeg) 

## Test Environment

* SkyWay-Android-SDK: [v1.04](https://github.com/skyway/skyway-android-sdk/tree/v1.0.4)
* RICOH THETA Plug-in SDK: [v1.0.0](https://github.com/ricohapi/theta-plugin-sdk/tree/v1.0.0)
* THETA V: 2.40.2
* Android Studio: 3.1.3
* OS: Windows10 version 18.03

## Steps
Get the code, build the apk, and install in THETA.

https://github.com/masasutzu/skyway-android-sdk

### You can also use the repository from gogoroya
https://github.com/goroya/skyway_theta_plugin_example

### Changes to p2p-videochat

Add RICOH THETA Plug-in SDK to SkyWay-Android-SDK.  Along with this, we will match build.gradle etc on SkyWay-Android-SDK side to RICOH THETA Plug-in SDK

Throw Intent to that effect with `onCreate ()` so that you can control the camera from SkyWay-Android-SDK

Initialize the camera with `startLocalStream()`

https://github.com/masasutzu/skyway-android-sdk/pull/1

## Acknowledgments

Thanks to gogoroya, I noticed the initialization process of the camera I was missing and I could write this article. thank you very much.

---

[Original article in Japanese](https://qiita.com/masasutzu/items/0073116d7d7a36491cd8)
