# PictureSelector
[![](https://jitpack.io/v/More-Stronger/PictureSelector.svg)](https://jitpack.io/#More-Stronger/PictureSelector)

   基于LuckSiege/PictureSelector2.2.3版本上进行修改。修改内容包含：
   <tab>1.原图选择是否显示
   <tab>2.导航栏颜色修改并将默认样式导航栏颜色改为黑色
   <tab>3.迁移androidx

![original.gif](https://github.com/More-Stronger/PictureSelector/blob/master/image/original.gif)
   
### **如何使用：**

#### PictureSelector库使用示例：

#### 1.Add the JitPack repository to your build file
      allprojects {
         repositories {
			   ...
			   maven { url 'https://jitpack.io' }
		   }
	   }
      
#### 2. Add the dependency
	   dependencies {
	          implementation 'com.github.More-Stronger.PictureSelector:picture_library:v2.2.5'
	   }
	   
#### 3.增加功能

##### 3.1功能配置

	 .isShowOriginalImg(false)
	 是否显示原图，默认为false不显示。 
	 注意：1.当true显示原图时，原图的选中状态会改变压缩状态;返回结果如下：
	      勾选原图时，返回LocalMedia实体中originalImg为true，compressed为false,compressPath为null;
	      不勾选原图，返回LocalMedia实体中originalImg为false，compressed为true,compressPath有值；
	      
	      2.当true显示原图时，原图默认是否选中判断如下：
	      如传入已选图片，则通过获取传入图片LocalMedia对象中的originalImg进行判断原图选择状态、压缩状态；
	      如传入已选图片为空或者不传入已选图片，则原图默认originalImg为false,compressed为true;

##### 3.2主题配置

	  <!--导航栏背景色 默认是黑色-->
          <item name="navigationBarColor">@color/black</item>
	
#### ==========华丽的分割线，原作者Github链接如下==========
##### https://github.com/LuckSiege/PictureSelector

      总结：使用方法和LuckSiege/PictureSelector一样，在功能配置上增加原图选择  在主题配置中改变导航栏颜色使用方式
	
