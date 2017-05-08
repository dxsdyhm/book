### Yoosee结构  

#### 1.结构简图  
  ![root][root]
#### 2.示例图片  
  ![struct][struct]
#### 3.音频简介  

* **AudioTrack**: P2P内部维护一个缓冲队列，存储设备端发来的音频数据（FFmpeg解码），java（APP）会在开始监控时启动一个播放声音的线程（```while(true)```）,线程负责取缓冲队列的数据交给Android，当没有数据时，等待。  
* **AudioRecoder**: Android 提供的音频框架中提供的类，内部同样维护着一个从手机硬件（MIC）采集的声音数据缓冲队列，java（APP）会在开始监控时启动一个采集声音的线程（```while(true)```）,线程负责取缓冲队列的数据交给通过P2P 数据通道传给设备，当没有数据时，等待。  

#### 4.视频简介  
* 与音频类似  
    
[root]:http://7xp6ld.com1.z0.glb.clouddn.com/Yoosee%E7%BB%93%E6%9E%84.bmp
[struct]:http://7xp6ld.com1.z0.glb.clouddn.com/struct.png