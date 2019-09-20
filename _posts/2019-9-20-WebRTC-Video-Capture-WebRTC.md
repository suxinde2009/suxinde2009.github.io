---
layout: post
title: WebRTC视频采集源码分析
author: suxinde2009
category: WebRTC
date: 2019-9-20
---

![](../assets/img/Resources/WebRTC/webrtc-video-capture-pic1.jpg)

![](../assets/img/Resources/WebRTC/webrtc-video-capture-pic2.jpg)

![](../assets/img/Resources/WebRTC/webrtc-video-capture-pic3.jpg)

![](../assets/img/Resources/WebRTC/webrtc-video-capture-pic4.jpg)

![](../assets/img/Resources/WebRTC/webrtc-video-capture-pic5.jpg)

![](../assets/img/Resources/WebRTC/webrtc-video-capture-pic6.jpg)

![](../assets/img/Resources/WebRTC/webrtc-video-capture-pic7.jpg)

![](../assets/img/Resources/WebRTC/webrtc-video-capture-pic8.jpg)

![](../assets/img/Resources/WebRTC/webrtc-video-capture-pic9.jpg)

```C++
private VideoTrack createVideoTrack(VideoCapturer capturer) {
    videoSource = factory.createVideoSource(capturer);
    capturer.startCapture(videoWidth, videoHeight, videoFps);

    localVideoTrack = factory.createVideoTrack(VIDEO_TRACK_ID, videoSource);
    localVideoTrack.setEnabled(renderVideo);
    localVideoTrack.addSink(localRender);
    return localVideoTrack;
}
```



# 参考文献
1. [webrtc源码分析之视频采集之一](https://www.jianshu.com/p/5902d4953ed9)
2. [webrtc源码分析之视频采集之二](https://www.jianshu.com/p/5624f1f0d8ee)



