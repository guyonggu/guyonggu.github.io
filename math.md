## 代数
集合S和二元运算"加法","乘法",记作(S,+)或(S,+,$\cdot$)  
(P1). 封闭性 (Closure)  
(P2). 结合律 (Associativity)  
(P3). 幺元 (Identity)  
(P4). 逆元 (Inverse)  
(P5). 交换律 (Commutativity)  
>记忆"凤姐咬你脚"

(P6). 分配律 (Distributity)

定义
* 半群(semigroup): (S,+)中加法满足P1,P2
* 群(group): (S,+)中加法满足P1,P2,P3,P4
* 交换群/阿贝尔群(Abelian group): (S,+)为群,且加法满足交换律
* 环(ring): (S,+,`$\cdot$`)中加法构成交换群,乘法构成半群,乘法和加法满足分配律
    >有的地方环的定义要求有幺元
* 半环(semiring): 不需要满足加法逆的含幺环
* 域: 含幺交换环
* Closed semiring: semiring with two additional properties:
    * if $a_1,a_2,\dots,a_n,\dots$ is a countable sequence of elements of S, then $a_1+a_2+\dots+a_n+\dots$ exists and is unique, the order in which the various elements are added is irrelevant.
    * the operation $\cdot$ distributes over countably infinite sums as well as finite sums. The the closure $a^*$ can be defined as $a^*=1+a+a^2+\dots+a^n+\dots$, which satisfies $a^*=1+a\cdot a^*$
    * 
(BEZOUT'S THEOREM) If a and b are positive integers, then there exists integers s and t such that gcd(a,b) = sa + tb.  (Not unique)

(extended) Euclidian algorithm
Chinese remainder theorem
Fermat's last theorem
Fermat's little theorem
mathmatical induction vs. strong induction