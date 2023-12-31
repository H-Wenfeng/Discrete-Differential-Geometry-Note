## Centeral Theme: 
- link the mathematically (differential geometry) and computationally (geometry processing)
- Discrete surfaces
- Exterior calculus
- Curvature
- Smoothing
- Parameterization
- Distance computation
- Direction Field Design
## Curvature?
- 曲率（curvature）是描述曲线或曲面弯曲程度的属性。对于曲线，曲率可以表示为曲线上某一点处的曲率半径的倒数。对于曲面，曲率可以表示为曲面上某一点处的主曲率的平均值或高斯曲率。如果我们将曲线或曲面的曲率函数关于弧长（对于曲线）或面积（对于曲面）进行积分，我们可以获得相应曲线或曲面的长度或表面积。当我们对曲线或曲面的曲率函数进行积分时，我们积累了曲率的变化。曲率的正负号告诉我们曲线的凸凹性，而曲率的绝对值告诉我们曲线的弯曲程度。 
- 对于曲线而言，通过积分曲率函数，我们可以计算曲线的总转角。当曲线是闭合的（形成一个环），总转角将与曲线围绕其内部孔的次数有关。这是由于当曲线绕着内部孔穿过时，曲率的正负号发生变化，对积分结果产生影响。因此，通过对曲线的曲率进行积分，我们可以获得曲线围绕孔的次数，从而得知曲线的拓扑特征。
 - 对于曲面而言，通过积分高斯曲率函数（或主曲率函数），我们可以计算曲面的总曲率量。对于封闭曲面，总曲率量与曲面包围的空间中孔的数量有关。这是因为曲面上的正曲率和负曲率区域的数量与孔的数量相对应。因此，通过对曲面的曲率函数进行积分，我们可以获得曲面的总曲率量，从而推断出曲面围绕孔的数量。

## 曲率不是单一的概念
![[./image/Pasted image 20230709104542.png]]
### 切线视角
- 曲率可以是切线的二阶导
- 而切线变化的方向在法向量方向
- 切线的变化有正负性
- 然而在离散微分几何情况下，切线的二阶导可能为0或∞
![[./image/Pasted image 20230710154408.png]]
![[Pasted image 20230709104704.png]]

### 角度变化视角

- 曲率变化实际上是角度变化
![[./image/Pasted image 20230710155444.png]]


### 长度变化视角
- The fastest way to decrease the length of a curve is to move it  in the normal direction, with speed proportional to curvature.
- 曲率越大处，延长越快

![[./image/Pasted image 20230710155632.png]]
- 斯坦纳公式
![[./image/Pasted image 20230710155923.png]]

### 圆的近似视角
- 三点确定一圆
- 微观视角下三点可确定该圆，近似曲线曲率
![[./image/Pasted image 20230710160046.png]]
![[./image/Pasted image 20230710160210.png]]

## No Free Lunch
![[./image/Pasted image 20230710160359.png]]
平滑曲线情况下,满足以下三点

- TOTAL: 总曲率在整个流动过程中保持不变。
	- 在离散微分几何中使用等弧长参数化（equi-length parameterization）
- DRIFT: 质心不会从原点漂移。
	- 在离散微分几何中使用等质量分布的情况。
- ROUND: 在重新缩放后，对于圆形曲线来说，流动是静止的。
	- 采用等角度参数化时，数据点之间的夹角相等，因此曲线的参数对应于曲线上每个数据点处的夹角。由于每个数据点之间的夹角相等，曲线的曲率分布在整个曲线上保持一致，从而导致重新缩放后的曲线形状接近圆形。

但在离散情况下，只能同时满足其中一点

这三个观点中，TOTAL 和 DRIFT 表明整体的性质保持不变，而 ROUND 则表示局部的性质保持不变。如果这三个性质同时存在，即总曲率保持不变、质心不漂移，且曲线在重新缩放后保持静止，那么曲线或曲面的形状就会受到限制，只能是圆形。
如果曲线或曲面是圆形，那么根据ROUND的观点，流动将保持静止。但在这种情况下，TOTAL的观点将无法满足，因为总曲率在流动过程中会发生变化。同样，如果我们想要TOTAL的观点成立，即总曲率保持不变，那么曲线或曲面将无法是圆形，因此ROUND的观点将无法满足。