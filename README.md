# better-react-qmap -- React 腾讯地图组件

#### 一个对腾讯 web 地图简单封装的 React 组件

该项目是对 react-qmap 的一次优化升级，原因是 react-qmap 不能添加插件或者修改版本号，修改了地图 API 的传入方式

#### react-qmap

**GitHub 源码地址：[戳我](https://github.com/yezihaohao/react-qmap)**

**栗子：[戳我](https://cheng_haohao.gitee.io/reactqmap/#/dashboard)**

**栗子源码：[戳我](https://github.com/yezihaohao/react-qmap/tree/master/examples/src/components/maps)**

![demo截图](https://raw.githubusercontent.com/yezihaohao/react-qmap/master/examples/src/styles/t.gif)

**安装**

```
npm install better-react-qmap
```

**基础用法**

```
import ReactQMap from 'better-react-qmap';

 <ReactQMap
      center={{ latitude: 30.53786, longitude: 104.07265 }}
      initialOptions={{ zoomControl: true, mapTypeControl: true }}
      apiVersonSrc='https://map.qq.com/api/js?v=2.exp&key=OB4BZ-D4W3U-B7VVO-4PJWW-6TKDJ-WPB77'
      style={{ height: 300 }} // 高度和宽度默认占父元素的100%
    />
```

#### API

| Method         | Type     | Optional | Default                                                                    | Description                                                                                                             |
| -------------- | -------- | -------- | -------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| getMap         | function | false    |                                                                            | 获取地图的对象和当前容器的 map 对象,第一个参数是 new 的当前 map 对象，第二个参数是全局 map 对象                         |
| style          | object   | false    |                                                                            | 设置组件的内联样式，默认样式 width: '100%', height: '100%'                                                              |
| className      | string   | false    |                                                                            | 设置组件的 class                                                                                                        |
| mySpot         | object   | false    |                                                                            | 设置地图的定位坐标                                                                                                      |
| initialOptions | object   | false    | zoom: 14,disableDefaultUI: true, zoomControl: false,mapTypeControl: false, | 初始化地图的参数，简单默认设置了几个，更多的初始化参数请参照[文档](http://lbs.qq.com/javascript_v2/doc/mapoptions.html) |
| apiVersonSrc   | string   | true     |                                                                            | 传入的地图 API js,可以附上相关的插件的                                                                                  |
| center         | object   | true     |                                                                            | 设置地图初始化的中心位置坐标                                                                                            |
| getContainer   | function | false    |                                                                            | 获取地图的 html dom 元素的函数，参数是当前地图挂载的元素 DOM                                                            |

#### 关于

更多例子请参考 react-qmap 示例
有问题请提 issue

#### license

MIT
