# OpenglModel

Minecraft  Skin Display Model
The drawing of the cube requires 12 triangles.


# Triangular loci are determined from the texture
``` java
/*
uv                      [my]

    [tb1] [tb2] [t1]
      a--L--b--L--c      [1]
      |    /|\    |
	  w  A  w  B  w
	  |/    |    \|
	  a--L--b--L--c      [2]
  a-W-b--L--c-W-d--L--e  [3] 
  |\  |    /|\  |\    |
  h C h  D  h E h  F  h
  |  \|/    |  \|    \|
  a-W-b--L--c-W-d--L--e  [4]

[mx][tb1] [tb2][b1]  [b2]

	 
	 //F
	 B2 / 64f, H2 / 64f, B2 / 64f, H1 / 64f, B1 / 64f, H1 / 64f
	 , B1 / 64f, H1 / 64f, B1 / 64f, H2 / 64f, B2 / 64f, H2 / 64f
	 //D
	 , TB1 / 64f, H2 / 64f, TB2 / 64f, H2 / 64f, TB2 / 64f, H1 / 64f
	 , TB2 / 64f, H1 / 64f, TB1 / 64f, H1 / 64f, TB1 / 64f, H2 / 64f
	 //B
	 , TB2 / 64f, mY / 64f, T1 / 64f, mY / 64f, T1 / 64f, H1 / 64f
	 , T1 / 64f, H1 / 64f, TB2 / 64f, H1 / 64f, TB2 / 64f, mY / 64f
	 //E
	 , B1 / 64f, H2 / 64f, B1 / 64f, H1 / 64f, TB2 / 64f, H1 / 64f
	 , TB2 / 64f, H1 / 64f, TB2 / 64f, H2 / 64f, B1 / 64f, H2 / 64f
	 //A
	 , TB2 / 64f, mY / 64f, TB1 / 64f, mY / 64f, TB1 / 64f, H1 / 64f
	 , TB1 / 64f, H1 / 64f, TB2 / 64f, H1 / 64f, TB2 / 64f, mY / 64f
	 //C
	 ,  mX / 64f, H1 / 64f,  mX / 64f, H2 / 64f, TB1 / 64f, H2 / 64f
	 , TB1 / 64f, H2 / 64f, TB1 / 64f, H1 / 64f,  mX / 64f, H1 / 64f
	 

*/
```
# How to use
``` java
ModelRender.java
 void DrawFrameStart();
 
public static float[] BuildModel(
		Pointer model/*模型 后 左上 点 */
		, float mLength, float mWidth, float mHeight/*长 宽 高 */
		, Pointer source/*旋转点*/
		, float degree,float off)/*角度*/
```
# Adjust as needed
``` java
model = JSON.parseObject(Rocker.getJsonFromAssets(context,"other"), FastModel.class);
```


