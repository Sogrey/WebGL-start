---
sidebarDepth: 3
---

# 核心功能


## WebGL着色器内置变量

顶点着色器中的内置变量


|           变量           |  类型   | 描述                                                         |
| :----------------------: | :-----: | ------------------------------------------------------------ |
|        `gl_color`        | `vec4`  | 用来输入的属性表示顶点的主颜色                               |
|      `gl_Secondary`      | `vec4`  | 输入属性表示顶点的辅助颜色                                   |
|       `gl_Normal`        | `vec3`  | 输入属性用来表示顶点的法线值                                 |
|       `gl_Vertex`        | `vec3`  | 输入属性表示 物体控件的顶点位置                              |
|   `gl_MultiTexCoordn`    | `vec4`  | 输入属性表示顶点的第n个纹理坐标                              |
|      `gl_FogCoord`       | `float` | 输入属性表示顶点的雾坐标                                     |
|      `gl_Position`       | `vec4`  | 输入属性变换后的顶点位置（经常用来表示，乘以相应的矩阵后的变换坐标） |
|     `gl_ClipVertex`      | `vec4`  | 输出坐标，用于用户裁剪平面的裁剪                             |
|      `gl_PointSize`      | `float` | 一般用来表示片元点的大小                                     |
|     `gl_FrontColor`      | `vec4`  | 正面主颜色varying输出                                        |
|      `gl_BackColor`      | `vec4`  | 背面主颜色varying输出                                        |
| `gl_FrontSecondaryColor` | `vec4`  | 正面的辅助颜色varying输出                                    |
| `gl_BackSecondaryColor`  | `vec4`  | 背面的辅助颜色varying输出                                    |
|     `gl_TexCoord[]`      | `vec4`  | 纹理坐标的数组varying输出                                    |
|    `gl_FogFragCoord`     | `float` | 雾坐标varying的输出                                          |

片元着色器的内置变量
|        变量         |  类型   | 描述                                                         |
| :-----------------: | :-----: | ------------------------------------------------------------ |
|     `gl_Color`      | `vec4`  | 包含主颜色的插值只读输入                                     |
| `gl_SecondaryColor` | `vec4`  | 包含辅助颜色的插值只读输入属性                               |
|   `gl_TexCoord[]`   | `vec4`  | 包含纹理坐标数组的插值只读输入                               |
|  `gl_FogFragCoord`  | `float` | 包含雾坐标的插值只读输入                                     |
|   `gl_FragCoord`    | `vec4`  | 只读输入属性 窗口的x,y,z和1/w                                |
|  `gl_FrontFacing`   | `bool`  | 只读输入，如果是窗口正面图元的一部分，则这个值为true         |
|   `gl_PointCoord`   | `vec2`  | 点精灵的二维空间坐标范围在(0.0, 0.0)到(1.0, 1.0)之间，仅用于点图元和点精灵开启的情况下。 |
|   `gl_FragData[]`   | `vec4`  | 使用glDrawBuffers输出的数据数组。不能与gl_FragColor结合使用。 |
|   `gl_FragColor`    | `vec4`  | 输出的颜色用于随后的像素操作                                 |
|   `gl_FragDepth`    | `float` | 输出的深度用于随后的像素操作，如果这个值没有被写，则使用固定功能管线的深度值代替 |

## 参考
- [WebGL着色器内置变量总结](https://blog.csdn.net/qq_34862021/article/details/98076495)
- [WebGL着色器内置变量gl_PointSize、gl_Position、gl_FragColor、gl_FragCoord、gl_PointCoord](https://blog.csdn.net/u014291990/article/details/103112914)
