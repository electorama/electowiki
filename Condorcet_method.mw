Any election method conforming to the [[Condorcet criterion]] - that is, one which always elects the pairwise champion if such exists - is known as a '''Condorcet method'''. The name comes from the 18th century mathematician and philosopher [[Marquis de Condorcet]], although the method was previously described by [[Ramon Llull]] in the 13th century.

At present, the synonymous phrase '''"Instant Round Robin Voting" (IRRV)''' is being coined to leverage the public's greater familiarity with [[IRV | Instant Runoff Voting]] (IRV). This phrase is currently being used in a [http://groups.yahoo.com/group/Condorcet legislative effort] to implement a Condorcet variant ([[CSSD]]) in the state of Washington.

'''Condorcet''' is sometimes used to indicate the family of Condorcet methods as a whole.


== Simple Explanation ==

If one candidate defeats all others head-to-head, that candidate is the [[Condorcet Criterion|Condorcet Winner]].  This can be determined through use of ranked ballots.  In rare occasions, each candidate is defeated by at least one other (e.g. rock, paper, scissors), so there is no Condorcet Winner.  In that case it is necessary to use some tiebreaking procedure.

== Casting ballots ==

Each voter fills out a [[preferential voting|ranked ballot]].  The voter can include less than all candidates under consideration.   Usually when a candidate ''is not listed'' on the voter's ballot they are considered less preferred than listed candidates, and ranked accordingly.  However, some variations allow a "no opinion" default option where no for- or against- preference is counted for that candidate.  Write-ins are possible, but are somewhat more difficult to implement for automatic counting than in other election methods.  This is a counting issue, but results in the frequent omission of the write-in option in ballot software.


== Counting ballots ==

Ballots are counted by considering all possible sets of two-candidate elections from all available candidates.  That is, each candidate is considered against each and every other candidate.  A candidate is considered to "win" against another on a single ballot if they are ranked higher than their opponent.  All the votes for candidate Alice over candidate Bob are counted, as are all of the votes for Bob over Alice.  Whoever has the most votes in each one-on-one election wins.

If a candidate is preferred over all other candidates, that candidate is the [[Condorcet Criterion|Condorcet candidate]].  However, a Condorcet candidate may not exist, due to a fundamental [[Voting paradox|paradox]]: It is possible for the electorate to prefer A over B, B over C, and C over A simultaneously.  This is called a majority rule cycle, and it must be resolved by some other mechanism.


=== Counting with matrices ===

A frequent implementation of this method will illustrate the basic counting method.  Consider an election between A, B, and C, and a ballot (B, C, A, D).  That is, a ballot ranking B first, C second, A third, and D forth.  This can be represented as a matrix, where the row is the runner under consideration, and the column is the opponent.  The cell at (runner,opponent) has a one if runner is preferred, and a zero if not.

{| border="1"
! !! A !! B !! C !! D
|-
! A || &mdash; || 0 || 0 || 1
|-
! B || 1 || &mdash; || 1 || 1
|-
! C || 1 || 0 || &mdash; || 1
|-
! D || 0 || 0 || 0 || &mdash;
|}

Cells marked "&mdash;" are logically zero, but are blank for clarity&mdash;they are not considered, as a candidate can not be defeated by himself.  This binary matrix is inversely symmetric: (runner,opponent) is &not;(opponent,runner).  The utility of this structure is that it may be easily added to other ballots represented the same way, to give us the number of ballots which prefer each candidate.  The sum of all ballot matrixes is called the sum matrix&mdash;it is not symmetric.

When the sum matrix is found, the contest between each candidate is considered.  The number of votes for runner over opponent (runner,opponent) is compared the number of votes for opponent over runner (opponent,runner).  The one-on-one winner has the most votes.  If one candidate wins against all other candidates, that candidate wins the election.

The sum of all ballot matrices, the '''Condorcet pairwise matrix''', is the primary piece of data used to resolve majority rule cycles.


== Key terms in ambiguity resolution ==

Handling cases where there is not a single Condorcet winner is called ambiguity resolution in this article, though other phrases such as "cyclic ambiguity resolution" and "Condorcet completion" are used as well.

The following are key terms when discussing ambiguity resolution methods:
* '''[[Smith set]]''':  the smallest set of candidates in a particular election who, when paired off in pairwise elections, can beat all other candidates outside the set.
* '''[[Schwartz set]]''': the union of all possible sets of candidates such that for every set:
*# every candidate inside the set is pairwise unbeatable by any other candidate outside the set, i.e., ties are allowed
*# no proper (smaller) subset of the set fulfills the first property 
* '''Cloneproof''': a method that is immune to the presence of '''clones''' (candidates which are essentially identical to each other).  In some voting methods, a party can increase its odds of selection if it provides a large number of "identical" options.  A cloneproof voting method prevents this attack. See [[strategic nomination]].


== Different ambiguity resolution methods ==

There are a countless number of "Condorcet methods" possible that resolve such ambiguities. The fact that Marquis de Condorcet himself already spearheaded the debate of which particular Condorcet method to promote has made the term "Condorcet's method" ambiguous.
Indeed, it can be argued that the large number of different competing Condorcet methods has made the adoption of any single method extremely difficult.

Examples of Condorcet methods include:
* '''[[Black]]''' chooses the Condorcet winner when it exists and otherwise the [[Borda count|Borda winner]]. It is named after Duncan Black.
* '''[[Baldwin]]''' Computes the [[Borda count]] for all candidates, then iteratively deletes the candidate with the lowest count.
* '''[[Smith/IRV]]''' is [[instant-runoff voting]] with the candidates restricted to the Smith set.
* '''[[Copeland's method|Copeland]]''' selects the candidate that wins the most pairwise matchups.  Note that if there is no Condorcet winner, Copeland will often still result in a tie.
* '''[[Llull-Approval Voting]]'''- Elects the member of the [[Schwartz set]] with the greatest number of approvals
* '''[[Minmax|Minimax]]''' (also called '''Simpson''') chooses the candidate whose worst pairwise defeat is less bad than that of all other candidates.<sup>1</sup>
* '''Smith/Minimax''' restricts the Minimax algorithm to the Smith set.<sup>1</sup>
* '''[[Ranked Pairs]]''' (RP) or '''Tideman''' (named after [[Nicolaus Tideman]]) with variations such as '''[[Maximize Affirmed Majorities]]''' (MAM) and  '''[[Maximum Majority Voting]]''' (MMV)<sup>1</sup>
* '''[[Schulze method|Schulze]]''' with several reformulations/variations, including '''Schwartz Sequential Dropping (SSD)''' and '''Cloneproof Schwartz Sequential Dropping (CSSD)'''<sup>1</sup>
* '''[[Approval-Condorcet Hybrids]]''', such as '''[[Definite Majority Choice]]''', use an [[Approval Cutoff]] to augment the Condorcet pair wise array.  Many believe that such a method would  make a good first-round public proposal.

<sup>1</sup> There are different ways to measure the strength of each defeat in some methods.  Some use the margin of defeat (the difference between votes for and votes against), while others use winning votes (the votes favoring the defeat in question).
Electionmethods.org argues that there are several disadvantages of systems that use margins instead of winning votes.
The website argues that using margins "destroys" some information about majorities, so that the method can no longer honor information about what majorities have determined and that consequently margin-based systems cannot support a number of desirable voting properties.

Ranked Pairs and Schulze are procedurally in some sense opposite approaches:
* Ranked Pairs (and variants) starts with the strongest information available and uses as much information as it can without creating ambiguity
* Schulze (and variants) repeatedly removes the weakest ambiguous information until ambiguity is removed.

The text below describes (variants of) these methods in more detail.

== Ranked Pairs, Maximize Affirmed Majorities (MAM), and Maximum Majority Voting (MMV) ==

In the Ranked Pairs (RP) voting method, as well as the variations Maximize Affirmed Majorities (MAM)
and Maximum Majority Voting (MMV), pairs of defeats are ranked (sorted)
from largest majority to smallest majority.
Then each pair is considered, starting with the defeat supported by the largest majority.
Pairs are "affirmed" only if they do not create a cycle with the pairs already affirmed.
Once completed, the affirmed pairs are followed to determine the winner.

In essence, RP and its variants (such as MAM and MMV)
treat each majority preference as evidence that the majority's more preferred 
alternative should finish over the majority's less preferred alternative, the weight of 
the evidence depending on the size of the majority.

The difference betweeen RP and its variants is in the details of the ranking approach.
Some definitions of RP use margins, while other definitions use winning votes (not margins).
Both MAM and MMV are explicitly defined in terms of winning votes, not winning margins.
In MAM and MMV, if two defeat pairs have the same number of votes for a victory, the defeat with
the smaller defeat is ranked higher.
If this still doesn't disambiguate between the two, MAM and MMV perform slightly differently.
In MAM, information from a "tiebreaker" vote is used
(which could be a distinguished vote such as the vote of a "speaker",
but unless there is a distinguished vote, a randomly-chosen vote is used).
In MMV all such conflicting matchups are ignored (though any non-conflicting matchups of that size are still included).


== Schulze method ==

The [[Schulze method]] resolves votes as follows:

# First, determine the Schwartz set (the innermost unbeaten set). If no defeats exist among the Schwartz set, then its members are the winners (plural only in the case of a tie, which must be resolved by another method).
# Otherwise, drop the weakest defeat information among the Schwartz set (i.e., where the number of votes favoring the defeat is the smallest). Determine the new Schwartz set, and repeat the procedure.

In other words, this procedure repeatedly throws away the narrowest defeats, until finally the largest number of votes left over produce an unambiguous decision.


== Related terms ==

Other terms related to the Condorcet method are:
* '''Condorcet loser''': the candidate who is less preferred than every other candidate in a pair wise matchup.
* '''weak Condorcet winner''': a candidate who beats or ties with every other candidate in a pair wise matchup. There can be more than one weak Condorcet winner.
* '''weak Condorcet loser''': a candidate who is defeated by or ties with every other candidate in a pair wise matchup. Similarly, there can be more than one weak Condorcet loser.


== An example ==

Imagine an election for the capital of Tennessee, a state in the United States that is over 500 miles east-to-west, and only 110 miles north-to-south.  Let's say the candidates for the capital are Memphis (on the far west end), Nashville (in the center), Chattanooga (129 miles southeast of Nashville), and Knoxville (on the far east side, 114 northeast of Chattanooga).    Here's the population breakdown by metro area (surrounding county): 
<div style="float:right;  padding:2px; text-align:center">
[[Image:CondorcetTennesee.png]]</div>

* Memphis (Shelby County): 826,330
* Nashville (Davidson County): 510,784
* Chattanooga (Hamilton County): 285,536
* Knoxville (Knox County): 335,749

Let's say that in the vote, the voters vote based on geographic proximity.  Assuming that the population distribution of the rest of Tennessee follows from those population centers, one could easily envision an election where the percentages of votes would be as follows:

<table border=1>
<tr>
<td>
'''42% of voters (close to Memphis)'''<br>
1. Memphis<br>
2. Nashville<br>
3. Chattanooga<br>
4. Knoxville
</td>
<td valign="top">
'''26% of voters (close to Nashville)'''<br>
1. Nashville<br>
2. Chattanooga<br>
3. Knoxville<br>
4. Memphis
</td>
<td>
'''15% of voters (close to Chattanooga)'''<br>
1. Chattanooga<br>
2. Knoxville<br>
3. Nashville<br>
4. Memphis
</td>
<td>
'''17% of voters (close to Knoxville)'''<br>
1. Knoxville<br>
2. Chattanooga<br>
3. Nashville<br>
4. Memphis
</td>
</tr>
</table>

The results would be tabulated as follows:
<table BORDER><caption>Pairwise Election Results</caption>
<tr><th colspan=2><th colspan=4 bgcolor="#c0c0ff">A</tr>

<tr>
<th colspan=2><th bgcolor="#c0c0ff">Memphis
<th bgcolor="#c0c0ff">Nashville
<th bgcolor="#c0c0ff">Chattanooga
<th bgcolor="#c0c0ff">Knoxville
</tr>
<tr><th  bgcolor="#ffc0c0" rowspan=4>B<th bgcolor="#ffc0c0">Memphis<td><td nowrap bgcolor="#e0e0ff">[A] 58% <br>[B] 42% <br><td nowrap bgcolor="#e0e0ff">[A] 58% <br>[B] 42% <br><td nowrap bgcolor="#e0e0ff">[A] 58% <br>[B] 42% <br></tr>
<tr><th bgcolor="#ffc0c0">Nashville<td nowrap bgcolor="#ffe0e0">[A] 42% <br>[B] 58% <br><td><td nowrap bgcolor="#ffe0e0">[A] 32% <br>[B] 68% <br><td nowrap bgcolor="#ffe0e0">[A] 32% <br>[B] 68% <br></tr>

<tr><th bgcolor="#ffc0c0">Chattanooga<td nowrap bgcolor="#ffe0e0">[A] 42% <br>[B] 58% <br><td nowrap bgcolor="#e0e0ff">[A] 68% <br>[B] 32% <br><td><td nowrap bgcolor="#ffe0e0">[A] 17% <br>[B] 83% <br></tr>
<tr><th bgcolor="#ffc0c0">Knoxville<td nowrap bgcolor="#ffe0e0">[A] 42% <br>[B] 58% <br><td nowrap bgcolor="#e0e0ff">[A] 68% <br>[B] 32% <br><td nowrap bgcolor="#e0e0ff">[A] 83% <br>[B] 17% <br><td></tr>
<tr><th colspan=2 bgcolor="#c0c0ff">Ranking (by repeatedly removing Condorcet winner):

<td bgcolor="#ffffff">4th
<td bgcolor="#ffffff">1st
<td bgcolor="#ffffff">2nd
<td bgcolor="#ffffff">3rd
</table>

* [A] indicates voters who preferred the candidate listed in the column caption to the candidate listed in the row caption
* [B] indicates voters who preferred the candidate listed in the row caption to the candidate listed in the column caption

In this election, Nashville is the Condorcet winner and thus the winner under all possible Condorcet methods. 


== Use of Condorcet voting ==

Condorcet voting is not currently used in government elections.  However, it is starting to receive support in some public organizations. Organizations which currently use some variant of the Condorcet method are:

# The [http://www.debian.org/ Debian] project uses the [[Schulze method]].
# The [http://www.spi-inc.org/ Software in the Public Interest (SPI)] project uses the [[Schulze method]].
# The [http://www.gentoo.org/ Gentoo Linux] project uses the [[Schulze method]].
# The [http://www.userlinux.com/ UserLinux] project uses the [[Schulze method]].
# The Free State Project used a Condorcet method for choosing its target state
# The voting procedure for the uk.* hierarchy of Usenet
#[http://www.rsabey.pwp.blueyonder.co.uk/rpc/fscc/ Five-Second Crossword Competition]
{{fromwikipedia}}

== External links ==

* [http://condorcet.ericgorr.net Condorcet Voting Calculator] by Eric Gorr
* [http://robla.net/1996/politics/condorcet.html Condorcet's Method] by Rob Lanphier
* [http://accuratedemocracy.com/ Accurate Democracy] by Rob Loring
* [http://fc.antioch.edu/~james_green-armytage/voting.htm Voting methods resource page] by James Green-Armytage
* [http://radicalcentrism.org/majority_voting.html Maximum Majority Voting] by Ernest Prabhakar
* [http://www.mcs.vuw.ac.nz/~ncj/comp303/schulze.pdf A New Monotonic and Clone-Independent Single-Winner Election Method] ([[Portable Document Format|PDF]]) by Markus Schulze ([http://www.citizensassembly.bc.ca/resources/submissions/csharman-10_0409201706-143.pdf mirror1], [http://lists.gnu.org/archive/html/demexp-dev/2003-09/pdflQW7IlpAfC.pdf mirror2])
* [http://www.OpenSTV.org/ OpenSTV] -- Software for computing Condorcet methods and STV by Jeffrey O'Neill
* [http://www5.cs.cornell.edu/~andru/civs/ CIVS, a free web poll service using the Condorcet method] by Andrew Myers
* [http://www1.fee.uva.nl/creed/pdffiles/MoulinCh4Elferink.pdf Voting and Social Choice] Demonstration and commentary on Condorcet method. ([[Portable Document Format|PDF]]) By Herve Moulin
* [http://groups.yahoo.com/group/Condorcet Yahoo work group] Helping a WA state legislator to draft Condorcet election rules to replace recently nullified statute. Moderated by Jeffry R. Fisher
