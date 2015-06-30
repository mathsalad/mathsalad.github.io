---
title: "A note on the \"trivial group presentation game\": \\(I\\) has a winning strategy on the group \\(F_2\\)"
---
In [my post on the strong measure zero game]({% post_url 2015-05-15-the-strong-measure-zero-game %}), I mentioned a game $$G_1(\mathcal {N}_H, \mathcal{N}_H)$$, where player one, who I will call $$I$$, presents player two, who I will call $$II$$, a subset from a group $$H$$, where the normal closure of the set is the full group, and $$II$$, chooses one element from each set presented, trying to get a set whose normal closure is again the full group. The game lasts $$\omega$$ innings ($$\mathbb{N}= \omega$$ if you prefer that notation). Essentially the idea is that $$I$$ gives presentations of the trivial group, and $$II$$ is trying to end up with a presentation of the trivial group. 

As a simple example, we can consider the group of integers $$(\mathbb Z,+)$$. Since the group is abelian any group that normally generates the group, also generates the group. This also means that there is some linear combination of elements from any presented set that has value $$1$$. What player $$II$$ can do to win, is choose a non identity element $$x_0$$, where $$\vert x_0 \vert$$ is the least among non identity elements. If $$\vert x_0 \vert=1$$, player $$II$$ has already chosen a set that normally generates and may choose arbitrarily. Suppose that $$II$$ has chosen $$x_0,...,x_n$$, if $$d:=\gcd(x_0,...,x_n)=1$$ we choose an arbitrary element. If we have $$d>1$$, then choose an element $$x_{n+1}$$, so that $$\gcd(d,x_{n+1})<d$$. Note that we can do that, since otherwise, every element in the presented set would have $$d > 1$$ dividing it, hence the greatest common divisor of the set, without the identity, would be greater than or equal to $$d$$, contradicting the set generates the group. So we can always decrease our greatest common divisor till we reach $$1$$. So we have a strategy where $$II$$ will win every time. A similar argument can be used to show that $$II$$ wins in groups where every strictly ascending chain of infinite index subgroups, is finite. 

It is pretty easy to find groups where $$I$$ wins, by using large groups, like $$(\mathbb{R},+)$$, but what about finitely generated groups? We will show, in this post, that $$I$$ has a winning strategy to win $$F_2$$, in fact it will be a "fixed strategy" where $$I$$ will play the same no matter what $$II$$ picks on $$II$$'s turns. 

Our proof will use facts from [small cancellation theory][sct], in particular small cancellation groups are not trivial. I will explain a bit of the idea of small cancellation conditions, and give key definitions. All the small cancellation that we discuss can be found in *Combinatorial Group Theory* Lyndon and Schupp, or *Geometry of Defining Relations in Groups* by Ol'shanskii, or [Wikipedia][sct].

The idea of small cancellation theory is that, if you have a set of relations, satisfying a "small cancellation condition", that is when you multiply the two different words, the length of the reduced product (remove the $$xx^{-1}$$) is not much shorter than the the sum of the lengths of the word. This, in a sense, gives control over what words end up representing the identity, and how words can be reduced using the relations that satisfy the small cancellation conditions. 

## Basic definition for small cancellation theory

The information in this section is all fairly basic stuff, you may want to skip this section, or just read the $$C'(1/6)$$ definition and come back if there are some words you do not know.

**Basic definitions for words in free groups.** related to words and free groups. A word is a string of elements from some some set called an alphabet. For example $$x, xyxx^{-1},$$ and $$xy$$ are all (not equal) words from the alphabet $$\{ x,y,x^{-1},y^{-1} \}$$. A word is reduced if there is no occurrence of $$tt^{-1}$$ or $$t^{-1}t$$ in the word, and cyclically reduced provided it is not a nontrivial conjugate, so $$w \neq t w' t^{-1}$$ and $$w \neq t^{-1} w' t$$. The length of a word $$w$$, which we call $$\vert w \vert$$ is the number of elements in the reduced version of the word; this is well defined. So $$ \vert xyxx^{-1} \vert = \vert xy \vert =2$$, for example.

**Definition of symmetrized  presentation.** Suppose $$G = \langle X \mid R \rangle$$. We say the set of relations $$R$$ is symmetrized provided it is closed under taking inverses, and taking cyclic permutations of words up to being cyclically reduced, and every word in $$R$$ is cyclical reduced. $$G$$ has a symmetrized presentation provided $$R$$ is symmetrized. For example 

$$
\begin{align*}
R = &\{ab^3ab^4,b^3ab^4a^{-1}, ab^4 a ^{-1} b^{-3}, \\
& b^4a^{-1} b^{-3} a ^{-1}, a^{-1}b^{-3}a^{-1}b^{-4},... \text{inverses} \}.
\end{align*}
$$

**Definition of $$C'(1/6)$$:** We say that $$p$$ is a piece relative to $$R$$ provided there exists two distinct elements $$r_1,r_2 \in R$$ with $$r_1=pc_1$$ and $$r_2=pc_2$$, where "$$=$$" is word equality, so no cancellation. We way $$R$$ has condition $$C'(1/6)$$ if $$r \in R$$ and $$r=pc$$ where $$p$$ is a piece, then $$ \vert p \vert < \frac{1}{6} \vert r \vert$$. There is an entirely similar definition for $$C'(\lambda).$$

The reason I only mention $$C'(1/6)$$ is that it is a strong enough small cancellation condition to guarantee a group is infinite. Note that you can have a group that has a $$C'(1/6)$$ presentation, but may not be given to you that way. It is an interesting fact that for $$\lambda > 1/5$$, every group has a $$C'(\lambda)$$ presentation. There are many other small cancellation conditions, $$C(p)$$ and $$T(p)$$ for example, and you can mix-and-match different conditions too, but that is really beyond this post.

## Player $$I$$ has a winning strategy in $$G_1( \mathcal{N}_{F_2},\mathcal{N}_{F_2})$$

Let $$F_2$$ be the free group of rank $$2$$, on the set $$\{x,y\}$$. We will show that $$F_2$$ has a winning strategy, by showing that there is a sequence of sets, $$A_0,...,A_n,...$$, that normally generate, even generates, the group $$F_2$$, and any one element choice from each of these sets gives a set $$\{a_0,...,a_n,...\}$$, which will correspond to a group, $$G=\langle x,y \mid a_0,...,a_n,... \rangle$$,  that is $$C'(1/6)$$, which means that $$\{a_0,...,a_n,...\}$$ can not normally generate $$F_2$$. The strategy for player $$I$$ will be to play $$A_n$$ on the $$n$$th turn.

There will be a couple parts where I make some estimates on inequalities, and make no attempt to make these as good as possible(the estimates I make are *good enough*). If you are sensitive to such disregard of sharp bounds, you will need to have your eyes covered for the rest of this proof. You have been warned.

**Proposition 1.** Let 

$$ w_n=\prod_{i=1}^{9 \cdot 100^{n+1}} xy^{100^{n+1}+i}=xy^{100^{n+1}+1}...xy^{100^{n+2}}.$$

 Then we have that $$A_n=\{w_{n+1},xw_{n+1},w_{n+1}y\}$$ generates the group $$F_2$$, but any one element choice from each $$A_n$$ results in a set of relations for a $$C'(1/6)$$ group. In particular this means that for any choice of $$a_i$$'s, where $$a_i \in A_i$$, that $$ \langle x ,y \mid a_0,...,a_n,... \rangle$$ is an infinite group since it will be $$C'(1/6)$$.

*proof of Lemma 1.* First it is clear that each $$A_n$$ generates $$F_2$$ since we can multiply $$w_{n+1}^{-1}$$ to cancel $$w_{n+1}$$ on each term to end up with $$x,y$$, which generates the group. Let $$R_w$$ be the smallest symmetrized set of words containing the word $$w$$, which is all the cyclically reduced, cyclic permutations of the word $$w$$ and their inverses. For $$R_{w_n}$$ all pieces are of the form $$b^i a^{\pm 1} b^j$$, where $$-100^{n+2} \leq i,j\leq 100^{n+2}$$ (note that for many $$i,j$$ can not actually be obtained). So the length of a pieces $$p$$ are bounded by 

$$2 \cdot 100^{n+2}+1<3\cdot 100^{n+2},$$ 

and the length of each $$w_n$$ is bounded from below by 

$$ 9\cdot 100^{n+1} \cdot 100^{n+1}.$$ 

We get that 

$$ \frac{ \vert p \vert }{ \vert w_n \vert } \le \frac{ 3 \cdot 100^{n+2} }{9 \cdot 100^{2n+2}}= \frac{1}{3 \cdot 100^n} $$

which for $$n>0$$ we have the right hand side is less than $$1/6$$. A very similar argument can be carried out for $$R_{w_ny}$$ and $$R_{xw_n}$$, and in fact you can use the same bounds, since  our bounds are so rough. So each $$R_w$$, for $$w \in A_n$$, gives a $$C'(1/6)$$ presentation. Say that $$m>n$$ and $$w \in A_m$$, and $$u \in A_n$$, and we consider $$R_w,R_u$$. Note, that at "worst" the amount of cancellation between words in $$R_w$$ and $$R_u$$ will be bounded by the cancellation bounds we established above for $$R_u$$, since elements in $$R_u$$ have small enough exponents on their $$y$$'s that they can not completely cancel out a $$y^k$$ term in $$R_w$$. This worked for arbitrary choices. So let $$a_0,...,a_n,...$$ be a sequence where $$a_i \in A_i$$, then $$R=\bigcup_{i< \omega} R_{a_i}$$ is a symmetrized set of relations, and we know that between two words, the cancellation is less than $$1/6$$ the length of either of the words, so it gives a $$C'(1/6)$$ presentation, hence $$ \langle x,y \mid a_0,...,a_n,... \rangle $$ is a $$C'(1/6)$$ group, and is infinite. $$\square$$

I came up with this game in a class I took on selection principles, and studied it as a final project, and at the time I knew very little group theory (I still know very little), and even thought all finitely generated groups had a winning strategy for player $$II$$. At the end of the class I only really found some conditions for player $$II$$ winning in finitely generated groups. It had been at the back of my mind since the class, I would pick it up and work on it for a while before setting down, multiple times. In a way, thinking about this problem and closely related things really influenced my mathematical interests, I have a feeling it will show in future posts. In the end I am actually not to sure these ideas are of interest, at least in the finitely generated group case. I suspect it will be a while before I discuss these games on groups again, but I will end this with a couple questions to ponder:

* For finitely generated groups is there a nice demarcation line between player $$I$$ or $$II$$ having a winning strategy? For groups in general?
* Are there groups where there is no winning strategy for either player? Are there finitely generated groups where there is no winning strategy?
* There are a couple of other, similar ideas to consider, one where you replace normally generate with simply generate, or replace with generate finite index subgroup, or normally generate finite index subgroup, or mix-and-match the different sets. (I have not really thought about them much, but there are probably a lot of equivalences, because once you reach a finite index subgroup, in many cases, reach the full group) Are there any interesting connections and differences among them?
* For those who have looked up the connection of these sorts of games with selection principles and Ramsey statements(see the [references in the strong measure zero game post]({% post_url 2015-05-15-the-strong-measure-zero-game %})): are there interesting connection between those and the games for finitely generated groups? For countable groups? For groups? In particular what would the Ramsey statements be? 
* Can you think of any cool group theoretic consequences of a group that has a winning strategy for $$I$$, how about for $$II$$?

[sct]: https://en.wikipedia.org/wiki/Small_cancellation_theory

