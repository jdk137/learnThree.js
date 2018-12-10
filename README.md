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
![8689e6e5442177d8b8ce3026613e8bcf.png](./images/8689e6e5442177d8b8ce3026613e8bcf.png)
![ecb392bf079129be6ba54c1004e4210b.png](./images/ecb392bf079129be6ba54c1004e4210b.png)

##### 2.4 three.js内建的几何体
src/chapter-02/04-geometries.html

##### 2.5 自定义几何体，复制几何体
src/chapter-02/05-custom-geometry.html

##### 2.6 网格对象的函数和属性 position, rotation, scale, translate, visible
src/chapter-02/06-mesh-properties.html
![40c01837e6870342886abff1f200ebe4.png](./images/40c01837e6870342886abff1f200ebe4.png)

##### 2.7 正投影相机和透视相机
src/chapter-02/07-both-cameras.html

![471de146be1f542f55cc8986cbd86575.png](./images/471de146be1f542f55cc8986cbd86575.png)
![ab0b9de346779a27a078872937ba786f.png](./images/ab0b9de346779a27a078872937ba786f.png)
![b7f95427eae44417c92b0fd9ff4387b3.png](./images/b7f95427eae44417c92b0fd9ff4387b3.png)
![fc9b6741607537bae0e67ca0094ff56d.png](./images/fc9b6741607537bae0e67ca0094ff56d.png)

##### 2.8 让相机在指定点上聚焦
src/chapter-02/08-cameras-lookat.html
camera.lookAt( new THREE.Vector3(x, y, z));






