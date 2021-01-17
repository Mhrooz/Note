# 1.1 Individual constants 独立常量？

The main difference between names in English and the individual constants of FOL is that we require the latter to refer to exactly one object.
individual constants的描述更加准确

individual constant 不允许不指代实体的名字存在

但是允许两者指代同一个实体

也允许没有名字

Remember in FOL：

1. Every individual constant must name an (actually existing) object.
2. No individual constant can name more than one object.
3. An object can have more than one name, or no name at all.

# 1.2 Predicate symbol 谓词符号

Predicate symbols are symbols used to express some property of objects or some relation between objects.
谓词符号是用来表示物品特性或者物品之间关系的符号

有时候也叫做relation symbols.

李华喜欢韩梅梅，是主谓句，其中李华是主语。在逻辑语句中，李华和韩梅梅都是主语，谓语“喜欢”表示了李华和韩梅梅的关系。这里的喜欢就是一个二元谓词(binary),因为它带了两个argument

用**arity**表示一共有几个argument。 只有一个叫 `unary`,两个叫`binary`，三个叫`ternary`

unary通常表示物品特性，比如我在家，在家就是unary

binary表示两个物品的关系

Every predicate is interpreted by a determinate property or relation of the same arity as the predicate
英语里每个谓语都可以被解释称特定的属性或者是有相通arity的在逻辑学中的谓语

# 1.3 Atomic sentence 原子语句

A sentence formed by a predicate followed by the right number of names is called an **atomic sentence**
一个谓语被用和谓语可以携带数量的名字所构成的句子叫做原子语句

infix 夹在两个argument中间，prefix就是谓语在argument前

原子语句同样必须有顺序Taller(a,b)和Taller(b,a)的意思是不同的

每个原子语句必须有一个真值：真或者假

# 1.4 General first-order language fol总论

如果要把自然语句翻译为fol，首先可能要预定义一些语句

首先要进行设计，拿捏哪些需要定义哪些不需要

然后挑选谓语动词。多位置的动词会更加灵活

尽量使用更小的动词。



























