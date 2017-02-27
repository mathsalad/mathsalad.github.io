---
layout: post
---

## Background

Originally, my first post was going to be an introduction to selection principles, especially those in topology, and a few other related concepts. I decided I could not do justice to the subject in one post (especially with my minimal knowledge), and have opted to present some very cool results that will, hopefully, give a taste of the ideas that come up when studying the subject.

 **Definition of the game $$G_1( \cal A, \cal B) $$.** Let $$ \mathcal{A}$$ and $$\mathcal{B} $$ be collections of sets, we define the game $$G_1(\cal{A}, \cal{B})$$ to be a game with two players, that we will denote $$I$$ and $$II$$, and the game will have [$$\omega$$ innings][ordinals], where each inning consists of a turn by $$I$$ and then a turn by $$II$$. By $$\omega$$ innings we mean there is an inning for each $$0,1,2,3, \dots $$ (if you prefer $$\omega = \mathbb N$$). The innings follow this pattern: player $$I$$ starts off, in inning $$n$$, by presenting a nonempty set $$A_n$$ from $$\cal A$$ which marks the end of player $$I$$'s turn, and then player $$II$$ picks an $$a_n \in  A_n$$. At the end of the $$\omega$$ innings we are left with a play 
 
 $$(A_0,a_0, \dots , A_i, a_i, \dots)$$
 
 of what happened in that game. Player $$II$$ wins if $$ \{ a_i \mid i \in \omega \} \in \cal B$$ and $$I$$ wins otherwise.
 
A couple of examples to consider:

* Let $$D$$ consist of all dense subsets of $$ \mathbb R $$. Consider $$G_1 (D,D) $$.
* Let $$X$$ be a countable subset of some topological space $$Y$$ and $${\cal{O}}_Y$$ is the set of all open covers of $$Y$$, and $${\cal {O}}_X$$ the set of covers for $$X$$. Consider $$G_1( {\cal{O}}_Y, {\cal{O}}_X) $$.
* $$V$$ is a finite dimensional rational vector space, and $$A$$ is the set of infinite vector subspaces of $$V$$, and $$B$$ is the set of sets that contain infinite rational vector subspaces of $$V$$. Consider $$ G_1(A,B) $$
* Let $$ U $$ be an [ultrafilter][ultrafilters] on some set. Consider $$G_1(U,U) $$.
* Let $$H$$ be a group and $$ {\mathcal N}_H $$ the set of subsets of $$H$$ that normally generate the group. Consider $$G_1({\mathcal N}_H, {\mathcal N}_H)$$ . There are also variation of considering sets that generate the group $$H$$, $$ {\mathcal K}_H $$ and looking at $$G_1({\mathcal K}_H, {\mathcal N}_H)$$, $$G_1({\mathcal N}_H, {\mathcal K}_H)$$, $$G_1({\mathcal K}_H, {\mathcal K}_H)$$ (there is a very good chance I am going to write about this bullet point, and related ideas, in future posts, since it is basically the reason I started the blog).
* etc. Think of some others!
 

A strategy for a player is a function that takes what has been played and outputs the next move. So $$ s_1,s_2$$ will be strategies for players $$I,II$$ respectively, and $$s_1: \varnothing \mapsto A_0 $$, and $$ s_1: (A_0,a_0,...,A_i,a_i) \mapsto A_{i+1}$$. We get a similar description for $$s_2$$. Basically they are instructions on a game tree that tell the player what to do next given where they are in the game tree. We call $$s_i$$ a winning strategy provided the cooresponding player will *always* win following that strategy. It is interesting that in some games there is no winning strategy for either player, and in fact the two main theorems that will be presented will give such an example(assuming [Borel's conjecture][smz] is false)

Do any of the above (bulleted)examples have winning strategies for one of the players? How about the games you came up with?

 **Definition of strong measure zero.** A set $$X \subseteq \mathbb R$$ is strong measure zero if, for all sequences $$ ( \epsilon_n \mid n  \in \omega) $$ of positive real numbers, then there exists a sequence of intervals $$I_n$$, where the length of $$I_n$$ is less than $$\epsilon_n $$ for all $$n$$, and $$X \subseteq  \cup_{n \in \omega} I_n$$.
 
 Every strong measure zero set is [Lebesgue measure zero][measurezero], although [not every measure zero set is strong measure zero][cannotsmz], the [Cantor set][cantor] provides such an example. It is also easy to see that every countable set is strong measure zero. In fact [Borel's conjecture][smz] actually conjectures that every strong measure zero set is countable. That conjecture ended up being independent of the usual axioms, ZFC, so it is consistent for there to be uncountable strong measure zero sets, and consistent for there to be only countable strong measure zero sets. [Luzin sets][luzin] provide examples of strong measure zero sets that are not countable.
 
 Let $$ J_{\epsilon} $$, $$ \epsilon >0 $$, be the set of all intervals of length less than $$\epsilon$$, and say $${\mathcal J}:= \{J_\epsilon \mid \epsilon >0 \} $$, and $${\mathcal O}_X $$ the set of open covers of some set $$X \subseteq \mathbb R$$ (where the open sets come from $$ \mathbb R$$ and not $$X$$ with the subspace topology).
 
 **Definition of the strong measure zero game.** Let $$X \subseteq \mathbb R$$. Then the strong measure zero game is the game $$G_1( {\mathcal J}, {\mathcal O}_X)$$.

There are a couple of other definitions I could have chosen, but I want to stress that the game has a very strong connection to strong measure zero, since player $$I$$ can choose a sequence of $$\epsilon_n$$ and play $$J_{\epsilon_n} $$, in inning $$n$$, and then $$II$$ tries to cover $$X$$ by collecting one interval from each $$J_{\epsilon_n}$$. 

A very natural question to ask is when does player $$I$$ have a winning strategy, and when does player $$II$$ have a winning strategy in $$G_1( {\mathcal J}, {\mathcal O}_X)$$? This brings us to "the main event":
 
 
**Theorem 1.** Player $$II$$ has a winning strategy in the strong measure zero game, if, and only if, $$X$$ is countable.

**Theorem 2.** Player $$I$$ has a winning strategy in the strong measure zero game, if, and only if, $$X$$ is not strong measure zero.

One of the things that makes these results interesting is that this means it is *consistent* for winning strategies to always exist, that is when all strong measure zero sets are countable, and it is consistent for there to be sets where there is no winning strategy, which is when there are uncountable strong measure zero sets(as an example the Luzin sets mentioned before).


## The Proofs of Theorem 1 and 2
The proofs of Theorem 1 and 2, that will be presented, is Galvin's with some modification and can be found in his paper *Indeterminacy of point-open games*. I found out about this proof in a class, taught by Marion Scheepers, a few years ago.

First, some notation, $$^\omega \omega$$ will be the set of infinite sequences of order type $$\omega$$, $$^{< \omega} \omega$$ will be the set of finite sequences indexed by finite ordinals. And if $$x,y$$ are sequences, then $$x \frown y$$ will be the concatenation of the sequences. As examples 

$$ (1,2,3,...) \in {^\omega \omega},$$

$$(7,10,2) \in {^{<\omega}} \omega$$

and 

$$ (7,10,2) \frown (24,1)= (7,10,2,24,1). $$

**Lemma 3.** Let $$X$$ be a set and suppose that for each $$x \in X$$ we have that a set $$B_x$$, which is a set of positive integer, finite length, sequences such that:

1. For every infinite sequence $$ (n_1,...,n_i,...) $$ there is a $$ k \in \omega $$ such that $$ (n_1,...,n_k) \in B_x $$.
2. For each finite sequence $$ (n_1,...,n_m) $$, 
    
    $$ \vert \bigcap_{k \in \omega} \{ x \in X \mid (n_1,...,n_m,k) \in B_x \} \vert \leq \aleph_0, $$ 

then we have that $$ \vert X \vert \leq \aleph_0 $$ ($$X$$ is countable).

*proof of Lemma 3.* We will prove by contradiction, so suppose that $$X$$ is an uncountable set with the above properties. This means that 

$$ X \setminus \bigcup_{ \alpha \in { ^{< \omega} \omega} } \left( \bigcap_{n \in \omega} \{ x \in X \mid \alpha \frown (n) \in B_x \} \right) \neq \varnothing $$

since the part that is being removed from $$X$$ is countable. Let $$x$$ be an element from this nonempty set. By the definition of the above set, we know that $$x$$ has the property, that for any sequence $$ \alpha \in {^{<\omega} \omega}$$, that there is an $$n$$ such that $$\alpha \frown (n) \not\in B_x$$. Starting with the empty sequence, $$ () $$, we know there is a least $$ n_1 $$ such that $$ (n_1) \not\in B_x$$, and we can continue doing this inductively, constructing sequences $$ (n_1,...,n_k) \not\in B_x$$ of length $$k$$. This contradicts property 1. $$\square$$

**Theorem 1.** Player $$II$$ has a winning strategy in the strong measure zero game, if, and only if, $$X$$ is countable.

*proof of Theorem 1.*  It is easy to see that $$II$$ has a winning strategy, when $$X$$ is countable, since we can enumerate the set $$X$$, and in turn $$n $$, $$II$$ covers the $$n$$-th element. For the other direction, we will need to define a different game. Let $$ (Y,d)$$ be a separable metric space, so it also has a countable basis. (Separable means contains a countable dense set subset.) The game has these rules:

1. There is an inning for each $$n \in \omega$$.
2. In inning $$n$$ player $$I$$ chooses a set $$ \{S_1,S_2\} $$, where $$ S_i \subseteq Y $$ is open and the distance between $$S_1$$ and $$S_2$$ is positive, where distance between the two sets is defined to be $$\inf \{ d(x,y) \mid (x,y) \in S_1 \times S_2 \}=d(S_1,S_2) $$. We will call such pairs playable
3. Player $$II$$ chooses one of the sets, which we will call $$T_n$$.
4. Player $$II$$ wins if $$ \bigcap_{n \in \omega} T_n = \varnothing $$.

 Lets call this game $$\Gamma(Y)$$, or the disjoint open ball game on $$Y$$. We will now show that when $$II$$ has a winning strategy for $$\Gamma(Y)$$ then the set $$Y$$ is countably infinite. Let $$ \sigma $$ be a winning strategy for $$\Gamma(Y)$$. Note that we may assume that $$I$$ only plays from sets from a basis, and since we have a countably basis, we may assume that $$I$$ plays from some countable basis. Let $$ W= \{ P_n \mid n \in \omega \} $$ where $$ (P_n)_{n \in \omega} $$ is an enumeration  of all playable $$ \\{ S_1, S_2\\} $$, where $$ S_i $$ are from our chosen countable basis. For $$x \in Y$$ we define 
 
  $$
  \begin{align*}
  
  B_x := \{ (n_1,...,n_k ) \in {^{<\omega} \omega} \mid &x \in \sigma(P_{n_1}),...., \\
  
  &x \in \sigma(P_{n_1},T_{n_1},...,P_{n_{k-1}}), \\
  
  &x \not\in \sigma(P_{n_1},....,P_{n_{k-1}},T_{n_{k-1}},P_{n_k}) \} 
  
  \end{align*}
  $$

Given that $$\sigma$$ is a winning strategy for $$II$$, we can see that for any $$ x \in B_x$$ and sequence $$ (n_1,...) \in {^\omega \omega} $$ that some segment $$ (n_1,...,n_k) \in B_x$$, since otherwise $$x \in \sigma(P_{n_1},...,P_{n_k})=T_{k-1}$$ for all $$k>0$$, so $$x \in \bigcap_{i>0} T_i$$ contradicting that set being empty. Hence we have condition 1, from Lemma 3. We will now show condition 2 of Lemma 3. Suppose that we have distinct 

$$x_1,x_2,x_3 \in \sigma( P_{n_1},....,P_{n_k} ) $$

for $$1 \leq k \leq m$$. We can choose playable pairs

$$ P_{n_{1,2}}=\{A_1,A_2\},P_{n_{1,3}}=\{B_1,B_3\},P_{n_{2,3}}= \{C_2,C_3\}$$

 where the index $$i$$ on the open sets says that it contains $$x_i$$ but not the $$x_j$$ where $$j \neq i$$, since we are in a metric space. And note that only one of the $$x_i=y_1$$ can be in 
 $$\sigma(P_{n_1},...,P_{n_m},P_{n_{k,l} }) $$, hence other two, $$y_2,y_3$$, are not contained in that set. This is true for each combination, so we have 
 
 $$ (n_1,...,n_m,n_{k,l}) \in \left(B_{y_2} \cap B_{y_3} \right)\setminus B_{y_1}. $$
 
  So we get that $$y_1 \not \in \{ x \mid (n_1,....,n_m,n_{k,l}) \in B_x $$, and by shuffling things around, we get that each of the three points, $$x_1,x_2,x_3$$, have cooresponding sets that they are not in, hence they are not in the intersection of all those sets. This worked for an arbitrary choice of three points, so it must be 
  
  $$ \bigcap_{n \in \omega} \{x \in Y \mid (n_1,...,n_m,n) \in B_x \}= \varnothing. $$ 
  
  Using Lemma 3, we get that the space is countable.

Let $$\Sigma$$ be a winning strategy for $$II$$ in the strong measure zero game on $$X$$. We are going to show that the strategy $$\Sigma$$ will help us construct a winning strategy $$\sigma$$ in the game $$\Gamma(X)$$, hence $$X$$ will be countable.

Say that player $$I$$ plays $$ P_1=\{S_1,S_2\} $$ in $$\Gamma(X)$$, and plays $$ J_{d(S_1,S_2)}=J_{\epsilon_1}$$ in the strong measure zero game. We will have player $$II$$ play $$A_1=\Sigma(J_{\epsilon_1})$$, and then $$ \sigma(P_1) $$ will be an element disjoint from $$A_1$$, which we can pick since the length of $$A_1$$ is less than $$d(S_1,S_2)$$. So we can define a strategy where 
$$\sigma( \{S_1^n,S_2^n\} )= S_1^n$$ if $$ \Sigma 
\left(J_{d(S_1^n,S_2^N)} \right) \cap S_1^n = \varnothing$$ and $$ \sigma \left(\{S_1^n,S_2^n\} \right)= S_2^n$$ otherwise. We will now show that this is in fact a winning strategy. Note that 

$$ \left(\bigcap_{n \in \omega} \sigma(P_1,...,P_n) \right) \cap \left( \bigcup_{n \in \omega} A_n \right) = \varnothing$$ 

but the union part covers the whole space so the intersection on the left must be empty. So player $$II$$ has a winning strategy for $$\Gamma(X)$$ when $$II$$ has a winning strategy for the strong measure zero game. Thus $$X$$ is countable.$$\square$$

**Lemma 4 (Lebesgue covering lemma).** If $$ X $$ is a compact metric space, then for any open cover of $$X$$, there exists a postive real number $$ \delta $$, the *Lebesgue number*, such that: for any $$F \subseteq X $$ of diameter less than $$ \delta $$ there is a $$U$$ in the open cover such that $$F \subseteq U$$.

*proof of Lemma 4.* This is a well known theorem, so no proof will be given. $$\square$$ 

**Theorem 2.** Player $$I$$ has a winning strategy in the strong measure zero game, if, and only if, $$X$$ is not strong measure zero.

*proof of Theorem 2.* First we will prove ($$ \Leftarrow $$), so suppose that $$X$$ is not strong measure zero. Hence there is a sequence $$ (\epsilon_n) $$ for $$n \in \omega$$ such that, such that $$X$$ for all sequences of intervals $$ (A_n) $$, for $${n \in \omega} $$, length of $$A_n$$ is less than or equal too $$ \epsilon_n $$. So have player $$I$$ plays $$J_{\epsilon_n} $$ in inning $$n$$, so player $$II$$ can not cover the space, since it will only pick intervals less than $$\epsilon_n$$ at inning $$n$$.

We will now prove ($$\Rightarrow$$), we will do the contrapositive, so we will show that if $$X$$ is strong measure zero then $$I$$ does not have a winning strategy. Let $$\sigma$$ be an arbitrary strategy for player $$I$$, and $$X$$ is strong measure zero. We will show that there is a play, by player $$II$$ that will beat this strategy. Here are some things that we are going to assume, to make the problem a bit easier:

1. That we are playing on strong measure zero sets, that are subsets of compact sets, and in fact we will assume to be working with $$ [0,1] $$. This is enough since we can write $$\mathbb {R}$$ as a countable union of compact sets, for example $$\bigcup_{i \in \mathbb Z} [i,i+1] $$, and partition the innings, into countably infinite many infinite sets (think of sets of the form $$\{p^n \mid n \in \mathbb{N} \} $$, $$p$$ prime ), so we play the strong measure zero game on the $$j$$th compact set when the inning we are in is in the $$j$$th partition.
2. We will assume that the $$J_\epsilon$$'s that are played by player $$I$$ have $$\epsilon$$'s of the form $$1/n$$, since for some $$\epsilon$$ we can just move to a smaller number of the form $$1/n$$ without losing any generality.
3. Let $$ s=(J_{\epsilon_1},...,J_{\epsilon_n},K_n) $$ be some sequence of turns, that is in the domain of player $$I$$'s strategy $$\sigma$$, then we define $$\hat\sigma(s)= \epsilon \iff \sigma(s) = J_\epsilon$$. 

We will now construct a play in which $$II$$ which beats player $$I$$ strategy $$\sigma$$. Say that $$\sigma( \varnothing)= J_{1/n_1} $$. Lets say $$ U_1 \subset J_{1/n_1}$$ is a finte open cover of $$[0,1] $$ (which exists since $$[0,1]$$ is compact). Consider $$ \min \{ \hat \sigma(K) \mid K \in U_1 \} $$, and we will choose $$m_1 \in \mathbb{N}$$ large enough so that:

1. $$n_1<m_1$$,
2. $$1/m_1 < \min \{ \hat \sigma(K) \mid K \in U_1 \} $$,
3. and $$1/m_1$$ is a Lebesgue number of the cover $$U_1$$.

Basically we are going to go down, and play every possible outcome of the strategy $$\sigma$$ possible. Let $$U_2 \subset J_{1/m_1} $$, be a finite open cover, so in particular this $$U_2$$ works as a subcover for $$\sigma(K)$$ for $$K \in U_2$$ since $$1/m_1 < \hat \sigma (K)$$. Then we are going to choose an $$ m_2  \in \mathbb N$$ large enough so that:

1. $$m_1 < m_2$$ (this also means that $$ \hat \sigma ( K ) < m_2$$ for $$K \in U_1$$, which are the corresponding "n_i" terms ),
2. $$1/m_2< \min\{ \hat \sigma (K_1,K_2) \mid K_1 \in U_1, K_2 \in U_2 \}$$,
3. And $$1/m_2$$ is a Lebesgue number of the cover $$U_2$$.  

Basically we continue in this fashion, and construct $$m_t$$, for arbitrary $$t$$ (which if that statement was good enough for you, I recommend skipping this paragraph). Suppose that we have $$m_1,...,m_{t-1}$$ constructed. Then we are going to construct $$m_t$$ by letting $$ U_t \subset J_{1/m_{t-1}} $$ be a finite open cover. Then we choose $$m_t \in \mathbb{N} $$ large enough such that:

1. $$m_{t-1} < m_t$$,
2. $$1/m_t < \min \{ \hat \sigma (K_1,...,K_t) \mid K_1 \in U_1,..., K_t \in U_t \} $$,
3. And $$1/m_t$$ is a Lebesgue number of the cover $$U_t$$.

So know we have a sequence $$(1/m_i)_{i \in \omega} $$, where each $$1/m_i$$ is a Lebesgue number of the coverings $$U_i$$. Since $$X$$ is strong measure zero we have that there is a covering  $$ \{L_i \mid i \in \omega\} $$ where each $$L_i$$ has length less than $$1/m_i$$. Since $$1/m_i$$ is a Lebesgue number of the cooresponding coverings, we can find an $$M_i \in U_i$$ such that $$L_i \subseteq M_i$$. We can choose the $$M_i$$ as our sets, and so we found a play where $$II$$ wins, hence $$\sigma $$ is not a winning strategy, and since $$\sigma$$ was arbitrary we are done.
$$\square$$


## Resources
 
 You can find out more about these sorts of things from this, *non-exhaustive*, list:
 
 * F. Galvin, Indeterminacy of point-open games, Bull. Acad. Pol. Sci., Sér. Sci. Math. Astron. Phys. 26 :5 (1978), 445–449 (this is sort of difficult to find, so included all the information, for libraries)
 * "The combinatorics of open covers (I): Ramsey theory" by Marion Scheepers, 
 * "The combinatorics of open covers (II)" by Winfried Just, Arnold W. Miller, Marion Scheepers, and Paul J. Szeptycki,
 * ...
 * "The combinatorics of open covers ($$N$$)" by ... (well there are at least 11 of these...),
 * "Ramsey theory of open covers lecture 1" by Nadav Samet and Boaz Tsaban,
 * ...
 * "Ramsey theory of open covers lecture 5" by Nadav Samet and Boaz Tsaban.
 * You can browse around [here](http://diamond.boisestate.edu/~spm/index.html)
 
 The "Ramsey theory of open covers" are more accessible and shorter than "The combinatorics of open covers..." and discuss some of the Ramsey theoretic aspects that are related to these games and to "selection principles" (which I did not discuss here, although are very related to games $$G(\mathcal A,B) $$).



[ordinals]: https://en.wikipedia.org/wiki/Ordinal_number

[ultrafilters]: https://en.wikipedia.org/wiki/Ultrafilter

[smz]: https://en.wikipedia.org/wiki/Strong_measure_zero_set

[measurezero]: https://en.wikipedia.org/wiki/Lebesgue_measure

[cantor]: https://en.wikipedia.org/wiki/Cantor_set

[cannotsmz]: http://math.stackexchange.com/questions/903973/the-cantor-set-is-not-strong-measure-zero

[luzin]: https://en.wikipedia.org/wiki/Luzin_space
