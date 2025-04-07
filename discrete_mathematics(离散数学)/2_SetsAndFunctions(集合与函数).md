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

> $x\in S\Rightarrow x\subseteq P(S)$

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

- 值得注意的是，当A，B，C是集合时， $(A\times B)\times C$ 与 $A\times B\times C$ 是不同的。

  

我们用 $A^2$ 来表示 $A\times A$ ,即集合A与自身的笛卡尔积，更一般地

$A^n=\\{(a_1,a_2,...,a_n)|a_i\in A,i=1,2,...,n\\}$

笛卡尔积 $A\times B$ 的一个子集R被称为从集合A到集合B的关系。从集合A到自身的一个关系称为A上的一个关系。
