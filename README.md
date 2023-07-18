# myMediaCodec
此项目是基于MediaCodec编解码框架在Android Studio中完成的视频播放和录制APP，通过MediaCodec的编码和解码过程，录制和播放功能可以稳定运行。

1.视频录制时使用 Surface 作为编码器 MediaCodec 的输入，即将 MediaCodec 创建的 Surface 作为其输入，这个 Surface 由 MediaCodec 的 createInputSurface 方法创建，相机将有效数据渲染到该 Surface 中，MediaCodec 就可以直接输出编码后的数据了；

2.音频录制采用MediaCodec即可，从外部传入视频数据进行编码录制；

3.音视频合成采用MediaMuxer合成。

4.视频播放时创建两个线程，分别使用MediaCodec对视频和音频进行解码，之后将进行音视频同步之后，渲染到Surface即可进行播放；
