---

---

## Background
Originally, my first post was going to be an introduction to selection principles, especially those in topology, and a few other related concepts. I decided I could not really do justice to the subject in one post (with my minimal knowledge), and have opted to present some very cool results, that give a taste of the ideas that one would run across when studying things like selection principles. 

 **Definition of the game \\(G_1( \cal A, \cal B) \\)** Let \\( \mathcal{A}\\) and \\(\mathcal{B} \\) be collections of sets, we define the game \\(G_1(\cal{A}, \cal{B})\\) to be a game with two players that we will denote \\(I\\) and \\(II\\), and the game will have [\\(\omega\\) innings](https://en.wikipedia.org/wiki/Ordinal_number), where each inning consists of a turn by \\(I\\) and then a turn by \\(II\\). By \\(\omega\\) innings we mean there is an inning for each \\(0,1,2,3, \dots \\) (if you prefer \\(\omega = \mathbb N\\)). The innings follow this pattern: player \\(I\\) starts off, in inning \\(n\\), by presenting a set \\(A_n\\) from \\(\cal A\\) which marks the end of player \\(I\\)'s turn, and then player \\(II\\) picks an \\(a_n \in  A_n\\). At the end of the \\(\omega\\) innings we are left with a play \\[(A_0,a_0, \dots , A_i, a_i, \dots)\\]
 of what happened in that game. Player \\(II\\) wins if \\( \\{ a_i \mid i \in \omega \\} \in \cal B\\) and \\(I\\) wins otherwise.
 
A couple of examples to consider:

* Let \\(D\\) consist of all dense subsets of \\( \mathbb R \\). Consider \\(G_1 (D,D) \\).
* Let \\(X\\) be a countable subset of some topological space \\(Y\\) and \\({\cal{O}}_Y\\) is the set of all open covers of \\(Y\\), and \\({\cal {O}}_X\\) the set of covers for \\(X\\). Consider \\(G_1( {\cal{O}}_Y, {\cal{O}}_X) \\).
* Let \\( U \\) be an [ultrafilter](https://en.wikipedia.org/wiki/Ultrafilter) on some set. Consider \\(G_1(U,U) \\).
* etc. You can come up with your own...
 

A strategy for a player is a function that takes what has been played and outputs the next move. So \\( s_1,s_2\\) will be strategies for players \\(I,II\\) respectively, and \\(s_1: \varnothing \mapsto A_0 \\), and \\( s_1: (A_0,a_0,...,A_i,a_i) \mapsto A_{i+1}\\). We get a similar description for \\(s_2\\). Basically they are instructions on a game trees that tell the player what to do next given where they are in the game tree. We call \\(s_i\\) a winning strategy provided the cooresponding player will *always* win following that strategy. It is interesting that in some games there is no winning strategy for either player, and in fact the two main theorems that will be presented will give such an example(assuming [Borel's conjecture](https://en.wikipedia.org/wiki/Strong_measure_zero_set) is false)
Do any of the above examples have winning strategies for one of the players?

 Definition of strong measure zero:
 : A set \\(X \subseteq \mathbb R\\) is strong measure zero if, for all sequences \\( ( \epsilon_n \mid n  \in \omega) \\) of positive real numbers, then there exists a sequence of intervals \\(I_n\\), where the length of \\(I_n\\) is less than \\(\epsilon_n \\) for all \\(N\\), and \\(A \subseteq  \cup_{n \in \omega} I_n\\).
 
 Every strong measure zero set is [Lebesgue measure zero](https://en.wikipedia.org/wiki/Lebesgue_measure), although not every measure zero set is strong measure zero, the [Cantor set](https://en.wikipedia.org/wiki/Cantor_set) provides [such an example](http://math.stackexchange.com/questions/903973/the-cantor-set-is-not-strong-measure-zero). It is also easy to see that every countable set is strong measure zero. In fact [Borel's conjecture](https://en.wikipedia.org/wiki/Strong_measure_zero_set) actually conjectured that every strong measure zero set was countable. That conjecture ended up being independent of the usual axioms, ZFC, so it is consistent for there to be uncountable strong measure zero sets, and consistent for there to be only countable strong measure zero sets. [Luzin sets](https://en.wikipedia.org/wiki/Luzin_space) provide examples of strong measure zero sets that are not countable.
 
 Let \\(J_\epsilon\\), \\(\epsilon >0\\), be the set of all intervals of length less than \\(\epsilon\\), and say \\({\mathcal{J}}:= \\{J_\epsilon \mid \epsilon >0 \\} \\), and \\({\mathcal O}_X \\) the set of open covers of some set \\(X \subseteq \mathbb R\\). 
 
 Definition of the strong measure zero game:
 : Let \\(X\\) be strong measure zero. Then the strong measure zero game is \\(G_1( {\mathcal J}, {\mathcal O}_X)\\).

A very natural question to ask is when does player \\(I\\) have a winning strategy, and when does player \\(II\\) have a winning strategy in \\(G_1( {\mathcal J}, {\mathcal O}_X)\\).
 
 
**Theorem 1.** Player \\(II\\) has a winning strategy in the strong measure zero game, if, and only if, \\(X\\) is countable.

**Theorem 2.** Player \\(I\\) has a winning strategy in the strong measure zero game, if, and only if, \\(X\\) is not strong measure zero.

One of the things that makes these two results interesting is that they show that it is *consistent* in ZFC for there to be a set where neither player has a winning strategy, since it is consistent that there are uncountable strong measure zero sets (and it is also consistent that there are only countable strong measure zero sets). So the Luzin sets mentioned before would give examples of sets where neither player has a winning strategy.

## The Proofs of Theorem 1 and 2
The proofs of Thm 1 and 2, that will be presented, have been attributed to Galvin, not sure what paper(s) though.* I found out about this proof in a class, taught by Marion Scheepers, in a class on selection principles in topology a few years ago.

Lemma 1.1 :
: df

*proof of Theorem 1.*

Lemma 2.1 Lebesgue covering lemma) :
: dfd

*proof of Theorem 2.*
 
 If this got you interested, you can find out more about these sorts of things from 
 
 * "The combinatorics of open covers (I): Ramsey theory" by Marion Scheepers, 
 * "The combinatorics of open covers (II)" by Winfried Just, Arnold W. Miller, Marion Scheepers, and Paul J. Szeptycki,
 * ...
 * "The combinatorics of open covers (\\(N\\))" by ... (well there is at least 11 of these...),
 * "Ramsey theory of open covers lecture 1" by Nadav Samet and Boaz Tsaban
 * ...
 * "Ramsey theory of open covers lecture 5" by Nadav Samet and Boaz Tsaban.
 * And you can browse around [here](http://diamond.boisestate.edu/~spm/index.html)
 
*I think the proof is in : `F. Galvin, Indeterminacy of point-open games, Bull. Acad. Pol. Sci., Sér. Sci. Math. Astron. Phys. 26 :5 (1978), 445–449` based on some citations, that paper proved the duality of the games used to prove Thm 1. I have not been able to find a copy of the paper though, or the results explicitly cited.