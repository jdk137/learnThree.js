# learnThree.js
存放一些learn three.js 的源码，方便查阅， 代码下载自华章出版社官网的源码。

huazhang目录下是第二版的修改源码。 huazhang3目录下面是第三版的源码。

第二版和第三版大同小异，第二版的three.js版本是69， 第三版的版本是95。


Three.js 开发指南（原书第二版）示例说明

本文档的图片可能无法显示，可以跳转到[这里](https://blog.csdn.net/jdk137/article/details/84943611)查看。


### 1. 用Three.js创建你的第一个三维场景
#### 1.1 [具有所有基本元素的hello world示例](https://jdk137.github.io/learnThree.js/huazhang/chapter-01/06-screen-size-change.html)

<br>


### 2. 使用构建Three.js场景的基本组件
#### 2.1 [添加、删除、枚举、通过名字获取场景中的对象](https://jdk137.github.io/learnThree.js/huazhang/chapter-02/01-basic-scene.html)
#### 2.2 [雾化效果](https://jdk137.github.io/learnThree.js/huazhang/chapter-02/02-foggy-scene.html)

#### 2.3 [材质效果覆盖](https://jdk137.github.io/learnThree.js/huazhang/chapter-02/03-forced-materials.html)

<center>场景对象最重要的函数和属性的总结</center>

![在这里插入图片描述](https://img-blog.csdnimg.cn/20181210172833206.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2pkazEzNw==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20181210172848581.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2pkazEzNw==,size_16,color_FFFFFF,t_70)

#### 2.4 [three.js内建的几何体](https://jdk137.github.io/learnThree.js/huazhang/chapter-02/04-geometries.html)

#### 2.5 [自定义几何体，复制几何体](https://jdk137.github.io/learnThree.js/huazhang/chapter-02/05-custom-geometry.html)

#### 2.6 [网格对象的函数和属性 position, rotation, scale, translate, visible](https://jdk137.github.io/learnThree.js/huazhang/chapter-02/06-mesh-properties.html)

![在这里插入图片描述](https://img-blog.csdnimg.cn/20181210172910619.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2pkazEzNw==,size_16,color_FFFFFF,t_70)

#### 2.7 [正投影相机和透视相机](https://jdk137.github.io/learnThree.js/huazhang/chapter-02/07-both-cameras.html)
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

#### 2.8 [让相机在指定点上聚焦](https://jdk137.github.io/learnThree.js/huazhang/chapter-02/08-cameras-lookat.html)
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

#### 3.1 [AmbientLight](https://jdk137.github.io/learnThree.js/huazhang/chapter-03/01-ambient-light.html)环境光
#### 3.2 [PointLight](https://jdk137.github.io/learnThree.js/huazhang/chapter-03/02-point-light.html) 点光源
#### 3.3 [SpotLight](https://jdk137.github.io/learnThree.js/huazhang/chapter-03/03-spot-light.html) 聚光灯
#### 3.4 [DirectionalLight](https://jdk137.github.io/learnThree.js/huazhang/chapter-03/04-directional-light.html) 方向光
#### 3.5 [HemisphereLight](https://jdk137.github.io/learnThree.js/huazhang/chapter-03/05-hemisphere-light.html) 半球环境光
#### 3.6 [AreaLight](https://jdk137.github.io/learnThree.js/huazhang/chapter-03/06-area-light.html) 区域光
#### 3.7 [LensflaresLight](https://jdk137.github.io/learnThree.js/huazhang/chapter-03/07-lensflares.html) 光晕光



<br>

### 4. 使用Three.js的材质
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190319112153578.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2pkazEzNw==,size_16,color_FFFFFF,t_70)
参数配置看这里： [Three.js - 材质的使用参数详解](https://blog.csdn.net/jdk137/article/details/88657132)

#### 4. 1 [MeshBasicMaterial](https://jdk137.github.io/learnThree.js/huazhang/chapter-04/01-basic-mesh-material.html) 网格基础材质
#### 4. 2 [MeshDepthMaterial](https://jdk137.github.io/learnThree.js/huazhang/chapter-04/02-depth-material.html) 网格深度材质， 颜色与离开相机的距离相关。
#### 4. 3 [材质结合： 基础材质 + 深度材质](https://jdk137.github.io/learnThree.js/huazhang/chapter-04/03-combined-material.html)
#### 4. 4 [MeshNormalMaterial](https://jdk137.github.io/learnThree.js/huazhang/chapter-04/04-mesh-normal-material.html) 网格法向材质, 法向材质可以将材质的颜色设置为其法向量的方向，有时候对于调试很有帮助。
#### 4. 5 [MeshFaceMaterial](https://jdk137.github.io/learnThree.js/huazhang/chapter-04/05-mesh-face-material.html) 网格面材质， 可以指定每个面使用的材质。
#### 4. 6 [MeshLambertMaterial](https://jdk137.github.io/learnThree.js/huazhang/chapter-04/06-mesh-lambert-material.html) 网格lambert材质， Lambert光照模型的主要特点是只考虑漫反射而不考虑镜面反射的效果，因而对于金属、镜子等需要镜面反射效果的物体就不适应，对于其他大部分物体的漫反射效果都是适用的。[效果示例](http://www.ituring.com.cn/book/miniarticle/51526)
#### 4. 7 [MeshPhongMaterial](https://jdk137.github.io/learnThree.js/huazhang/chapter-04/07-mesh-phong-material.html) 网格phong材质， 和Lambert不同的是，Phong模型考虑了镜面反射的效果，因此对于金属、镜面的表现尤为适合。[效果示例](http://www.ituring.com.cn/book/miniarticle/51807)
#### 4. 8 [ShaderMaterial](https://jdk137.github.io/learnThree.js/huazhang/chapter-04/08-shader-material.html) 着色器材质, glsl自定义材质，
#### 4. 9 [LineBasicMaterial](https://jdk137.github.io/learnThree.js/huazhang/chapter-04/09-line-material.html) 直线基础材质
#### 4. 10 [LineDashMaterial](https://jdk137.github.io/learnThree.js/huazhang/chapter-04/10-line-material-dashed.html) 虚线材质

着色器资源, 创建和分享着色器的好网站： [http://glslsandbox.com/](http://glslsandbox.com/)和[https://www.shadertoy.com](https://www.shadertoy.com)  


<br>

### 5. 学习使用几何体

简单的参数可以看[这里](https://blog.csdn.net/u011135260/article/details/52725162)

#### 5. 1 二维几何体
#### 5.1.1 [PlaneGeometry](https://jdk137.github.io/learnThree.js/huazhang/chapter-05/01-basic-2d-geometries-plane.html) 二维矩形
#### 5.1.2 [CircleGeometry](https://jdk137.github.io/learnThree.js/huazhang/chapter-05/02-basic-2d-geometries-circle.html) 二维圆
#### 5.1.3 [RingGeometry](https://jdk137.github.io/learnThree.js/huazhang/chapter-05/03-basic-3d-geometries-ring.html) 二维环
#### 5.1.4 [ShapeGeometry](https://jdk137.github.io/learnThree.js/huazhang/chapter-05/03-basic-2d-geometries-shape.html) 自定义二维图形, 可以通过一些函数画出二维图形。[自定义参数示例](https://blog.csdn.net/qq_30100043/article/details/78808725)
#### 5. 2 三维几何体
#### 5.2.1 [BoxGeometry](https://jdk137.github.io/learnThree.js/huazhang/chapter-05/04-basic-3d-geometries-cube.html) 长方体
#### 5.2.2 [SphereGeometry](https://jdk137.github.io/learnThree.js/huazhang/chapter-05/05-basic-3d-geometries-sphere.html) 球体  可以通过设置参数获得特殊的多面体,半球，伞形
#### 5.2.3 [CylinderGeometry](https://jdk137.github.io/learnThree.js/huazhang/chapter-05/06-basic-3d-geometries-cylinder.html) 圆柱体 可以通过参数获得多边形柱体
#### 5.2.4 [TorusGeometry](https://jdk137.github.io/learnThree.js/huazhang/chapter-05/07-basic-3d-geometries-torus.html) 三维圆环
#### 5.2.5 [TorusKnotGeometry](https://jdk137.github.io/learnThree.js/huazhang/chapter-05/08-basic-3d-geometries-torus-knot.html) 环状扭结
#### 5.2.6 [各种多面体](https://jdk137.github.io/learnThree.js/huazhang/chapter-05/09-basic-3d-geometries-polyhedron.html)
其实几何体还有线性几何体，可以看上一章。  


<br>

### 6. 高级几何体和二元操作
这一章非常实用，介绍了很多将一维和二维的几何体转化为三维的方法。以及三维几何体合并、相减、相交等操作。对数据可视化应该比较有用。

#### 6.1 [ConvexGeometry](https://jdk137.github.io/learnThree.js/huazhang/chapter-06/01-advanced-3d-geometries-convex.html) 凸包几何体  包含三维点集的多面体 [详细参数设置](https://blog.csdn.net/qq_30100043/article/details/78787260)

#### 6.2 [LatheGeometry](https://jdk137.github.io/learnThree.js/huazhang/chapter-06/02-advanced-3d-geometries-lathe.html) 通过旋转创建几何体    让一根曲线绕Z轴旋转一周，创建几何体 [详细参数设置](https://blog.csdn.net/qq_30100043/article/details/78797814)

#### 6.3 [ExtrudeGeometry](https://jdk137.github.io/learnThree.js/huazhang/chapter-06/03-extrude-geometry.html) 让一个平面形状沿某一根曲线拉伸，创建几何体 [详细参数设置](https://blog.csdn.net/qq_30100043/article/details/78838429)

#### 6.4 [TubeGeometry](https://jdk137.github.io/learnThree.js/huazhang/chapter-06/04-extrude-tube.html) 管道几何体，让某一根曲线变粗，创建几何体 [详细参数设置](https://blog.csdn.net/qq_30100043/article/details/78848765)

#### 6.5 [把svg拉伸](https://jdk137.github.io/learnThree.js/huazhang/chapter-06/05-extrude-svg.html) 让一个svg平面形状沿某一根曲线拉伸，创建几何体 [详细参数设置](https://blog.csdn.net/qq_30100043/article/details/78858886)， 依赖于d3-threeD.js库


#### 6.6 [ParametricGeometry](https://jdk137.github.io/learnThree.js/huazhang/chapter-06/06-parametric-geometries.html) 参数化几何体， 通过设置函数，创建各种几何体 [详细参数设置](https://blog.csdn.net/qq_30100043/article/details/78898102)

#### 6.7 [textGeometry](https://jdk137.github.io/learnThree.js/huazhang/chapter-06/07-text-geometry.html) 文字几何体 [详细参数设置](https://blog.csdn.net/qq_30100043/article/details/78907566) 示例中是老版本threejs的js文字方式，参数设置中是新版本的json文字方式 [typeface在线字体库获取相关字体文件](http://gero3.github.io/facetype.js/)

#### 6.8 [几何体的二元操作](https://jdk137.github.io/learnThree.js/huazhang/chapter-06/08-binary-operations.html) 几何体的合并、相减、相交操作 [详细参数设置](https://blog.csdn.net/qq_30100043/article/details/78944426)  依赖于ThreeBSP库



<br>

### 7. 粒子，sprite和点云
这一章介绍了两种粒子系统： sprite和点云。sprite可以定制每一个粒子的样式，支持的点比较少。点云可以定制一群粒子的材质，支持的点更多；点云只可以定制单个粒子的颜色，单个粒子其他的属性都是通过修改材质统一设置的。粒子的位置在sprite和点云中都可以单独修改。

#### 7.1 [理解粒子](https://jdk137.github.io/learnThree.js/huazhang/chapter-07/01-particles.html)

#### 7.2 [粒子颜色](https://jdk137.github.io/learnThree.js/huazhang/chapter-07/02-particles-webgl.html)

#### 7.3 [点云基础](https://jdk137.github.io/learnThree.js/huazhang/chapter-07/03-basic-point-cloud.html)

#### 7.4 [sprite + canvasRenderer](https://jdk137.github.io/learnThree.js/huazhang/chapter-07/04-program-based-sprites.html) 通过代码绘制canvas内容，并设置为THREE.SpriteCanvasMaterial的program属性值。

#### 7.5a [pointCloud + webglRenderer](https://jdk137.github.io/learnThree.js/huazhang/chapter-07/05a-program-based-point-cloud-webgl.html) 通过代码绘制canvas内容，并设置为THREE.PointCloudMaterial的map属性值。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190328163231605.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2pkazEzNw==,size_16,color_FFFFFF,t_70)

#### 7.5b [sprite + webglRenderer](https://jdk137.github.io/learnThree.js/huazhang/chapter-07/05b-program-based-sprites-webgl.html) 通过代码绘制canvas内容，并设置为THREE.SpriteMaterial的map属性值。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190328162951790.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2pkazEzNw==,size_16,color_FFFFFF,t_70)

#### 7.6 [雨滴 单个纹理](https://jdk137.github.io/learnThree.js/huazhang/chapter-07/06-rainy-scene.html) 使用纹理图片来设置THREE.PointCloudMaterial的map属性值。

#### 7.7 [雪花 多个纹理](https://jdk137.github.io/learnThree.js/huazhang/chapter-07/07-snowy-scene.html) 使用多个纹理图片来创建多个pointCloud。

#### 7.8 [sprite 使用大纹理图片的一部分](https://jdk137.github.io/learnThree.js/huazhang/chapter-07/08-sprites.html)  

#### 7.9 [sprite 使用大纹理图片的多个部分](https://jdk137.github.io/learnThree.js/huazhang/chapter-07/09-sprites-3D.html)  

#### 7.10 [利用几何体模型的结点创建粒子系统](https://jdk137.github.io/learnThree.js/huazhang/chapter-07/10-create-particle-system-from-model.html)  




<br>

### 8. 创建、加载高级网格和几何体
这一章介绍了 1. 如何组合几何体。如果说第7章的粒子中的最小单元是平面的，那么这一章最小单元就是立体的。group之于merge, 有点类似于sprite之于pointCloud。  2. 如何加载三维模型文件。Blender是一个开源的制作三维几何体的软件，介绍了如何从Blender导出三维模型文件。
[多种格式的比较和说明](http://www.bgteach.com/article/132)

#### 8.1 [group 组](https://jdk137.github.io/learnThree.js/huazhang/chapter-08/01-grouping.html)  group可以把多个object组合成一个object, 并对合成的object进行统一的位移、旋转、缩放操作。使用组的时候，还可以单独引用、修改、定位每一个单独的几何体，唯一需要注意的是，所有的位移、旋转、缩放操作都是相对于父对象的。
#### 8.2 [merge 合并](https://jdk137.github.io/learnThree.js/huazhang/chapter-08/02-merging.html) merge可以把多个几何体合并成一个几何体。内部的几何体共享一个材质。无法单独控制。merge的性能优于group，书中说可以提升5倍。
#### 8.3 [json object导入导出](https://jdk137.github.io/learnThree.js/huazhang/chapter-08/03-load-save-json-object.html)
#### 8.4 [json scene导入导出](https://jdk137.github.io/learnThree.js/huazhang/chapter-08/04-load-save-json-scene.html)
#### 8.5 [blender 模型导出并显示](https://jdk137.github.io/learnThree.js/huazhang/chapter-08/05-blender-from-json.html)
#### 8.6 [obj格式](https://jdk137.github.io/learnThree.js/huazhang/chapter-08/06-load-obj.html)
#### 8.7 [obj-mtl格式](https://jdk137.github.io/learnThree.js/huazhang/chapter-08/07-load-obj-mtl.html)
#### 8.8 [collada(.dae)格式](https://jdk137.github.io/learnThree.js/huazhang/chapter-08/08-load-collada.html)
#### 8.9 [stl格式](https://jdk137.github.io/learnThree.js/huazhang/chapter-08/09-load-stl.html)
#### 8.10 [ctm格式](https://jdk137.github.io/learnThree.js/huazhang/chapter-08/10-load-ctm.html)
#### 8.11 [vtk格式](https://jdk137.github.io/learnThree.js/huazhang/chapter-08/11-load-vtk.html)
#### 8.12 [pdb格式](https://jdk137.github.io/learnThree.js/huazhang/chapter-08/12-load-pdb.html)
#### 8.13 [PLY格式](https://jdk137.github.io/learnThree.js/huazhang/chapter-08/13-load-PLY.html) 粒子效果示例
#### 8.14 [awd格式](https://jdk137.github.io/learnThree.js/huazhang/chapter-08/14-load-awd.html)
#### 8.15 [assimp格式](https://jdk137.github.io/learnThree.js/huazhang/chapter-08/15-load-assimp.html)
#### 8.16 [vrml格式](https://jdk137.github.io/learnThree.js/huazhang/chapter-08/16-load-vrml.html)
#### 8.17 [babylon格式](https://jdk137.github.io/learnThree.js/huazhang/chapter-08/17-load-babylon.html) babylon可以整个scene导入




<br>

### 9. 创建动画和移动摄像机
RequestAnimationFrame 实现动画。 Tween.js实现补间。 光线追踪实现交互。  各种内置控制器。   变形和骨骼动画。

#### 9.1.1 [简单动画](https://jdk137.github.io/learnThree.js/huazhang/chapter-09/01-basic-animation.html) 
#### 9.1.2 [选择对象](https://jdk137.github.io/learnThree.js/huazhang/chapter-09/02-selecting-objects.html)  ![在这里插入图片描述](https://img-blog.csdnimg.cn/20191012143107858.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2pkazEzNw==,size_16,color_FFFFFF,t_70)![在这里插入图片描述](https://img-blog.csdnimg.cn/20191012143155844.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2pkazEzNw==,size_16,color_FFFFFF,t_70)
#### 9.1.3 [使用tween.js实现动画](https://jdk137.github.io/learnThree.js/huazhang/chapter-09/03-animation-tween.html)  
![在这里插入图片描述](https://img-blog.csdnimg.cn/20191012143453404.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2pkazEzNw==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20191012143528196.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2pkazEzNw==,size_16,color_FFFFFF,t_70)
#### 9.2.1 [轨迹球控制器](https://jdk137.github.io/learnThree.js/huazhang/chapter-09/04-trackball-controls-camera.html)  
![在这里插入图片描述](https://img-blog.csdnimg.cn/20191012143659980.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2pkazEzNw==,size_16,color_FFFFFF,t_70)
#### 9.2.2 [飞行控制器](https://jdk137.github.io/learnThree.js/huazhang/chapter-09/05-fly-controls-camera.html)  
![在这里插入图片描述](https://img-blog.csdnimg.cn/20191012143801231.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2pkazEzNw==,size_16,color_FFFFFF,t_70)
#### 9.2.3 [翻滚控制器](https://jdk137.github.io/learnThree.js/huazhang/chapter-09/06-roll-controls-camera.html) 
![在这里插入图片描述](https://img-blog.csdnimg.cn/20191012143916717.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2pkazEzNw==,size_16,color_FFFFFF,t_70)
#### 9.2.4 [第一视角控制器](https://jdk137.github.io/learnThree.js/huazhang/chapter-09/07-first-person-camera.html) 
![在这里插入图片描述](https://img-blog.csdnimg.cn/2019101214404943.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2pkazEzNw==,size_16,color_FFFFFF,t_70)
#### 9.2.5 [轨道控制器](https://jdk137.github.io/learnThree.js/huazhang/chapter-09/08-controls-orbit.html) 
适合用来做地球的3D控制
![在这里插入图片描述](https://img-blog.csdnimg.cn/20191012144204554.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2pkazEzNw==,size_16,color_FFFFFF,t_70)
### 9.3 变形动画和骨骼动画
#### 9.3.1 用变形目标创建动画
#### 9.3.1.1 [用MorphAnimMesh创建动画](https://jdk137.github.io/learnThree.js/huazhang/chapter-09/10-morph-targets.html) 需要带有变形目标的模型
#### 9.3.1.2 [通过设置morphTargetInfluence创建动画](https://jdk137.github.io/learnThree.js/huazhang/chapter-09/11-morph-targets-manually.html) 通过代码创建变形目标
#### 9.3.2 [用骨骼和蒙皮来创建动画](https://jdk137.github.io/learnThree.js/huazhang/chapter-09/12-bones-manually.html) 
### 9.4 使用外部模型创建动画
#### 9.4.1 [用Blender创建骨骼动画](https://jdk137.github.io/learnThree.js/huazhang/chapter-09/13-animation-from-blender.html) 
#### 9.4.2 [用Collada创建骨骼动画](https://jdk137.github.io/learnThree.js/huazhang/chapter-09/14-animation-from-collada.html) 
#### 9.4.3 [用md2创建骨骼动画](https://jdk137.github.io/learnThree.js/huazhang/chapter-09/15-animation-from-md2.html) 


<br>

### 10. 加载和使用纹理
![在这里插入图片描述](https://img-blog.csdnimg.cn/20191014143928761.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2pkazEzNw==,size_16,color_FFFFFF,t_70)

#### 10.1 [加载纹理并应用到网格](https://jdk137.github.io/learnThree.js/huazhang/chapter-10/01-basic-texture.html)  
 [dds格式纹理](https://jdk137.github.io/learnThree.js/huazhang/chapter-10/01-basic-texture-dds.html)    [pvr格式纹理](https://jdk137.github.io/learnThree.js/huazhang/chapter-10/01-basic-texture-pvr.html)    [tga格式纹理](https://jdk137.github.io/learnThree.js/huazhang/chapter-10/01-basic-texture-tga.html)

#### 10.2 [凹凸贴图](https://jdk137.github.io/learnThree.js/huazhang/chapter-10/02-bump-map.html)   
###### bump map这种贴图是一种灰度图，用表面上灰度的变化来描述目标表面的凹凸。Bump Map并没有改变物体的表面而只是影响光照的结果。把Bump Map叠加在已经渲染好的表面上，造成亮度上的扰动，从而让人以为是凹凸的。 [更多贴图相关原理](https://blog.csdn.net/weiwangchao_/article/details/7043087)
#### 10.3 [法向量贴图](https://jdk137.github.io/learnThree.js/huazhang/chapter-10/03-normal-map.html)   
###### normal-map图中存储的东西是每个原始表面法线的迭代。使用Normal Map的先决条件－－逐像素著色。引入NormalMap。这时光照计算和以往有点不同，把表面的法线用NormalMap中存储的法线来替代。这样当我们在计算表面光照情况的时候，就会因为法线不断的变化而产生比原来丰富的多的明暗变化。至于为什么会感觉出凹凸来这个就是人的眼睛自己骗自己了……其实那里本没有凹凸。
#### 10.4 [用光照贴图创建阴影效果](https://jdk137.github.io/learnThree.js/huazhang/chapter-10/04-light-map.html)  用阴影贴图来模拟阴影。只能用于静态场景。

#### 10.5 [用环境贴图创建反光效果（静态）](https://jdk137.github.io/learnThree.js/huazhang/chapter-10/05-env-map-static.html) ，[用环境贴图创建反光效果（动态）](https://jdk137.github.io/learnThree.js/huazhang/chapter-10/05-env-map-dynamic.html) 
#### 10.6 [高光贴图](https://jdk137.github.io/learnThree.js/huazhang/chapter-10/06-specular-map.html)   地球的海洋部分可以用反光更亮的部分来修饰。
#### 10.7 [自定义纹理映射](https://jdk137.github.io/learnThree.js/huazhang/chapter-10/07-uv-mapping.html)   blender等建模软件可以设置uv映射，导出不同的obj文件。 [Three.js也可以设置UV映射](https://jdk137.github.io/learnThree.js/huazhang/chapter-10/07-uv-mapping-manual.html)  
#### 10.8 [重复纹理](https://jdk137.github.io/learnThree.js/huazhang/chapter-10/08-repeat-wrapping.html)  
#### 10.9 [使用canvas作为纹理](https://jdk137.github.io/learnThree.js/huazhang/chapter-10/09-canvas-texture.html)  
```js
var canvas = document.createElement("canvas");
var canvasMap = new THREE.Texture(canvas);
var mat = new THREE.MeshPhongMaterial();
mat.map = canvasMap;
var mesh = new THREE.Mesh(geom, mat);
```
#### 10.10 [将画布作为凹凸贴图](https://jdk137.github.io/learnThree.js/huazhang/chapter-10/10-canvas-texture-bumpmap.html)  

#### 10.11 [将视频输出作为纹理](https://jdk137.github.io/learnThree.js/huazhang/chapter-10/11-video-texture-alternative.html)  , [使用Three.VideoTexture的简化版本](https://jdk137.github.io/learnThree.js/huazhang/chapter-10/11-video-texture.html)  
```js
var video = document.getElementById('video');
texture = new THREE.VideoTexture(video);
```





<br>

### 11. 自定义着色器和后期处理
这一章主要讲了后期处理。 可以对Three.js 输出的画面做一些After Effect 特效，比如模糊、电影、泛光等等，对提升视觉品质有很好的效果。各种不同的特效感觉像ps的滤镜，需要比较熟悉才能运用好。最后还介绍了用自定义着色器才制作后期特效。 自定义着色器也可应通过第4章4.8中的自定义材质来实现。

#### 11.1 [配置Three.js以进行后期处理](https://jdk137.github.io/learnThree.js/huazhang/chapter-11/01-basic-effect-composer.html)    THREE.EffectComposer基础示例

#### 11.2 后期处理通道
#### 11.2.1 [简单后期处理通道](https://jdk137.github.io/learnThree.js/huazhang/chapter-11/02-post-processing-simple-passes.html)  这个示例分别展示了FilmPass的电视效果，BloomPass的泛光效果，DotScreenPass的点集效果，以及三者的融合效果。
[GlitchPass电脉冲效果](https://jdk137.github.io/learnThree.js/huazhang/chapter-11/03-glitch-pass.html) 
#### 11.2.2 使用掩码的高级效果组合器
[地球与火星](https://jdk137.github.io/learnThree.js/huazhang/chapter-11/03-post-processing-masks.html) maskPass可以对单独的物体做后期处理，比如地球和火星有不同的后期处理特效。
#### 11.2.3 使用THREE.ShaderPass自定义效果
ShaderPass里面可以设置shader， 达到不同的效果。这些Shader都以Shader结尾。
[shader合集](https://jdk137.github.io/learnThree.js/huazhang/chapter-11/04-shaderpass-simple.html)
[shader模糊效果](https://jdk137.github.io/learnThree.js/huazhang/chapter-11/05-shaderpass-blur.html)
[更多高级的shader效果](https://jdk137.github.io/learnThree.js/huazhang/chapter-11/06-shaderpass-advanced.html)

#### 11.3 [创建自定义后期处理着色器](https://jdk137.github.io/learnThree.js/huazhang/chapter-11/07-shaderpass-custom.html)   自定义的shader效果




<br>

### 12. 在场景中添加物理效果和声音
这一章主要讲物理碰撞检测库Physijs, 它是一个three.js的配套库，在物理碰撞引擎ammo.js或者cannon.js上做了一层封装，方便three.js调用。

#### 12.1创建基本的Three.js场景
[多米诺骨牌](https://jdk137.github.io/learnThree.js/huazhang/chapter-12/01-basic-scene.html)

#### 12.2 [材质属性](https://jdk137.github.io/learnThree.js/huazhang/chapter-12/02-material-properties.html) 设置物理的摩擦系数和弹性

#### 12.3 [基础图形](https://jdk137.github.io/learnThree.js/huazhang/chapter-12/03-shapes.html) Physijs默认封装了不少网格几何体

#### 12.4 [使用约束限制对象的移动](https://jdk137.github.io/learnThree.js/huazhang/chapter-12/04-constraints.html) PointConstraint限制对象在两点间移动；HingeConstraint创建类似门的约束；SlideConstraint将移动限制在一个轴上；ConeTwistConstraint创建类似于球销的约束。

[运动的四轮小车](https://jdk137.github.io/learnThree.js/huazhang/chapter-12/05-dof-constraint.html) DOFConstraint实现细节的控制

#### 12.4.6 [在场景中添加声源](https://jdk137.github.io/learnThree.js/huazhang3/src/chapter-12/07-audio.html) 几何体上绑定声源，camera上绑定听筒，声音的大小随着距离的远近而变化。






