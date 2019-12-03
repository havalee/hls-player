[示例](https://www.weekweekup.cn/course/contribute/detail?i=26)

# 文件/文件夹说明
文件 | 说明
:-: | :-: 
TcPlayer-2.3.2_hava.js | 基于TcPlayer-2.3.2改造后带有hls加密\倍速\防盗录的tcplayer文件,不能直接使用,仅用于参考
# 使用说明
## 增加参数&说明
参数 | 类型 | 默认值 | 参数说明
:-: | :-: | :-: | :-:
rates | Array | [2, 1.75, 1.5, 1.25, 1.0, 0.75, 0.5] |　倍速数组
curRateIndex | Number | 4 | 默认倍速的索引
appear_text | String | 无 | 防录屏文字,无则表示不出现防录屏文字
appear_time | Number | 10 | 防录屏文字出现是时长最大值
disappear_time | Number | 100 | 防录屏文字消失的时长最大值
appear_color | Array | ['#fff', '#000'] | 防录屏文字出现时的颜色
appear_fontsize_min | Number | 12 | 防录屏文字出现时字体的最小值
appear_fontsize_max | Number | 22 | 防录屏文字出现时字体的最大值

## hls自定义加密
- 加入m3u8索引文件的自定义加密方式
  - hls.min.0.12.4_hava.js文件中定位'解密操作'字样,加入自定义的解密方式,将解密后的m3u8索引字符串赋值给u
- 修改tcplayer中调用的hls.js文件地址
  - TcPlayer-2.3.2_encrypt_hava.js文件中定位'hls.js文件地址'字样,将地址改为自己的hls文件地址即可

- 使用示例

```javascript
var player = new TcPlayer('id_test_video', {
	"m3u8": "http://2157.liveplay.myqcloud.com/2157_358535a.m3u8",
	"autoplay" : true,
	"poster" : "http://www.test.com/myimage.jpg",
	"width" :  '480',
	"height" : '320',
	"x5_player": true,
    "systemFullscreen": true,
    "x5_type": "h5",
    "x5_fullscreen": true,
    "x5_orientation": 2,
	"rates": [2, 1.5, 1.0, 0.5],
	"curRateIndex": 2,
	"appear_text": "",
	"appear_time": 10,
	"disappear_time": 100,
	"appear_color": ['#fff', '#F4F4F4'],
	"appear_fontsize_min": 12,
	"appear_fontsize_max": 22,
});
```

# 教程
- [tcplayer源码改造第一弹 -> 自定义hls加密播放器](https://blog.csdn.net/z13192905903/article/details/102862664)
- [tcplayer源码改造第二弹 -> 加入倍速播放](https://blog.csdn.net/z13192905903/article/details/102862664)
- [tcplayer源码改造第三弹 -> 防盗录](https://blog.csdn.net/z13192905903/article/details/103366173)
