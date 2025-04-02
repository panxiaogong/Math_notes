# 第一章 基础:逻辑和证明

## 命题逻辑

### 命题

命题(proposition)是逻辑的基本构件，是一个只能或真或假，而不能既真又假的陈述语句(a declarative sentence that is either true or false, but not both)

> 对于大部分语句，我们是极其容易判断的。比如说“几点了？”“仔细读这个”之类的疑问句或者是祈使句显然就不是命题，而所谓“x+1=2”之类的语句也并不是命题，因为它既不为真，也不为假，再难一些，"This statement is false(这句话是假的)"这个语句也依然不是个命题，因为它既不能是真，也不能是假。
>
> 但是有一些奇怪语句，虽然看上去不合理，但却是一个命题，比如“我吃了一百粒米”，这个语句要么为真要么为假，它确实是一个命题。

我们习惯上用字母p,q,r,s,...来表示命题变量(propositional variables)(语句变量sentential variables),即表示命题的变量.

如果一个命题是真命题,则他的真值(truth value)为真,用T表示,反之则真值为假,用F表示.

另外,不能用简单命题来表示的命题称为原子命题(atomic proposition),换句话说，原子命题不能被分解为更简单的陈述句。
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

但只有逆否命题总是与原命题具有相同的真值.

当两个复合命题总是具有相同的真值时,无论其命题变量的真值是什么,我们称他们是等价的.因此一个条件语句与它的逆否命题是等价的,逆命题和反命题是等价的

#### 双条件语句

令p,q为命题,双条件语句(biconditional statement) $p \leftrightarrow q$ 是命题"p当且仅当q(p if and only if q)",当p和q具有相同的真值时,双条件语句为真,否则为假.双条件语句也被称为双向蕴含(bi-implications)

|  P   |  Q   | $p \leftrightarrow q$ |
| :--: | :--: | :-------------------: |
|  T   |  T   |           T           |
|  T   |  F   |           F           |
|  F   |  T   |           F           |
|  F   |  F   |           T           |



> 个人感觉双条件语句的作用与异或恰好相反,双条件语句相同为1,不同为0,而异或则是相同为0,不同为1

双条件语句也有一些其他的表达方式:

- p是q的充分必要条件(p is necessary and sufficient for q)

- 如果p那么q,反之亦然(if p then q, and conversely)

- p当且仅当q(p iff q)

- p恰好当q(p exactly q)

  

> 不难理解, $p \leftrightarrow q$ 与 $p\rightarrow q\wedge q\rightarrow q$ 具有相同的真值

### 复合命题的真值表

一图胜千言,直接上图

|  p   | q    | $\neg Q$ | $P\vee \neg Q$ | $P\wedge Q$ | $P\vee \neg Q\rightarrow P\wedge Q$ |
| :--: | ---- | :------: | :------------: | :---------: | :---------------------------------: |
|  T   | T    |    F     |       T        |      T      |                  T                  |
|  T   | F    |    T     |       T        |      F      |                  F                  |
|  F   | T    |    F     |       F        |      F      |                  T                  |
|  F   | F    |    T     |       T        |      F      |                  F                  |

就是说,采用单独的列来找出复合命题的构造过程中出现的每个复合表达式的值

### 逻辑运算符的优先级

(Precedence of Logical Operators)

其实,圆括号()具有最高的优先级,其次才是逻辑运算符

|      运算符       | 优先级 |
| :---------------: | :----: |
|      $\neg$       |   1    |
|     $\wedge$      |   2    |
|      $\vee$       |   3    |
|   $\rightarrow$   |   4    |
| $\leftrightarrow$ |   5    |
|     $\oplus$      |   6    |

### 逻辑运算和比特运算

如果一个变量的值为真或为假,则此变量称为布尔变量(Boolean variable)

计算机的比特运算(bit operations,或称为位运算)

## 命题等价式


用真值相同的语句替换另一条语句是数学证明中常用的(认真体会),因此,从给定符合命题生成相同真值命题的方法广泛用于数学构造.

#### 永真,矛盾,可能

定义:一个真值永远是真的复合命题(无论其中出现的命题变量的值是什么),称为永真式(tautology),也称为重言式.一个真值永远为假的复合命题称为矛盾式(contradiction).既不是永真式又不是矛盾式的复合命题称为可能式(contingency).

> 我们其实可以只用一个变量便可以构造出永真式和矛盾式,比如说 $p\wedge\neg p$ 便是一个矛盾式,而 $p\vee \neg p$ 便是一个永真式

### 逻辑等价式

在所有可能的情况下都具有相同真值的两个复合命题称为逻辑等价的.我们也可以如下定义:

如果 $p\leftrightarrow q$ 是永真式,则复合命题p和q是逻辑等价(logically equivalent)的.用记号 $p\equiv q$ 来表示(也可以用 $p\Leftrightarrow q$ 来表示)

> 需要注意的是,符号" $\equiv$ "并不是一个逻辑联结词， $p\equiv q$ 也不是一个复合命题.

我们可以用真值表去证明逻辑等价式,但是一旦变量数量变多真值表就会难以绘制,所以我们给出一些基本的逻辑等价式:

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

实际上,德摩根律可以扩展为n个命题的形式

$\neg(p_1\vee p_2\vee...\vee p_n)\equiv(\neg p_1\wedge\neg p_2\wedge...\wedge\neg p_n)$

$\neg(p_1\wedge p_2\wedge...\wedge p_n)\equiv(\neg p_1\vee\neg p_2\vee...\vee\neg p_n)$

我们当然还可以写的更简洁:

$\neg\bigvee^n_{j=1}p_j\equiv\bigwedge^n_{j=1}\neg p_j$

$\neg\bigwedge^n_{j=1}p_j\equiv\bigvee^n_{j=1}\neg p_j$

### 构造新的逻辑等价式

其实就是灵活使用各种逻辑等价式来进行化简之类的,不过多赘述

### 补充

定义:命题变元及其否定统称为文字,一些文字的合取称为基本合取式或短语,一些文字的析取称为基本析取式或句子.

(1)disjunctive normal form: 假设 $A_i$ (i=1,2,...,n)为基本合取式,则 $A=A_1\vee A_2\vee...\vee A_n$ 称为析取范式

(2)conjunctive normal form:假设 $A_i$ (i=1,2,...,n)为基本析取式,则 $A=A_1\wedge A_2\wedge...\wedge A_n$ 称为合取范式

任何一个命题公式都存在与它等价的析取范式和合取范式

极大项:包含全部数目的命题变元的析取表达式
        极小项:包含全部数目的命题变元的合取表达式

主析取范式:仅由最小项的析取构成的等值式
	主合取范式:仅由最大项的合取构成的等值式

例:求 $(p\wedge q)\vee r$ 的主析取范式和主合取范式

主析取范式:

$(p\wedge q)\vee r\equiv(p\wedge q\wedge r)\vee(p\wedge q\wedge \neg r)\vee(\neg p\wedge q\wedge r)\vee(p\wedge \neg q\wedge r)\vee(\neg p\wedge \neg q\wedge r)$ 

主合取范式:

 $(p\wedge q)\vee r\equiv(r\vee p)\wedge(r\vee q)\equiv(r\vee p\vee \neg q)\wedge(r\vee p\vee q)\wedge(r\vee\neg p\vee q)$ 



### 可满足性

一个复合命题称为是可满足的,如果存在一个对其变量的真值赋值使其为真(也就是说,当他是一个永真式或者说是可满足式的时候).当不存在这样的赋值时,即当复合命题对所有变量的真值赋值都是假的,则复合命题是不可满足的.

一个复合命题是不可满足的当且仅当它的否定是永真式

当我们找到一个特定的使得复合命题为真的真值赋值时,就证明了它是可满足的.这样的赋值称为这个特定的可满足性的问题的一个解.


