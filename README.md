## VideoEditor
A library for edit video without JNI base on **MediaCodec** farmework on Android

**Support Android 4.3+**

#### Feature:
* Compress video with specific bitrate
* Scale video with specific width/height
* Trim video with specific start/end time
* High performance

#### HowToUse

``` kotlin
val coder = VideoAudioCoder(videoPath, destPath)

coder.setWithAudio(false)
coder.withScale(720, 480)
coder.withTrim(3000, 6000)

coder.setCallback(object : VideoAudioCoder.ResultCallback {
    override fun onSucceed() {
         
    },
    override fun onFailed(errorMessage: String) {
                  
    },
    Handler(Looper.getMainLooper()))
}

coder.startAsync()

```
