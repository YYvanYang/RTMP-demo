# RTMP DEMO


## [How can I play RTMP video in video.js?](http://docs.videojs.com/tutorial-faq.html#q-how-can-i-play-rtmp-video-in-videojs)

>Make sure that the Flash tech is available -- RTMP is not playable on browsers without Flash including mobile. Flash will only be available on video.js 6 with the videojs-flash package, in previous versions it was builtin to video.js. Then, just set the rtmp source with an appropriate type -- rtmp/mp4 or rtmp/flv. The main thing to be aware of is that video.js splits the connection url and stream name with the & character. So, you'd want to update the url to follow that format. For example: rtmp://example.com/live&foo or rtmp://example.com/fms&mp4:path/to/file.mp4.

>If the server requires query parameters for authentication, these should be added to the connection part url, for example rtmp://example.com/live?token=1234&foo.

## Step Guide

### Installation

```
npm install --save videojs-flash
```

### Adding the Flash Tech to video.js

```
<script src="//path/to/video.min.js"></script>
<script src="//path/to/videojs-flash.min.js"></script>
<script>
  var player = videojs('my-video');
</script>
```


### [Force Flash playback](https://github.com/videojs/videojs-flash#force-flash-playback)

```
videojs('some-video-id', {techOrder: ['flash']});
```