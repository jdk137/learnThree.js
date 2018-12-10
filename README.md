# learnThree.js
存放一些learn three.js 的源码，方便以后查看

Three.js 学习指南示例说明




#### 1. 用Three.js创建你的第一个三维场景
##### 1.1 具有所有基本元素的hello world示例
src/chapter-01/06-screen-size-change.html
 
 
#### 2. 使用构建Three.js场景的基本组件
##### 2.1 添加、删除、枚举、通过名字获取场景中的对象
src/chapter-02/01-basic-scene.html
##### 2.2 雾化效果
src/chapter-02/02-foggy-scene.html

##### 2.3 材质效果覆盖
src/chapter-02/03-forced-material.html

场景对象最重要的函数和属性的总结
![在这里插入图片描述](https://img-blog.csdnimg.cn/20181210172833206.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2pkazEzNw==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20181210172848581.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2pkazEzNw==,size_16,color_FFFFFF,t_70)
##### 2.4 three.js内建的几何体
src/chapter-02/04-geometries.html

##### 2.5 自定义几何体，复制几何体
src/chapter-02/05-custom-geometry.html

##### 2.6 网格对象的函数和属性 position, rotation, scale, translate, visible
src/chapter-02/06-mesh-properties.html
![在这里插入图片描述](https://img-blog.csdnimg.cn/20181210172910619.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2pkazEzNw==,size_16,color_FFFFFF,t_70)

##### 2.7 正投影相机和透视相机
src/chapter-02/07-both-cameras.html
![在这里插入图片描述](https://img-blog.csdnimg.cn/20181210172918292.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2pkazEzNw==,size_16,color_FFFFFF,t_70)

![在这里插入图片描述](https://img-blog.csdnimg.cn/20181210172956565.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2pkazEzNw==,size_16,color_FFFFFF,t_70)

![在这里插入图片描述](https://img-blog.csdnimg.cn/2018121017300945.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2pkazEzNw==,size_16,color_FFFFFF,t_70)

![在这里插入图片描述](https://img-blog.csdnimg.cn/20181210173022101.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2pkazEzNw==,size_16,color_FFFFFF,t_70)

##### 2.8 让相机在指定点上聚焦
src/chapter-02/08-cameras-lookat.html
camera.lookAt( new THREE.Vector3(x, y, z));







