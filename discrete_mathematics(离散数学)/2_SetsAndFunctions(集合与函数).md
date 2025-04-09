# 第二章 基本结构：集合、函数、序列、求和和矩阵

## 集合

其他所有的离散结构都建立于集合的基础之上

Any collection of objects is called a set.

集合用于把对象组织在一起。

定义：集合是不同对象的一个无序的聚集，对象也称为集合的元素(element)或成员(member),集合包含(contain)它的元素。\
我们使用 $a\in A$ 来表示a是集合A中的一个元素，记号 $a\notin A$ 表示a不是集合A中的一个元素。

> 通常用大写字母表示集合，而用小写字母表示集合中的元素。

集合的描述方法：

- 花名册方法{a,b,c,d},就是把所有元素穷举
- 用"...",比如{...,-3,-1},适用于那些元素之间规律十分明显的
- 使用集合构造器(set builder)符号{x|P(x)}
- 文氏图

> 值得注意的是，尽管集合常用来聚集具有共同性质的元素，但也不妨碍集合拥有表面上看起来毫不相干的元素，比如{a, 2, Alice}等等

定义：两个集合相等当且仅当它们拥有相同的元素，如果A和B是集合，那么 $\forall x(x\in A\leftrightarrow x\in B)$ ，记为A=B

注意：

- 集合中元素的排列顺序无关紧要(无序性)
- 集合中元素出现不止一次也没关系，{1,2}与{1,2,2}是相同的集合(互异性)

空集：不含任何元素的集合，记为 $\varnothing$ ，也可以记为{ }

单元素集：只含有1个元素的集合。

> 但是我们要区分 $\varnothing$ 和{ $\varnothing$ },前者为空集，而后者为单元素集。

### 文氏图
文氏图是用来描述集合的图表

在文氏图中全集(universal set)U,包含所考虑的全部对象，用矩形框来表示。\
在矩形框内部，圆形或其他几何图形用于表示集合。有时候用点来表示集合中特定的元素。

文氏图常用于表示集合之间的关系。

### 子集

定义：集合A是集合B的子集并且集合B是集合A的超集当且仅当A的每个元素也是B的元素，我们使用 $A\subseteq B$ 表示集合A是集合B的子集。\
另外，如果我们要强调集合B是集合A的超集，我们使用 $B\supseteq A$ (当然这两种表达方式是一致的)

换句话说， $A\subseteq B$ 当且仅当 $\forall x(x\in A\rightarrow x\in B)$ 为真。

对于任意一个集合S，都有下面的定理：\
定理：1） $\varnothing\subseteq S$    2） $S\subseteq S$ 

当我们要强调集合A是集合B的子集但是 $A\neq B$ 时，我们就写成 $A\subset B$ 并说A是B的真子集，也就是说B中有一个元素并不是A中的元素。

A是B的真子集当且仅当 $\forall x(x\in A\rightarrow x\in B)\wedge\exists x(x\in B\wedge x\notin A)$ 

但如果我们要证明两集合相等，我们需要证明 $A\subseteq B$ 和 $B\supseteq A$ 

### 集合的大小

定义：令S为集合。如果S中恰有n个不同元素(distinct elements)，这里n是非负整数，我们就说S为有限集，而n是S的基数(cardinality,也称为势)。S的基数记为|S|

> 基数作为衡量有限集合大小的一个重要常用语

定义：一个集合是无限的，如果它不是有限的(呃。。。。)

### 幂集

定义：给定集合S，S的幂集(power set)是集合S所有子集的集合。S的幂集记为P(S).

> 注意，该集合本身以及空集也是这个幂集中的元素。

> 若|S|=n，则|P(S)|= $2^n$ .

> $x\in P(S)\Rightarrow x\subseteq S$

> $x\in S\Rightarrow \\{x\\}\subseteq P(S)$

> $S\in P(S)$

但我们要注意空集的幂集，

- P( $\varnothing$ )={ $\varnothing$ },但是

- P({ $\varnothing$ })={ $\varnothing$ ,{ $\varnothing$ }},

- P({ $\varnothing$ ,{ $\varnothing$ }})={ $\varnothing$ ,{ $\varnothing$ },{{ $\varnothing$ }},{ $\varnothing$ ,{ $\varnothing$ }}}


$$\begin{align\*}
P(A)\in P(B)\Rightarrow P(A)\subseteq B\\
A\in P(A)\subseteq B\Rightarrow A\in B\\
也就是说，P(A)\in P(B)\Rightarrow A\in B
\end{align\*}$$

我们还有：


```math
A\subseteq B\Rightarrow P(A)\subseteq P(B)
```

### 笛卡尔积

由于集合是无序的，所以我们就需要用一种不同的结构来表示有序的聚集。这就是有序n元组。

定义：有序n元组(ordered n-tuple)( $a_1,a_2,...,a_n$ )是以 $a_1$ 为第一个元素， $a_2$ 为第二个元素，...， $a_n$ 为第n个元素的**有序**聚集。

两个有序n元组相等当且仅当每一对对应的元素都相等。

> 有序二元组也被称为序偶(ordered pairs)。

定义：令A和B为集合。A和B的笛卡尔积(Cartesian product)用 $A\times B$ 表示，是所有序偶(a,b)的集合，其中 $a\in A$ 且 $b\in B$ 。于是

$A\times B=\\{(a,b)|a\in A\wedge b\in B\\}$

注意：

- $\varnothing\times A=A\times\varnothing=\varnothing$

- $A\times B$ 与 $B\times A$ 一般不相等，除非A= $\varnothing$ 或 $B=\varnothing$ 或 $A=B$ 

  

定义：集合 $A_1,A_2,...,A_n$ 的笛卡尔积用 $A_1\times A_2\times...\times A_n$ 来表示，是有序n元组 $(a_1,a_2,...,a_n)$ 的集合，其中 $a_i\in A_i,i=1,2,...,n$ 

$A_1\times A_2\times...\times A_n$ ={ $(a_1,a_2,...,a_n)$ | $a_i\in A_i,i=1,2,...,n$ }

- 值得注意的是，当A，B，C是集合时， $(A\times B)\times C$ 与 $A\times B\times C$ 是不同的，前者是有序二元组，而后者是有序三元组。

  

我们用 $A^2$ 来表示 $A\times A$ ,即集合A与自身的笛卡尔积，更一般地

$A^n=\\{(a_1,a_2,...,a_n)|a_i\in A,i=1,2,...,n\\}$

笛卡尔积 $A\times B$ 的一个子集R被称为从集合A到集合B的关系。从集合A到自身的一个关系称为A上的一个关系。

## 集合运算

实际上，命题演算和集合理论都是布尔代数这一代数系统的实例。集合理论上的操作，是依据与命题演算操作相对应而定义的。

通常我们会有一个全集，而所有集合都假定是全集的子集。

### 引言

定义一：集合A与集合B的并集(Union)，用 $A\cup B$ 来表示，仍是一个集合，包含A或B中或同时在A和B中的元素。

$$\begin{align\*}
A\cup B=\\{x|x\in A \vee x\in B\\}
\end{align\*}$$


- $A\subseteq A\cup B$, $B\subseteq A\cup B$ 

- $A\subseteq C,B\subseteq C\Rightarrow A\cup B\subseteq C$

- $|A\cup B|\leqslant|A|+|B|$

- $A\cup B=B\Leftrightarrow A\subseteq B$

  

定义二：集合A与集合B的交集(Intersection)，用 $A\cap B$ 来表示，是一个集合，它包含同时在A和B中的元素。

$$\begin{align\*}
A\cap B=\\{x|x\in A\wedge x\in B\\}
\end{align\*}$$

- $A\cap B\subseteq A$,     $A\cap B\subseteq B$

- $C\subseteq A,C\subseteq B\Rightarrow C\subseteq A\cap B$

- $|A\cap B|\leqslant|A|$,    $|A\cap B|\leqslant|B|$

- $A\cap B= A\Leftrightarrow A\subseteq B$

  



定义三：两个集合是不相交的，如果他们的交集为空集。

容斥原理： $|A\cup B|=|A|+|B|-|A\cap B|$ 

定义四：集合A和集合B的差集(Difference of A and B)

A-B={ $x|x\in A\wedge x\notin B$ }= $A\cap\overline{B}$ 

定义五：集合A的补集(the complement of a set),用 $\overline{A}$ 来表示，其实就是U-A

定义六：集合A和集合B的对称差(Symmetric difference)

$A\oplus B=(A\bigcup B)-(A\bigcap B)=(A-B)\bigcup(B-A)$

### 集合恒等式

- $A\cap U=A$
- $A\cup\varnothing=A$(恒等律)
- $A\cup U=U$
- $A\cap \varnothing=\varnothing$(支配律)
- $A\cup A=A$
- $A\cap A=A$(幂等律)
- $\overline{(\overline{A})}=A$(补律)
- $A\cup B=B\cup A$
- $A\cap B=B\cap A$(交换律)
- $A\cup(B\cup C)=(A\cup B)\cup C$
- $A\cap(B\cap C)=(A\cap B)\cap C$(结合律)
- $A\cup(B\cap C)=(A\cup B)\cap(A\cup C)$
- $A\cap(B\cup C)=(A\cap B)\cup(A\cap C)$(分配律)
- $\overline{A\cap B}=\overline{A}\cup\overline{B}$
- $\overline{A\cup B}=\overline{A}\cap\overline{B}$(德摩根律)
- $A\cup(A\cap B)=A$
- $A\cap(A\cup B)=A$(吸收律)
- $A\cup\overline{A}=U$
- $A\cap\overline{A}=\varnothing$(互补律)

## 函数

### 引言

定义：令A和B为非空集合。从A到B的函数f是对元素的一种指派，对A的每个元素恰好指派B的一个元素。如果B中元素b是唯一由函数f指派给A中元素a的，则我们就写成f(a)=b。如果f是从A到B的函数，就记为 $A\rightarrow B$ 。

函数f: $A\rightarrow B$ 也能从A到B的关系( $A\times B$ 的子集)来定义(用序偶(a,b)去定义f(a)=b)。

> 函数有时也被称为映射(mapping)或者变换(transformation)。

定义：如果f是从A到B的函数，我们说A是f的定义域(domain),而B是f的陪域(codomain) 。如果f(a)=b，我们说b是a的像(image)，而a是b的原像(preimage)。f的值域(range)或像是A中元素所有像的集合。如果f是从A到B的函数，我们说f把A映射到B。



> 注意区分陪域与值域，实际上值域是陪域的子集。

定义函数的时候，我们需要指定它的定义域、陪域、定义域中元素到陪域的映射。当两个函数的这三个因素相同时，我们称这两个函数是相等的。

如果一个函数的陪域是实数集合，那么该函数称为实值函数。如果其陪域为整数集合，那么该函数称为整数值函数。具有相同定义域的两个实值函数或两个整数值函数可以相加和相乘。

定义：令 $f_1,f_2$ 是从A到R的函数，那么 $f_1+f_2,f_1f_2$ 也是从A到R的函数

$$\begin{align\*}
\forall x\in A\\
(f_1+f_2)(x)=f_1(x)+f_2(x)\\
(f_1f_2)(x)=f_1(x)f_2(x)
\end{align\*}$$

### 一对一函数和映上函数

定义：若对于函数f的定义域中所有的a和b都有f(a)=f(b)蕴含a=b，则称该函数f(x)为一对一(one-to-one)函数或者单射(injection)函数。

换句话说，像只对应一个原像。

$\forall x\forall y(f(x)=f(y)\rightarrow x=y)$

$\forall x\forall y(x\neq y\rightarrow f(x)\neq f(y))$

定义：递增/严格递增/递减/严格递减/

定义：若对函数f的陪域中任意元素b都有元素a使得f(a)=b，则称该函数f为映上(onto)函数或满射(surjection)函数

定义：既是单射函数又是满射函数的函数为双射(bijection)函数或一一对应(one-to-one correspondence)函数。此时两集合具有相同的基数(势)。

假设f: $A\rightarrow B$ 

要证明f是单射的： $\forall x,y\in A,如果f(x)=f(y),则x=y$ 

要证明f不是单射的：找到特定的 $x,y\in A$ 使得 $x\neq y$ 且 $f(x)= f(y)$ 

要证明f是满射的：考虑 $\forall y\in B$ ,并找到一个元素 $x\in A$ 使得f(x)=y

要证明f不是满射的：找到一个特定的 $y\in B$ ,使得对于任意 $x\in A$ 有f(x) $\neq y$ 



### 反函数和函数合成

定义：令f为从集合A到集合B的双射函数。f的反函数指派给B中的元素b是A中使得f(a)=b唯一元素a。f的反函数用 $f^{-1}$ 来表示。

只有双射函数才能有逆函数(也被称为是可逆的)。

定义：(函数的合成)令g为集合A到集合B的函数，f是从集合B到集合C的函数，函数f和g的合成(composition)记作f $\circ$ g。定义为对任意A中的元素a，有(f $\circ$ g)(a)=f(g(a))。



### 函数的图

函数f的图像其实是序偶集合(笛卡尔积 $A\times B$ 的子集)

$\\{(a,b)|a\in A\ and\ f(a)=b\\}$

### 一些重要的函数

一、低函数：

低函数指派给实数x的是小于或等于x的最大整数，用 $\lfloor x\rfloor$ 来表示(其实就是下取整函数(floor))。

二、顶函数

顶函数指派给实数x的是大于或等于x的最小整数，用 $\lceil x\rceil$ (其实就是上取整(ceiling)函数)

- $x-1<\lfloor x\rfloor\leqslant x\leqslant\lceil x\rceil x+1$
- $\lfloor -x\rfloor=-\lceil x\rceil$
- $\lceil -x\rceil=-\lfloor x\rfloor$
- $\lfloor x+m\rfloor=\lfloor x\rfloor+m$ 当m是整数时
- $\lceil x+m\rceil=\lceil x\rceil+m$ 当m是整数时

## 集合的基数

### 引言

定义：集合A和集合B有相同的基数(cardinality)，当且仅当存在从A到B的一个一一对应。当A和B有相同的基数时，就写成|A|=|B|。

对于无限集，基数的定义提供了一个衡量两个集合相对大小的方法，而不是衡量一个集合大小的办法。

例：设区间(a,b)中含有实数的集合记为集合A，区间(0,1)中含有的实数集合记为集合B，证明集合A,B具有相同的基数。

$$\begin{align\*}
令f(x)=\frac{x-a}{b-a},x\in(a,b)\\
显然f(x)是一个从集合(a,b)到集合(0,1)的双射函数\\
故两集合具有相同的基数
\end{align\*}$$


定义：如果存在一个从A到B的一对一函数，则A的基数小于或等于B的基数，并写成|A| $\leqslant$ |B|。再者，当|A| $\leqslant$ |B|并且A和B有不同的基数时，我们说A的基数小于B的基数。

### 可数集合

定义：一个集合或者是有限集或者与自然数集具有相同的基数，这个集合就称为可数的。一个集合不是可数的，就称为不可数的。(如果该集合与自然数集具有相同的基数，我们称其为无限可数的)

可数分为两种情况，一是有限可数，二是无限可数。

如果我们要证明一个集合是无限可数的，那么我们必须给出一个该集合与正整数集合之间的一一映射，在这之中，该集合可以做定义域，也可以做陪域。

我们记自然数集合的势为 $\aleph_0$ 。

一些无穷可数的集合：

- 整数集合Z
- 正偶数集合E
- 正有理数集合 $Q^+$ 

1.整数集合Z

$$\begin{align\*}
Z=\{0,-1,1,-2,2,...\}\\
f(i)=
\begin{cases}
2|i|\\;\\;\\;i<0\\
1\\;\\;\\;i=0\\
2|i|+1\\;\\;\\;i>0\\
\end{cases}\\
f是一个从集合Z到集合N的双射函数\\
故Z是一个无限可数的集合
\end{align\*}$$

2.正偶数集合E

$$\begin{align\*}
E=\{2n|n\in N\}\\
f(x)=2x\\;\\;\\;x\in N\\
f是一个从集合N到集合E的一个双射\\
故集合E是一个无限可数的集合\\
同理可得正奇数集合也是一个无限可数集合
\end{align\*}$$

- 值得注意的是，尽管正偶数集合是自然数集合的真子集，但是正偶数集合与自然数集合的势是相同的。

3.正有理数集合 $Q^+$ 

$$\begin{align\*}
\forall x\in Q^+,x=\frac{q}{p}\\;\\;p,q\in N且互质\\
令集合S=\\{(p,q)|p,q\in N\\}=N\times N\\
令函数f(x)=f(\frac{q}{p})=(p,q)\\;\\;x\in Q^+\\
显然f是一个从Q^+到S的单射函数,故|Q^+|\leqslant|S|\\
\begin{matrix}
(1,1)&(1,2)&(1,3)&...&(1,q)&...\\
(2,1)&(2,2)&(2,3)&...&(2,q)&...\\
(3,1)&(3,2)&(3,3)&...&(3,q)&...\\
...\\
(p,1)&(p,2)&(p,3)&...&(p,q)&...\\
...
\end{matrix}\\
对于上面的矩阵，我们以对角线顺序向自然数集对应\\
(1,1)对应1，(1,2)对应2，(2,1)对应3...以此类推\\
令g(x)=g((p,q))=\frac{(p+q-2)(p+q-1)}{2}+p\\;\\;\\;x\in S\\
g是一个从S到N的满射函数,故|S|=|N|\\
又因为N\subseteq Q^+,故|N|\leqslant|Q^+|\\
综上有|N|=|Q^+|
\end{align\*}$$

- 有理数集合Q也是无限可数的。

无限可数集合的性质：

- 不存在一个无限集合比一个可数集合的基数还小
- 两个可数集合的并还是可数的。
- 有限个可数集合的并还是可数的。
- 可数的可数集合的并还是可数的。

康托尔对角化论证：

定理：在0和1之间的实数集合是不可数的。

$$\begin{align\*}
A=\{x|x\in(0,1)\wedge x\in R\}\\
B=\{\frac{1}{n+1}|n\in N\}\\
显然|N|=|B|，B\subseteq A\\
所以|N|\leqslant|A|\\
假设集合A是无限可数的，A=\{r_1,r_2,...,r_n,...\}\\
将A中的每个数都已十进制的形式表示出来：\\
比如\frac{1}{3}=0.3333333...,\frac{1}{2}=0.50000...\\
r_1=0.d_{11}d_{12}d_{13}d_{14}d_{15}d_{16}d_{17}...\\
r_2=0.d_{21}d_{22}d_{23}d_{24}d_{25}d_{26}d_{27}...\\
r_1=0.d_{31}d_{32}d_{33}d_{34}d_{35}d_{36}d_{37}...\\
...\\
现在我们构造一个实数x=0.x_1x_2x_3x_4x_5x_6...\\
如果d_{ii}\neq 3,x_i=3\\
如果d_{ii}=3,x_i=4\\
我们发现x不同于集合A中的任意一个元素\\
但x确实属于区间(0,1)之间，说明假设错误\\
即集合A是无限不可数的，并且|N|<|A|\\
\end{align\*}$$


定理：从负无穷大到正无穷大区间的实数个数在0和1之间的实数个数的基数是相同的。

> 提示：使用f(x)= $\frac{2tanx}\pi$ 来证明。

例：证明集合[0,1]的势为 $\aleph$ 。

$$\begin{align\*}
A=[0,1],B=(0,1)\\
故B\subseteq A,则有|B|\leqslant|A|\\
令g(x)=\frac{1}{2}x+\frac{1}{4}\\;\\;\\;x\in [0,1]\\
g是一个从[0,1]到[\frac{1}{4},\frac{3}{4}]的双射函数\\
所以|A|\leqslant|B|\\
综上|A|=|B|
\end{align\*}$$


我们记实数集合R的势为 $\aleph$ 。

连续性假设：不存在一个基数a，使得 $\aleph_0<a<\aleph$ 


