## 使用说明
- 将tcplayer.js和hls.js进行压缩
- 加入m3u8索引文件的自定义加密方式
  - hls.min.0.12.4_hava.js文件中定位'解密操作'字样,加入自定义的解密方式,将解密后的m3u8索引字符串赋值给u
- 修改tcplayer中调用的hls.js文件地址
  - TcPlayer-2.3.2_encrypt_hava.js文件中定位'hls.js文件地址'字样,将地址改为自己的hls文件地址即可
