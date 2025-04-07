# 第一章 基础:逻辑和证明

## 命题逻辑

### 命题

命题(proposition)是逻辑的基本构件，是一个只能或真或假，而不能既真又假的陈述语句(a declarative sentence that is either true or false, but not both)

> 对于大部分语句，我们是极其容易判断的。比如说“几点了？”“仔细读这个”之类的疑问句或者是祈使句显然就不是命题，而所谓“x+1=2”之类的语句也并不是命题，因为它既不为真，也不为假，再难一些，"This statement is false(这句话是假的)"这个语句也依然不是个命题，因为它既不能是真，也不能是假。
>
> 但是有一些奇怪语句，虽然看上去不合理，但却是一个命题，比如“我吃了一百粒米”，这个语句要么为真要么为假，它确实是一个命题。

我们习惯上用字母p,q,r,s,...来表示命题变量(propositional variables)(语句变量sentential variables)，即表示命题的变量。

如果一个命题是真命题，则他的真值(truth value)为真，用T表示，反之则真值为假，用F表示。

另外，不能用简单命题来表示的命题称为原子命题(atomic proposition)，换句话说，原子命题不能被分解为更简单的陈述句。
由已知命题用逻辑运算符(logic operators)组合而来的新命题被称为复合命题(compound propositions)。

> 涉及命题的逻辑领域称为命题演算(propositional calculus)或命题逻辑(propositional logic)

#### 否定(Negation)

令p为一命题，则p的否定记作 $\neg p$ ，指“不是p所指的情形”，p的否定与p的真值相反。(NOT)

> 否定运算符的记号并没有统一的标准，只是" $\neg$ "比较常用而已

命题的否定也可以看作否定运算符(negation operator)作用在命题上的结果。

#### 合取(Conjunction)

令p,q为命题，p,q的合取即命题“p并且q”，记作“ $p\wedge q$ ”，当p,q皆为真命题时， $p\wedge q$ 为真，否则为假。(AND)

#### 析取(Disjunction)

令p,q为命题，p,q的析取即命题"p或q"，记作" $p\vee q$ "，当p,q皆为假命题时，p $\vee$ q为假,否则为真(Inclusive or,兼或,也叫同或)(OR)

#### 异或(Exclusive or)

令p,q为命题，p,q的异或(记作 $p\oplus q$ )是这样的一个命题：当p,q中恰好有一个为真时命题为真，否则为假。

换句话说,命题p,q的真值相同则为假(0)，真值不同则为真(1)。

|  p   |  q   | $p\oplus q$ |
| :--: | :--: | :---------: |
|  T   |  T   |      F      |
|  T   |  F   |      T      |
|  F   |  T   |      T      |
|  F   |  F   |      F      |



> 联想到异或运算，其实是同一个概念，二进制位相同则为0，二进制位不同则为1。

### 条件语句(Conditional Statements)

令p,q为命题，条件语句 $p\rightarrow q$ 是命题“如果p，则q”，当p为真而q为假时，条件语句 $p\rightarrow q$ 为假，否则为真。在条件语句中，p称为假设(hypothesis)(前件antecedent，前提premise)，q称为结论(conclusion)(后件consequence)。而条件语句也被称为“蕴含(implication)”。

| $p$  | $q$  | $p\rightarrow q$ |
| :--: | :--: | :--------------: |
|  T   |  T   |        T         |
|  T   |  F   |        F         |
|  F   |  T   |        T         |
|  F   |  F   |        T         |

实际上,我们还会碰到几个比较常用的条件语句表达方式:

- 如果p，则q。(if p, then q.)
- 如果p，q。(if p, q.)
- p是q的充分条件(p is sufficient for q.)
- q是p的必要条件(q is necessary for p.)
- q如果p(q if p)      q当p(q when p)
- q除非 $\neg p$ (q unless $\neg p$ )
- p蕴含q(p implies q)
- p仅当q(p only if q)
- q每当p(q whenever p)
- q由p得出(q follows from p)
- q假定p(q provided that p)

#### 逆命题,逆否命题,反命题

从条件语句 $p\rightarrow q$ 出发,我们还可以构造出其逆命题等

- $q\rightarrow p$为其逆命题(converse)
- $\neg q\rightarrow \neg p$为其逆否(倒置)命题(contrapositive)
- $\neg p\rightarrow \neg q$为其反命题(inverse)

但只有逆否命题总是与原命题具有相同的真值。

当两个复合命题总是具有相同的真值时，无论其命题变量的真值是什么，我们称他们是等价的。
因此一个条件语句与它的逆否命题是等价的,逆命题和反命题是等价的

#### 双条件语句

令p,q为命题，双条件语句(biconditional statement) $p \leftrightarrow q$ 是命题“p当且仅当q(p if and only if q)”，当p和q具有相同的真值时，双条件语句为真，否则为假。
双条件语句也被称为双向蕴含(bi-implications)

|  P   |  Q   | $p \leftrightarrow q$ |
| :--: | :--: | :-------------------: |
|  T   |  T   |           T           |
|  T   |  F   |           F           |
|  F   |  T   |           F           |
|  F   |  F   |           T           |



> 个人感觉双条件语句的作用与异或恰好相反,双条件语句相同为1,不同为0,而异或则是相同为0,不同为1

双条件语句也有一些其他的表达方式:

- p是q的充分必要条件(p is necessary and sufficient for q)

- 如果p那么q，反之亦然(if p then q, and conversely)

- p当且仅当q(p iff q)

- p恰好当q(p exactly q)

  

> 不难理解, $p \leftrightarrow q$ 与 $p\rightarrow q\wedge q\rightarrow q$ 具有相同的真值

### 复合命题的真值表

一图胜千言，直接上图

|  p   | q    | $\neg Q$ | $P\vee \neg Q$ | $P\wedge Q$ | $P\vee \neg Q\rightarrow P\wedge Q$ |
| :--: | ---- | :------: | :------------: | :---------: | :---------------------------------: |
|  T   | T    |    F     |       T        |      T      |                  T                  |
|  T   | F    |    T     |       T        |      F      |                  F                  |
|  F   | T    |    F     |       F        |      F      |                  T                  |
|  F   | F    |    T     |       T        |      F      |                  F                  |

就是说，采用单独的列来找出复合命题的构造过程中出现的每个复合表达式的值

### 逻辑运算符的优先级

(Precedence of Logical Operators)

其实，圆括号()具有最高的优先级，其次才是逻辑运算符

|      运算符       | 优先级 |
| :---------------: | :----: |
|      $\neg$       |   1    |
|     $\wedge$      |   2    |
|      $\vee$       |   3    |
|   $\rightarrow$   |   4    |
| $\leftrightarrow$ |   5    |
|     $\oplus$      |   6    |

### 逻辑运算和比特运算

如果一个变量的值为真或为假，则此变量称为布尔变量(Boolean variable)

计算机的比特运算(bit operations，或称为位运算)

## 命题等价式

用真值相同的语句替换另一条语句是数学证明中常用的(认真体会)，因此，从给定符合命题生成相同真值命题的方法广泛用于数学构造。

#### 永真,矛盾,可能

定义：一个真值永远是真的复合命题(无论其中出现的命题变量的值是什么)，称为永真式(tautology)，也称为重言式。
一个真值永远为假的复合命题称为矛盾式(contradiction)。
既不是永真式又不是矛盾式的复合命题称为可能式(contingency)。

> 我们其实可以只用一个变量便可以构造出永真式和矛盾式，比如说 $p\wedge\neg p$ 便是一个矛盾式，而 $p\vee \neg p$ 便是一个永真式。

### 逻辑等价式

在所有可能的情况下都具有相同真值的两个复合命题称为逻辑等价的。
们也可以如下定义:

如果 $p\leftrightarrow q$ 是永真式，则复合命题p和q是逻辑等价(logically equivalent)的。用记号 $p\equiv q$ 来表示(也可以用 $p\Leftrightarrow q$ 来表示)

> 需要注意的是，符号" $\equiv$ "并不是一个逻辑联结词， $p\equiv q$ 也不是一个复合命题.

我们可以用真值表去证明逻辑等价式，但是一旦变量数量变多真值表就会难以绘制，所以我们给出一些基本的逻辑等价式：

- $p\wedge T\equiv p$\
  $p\vee F\equiv p$(恒等律Identity laws)

- $p\vee T\equiv T$\
  $p\wedge F\equiv F$(支配律Domination laws)

- $p\vee p\equiv p$\
  $p\wedge p\equiv p$(幂等律Idempotent laws)

- $\neg(\neg p)$(双重否定律Double negation law)

- $p\vee q\equiv q\vee p$

  $p\wedge q\equiv q\wedge p$(交换律Commutative law)

- $(p\vee q)\vee r\equiv p\vee(q\vee r)$\
  $(p\wedge q)\wedge r\equiv p\wedge(q\wedge r)$(结合律Associate law)

- $p\vee(q\wedge r)\equiv (p\vee q)\wedge(p\vee r)$\
  $p\wedge(q\vee r)\equiv(p\wedge q)\vee(p\wedge r)$(分配律Distributive laws)

- $\neg(p\vee q)\equiv \neg p\wedge\neg q$\
  $\neg(p\wedge q)\equiv\neg p\vee \neg q$(德摩根律De Morgan's laws)

- $p\vee(p\wedge q)\equiv p$\
  $p\wedge(p\vee q)\equiv p$(吸收律Absorption laws)

- $p\vee\neg p\equiv T$\
  $p\wedge \neg p\equiv F$(否定律Negation laws)

条件命题的逻辑等价式

- $(p\wedge q)\rightarrow r\equiv p\rightarrow(q\rightarrow r)$(Exportation law)

- $p\rightarrow q\equiv\neg p\vee q$

- $p\rightarrow q\equiv\neg q\rightarrow \neg p$

- $p\vee q\equiv \neg p\rightarrow q$

- $p\wedge q\equiv \neg(p\rightarrow \neg q)$

- $\neg(p\rightarrow q)\equiv p\wedge\neg q$

- $(p\rightarrow q)\wedge (p\rightarrow r)\equiv p\rightarrow(q\wedge r)$

- $(p\rightarrow q)\vee(p\rightarrow r)\equiv p\rightarrow(q\vee r)$

- $(p\rightarrow r)\wedge(q\rightarrow r)\equiv(p\vee q)\rightarrow r$

- $(p\rightarrow r)\vee(q\rightarrow r)\equiv (p\wedge q)\rightarrow r$

- $(p\rightarrow q)\wedge(p\rightarrow\neg q)\equiv \neg p$

  

双条件命题的逻辑等价式

- $p\leftrightarrow q\equiv(p\rightarrow q)\wedge(q\rightarrow p)$

- $p\leftrightarrow q\equiv\neg p\leftrightarrow \neg q$

- $p\leftrightarrow q\equiv(p\wedge q)\vee(\neg p\wedge \neg q)$

- $\neg(p\leftrightarrow q)\equiv p\leftrightarrow \neg q$

  

### 德摩根律的应用

实际上，德摩根律可以扩展为n个命题的形式

$\neg(p_1\vee p_2\vee...\vee p_n)\equiv(\neg p_1\wedge\neg p_2\wedge...\wedge\neg p_n)$

$\neg(p_1\wedge p_2\wedge...\wedge p_n)\equiv(\neg p_1\vee\neg p_2\vee...\vee\neg p_n)$

我们当然还可以写的更简洁:

$\neg\bigvee^n_{j=1}p_j\equiv\bigwedge^n_{j=1}\neg p_j$

$\neg\bigwedge^n_{j=1}p_j\equiv\bigvee^n_{j=1}\neg p_j$

### 构造新的逻辑等价式

其实就是灵活使用各种逻辑等价式来进行化简之类的，不过多赘述

### 补充

定义：命题变元及其否定统称为文字，一些文字的合取称为基本合取式或短语，一些文字的析取称为基本析取式或句子。

(1)disjunctive normal form: 假设 $A_i$ (i=1,2,...,n)为基本合取式，则 $A=A_1\vee A_2\vee...\vee A_n$ 称为析取范式

(2)conjunctive normal form：假设 $A_i$ (i=1,2,...,n)为基本析取式，则 $A=A_1\wedge A_2\wedge...\wedge A_n$ 称为合取范式

任何一个命题公式都存在与它等价的析取范式和合取范式

极大项：包含全部数目的命题变元的析取表达式\
极小项：包含全部数目的命题变元的合取表达式

主析取范式：仅由最小项的析取构成的等值式\
主合取范式：仅由最大项的合取构成的等值式

例:求 $(p\wedge q)\vee r$ 的主析取范式和主合取范式

主析取范式：

$(p\wedge q)\vee r\equiv(p\wedge q\wedge r)\vee(p\wedge q\wedge \neg r)\vee(\neg p\wedge q\wedge r)\vee(p\wedge \neg q\wedge r)\vee(\neg p\wedge \neg q\wedge r)$ 

主合取范式：

 $(p\wedge q)\vee r\equiv(r\vee p)\wedge(r\vee q)\equiv(r\vee p\vee \neg q)\wedge(r\vee p\vee q)\wedge(r\vee\neg p\vee q)$ 


我们其实可以根据真值表来书写主析取范式和主合取范式

| $p$  | $q$  | $r$  | $(p\wedge q)\vee(\neg p\wedge r)$ |
| ---- | ---- | ---- | :-------------------------------: |
| T    | T    | T    |                 T                 |
| T    | T    | F    |                 T                 |
| T    | F    | T    |                 F                 |
| T    | F    | F    |                 F                 |
| F    | T    | T    |                 T                 |
| F    | T    | F    |                 F                 |
| F    | F    | T    |                 T                 |
| F    | F    | F    |                 F                 |

如果要书写主析取范式，那么需要关注使得复合命题真值为真的真值组合，这些真值组合对应主析取范式中的极小项，并且使得该项在对应的真值组合下取T。

比如：在真值表中，使得复合命题 $(p\wedge q)\vee(\neg p\wedge r)$ 为真的真值组合有TTT，TTF，FTT，FFT，对应的极小项分别是 $(p\wedge q\wedge r)$ , $(p\wedge q\wedge\neg r)$ , $(\neg p\wedge q\wedge r)$ , $(\neg p\wedge\neg q\wedge r)$ ，这样我们就写出了如下的主析取范式。

$$\begin{align\*}
(p\wedge q)\vee(\neg p\wedge r)\equiv (p\wedge q\wedge r)\vee(p\wedge q\wedge\neg r)\vee(\neg p\wedge q\wedge r)\vee(\neg p\wedge\neg q\wedge r)
\end{align\*}$$

如果要书写主合取范式，那么需要关注使得复合命题真值为假的真值组合，这些真值组合对应主合取范式中的极大项，并且使得该项在对应的真值组合下取F。

比如：在真值表中，使得复合命题 $(p\wedge q)\vee(\neg p\wedge r)$ 为真的真值组合有TFT，TFF，FTF，FFF，这里拿TFT这一真值组合来举例，它所对应的极大项是 $\neg p\vee q\vee\neg r$ （很别扭，对吧？），其他的真值组合同理，我们就能写出如下的主合取范式。

$$\begin{align\*}
(p\wedge q)\vee(\neg p\wedge r)\equiv (\neg p\vee q\vee\neg r)\wedge(\neg p\vee q\vee r)\wedge(p\vee\neg q\vee r)\wedge(p\vee q\vee r)
\end{align\*}$$


思考：1.含有t个命题变元的真值表除了表头之外最多有多少行？

答案是显然的，t个命题变元，每个都有0，1两种取值，所以一共有 $2^t$ 个。

2.t个命题变元最多能形成多少个不等价的复合命题？

这个问题并不好思考，因为哪怕是只有两个命题变元，其不断地组合能形成无限个复合命题，再判断其等价与否更是难办。
我们不妨思考含有t个命题变元的真值表，这个表的最后一列是复合命题的真值，这时候我们大概会意识到，我们其实没有必要知到复合命题的形式，我们其实只需要知道复合命题的真值就可以了（也就是真值表的最后一列），结合上一道思考题，一共有 $2^t$ 行，复合命题在每行都有0，1两个选择，那就一共有 $2^{2^t}$ 个不等价的复合命题。

但是这时候我们就不禁要问了，对于任意一种选择，我们都能写出对应的复合命题的形式吗？其实是能的，因为我们可以根据真值表来写出主合取范式或者主析取范式，所以对于任意一种选择，我们都能够写出来。
### 可满足性

一个复合命题称为是可满足的，如果存在一个对其变量的真值赋值使其为真(也就是说,当他是一个永真式或者说是可满足式的时候)。
当不存在这样的赋值时，即当复合命题对所有变量的真值赋值都是假的，则复合命题是不可满足的。

一个复合命题是不可满足的当且仅当它的否定是永真式

当我们找到一个特定的使得复合命题为真的真值赋值时，就证明了它是可满足的。这样的赋值称为这个特定的可满足性的问题的一个解。


## 谓词和量词

### 谓词

**什么是谓词？**

例：考虑一个陈述句“x大于3”，显然这个陈述句可以使用P(x)来表示，那么显然，这里的P代表“大于3”这个性质，是一个“**命题函数**”，而x是变量。\
如果我们在考虑一个陈述句“x大于y”，那么这个陈述句就可以使用G(x,y)来表示，这里G仍然是一个命题函数，x，y是变量，以此类推

一般地，涉及n个变量 $x_1,x_2,...,x_n$ 的语句可以表示成为P( $x_1,x_2,...,x_n$ )。
形式为P( $x_1,x_2,...,x_n$ )的语句是命题函数P在n元组( $x_1,x_2,...,x_n$ )的值，P也称为n元谓词或者n位谓词。

- 注意，命题函数并没有真值，但是当命题函数所涉及到的变量各自被指派一个值时，命题函数就变为了一个有确定真值的命题。比如说P(x):x>3，当x=2时P(2)就是一个假命题，P(4)就是一个真命题。
### 量词

量化是一种方式，一种从命题函数生成一个命题的方式。\
量化表示在何种程度上谓词对于一定范围内的个体成立.

> 处理谓词和量词的逻辑领域成为谓词演算

变量的取定区域称为**变量的论域**(domain of discourse)，或**全体域**(universe of discourse)，时常简称为域。简单一些理解，就是变量取值的集合。\
值得注意的是，当我们改变命题的论域时，命题的量化的意义也会随着而改变，在我们使用量词时必须指定论域，否则语句的量化就是无意义的

所以，到底什么是**命题的量化**？

定义1：P(x)的**全称量化**是语句“P(x)对x在其论域的所有值为真”，符号 $\forall xP(x)$ 表示P(x)的全称量化。\
符号 $\forall$ 称为**全称量词**(universial quantifiers).

> 注意，如果论域为空，我们规定 $\forall xP(x)$ 对任何命题函数P(x)都为真,因为论域中不存在x使P(x)为假

定义2：P(x)的**存在量化**是命题"论域中存在一个个体x满足P(x)”，我们用 $\exists xP(x)$ 来表示。\
其中 $\exists$ 称为**存在量词**(existential quantifiers)

> 注意，如果论域为空，那么 $\exists xP(x)$ 对任何命题函数P(x)为假，因为没有一个个体x使P(x)为真。

> 其实我们还会有唯一性量词，用符号 $\exists !$ 或者是 $\exists _1$ ，表示存在唯一的一个个体使得命题函数为真，但是并不常用。

例：有一些实数是有理数。\
解：我们令命题P(y)表示y是实数，令命题Q(y)表示y是有理数，那么上式可以表示为 $\exists y(P(y)\wedge Q(y))$ 。
> 为什么我们在这里使用命题的合取而不是条件语句呢？如果我们使用条件语句，那么当y不是实数的时候，条件语句的前件为假，这个命题就变成真命题了，这显然不是我们想看到的。
### 有限域上的量词

当论域中的元素为有限个时，比如 $x_1,x_2,...,x_n$ ，则全称量词命题 $\forall xP(x)\equiv P(x_1)\wedge P(x_2)\wedge...\wedge P(x_n)$ 

> 要证明上述结论并不困难，我们只需要证当等式左侧真值为1时等式右侧的真值也为1，当等式右侧真值为1时等式左侧真值也为1。

同样地，存在量词命题 $\exists xP(x)\equiv P(x_1)\vee P(x_2)\vee...\vee P(x_n)$ 

> 证明这个与证明全称量词的并不相同，这里我们证明当等式左侧真值为0时等式右侧真值也为0，当等式右侧真值为0时等式左侧真值也为0。

### 受限域的量词

在我们限定一个量词的论域时，有时会把变量必须满足的条件直接放在量词后面，比如说 $\forall x<0(x^2>0)$ , $\exists z>0(z^2=2)$ 等等。

注意，受限的全称量化和一个条件语句的全称量化等价。\
比如 $\forall x<0(x^2>0)$ 等价于 $\forall x(x<0\rightarrow x^2>0)$ 。\
另一方面，受限的存在量化和一个合取式的存在量化等价。\
比如 $\exists z>0(z^2=2)$ 等价于 $\exists z(z>0\wedge z^2=2)$ 。

> 实际上我们在后来学习将自然语言翻译成命题语言的过程中，也会了解到全称量词一般会和条件语句联系在一起，而存在量词会和合取表达式联系在一起。

### 量词的优先级

量词 $\forall$ 和 $\exists$ 比命题演算中的所有逻辑运算符都具有更高的优先级

### 变量绑定

当量词作用于变量x时，我们说此变量的这次出现为约束的。\
如果变量没有被量词约束或者设置为某一特定值，那么该变量被称为是自由的。

而命题函数中的所有变量必须是约束的或者被设置为等于某一个特定值的，才能把他转变为一个命题。\
这可以通过对变量采用全程量词，存在量词，赋值来实现。

逻辑表达式中一个量词作用到的部分称为量词的作用域。\
一个变量是自由的当且仅当它在公式中所有限定该变量的量词作用域之外.

比如说 $\forall x<0(x^2>0)$ ，变量x就是被约束的。再比如说 $\exists y(P(y)\wedge Q(y))$ ， $(P(y)\wedge Q(y))$ 就是该命题中存在量词的作用域。

> 值得注意的是，我们经常会用同一个字母表示不同量词约束的变量，只要其作用域不重叠的。

### 涉及量词的逻辑等价式

$$\begin{align\*}
\forall x(A(x)\wedge B(x))\Leftrightarrow \forall xA(x)\wedge\forall xB(x)\\
\exists x(A(x)\vee B(x))\Leftrightarrow \exists xA(x)\vee\exists xB(x)\\
\forall xA(x)\vee\forall xB(x)\Rightarrow\forall x(A(x)\vee B(x))\\
\exists x(A(x)\wedge B(x))\Rightarrow\exists xA(x)\wedge\exists xB(x)\\
\end{align\*}$$

> 值得注意的是最后两行是" $\Rightarrow$ "，前两行是" $\Leftrightarrow$ "。
> 要证明上述结论也非常容易，将论域分为互不相交的两部分，一部分内的x使A(x)为真而B(x)为假，而另一部分使A(x)为假而B(x)为真，便可证明后两行公式左右两侧的真值并不为真。

$$\begin{align\*}
x\; is\; not\; occuring\; in\; P\; and\; B.\\
\forall xA(x)\vee P\Leftrightarrow \forall x(A(x)\vee P)\\
\forall xA(x)\wedge P\Leftrightarrow \forall x(A(x)\wedge P)\\
\exists xA(x)\vee P\Leftrightarrow \exists x(A(x)\vee P)\\
\exists xA(x)\wedge P\Leftrightarrow\exists x(A(x)\wedge P)\\
\forall x(B\rightarrow A(x))\Leftrightarrow B\rightarrow\forall xA(x)\\
\exists x(B\rightarrow A(x))\Leftrightarrow B\rightarrow \exists xA(x)\\
\forall x(A(x)\rightarrow B)\Leftrightarrow \exists xA(x)\rightarrow B\\
\exists x(A(x)\rightarrow B)\Leftrightarrow\forall xA(x)\rightarrow B\\
\end{align\*}$$

> 也就是说，当出现量词与无关命题合取或者析取时，括号的作用其实并不大。
> 当出现量词与条件语句时，则要注意命题函数的位置。如果命题函数位于条件语句的结论处，那么括号的作用其实也不大，但如果命题函数位于条件语句的假设处，那么去掉括号后量词就会发生变化。

### 量化表达式的否定

$$\begin{align\*}
\neg\exists xA(x)\equiv\forall x\neg A(x)\\
\neg\forall xA(x)\equiv\exists x\neg A(x)\\
\end{align\*}$$

> 量词的否定规则被称为量词的德摩根律，其实我们不难发现，当论域中的元素为有限个时，量词的德摩根律与我们之前提到过的德摩根律完全相同

### 语句到逻辑表达式的翻译
第一步：确定恰当的量词。\
第二步：引入变量和谓词。\
第三步：用量词，谓词，和逻辑操作来转化。


判断是全称量词命题还是存在量词命题其实并不困难，困难的事情其实在于如何使用命题函数来表述。\
实际上，当我们在表述全称量词命题时通常会使用条件语句，表述存在量词命题时通常会使用合取表达式。

## 嵌套量词


嵌套量词(nested quantifiers)，即一个量词出现在另一个量词的作用域内，如 $\forall x\exists y(x+y=0)$ 。

> 值得注意的是，量词范围内的一切都可以认为是一个命题函数，也就是说，对于 $\forall x\exists y(x+y=0)$ ，我们可以将其看作是 $\forall xQ(x)$ ,其中Q(x)表示 $\exists yP(x,y)$ ,而P(x,y)表示x+y=0。

### 理解涉及嵌套量词的语句

我们可以把嵌套量词当成多重循环去处理，尤其是当论域中的元素为有限个的时候。其实和剥洋葱差不多，先剥掉最外面的变量，再剥掉倒数第二个，以此类推。

### 量词的顺序

许多数学语句会涉及对多变量命题函数的多重量化。量词的顺序是很重要的，除非所有量词均为全称量词或者存在量词。\
比如说 $\exists y\forall x(x+y=0)$ 和 $\forall x\exists y(x+y=0)$ ,前者表示有一个y对于任意的x都会有x+y=0，而后者表示对于任意的x都会存在一个y使得x+y=0。显然前者为假命题，而后者为真命题。


原理：在没有其他量词的语句中，在不改变量化式意义的前提下，嵌套全称量词的顺序是可以改变的。\
比如说， $\forall x\forall y\forall z((x+y)+z=x+(y+z))$ 中的 $\forall x\forall y\forall z$ 还可以写为 $\forall y\forall x\forall z$ 等等，但只有嵌套的全称量词才可以这样写。


### 数学语句到嵌套量词语句的翻译

例：除了0以外的每个实数都有一个乘法逆元。

$$\begin{align\*}
\forall x\exists y(x\neq0\rightarrow xy=1)
\end{align\*}$$

例：用量词表示实变量x的实函数f(x)在其定义域中点a处的极限的定义

$$\begin{align\*}
\forall\varepsilon>0\exists\delta>0\forall x(0<|x-a|<\delta\rightarrow|f(x)-L|<\varepsilon)
\end{align\*}$$

那么我们实际上可以表述的更复杂一些：

令命题R(x)表示x是实数，P(x,y)表示x<y,我们还可以把定义写为：

$$\begin{align\*}
\forall\varepsilon(R(\varepsilon)\wedge P(0,\varepsilon)\rightarrow\exists\delta(R(\delta)\wedge P(0,\delta)\wedge\forall x(R(x)\wedge P(|x-a|,\delta)\rightarrow P(|f(x)-L|,\varepsilon))))
\end{align\*}$$


### 自然语句到逻辑表达式的翻译

例：每个人恰好有一个最好的朋友

引入谓词B(x,y)表示y是x的最好的朋友

$$\begin{align\*}
\forall x\exists y(B(x,y)\wedge\forall z((y\neq z)\rightarrow\neg B(x,z))
\end{align\*}$$

例：有一位妇女搭乘过世界上每一条航线上的一个航班

令P(w,f)为“w搭乘过航班f”，Q(f,a)为“f是a上的一条航班”

$$\begin{align\*}
\exists w\forall a\exists f(P(w,f)\wedge Q(f,a))
\end{align\*}$$

### 嵌套的量词的否定

前面说过理解嵌套量词语句就像剥洋葱，对吧。\
实际上，嵌套量词语句的否定也就像剥洋葱。把否定词一层一层地往里放。

$$\begin{align\*}
\neg\forall x\exists y(xy=1)\\
\Leftrightarrow \exists x\neg \exists y(xy=1)\\
\Leftrightarrow \exists x\forall y\neg(xy=1)\\
\Leftrightarrow \exists x\forall y(xy\neq 1)\\
\end{align\*}$$

## 推理规则

### 引言

数学中的证明是建立数学命题真实性的有效论证。

所谓的论证，是指一连串的命题并以结论为最后的命题。

所谓有效性，是指结论或论证的最后一个命题必须根据论证过程前面的命题或前提的真实性推出

### 命题逻辑的有效逻辑

无论什么时候，只要所有前提为真，那么结论也必须为真，我们就说语句的这种论证形式是有效的。实际上，我们为了分析一个论证，我们用命题变量代替命题，这将一个论证变为一个论证形式。

> 乍一听非常难理解，所谓的论证变成一个论证形式，其实就是将这种论证思路做成类似于公示的样子，使得用起来更加方便，比如我们在高中里用过的二级结论一样，方便而且快。

定义：命题逻辑中的一个论证是一连串命题的组合。除了论证中最后一个命题外的命题都叫做前提，最后那个命题叫作结论。如果所有前提为真蕴含着结论为真，那么一个论证是有效的。

命题逻辑中的论证形式是一连串涉及命题变量的复合命题。无论用什么特定命题替换其中的命题变量，如果前提均真时结论为真，则称该论证形式是有效的。

> 当 $(p_1\wedge p_2\wedge...\wedge p_n)\rightarrow q$ 是永真式时，带有前提 $p_i(i=1,2,...,n)$ 以及结论q的论证形式是有效的。

### 命题逻辑的推理规则

一共有九个，如下：

| 永真式                                                       | 名称       | 英文                   |
| ------------------------------------------------------------ | ---------- | ---------------------- |
| $p\rightarrow (p\vee q)$                                     | 附加律     | Addition               |
| $(p\wedge q)\rightarrow p$                                   | 化简律     | Simplification         |
| $((p)\wedge(q))\rightarrow p\wedge q$                        | 合取律     | Conjunction            |
| $(p\wedge(p\rightarrow q))\rightarrow q$                     | 假言推理   | Modus ponens           |
| $(\neg q\wedge(p\rightarrow q))\rightarrow\neg p$            | 取拒式     | Modus Tollens          |
| $((p\rightarrow q)\wedge(q\rightarrow r))\rightarrow(p\rightarrow r)$ | 假言三段论 | Hypothetical syllogism |
| $((p\vee q)\wedge\neg q)\rightarrow p$                       | 析取三段论 | Disjunctive syllogism  |
| $(p\rightarrow r)\wedge(q\rightarrow r)\wedge(p\vee q)\rightarrow r$ | 构造性两难 | Constructive dilemma   |
| $((p\vee q)\wedge(\neg p\vee r))\rightarrow(q\vee r)$        | 消解律     | Resolution             |

补充：

1.如果有 $p\rightarrow q$ 这样的结论形式，我们就能把原问题转换成下面这个式子：

$$\begin{align\*}
p_1\wedge p_2\wedge...\wedge p_n\wedge p\rightarrow q
\end{align\*}$$

所以我们实际上可以把结论中p来作为前提进行推理，如果能推出q，便能证明原来的结论 $p\rightarrow q$ 

2.在有些问题上，我们还可以使用归谬法：

假设结论为假，推出前提的否定为真，与已知矛盾。

3.实际上我们还可以通过构造消解律来论证

### 消解律

$$\begin{align\*}
((p\vee q)\wedge(\neg p\vee r))\rightarrow (q\vee r)
\end{align\*}$$

消解规则最后的析取式 $q\vee r$ 称为消解式，当令r=F时，就能得到析取三段论。

要使用消解律作为仅有的推理规则来构造命题逻辑中的证明，假设和结论必须表示为子句，这里子句是指变量或其否定的一个析取式。我们将命题逻辑中非子句的语句用一个或多个等价的子句语句来替换。比如 $p\vee (q\wedge r)$ ,就可以使用分配律来获得 $(p\vee q)\wedge (p\vee r)$ ，从而获得 $(p\vee q)$ 和$(p\vee r)$ ，也可以使用 $\neg p\vee q$ 来代替条件语句 $p\rightarrow q$ 等等。

### 谬误



1.肯定结论的谬误

原因在于 $((p\rightarrow q)\wedge q)\rightarrow p$ 不是永真式。

2.否定假设的谬误

原因在于 $((p\rightarrow q)\wedge \neg p)\rightarrow \neg q$ 不是永真式。

### 量化命题的推理规则

以下这些推理规则广泛地应用在数学论证中，但通常不会显式提及

1.全称实例：是从给定前提 $\forall xP(x)$ 得出 $P(c)$ 为真的推理规则

2.全称引入：对论域里所有元素c都有P(c)为真来推出 $\forall xP(x)$ 

3.存在实例：从 $\exists xP(x)$ 推出存在一个元素c使得P(c)为真

> 但是，在存在实例中，我们一般并不知道c是什么，但我们只知道它存在，因为存在，所以给它一个名称c从而继续论证。

4.存在引入：从已知有一个特定的c使得P(c)为真得出 $\exists xP(x)$ 为真

## 证明导论

### 引言

一个证明是建立数学语句真实性的有效论证，换句话说，有效的论证才是证明

> 之前我们所给出的证明皆为形式化证明(提供了所有的步骤，并且给出了所有用到的规则)，但之后我们将转向非形式化证明，这不会显式地列出所用到的假设公理和推理规则，这也是计算机所乐于使用的。

### 一些专用术语

定理(theorem):一个能够被证明为真的语句。也被称为事实(fact)或结论(result)

> 不太重要的定理有时会被称为命题。

公理(axiom):在数学框架下假定为真的语句。

引理(lemma):一个重要性略低但有助于证明其他结论的定理。

推论(corollary):从一个已经被证明的定理直接建立起来的一个定理。

猜想(conjucture):被提出认为是真的命题。


### 证明定理的方法

1.直接证明

2.间接证明：证明逆否命题。

3.空证明(vacuous proof):证明条件语句的前提为假

4.平凡证明(Trivial proof)：直接证明结论真值为1

5.归谬证明法(Proof by contradiction)：假设结论为假，推出矛盾

6.Proof by cases(分情况证明)

$$\begin{align\*}
(p_1\vee p_2\vee...\vee p_n)\rightarrow q\\
其实就是证明p_i\rightarrow q(i=1,2,3...,n)\\
\end{align\*}$$

7.存在性证明(existence proof)

8.Disproof by Counterexample(找出反例)

9.Nonexistence Proofs

### 直接证明法

对于条件语句 $p\rightarrow q$ 来使用直接证明：

第一步：假设p为真

第二步：使用推理规则构造

第三步：推出q为真

直接证明就是从假设直接导向结论。

### 反证法

反证法(proof by contraposition):证明原命题的逆否命题成立，或者说利用逆否命题的结论去推导出与原题设不符的矛盾。

> 实际上我们在高中使用的反证法并不是真正的反证法，而是归谬证明法(proof by contradiction)

空证明：证明命题的假设为假

平凡证明：直接证明命题的结论为真(换句话说，就是不使用前提)

### 归谬证明法

使用归谬证明法的经典例题就是“证明素数有无限个”


### 存在性证明

存在性证明就是找到一个特例，然后进行存在引入。

> 但是，这个特例的寻找往往极其考察数学直觉而无特别好的方法。

例：证明：对于任意正整数n，都有n个连续的正整数且这些正整数皆为合数。



证明：存在无理数x，存在无理数y，证明x的y次方有理。
