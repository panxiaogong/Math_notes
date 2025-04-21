# 第八章 多元函数微分学及其应用
## 微分法在几何上的应用

### 空间曲线的切线和法平面
&emsp;&emsp;设空间曲线 $\Gamma$ 的参数方程为(假定这三个函数均可导)

$$\begin{align\*}
\begin{cases}
x=\varphi(t)\\
y=\psi(t)\\
z=\omega(t)\\
\end{cases}
\end{align\*}$$

&emsp;&emsp;我们在曲线 $\Gamma$ 上取一点 $M(x_0,y_0,z_0)$ ，其中 $x_0=\varphi(t_0)$ , $y_0=\psi(t_0)$ , $z=\omega(t_0)$ ，也就是说它对应于参数t= $t_0$ ，我们再取另外一点t= $t_0+\Delta t$ ,
我们就得到了一点 $N(\varphi(t_0+\Delta t),\psi(t_0+\Delta t),\omega(t_0+\Delta t))$ ，显然我们会有

$$\begin{align\*}
\Delta x=\varphi(t_0+\Delta t)-\varphi(t_0)\\
\Delta y=\psi(t_0+\Delta t)-\psi(t_0)\\
\Delta z=\omega(t_0+\Delta t)-\omega(t_0)\\
\end{align\*}$$

&emsp;&emsp;或者说点 $N坐标为(x+\Delta x,y+\Delta y,z+\Delta z)$ ，于是我们就能得到割线MN的方向向量 $(\Delta x,\Delta y,\Delta z)$ ，故割线MN的方程为

$$\begin{align\*}
\frac{x-x_0}{\Delta x}=\frac{y-y_0}{\Delta y}=\frac{z-z_0}{\Delta z}\\
\end{align\*}$$

&emsp;&emsp;当点N沿曲线 $\Gamma$ 趋近于点M时，我们其实会有 $\Delta t\rightarrow 0$ ，此时割线MN的极限位置MN'就是曲线 $\Gamma$ 在点M处的切线。
但我们仅靠上式不能计算出什么，我们做如下的操作：

$$\begin{align\*}
\frac{x-x_0}{\frac{\Delta x}{\Delta t}}=\frac{y-y_0}{\frac{\Delta y}{\Delta t}}=\frac{z-z_0}{\frac{\Delta z}{\Delta t}}\\
\end{align\*}$$

&emsp;&emsp;我们发现：

$$\begin{align\*}
\lim\limits_{\Delta t\to0}\frac{\Delta x}{\Delta t}=\lim\limits_{\Delta t\to0}\frac{\varphi(t_0+\Delta t)-\varphi(t_0)}{\Delta t}=\varphi'(t_0)\\
\lim\limits_{\Delta t\to0}\frac{\Delta y}{\Delta t}=\lim\limits_{\Delta t\to0}\frac{\psi(t_0+\Delta t)-\psi(t_0)}{\Delta t}=\psi'(t_0)\\
\lim\limits_{\Delta t\to0}\frac{\Delta z}{\Delta t}=\lim\limits_{\Delta t\to0}\frac{\omega(t_0+\Delta t)-\omega(t_0)}{\Delta t}=\omega'(t_0)\\
\end{align\*}$$

&emsp;&emsp;于是，切线的方程为(假定 $\varphi'(t_0)$ , $\psi'(t_0)$ , $\omega'(t_0)$ 不全为零) ：

$$\begin{align\*}
\frac{x-x_0}{\varphi'(t_0)}=\frac{y-y_0}{\psi'(t_0)}=\frac{z-z_0}{\omega'(t_0)}\\
\end{align\*}$$

&emsp;&emsp;这里**T**=( $\varphi'(t_0)$ , $\psi'(t_0)$ , $\omega'(t_0)$ )是该点切线的方向向量，也被称为曲线 $\Gamma$ 在点M处的**切向量**。

&emsp;&emsp;通过点M并与切线垂直的平面称之为**法平面**，故**切向量T**就是此处法平面的法向量，所以曲线 $\Gamma$ 在点M处的法平面方程为：

$$\begin{align\*}
\varphi'(t_0)(x-x_0)+\psi'(t_0)(y-y_0)+\omega'(t_0)(z-z_0)=0\\
\end{align\*}$$

&emsp;&emsp;实际上，给出曲线的参数方程是最简单的一种情形，下面我们来看一种稍微复杂些的：

&emsp;&emsp;下面我们有(其实此曲线是两柱面的交线，体会一下)：

$$\begin{align\*}
\begin{cases}
y=\psi(x)\\
z=\omega(x)\\
\end{cases}
\end{align\*}$$

&emsp;&emsp;其实这与刚才的参数方程差不了多少，我们依然会得到下面的式子：

$$\begin{align\*}
\frac{x-x_0}{\Delta x}=\frac{y-y_0}{\Delta y}=\frac{z-z_0}{\Delta z}\\
\end{align\*}$$

&emsp;&emsp;我们进行相似的操作：

$$\begin{align\*}
\frac{x-x_0}{\frac{\Delta x}{\Delta x}}=\frac{y-y_0}{\frac{\Delta y}{\Delta x}}=\frac{z-z_0}{\frac{\Delta z}{\Delta x}}\\
\end{align\*}$$

&emsp;&emsp;我们同样会有：

$$\begin{align\*}
\lim\limits_{\Delta x\to0}\frac{\Delta y}{\Delta x}=\lim\limits_{\Delta x\to0}\frac{\psi(x_0+\Delta x)-\psi(x_0)}{\Delta x}=\psi'(x_0)\\
\lim\limits_{\Delta x\to0}\frac{\Delta z}{\Delta x}=\lim\limits_{\Delta x\to0}\frac{\omega(x_0+\Delta x)-\omega(x_0)}{\Delta x}=\omega'(x_0)\\
\end{align\*}$$

&emsp;&emsp;我们就能得到曲线在点 $(x_0,y_0,z_0)$ 的切向量为 $(1,\psi'(x_0),\omega'(x_0)$ ,故切线方程和法平面方程如下：

$$\begin{align\*}
\frac{x-x_0}{1}=\frac{y-y_0}{\psi'(x_0)}=\frac{z-z_0}{\omega'(x_0)}\\
(x-x_0)+\psi'(x_0)(y-y_0)+\omega'(x_0)(z-z_0)=0\\
\end{align\*}$$

&emsp;&emsp;接下来就是最复杂的情况了：

&emsp;&emsp;如果空间曲线 $\Gamma$ 为：

$$\begin{align\*}
\begin{cases}
F(x,y,z)=0\\
G(x,y,z)=0\\
\end{cases}
\end{align\*}$$

&emsp;&emsp;我们把y,x看作是x的函数(至于为什么一会再说)， $y=\psi(x),z=\omega(x)$ ,对隐函数两边同时求偏导，可得：

$$\begin{align\*}
\begin{cases}
\frac{\partial F}{\partial x}+\frac{\partial F}{\partial y}\frac{dy}{dx}+\frac{\partial F}{\partial z}\frac{dz}{dx}=0\\
\frac{\partial G}{\partial x}+\frac{\partial G}{\partial y}\frac{dy}{dx}+\frac{\partial G}{\partial z}\frac{dz}{dx}=0
\end{cases}
\end{align\*}$$

> 个人理解，对于每个确定的x值，其实都确定了一个未知量是y，z的方程组，两个方程，两个未知数，所以一定能够把两个未知数解出来。换句话说，真正自由的变量是x，而y和z都随着x的确定而确定，
> 所以我们说y和z分别是关于x的函数。

&emsp;&emsp;即：

$$\begin{align\*}
\begin{cases}
F_y'\psi'(x)+F_z'\omega'(x)=-F_x'\\
G_y'\psi'(x)+G_z'\omega'(x)=-G_z'
\end{cases}
\end{align\*}$$

&emsp;&emsp;我们将点M $(x_0,y_0,x_0)$ 代入，就获得了上述关于 $\psi'(x),\omega'(x)$ 的二元一次方程组(因为此时F或G对于x,y,z的偏导数都确定了，即方程的系数都已知了）

&emsp;&emsp;根据线性代数的知识(尽管我在写这里时还没有开始更新线性代数的笔记)

$$\begin{align\*}
\psi'(x_0) = \frac{
\begin{vmatrix}
-F'_x & F'_z \\
-G'_x & G'_z
\end{vmatrix}_M
}{
\begin{vmatrix}
F'_y & F'_z \\
G'_y & G'_z
\end{vmatrix}_M
}=\frac{
-\begin{vmatrix}
F'_x & F'_z \\
G'_x & G'_z
\end{vmatrix}_M
}{
\begin{vmatrix}
F'_y & F'_z \\
G'_y & G'_z
\end{vmatrix}_M
}=\frac{
\begin{vmatrix}
F'_z & F'_x \\
G'_z & G'_x
\end{vmatrix}_M
}{
\begin{vmatrix}
F'_y & F'_z \\
G'_y & G'_z
\end{vmatrix}_M
}\\
\omega'(x_0)=\frac{
\begin{vmatrix}
F'_y & -F'_x \\
G'_y & -G'_x
\end{vmatrix}_M
}{
\begin{vmatrix}
F'_y & F'_z \\
G'_y & G'_z
\end{vmatrix}_M
}=\frac{
\begin{vmatrix}
F'_x & F'_y \\
G'_x & G'_y
\end{vmatrix}_M
}{
\begin{vmatrix}
F'_y & F'_z \\
G'_y & G'_z
\end{vmatrix}_M
}
\end{align\*}$$

&emsp;&emsp;故曲线在点M处的切向量为 $(1,\psi'(x_0),\omega'(x_0))$ 或：

$$\begin{align\*}
T=\Bigg(\begin{vmatrix}
F'_y & F'_z \\
G'_y & G'_z
\end{vmatrix}_M,
\begin{vmatrix}
F'_z & F'_x \\
G'_z & G'_x
\end{vmatrix}_M,
\begin{vmatrix}
F'_x & F'_y \\
G'_x & G'_y
\end{vmatrix}_M\Bigg)
\end{align\*}$$

&emsp;&emsp;所以曲线在该点的切线方程为

$$\begin{align\*}
\frac{x-x_0}
{\begin{vmatrix}
F'_y & F'_z \\
G'_y & G'_z
\end{vmatrix}_M}=
\frac{y-y_0}
{\begin{vmatrix}
F'_z & F'_x \\
G'_z & G'_x
\end{vmatrix}_M}=
\frac{z-z_0}
{\begin{vmatrix}
F'_x & F'_y \\
G'_x & G'_y
\end{vmatrix}_M}
\end{align\*}$$

&emsp;&emsp;法平面方程为

$$\begin{align\*}
\begin{vmatrix}
F'_y & F'_z \\
G'_y & G'_z
\end{vmatrix}_M(x-x_0)+
\begin{vmatrix}
F'_z & F'_x \\
G'_z & G'_x
\end{vmatrix}_M(y-y_0)+
\begin{vmatrix}
F'_x & F'_y \\
G'_x & G'_y
\end{vmatrix}_M(z-z_0)=0
\end{align\*}$$


### 空间曲面的切平面和法线

设空间曲面的方程为 $F(x,y,z)=0$ ， $M(x_0,y_0,z_0)$ 是曲面上一点，设函数F(x,y,x)在该点有连续的偏导数，且同时不为0，我们在曲面上任取一条过点 $M(x_0,y_0,z_0)$ 的曲线 $\Gamma$ ，设曲线 $\Gamma$ 的参数方程为 $x=\varphi(t),y=\psi(t),z=\omega(t)$ ，易知曲线 $\Gamma$ 在点M处的切向量为( $\varphi'(t_0)$ , $\psi'(t_0)$ , $\omega'(t_0)$ )，又因为

$$\begin{align\*}
F\[\varphi(t),\psi(t),\omega(t)\]\equiv0
\end{align\*}$$

&emsp;&emsp;上式两边对 $t=t_0$ 求全导数，有

$$\begin{align\*}
F_x'(x_0,y_0,z_0)\varphi'(t_0)+F_y'(x_0,y_0,z_0)\psi'(t_0)+F_z'(x_0,y_0,z_0)\omega'(t_0)=0
\end{align\*}$$

&emsp;&emsp;如果我们令向量 $n$ 为：

$$\begin{align\*}
(F_x'(x_0,y_0,z_0),F_y'(x_0,y_0,z_0),F_z'(x_0,y_0,z_0))
\end{align\*}$$

&emsp;&emsp;那么就会有向量 $n$ 与切向量垂直（这也是个人觉得非常巧妙的一个推导）。我们以向量 $n$ 为法向量，过点M做平面，则曲线 $\Gamma$ 在点M处的切线在此平面上。

&emsp;&emsp;而在我们刚才的讨论过程中，曲线 $\Gamma$ 是任取的，所以：曲面上所有通过点M的曲线，在点M处的切线都在同一平面上。该平面称为曲面在点M处的切平面。方程为：

$$\begin{align\*}
F_x'(x_0,y_0,z_0)(x-x_0)+F_y'(x_0,y_0,z_0)(y-y_0)+F_z'(x_0,y_0,z_0)(z-z_0)=0
\end{align\*}$$

&emsp;&emsp;过点M且垂直于曲面在点M处切平面的直线称为曲面在点M处的法线，其方程为：

$$\begin{align\*}
\frac{x-x_0}{F_x'(x_0,y_0,z_0)}=\frac{y-y_0}{F_y'(x_0,y_0,z_0)}=\frac{z-z_0}{F_z'(x_0,y_0,z_0)}
\end{align\*}$$

&emsp;&emsp;垂直于切平面的向量称为法向量，故向量 $n$ 就是一个法向量。

&emsp;&emsp;另外，当曲面由显式方程 $z=f(x,y)$ 给出时,我们可以做如下操作：

$$\begin{align\*}
F(x,y,z)=f(x,y)-z
\end{align\*}$$

&emsp;&emsp;所以我们能得到切平面的法向量为 $(f_x'(x,y),f_y'(x,y),-1)$ 。

### 习题：

&emsp;&emsp;1.设函数 $f(x,y)$ 在点(0,0)附近有定义，且 $f_x'(0,0)=3,f_y'(0,0)=1$ ,则：\
&emsp;&emsp;A. $dz|_{(0,0)}=3dx+dy$ \
&emsp;&emsp;B.曲 $z=f(x,y)$ 在点(0,0)处的法向量为(3,1,1)\
&emsp;&emsp;C.曲线 $z=f(x,y),y=0$ 在点(0,0)处的切向量为(1,0,3)\
&emsp;&emsp;D.曲线 $z=f(x,y),y=0$ 在点(0,0)处的切向量为(3,0,1)

&emsp;&emsp;分析：偏导数存在且连续才能保证函数可微，故A错误；曲线方程由 $z=f(x,y)$ 显式给出，所以法向量为(3,1,-1)，故B错误。对于C，曲线 $z=f(x,y),y=0$ 其实就是曲面 $f(x,y)$ 与平面 $y=0$ 的交线，所以曲线 $z=f(x,y),y=0$ 在点(0,0)处的切线其实就在平面 $xOz$ 内，我们类比之前推导过的操作，应有如下的等式：

$$\begin{align\*}
\frac{x-0}{\Delta x}=\frac{z-0}{\Delta z}\Rightarrow\frac{x-0}{\frac{\Delta x}{\Delta x}}=\frac{z-0}{\frac{\Delta z}{\Delta x}}\Rightarrow\frac{x-0}{1}=\frac{z-0}{f_x'(0,0)} \\
\end{align\*}$$

&emsp;&emsp;故曲线 $z=f(x,y),y=0$ 在点(0,0)处的切向量为(1,0,3)，C正确

&emsp;&emsp;2.试证曲面 $z=xf(\frac{y}{x})$ 上任意一点处的切平面都过原点。





