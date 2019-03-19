# learnThree.js
存放一些learn three.js 的源码，方便查阅

Three.js 学习指南示例说明


### 1. 用Three.js创建你的第一个三维场景
##### 1.1 [具有所有基本元素的hello world示例](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-01/06-screen-size-change.html)

<br>


### 2. 使用构建Three.js场景的基本组件
##### 2.1 [添加、删除、枚举、通过名字获取场景中的对象](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-02/01-basic-scene.html)
##### 2.2 [雾化效果](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-02/02-foggy-scene.html)

##### 2.3 [材质效果覆盖](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-02/03-forced-materials.html)

<center>场景对象最重要的函数和属性的总结</center>

![在这里插入图片描述](https://img-blog.csdnimg.cn/20181210172833206.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2pkazEzNw==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20181210172848581.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2pkazEzNw==,size_16,color_FFFFFF,t_70)

##### 2.4 [three.js内建的几何体](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-02/04-geometries.html)

##### 2.5 [自定义几何体，复制几何体](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-02/05-custom-geometry.html)

##### 2.6 [网格对象的函数和属性 position, rotation, scale, translate, visible](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-02/06-mesh-properties.html)

![在这里插入图片描述](https://img-blog.csdnimg.cn/20181210172910619.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2pkazEzNw==,size_16,color_FFFFFF,t_70)

##### 2.7 [正投影相机和透视相机](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-02/07-both-cameras.html)
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

##### 2.8 [让相机在指定点上聚焦](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-02/08-cameras-lookat.html)
```js
camera.lookAt( new THREE.Vector3(x, y, z));
```


### 3 . 学习使用Three.js中的光源
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190314150543755.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2pkazEzNw==,size_16,color_FFFFFF,t_70)新版本Three.js中PointLight已经可以创建阴影。

详细参数可以参考：
[three.js光源使用详解](https://blog.csdn.net/jdk137/article/details/88552491)

颜色对象方法可参考：
[THREE.Color颜色对象详解](https://blog.csdn.net/jdk137/article/details/88552791)

##### 3.1 [AmbientLight](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-03/01-ambient-light.html)环境光
##### 3.2 [PointLight](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-03/02-point-light.html) 点光源
##### 3.3 [SpotLight](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-03/03-spot-light.html) 聚光灯
##### 3.4 [DirectionalLight](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-03/04-directional-light.html) 方向光
##### 3.5 [HemisphereLight](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-03/05-hemisphere-light.html) 半球环境光
##### 3.6 [AreaLight](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-03/06-area-light.html) 区域光
##### 3.7 [LensflaresLight](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-03/07-lensflares.html) 光晕光




### 4. 使用Three.js的材质
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190319112153578.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2pkazEzNw==,size_16,color_FFFFFF,t_70)
参数配置看这里： [Three.js - 材质的使用参数详解](https://blog.csdn.net/jdk137/article/details/88657132)

##### 4. 1 [MeshBasicMaterial](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-04/01-basic-mesh-material.html) 网格基础材质
##### 4. 2 [MeshDepthMaterial](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-04/02-depth-material.html) 网格深度材质
##### 4. 3 [材质结合： 基础材质 + 深度材质](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-04/03-combined-material.html)
##### 4. 4 [MeshNormalMaterial](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-04/04-mesh-normal-material.html) 网格法向材质, 法向材质可以将材质的颜色设置为其法向量的方向，有时候对于调试很有帮助。
##### 4. 5 [MeshFaceMaterial](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-04/05-mesh-face-material.html) 网格面材质， 可以指定每个面使用的材质。
##### 4. 6 [MeshLambertMaterial](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-04/06-mesh-lambert-material.html) 网格lambert材质， Lambert光照模型的主要特点是只考虑漫反射而不考虑镜面反射的效果，因而对于金属、镜子等需要镜面反射效果的物体就不适应，对于其他大部分物体的漫反射效果都是适用的。[效果示例](http://www.ituring.com.cn/book/miniarticle/51526)
##### 4. 7 [MeshPhongMaterial](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-04/07-mesh-phong-material.html) 网格phong材质， 和Lambert不同的是，Phong模型考虑了镜面反射的效果，因此对于金属、镜面的表现尤为适合。[效果示例](http://www.ituring.com.cn/book/miniarticle/51807)
##### 4. 8 [ShaderMaterial](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-04/08-shader-material.html) 着色器材质, glsl自定义材质，
##### 4. 9 [LineBasicMaterial](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-04/09-line-material.html) 直线基础材质
##### 4. 10 [LineDashMaterial](http://htmlpreview.github.io/?https://github.com/jdk137/learnThree.js/master/huazhang/chapter-04/10-line-material-dashed.html) 虚线材质

着色器资源, 创建和分享着色器的好网站： [http://glslsandbox.com/](http://glslsandbox.com/), [https://www.shadertoy.com](https://www.shadertoy.com)


