# learnThree.js
存放一些learn three.js 的源码，方便查阅， 代码下载自华章出版社官网的源码。

Three.js 开发指南（原书第二版）示例说明


### 1. 用Three.js创建你的第一个三维场景
#### 1.1 [具有所有基本元素的hello world示例](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-01/06-screen-size-change.html)

<br>


### 2. 使用构建Three.js场景的基本组件
#### 2.1 [添加、删除、枚举、通过名字获取场景中的对象](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-02/01-basic-scene.html)
#### 2.2 [雾化效果](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-02/02-foggy-scene.html)

#### 2.3 [材质效果覆盖](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-02/03-forced-materials.html)

<center>场景对象最重要的函数和属性的总结</center>

![在这里插入图片描述](https://img-blog.csdnimg.cn/20181210172833206.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2pkazEzNw==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20181210172848581.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2pkazEzNw==,size_16,color_FFFFFF,t_70)

#### 2.4 [three.js内建的几何体](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-02/04-geometries.html)

#### 2.5 [自定义几何体，复制几何体](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-02/05-custom-geometry.html)

#### 2.6 [网格对象的函数和属性 position, rotation, scale, translate, visible](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-02/06-mesh-properties.html)

![在这里插入图片描述](https://img-blog.csdnimg.cn/20181210172910619.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2pkazEzNw==,size_16,color_FFFFFF,t_70)

#### 2.7 [正投影相机和透视相机](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-02/07-both-cameras.html)
```js

          if (camera instanceof THREE.PerspectiveCamera) {
              camera = new THREE.OrthographicCamera(window.innerWidth / -16, window.innerWidth / 16, window.innerHeight / 16, window.innerHeight / -16, -200, 500);
              camera.position.x = 120;
              camera.position.y = 60;
              camera.position.z = 180;
              camera.lookAt(scene.position);

              trackballControls = initTrackballControls(camera, renderer);
              this.perspective = "Orthographic";
          } else {
              camera = new THREE.PerspectiveCamera(45, window.innerWidth / window.innerHeight, 0.1, 1000);
              camera.position.x = 120;
              camera.position.y = 60;
              camera.position.z = 180;

              camera.lookAt(scene.position);
              trackballControls = initTrackballControls(camera, renderer);
              this.perspective = "Perspective";
          }
```
![在这里插入图片描述](https://img-blog.csdnimg.cn/20181210172918292.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2pkazEzNw==,size_16,color_FFFFFF,t_70)

![在这里插入图片描述](https://img-blog.csdnimg.cn/20181210172956565.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2pkazEzNw==,size_16,color_FFFFFF,t_70)

![在这里插入图片描述](https://img-blog.csdnimg.cn/2018121017300945.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2pkazEzNw==,size_16,color_FFFFFF,t_70)

![在这里插入图片描述](https://img-blog.csdnimg.cn/20181210173022101.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2pkazEzNw==,size_16,color_FFFFFF,t_70)

#### 2.8 [让相机在指定点上聚焦](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-02/08-cameras-lookat.html)
```js
camera.lookAt( new THREE.Vector3(x, y, z));
```

<br>

### 3 . 学习使用Three.js中的光源
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190314150543755.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2pkazEzNw==,size_16,color_FFFFFF,t_70)新版本Three.js中PointLight已经可以创建阴影。

详细参数可以参考：
[three.js光源使用详解](https://blog.csdn.net/jdk137/article/details/88552491)

颜色对象方法可参考：
[THREE.Color颜色对象详解](https://blog.csdn.net/jdk137/article/details/88552791)

#### 3.1 [AmbientLight](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-03/01-ambient-light.html)环境光
#### 3.2 [PointLight](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-03/02-point-light.html) 点光源
#### 3.3 [SpotLight](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-03/03-spot-light.html) 聚光灯
#### 3.4 [DirectionalLight](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-03/04-directional-light.html) 方向光
#### 3.5 [HemisphereLight](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-03/05-hemisphere-light.html) 半球环境光
#### 3.6 [AreaLight](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-03/06-area-light.html) 区域光
#### 3.7 [LensflaresLight](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-03/07-lensflares.html) 光晕光



<br>

### 4. 使用Three.js的材质
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190319112153578.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2pkazEzNw==,size_16,color_FFFFFF,t_70)
参数配置看这里： [Three.js - 材质的使用参数详解](https://blog.csdn.net/jdk137/article/details/88657132)

#### 4. 1 [MeshBasicMaterial](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-04/01-basic-mesh-material.html) 网格基础材质
#### 4. 2 [MeshDepthMaterial](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-04/02-depth-material.html) 网格深度材质， 颜色与离开相机的距离相关。
#### 4. 3 [材质结合： 基础材质 + 深度材质](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-04/03-combined-material.html)
#### 4. 4 [MeshNormalMaterial](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-04/04-mesh-normal-material.html) 网格法向材质, 法向材质可以将材质的颜色设置为其法向量的方向，有时候对于调试很有帮助。
#### 4. 5 [MeshFaceMaterial](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-04/05-mesh-face-material.html) 网格面材质， 可以指定每个面使用的材质。
#### 4. 6 [MeshLambertMaterial](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-04/06-mesh-lambert-material.html) 网格lambert材质， Lambert光照模型的主要特点是只考虑漫反射而不考虑镜面反射的效果，因而对于金属、镜子等需要镜面反射效果的物体就不适应，对于其他大部分物体的漫反射效果都是适用的。[效果示例](http://www.ituring.com.cn/book/miniarticle/51526)
#### 4. 7 [MeshPhongMaterial](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-04/07-mesh-phong-material.html) 网格phong材质， 和Lambert不同的是，Phong模型考虑了镜面反射的效果，因此对于金属、镜面的表现尤为适合。[效果示例](http://www.ituring.com.cn/book/miniarticle/51807)
#### 4. 8 [ShaderMaterial](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-04/08-shader-material.html) 着色器材质, glsl自定义材质，
#### 4. 9 [LineBasicMaterial](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-04/09-line-material.html) 直线基础材质
#### 4. 10 [LineDashMaterial](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-04/10-line-material-dashed.html) 虚线材质

着色器资源, 创建和分享着色器的好网站： [http://glslsandbox.com/](http://glslsandbox.com/)和[https://www.shadertoy.com](https://www.shadertoy.com)  


<br>

### 5. 学习使用几何体

简单的参数可以看[这里](https://blog.csdn.net/u011135260/article/details/52725162)

#### 5. 1 二维几何体
#### 5.1.1 [PlaneGeometry](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-05/01-basic-2d-geometries-plane.html) 二维矩形
#### 5.1.2 [CircleGeometry](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-05/02-basic-2d-geometries-circle.html) 二维圆
#### 5.1.3 [RingGeometry](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-05/03-basic-3d-geometries-ring.html) 二维环
#### 5.1.4 [ShapeGeometry](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-05/03-basic-2d-geometries-shape.html) 自定义二维图形, 可以通过一些函数画出二维图形。[自定义参数示例](https://blog.csdn.net/qq_30100043/article/details/78808725)
#### 5. 2 三维几何体
#### 5.2.1 [BoxGeometry](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-05/04-basic-3d-geometries-cube.html) 长方体
#### 5.2.2 [SphereGeometry](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-05/05-basic-3d-geometries-sphere.html) 球体  可以通过设置参数获得特殊的多面体,半球，伞形
#### 5.2.3 [CylinderGeometry](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-05/06-basic-3d-geometries-cylinder.html) 圆柱体 可以通过参数获得多边形柱体
#### 5.2.4 [TorusGeometry](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-05/07-basic-3d-geometries-torus.html) 三维圆环
#### 5.2.5 [TorusKnotGeometry](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-05/08-basic-3d-geometries-torus-knot.html) 环状扭结
#### 5.2.6 [各种多面体](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-05/09-basic-3d-geometries-polyhedron.html)
其实几何体还有线性几何体，可以看上一章。  


<br>

### 6. 高级几何体和二元操作
这一章非常实用，介绍了很多将一维和二维的几何体转化为三维的方法。以及三维几何体合并、相减、相交等操作。对数据可视化应该比较有用。

#### 6.1 [ConvexGeometry](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-06/01-advanced-3d-geometries-convex.html) 凸包几何体  包含三维点集的多面体 [详细参数设置](https://blog.csdn.net/qq_30100043/article/details/78787260)

#### 6.2 [LatheGeometry](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-06/02-advanced-3d-geometries-lathe.html) 通过旋转创建几何体    让一根曲线绕Z轴旋转一周，创建几何体 [详细参数设置](https://blog.csdn.net/qq_30100043/article/details/78797814)

#### 6.3 [ExtrudeGeometry](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-06/03-extrude-geometry.html) 让一个平面形状沿某一根曲线拉伸，创建几何体 [详细参数设置](https://blog.csdn.net/qq_30100043/article/details/78838429)

#### 6.4 [TubeGeometry](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-06/04-extrude-tube.html) 管道几何体，让某一根曲线变粗，创建几何体 [详细参数设置](https://blog.csdn.net/qq_30100043/article/details/78848765)

#### 6.5 [把svg拉伸](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-06/05-extrude-svg.html) 让一个svg平面形状沿某一根曲线拉伸，创建几何体 [详细参数设置](https://blog.csdn.net/qq_30100043/article/details/78858886)， 依赖于d3-three.js库


#### 6.6 [ParametricGeometry](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-06/06-parametric-geometries.html) 参数化几何体， 通过设置函数，创建各种几何体 [详细参数设置](https://blog.csdn.net/qq_30100043/article/details/78898102)

#### 6.7 [textGeometry](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-06/07-text-geometry.html) 文字几何体 [详细参数设置](https://blog.csdn.net/qq_30100043/article/details/78907566) 示例中是老版本threejs的js文字方式，参数设置中是新版本的json文字方式 [typeface在线字体库获取相关字体文件](http://gero3.github.io/facetype.js/)

#### 6.8 [几何体的二元操作](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-06/08-binary-operations.html) 几何体的合并、相减、相交操作 [详细参数设置](https://blog.csdn.net/qq_30100043/article/details/78944426)  依赖于ThreeBSP库



<br>

### 7. 粒子，sprite和点云
这一章介绍了两种粒子系统： sprite和点云。sprite可以定制每一个粒子的样式，支持的点比较少。点云可以定制一群粒子的材质，支持的点更多；点云只可以定制单个粒子的颜色，单个粒子其他的属性都是通过修改材质统一设置的。粒子的位置在sprite和点云中都可以单独修改。

#### 7.1 [理解粒子](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-07/01-particles.html)

#### 7.2 [粒子颜色](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-07/02-particles-webgl.html)

#### 7.3 [点云基础](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-07/03-basic-point-cloud.html)

#### 7.4 [sprite + canvasRenderer](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-07/04-program-based-sprites.html) 通过代码绘制canvas内容，并设置为THREE.SpriteCanvasMaterial的program属性值。

#### 7.5a [pointCloud + webglRenderer](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-07/05a-program-based-point-cloud-webgl.html) 通过代码绘制canvas内容，并设置为THREE.PointCloudMaterial的map属性值。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190328163231605.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2pkazEzNw==,size_16,color_FFFFFF,t_70)

#### 7.5b [sprite + webglRenderer](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-07/05b-program-based-sprites-webgl.html) 通过代码绘制canvas内容，并设置为THREE.SpriteMaterial的map属性值。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190328162951790.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2pkazEzNw==,size_16,color_FFFFFF,t_70)

#### 7.6 [雨滴 单个纹理](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-07/06-rainy-scene.html) 使用纹理图片来设置THREE.PointCloudMaterial的map属性值。

#### 7.7 [雪花 多个纹理](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-07/07-snowy-scene.html) 使用多个纹理图片来创建多个pointCloud。

#### 7.8 [sprite 使用大纹理图片的一部分](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-07/08-sprites.html)  

#### 7.9 [sprite 使用大纹理图片的多个部分](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-07/09-sprites-3D.html)  

#### 7.10 [利用几何体模型的结点创建粒子系统](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-07/10-create-particle-system-from-model.html)  




<br>

### 8. 创建、加载高级网格和几何体
这一章介绍了 1. 如何组合几何体。如果说7章的粒子中的最小单元是平面的，那么这一章最小单元就是立体的。group之于merge, 有点类似于sprite之于pointCloud。  2. 如何加载三维模型文件。Blender是一个开源的制作三维几何体的软件,介绍了如何从Blender导出三维模型文件。
[多种格式的比较和说明]（http://www.bgteach.com/article/132）

#### 8.1 [group 组](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-08/01-grouping.html)  group可以把多个object组合成一个object, 并对合成的object进行统一的位移、旋转、缩放操作。使用组的时候，还可以单独引用、修改、定位每一个单独的几何体，唯一需要注意的是，所有的位移、旋转、缩放操作都是相对于父对象的。
#### 8.2 [merge 合并](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-08/02-merging.html) merge可以把多个几何体合并成一个几何体。内部的几何体共享一个材质。无法单独控制。merge的性能优于group，书中说可以提升5倍。
#### 8.3 [json object导入导出](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-08/03-load-save-json-object.html)
#### 8.4 [json scene导入导出](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/cahpter-08/04-load-save-json-scene.html)
#### 8.5 [blender 模型导出并显示](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/cahpter-08/05-blender-from-json.html)
#### 8.6 [obj格式](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/cahpter-08/06-load-obj.html)
#### 8.7 [obj-mtl格式](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/cahpter-08/07-load-obj-mtl.html)
#### 8.8 [collada(.dae)格式](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/cahpter-08/08-load-collada.html)
#### 8.9 [stl格式](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/cahpter-08/09-load-stl.html)
#### 8.10 [ctm格式](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/cahpter-08/10-load-ctm.html)
#### 8.11 [vtk格式](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/cahpter-08/11-load-vtk.html)
#### 8.12 [pdb格式](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/cahpter-08/12-load-pdb.html)
#### 8.13 [PLY格式](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/cahpter-08/13-load-PLY.html) 粒子效果示例
#### 8.14 [awd格式](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/cahpter-08/14-load-awd.html)
#### 8.15 [assimp格式](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/cahpter-08/15-load-assimp.html)
#### 8.16 [vrml格式](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/cahpter-08/16-load-vrml.html)
#### 8.17 [babylon格式](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/cahpter-08/17-load-babylon.html) babylon可以整个scene导入



