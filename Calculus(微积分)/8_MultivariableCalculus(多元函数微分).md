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
\end{align\*}

&emsp;&emsp;
