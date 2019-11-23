## 使用说明
- 在原有播放器支持的参数下添加了两个参数

参数 | 类型 | 默认值 | 参数说明
:-: | :-: | :-: | :-:
rates | Array | [2, 1.75, 1.5, 1.25, 1.0, 0.75, 0.5] |　倍速数组
curRateIndex | Number | 4 | 默认倍速的索引


- 使用示例

```javascript
var player = new TcPlayer('id_test_video', {
	"m3u8": "http://2157.liveplay.myqcloud.com/2157_358535a.m3u8", //请替换成实际可用的播放地址
	"autoplay" : true,      //iOS 下 safari 浏览器，以及大部分移动端浏览器是不开放视频自动播放这个能力的
	"poster" : "http://www.test.com/myimage.jpg",
	"width" :  '480',//视频的显示宽度，请尽量使用视频分辨率宽度
	"height" : '320'//视频的显示高度，请尽量使用视频分辨率高度
	"rates": [2, 1.5, 1.0, 0.5],
	"curRateIndex": '2'
});
```
