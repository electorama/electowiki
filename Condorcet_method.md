Any election method conforming to the [Condorcet
criterion](Condorcet_criterion "wikilink") - that is, one which always
elects the pairwise champion if such exists - is known as a **Condorcet
method**. The name comes from the 18th century mathematician and
philosopher [Marquis de Condorcet](Marquis_de_Condorcet "wikilink"),
although the method was previously described by [Ramon
Llull](Ramon_Llull "wikilink") in the 13th century.

At present, the synonymous phrase **“Instant Round Robin Voting”
(IRRV)** is being coined to leverage the public's greater familiarity
with [ Instant Runoff Voting](IRV "wikilink") (IRV). This phrase is
currently being used in a [legislative
effort](http://groups.yahoo.com/group/Condorcet) to implement a
Condorcet variant ([CSSD](CSSD "wikilink")) in the state of Washington.

**Condorcet** is sometimes used to indicate the family of Condorcet
methods as a whole.

## Simple Explanation

If one candidate defeats all others head-to-head, that candidate is the
[Condorcet Winner](Condorcet_Criterion "wikilink"). This can be
determined through use of ranked ballots. In rare occasions, each
candidate is defeated by at least one other (e.g. rock, paper,
scissors), so there is no Condorcet Winner. In that case it is necessary
to use some tiebreaking procedure.

## Casting ballots

Each voter fills out a [ranked ballot](preferential_voting "wikilink").
The voter can include less than all candidates under consideration.
Usually when a candidate *is not listed* on the voter's ballot they are
considered less preferred than listed candidates, and ranked
accordingly. However, some variations allow a “no opinion” default
option where no for- or against- preference is counted for that
candidate. Write-ins are possible, but are somewhat more difficult to
implement for automatic counting than in other election methods. This is
a counting issue, but results in the frequent omission of the write-in
option in ballot software.

## Counting ballots

Ballots are counted by considering all possible sets of two-candidate
elections from all available candidates. That is, each candidate is
considered against each and every other candidate. A candidate is
considered to “win” against another on a single ballot if they are
ranked higher than their opponent. All the votes for candidate Alice
over candidate Bob are counted, as are all of the votes for Bob over
Alice. Whoever has the most votes in each one-on-one election wins.

If a candidate is preferred over all other candidates, that candidate is
the [Condorcet candidate](Condorcet_Criterion "wikilink"). However, a
Condorcet candidate may not exist, due to a fundamental
[paradox](Voting_paradox "wikilink"): It is possible for the electorate
to prefer A over B, B over C, and C over A simultaneously. This is
called a majority rule cycle, and it must be resolved by some other
mechanism.

### Counting with matrices

A frequent implementation of this method will illustrate the basic
counting method. Consider an election between A, B, and C, and a ballot
(B, C, A, D). That is, a ballot ranking B first, C second, A third, and
D forth. This can be represented as a matrix, where the row is the
runner under consideration, and the column is the opponent. The cell at
(runner,opponent) has a one if runner is preferred, and a zero if not.

<table>
<thead>
<tr class="header">
<th></th>
<th><p>A</p></th>
<th><p>B</p></th>
<th><p>C</p></th>
<th><p>D</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>A</p></td>
<td><p>—</p></td>
<td><p>0</p></td>
<td><p>0</p></td>
<td><p>1</p></td>
</tr>
<tr class="even">
<td><p>B</p></td>
<td><p>1</p></td>
<td><p>—</p></td>
<td><p>1</p></td>
<td><p>1</p></td>
</tr>
<tr class="odd">
<td><p>C</p></td>
<td><p>1</p></td>
<td><p>0</p></td>
<td><p>—</p></td>
<td><p>1</p></td>
</tr>
<tr class="even">
<td><p>D</p></td>
<td><p>0</p></td>
<td><p>0</p></td>
<td><p>0</p></td>
<td><p>—</p></td>
</tr>
</tbody>
</table>

Cells marked “—” are logically zero, but are blank for clarity—they are
not considered, as a candidate can not be defeated by himself. This
binary matrix is inversely symmetric: (runner,opponent) is
¬(opponent,runner). The utility of this structure is that it may be
easily added to other ballots represented the same way, to give us the
number of ballots which prefer each candidate. The sum of all ballot
matrixes is called the sum matrix—it is not symmetric.

When the sum matrix is found, the contest between each candidate is
considered. The number of votes for runner over opponent
(runner,opponent) is compared the number of votes for opponent over
runner (opponent,runner). The one-on-one winner has the most votes. If
one candidate wins against all other candidates, that candidate wins the
election.

The sum of all ballot matrices, the **Condorcet pairwise matrix**, is
the primary piece of data used to resolve majority rule cycles.

## Key terms in ambiguity resolution

Handling cases where there is not a single Condorcet winner is called
ambiguity resolution in this article, though other phrases such as
“cyclic ambiguity resolution” and “Condorcet completion” are used as
well.

The following are key terms when discussing ambiguity resolution
methods:

  - **[Smith set](Smith_set "wikilink")**: the smallest set of
    candidates in a particular election who, when paired off in pairwise
    elections, can beat all other candidates outside the set.
  - **[Schwartz set](Schwartz_set "wikilink")**: the union of all
    possible sets of candidates such that for every set:
    1.  every candidate inside the set is pairwise unbeatable by any
        other candidate outside the set, i.e., ties are allowed
    2.  no proper (smaller) subset of the set fulfills the first
        property
  - **Cloneproof**: a method that is immune to the presence of
    **clones** (candidates which are essentially identical to each
    other). In some voting methods, a party can increase its odds of
    selection if it provides a large number of “identical” options. A
    cloneproof voting method prevents this attack. See [strategic
    nomination](strategic_nomination "wikilink").

## Different ambiguity resolution methods

There are a countless number of “Condorcet methods” possible that
resolve such ambiguities. The fact that Marquis de Condorcet himself
already spearheaded the debate of which particular Condorcet method to
promote has made the term “Condorcet's method” ambiguous. Indeed, it can
be argued that the large number of different competing Condorcet methods
has made the adoption of any single method extremely difficult.

Examples of Condorcet methods include:

  - **[Black](Black "wikilink")** chooses the Condorcet winner when it
    exists and otherwise the [Borda winner](Borda_count "wikilink"). It
    is named after Duncan Black.
  - **[Baldwin](Baldwin "wikilink")** Computes the [Borda
    count](Borda_count "wikilink") for all candidates, then iteratively
    deletes the candidate with the lowest count.
  - **[Smith/IRV](Smith/IRV "wikilink")** is [instant-runoff
    voting](instant-runoff_voting "wikilink") with the candidates
    restricted to the Smith set.
  - **[Copeland](Copeland's_method "wikilink")** selects the candidate
    that wins the most pairwise matchups. Note that if there is no
    Condorcet winner, Copeland will often still result in a tie.
  - **[Llull-Approval Voting](Llull-Approval_Voting "wikilink")**-
    Elects the member of the [Schwartz set](Schwartz_set "wikilink")
    with the greatest number of approvals
  - **[Minimax](Minmax "wikilink")** (also called **Simpson**) chooses
    the candidate whose worst pairwise defeat is less bad than that of
    all other candidates.<sup>1</sup>
  - **Smith/Minimax** restricts the Minimax algorithm to the Smith
    set.<sup>1</sup>
  - **[Ranked Pairs](Ranked_Pairs "wikilink")** (RP) or **Tideman**
    (named after [Nicolaus Tideman](Nicolaus_Tideman "wikilink")) with
    variations such as **[Maximize Affirmed
    Majorities](Maximize_Affirmed_Majorities "wikilink")** (MAM) and
    **[Maximum Majority Voting](Maximum_Majority_Voting "wikilink")**
    (MMV)<sup>1</sup>
  - **[Schulze](Schulze_method "wikilink")** with several
    reformulations/variations, including **Schwartz Sequential Dropping
    (SSD)** and **Cloneproof Schwartz Sequential Dropping
    (CSSD)**<sup>1</sup>
  - **[Approval-Condorcet
    Hybrids](Approval-Condorcet_Hybrids "wikilink")**, such as
    **[Definite Majority Choice](Definite_Majority_Choice "wikilink")**,
    use an [Approval Cutoff](Approval_Cutoff "wikilink") to augment the
    Condorcet pair wise array. Many believe that such a method would
    make a good first-round public proposal.

<sup>1</sup> There are different ways to measure the strength of each
defeat in some methods. Some use the margin of defeat (the difference
between votes for and votes against), while others use winning votes
(the votes favoring the defeat in question). Electionmethods.org argues
that there are several disadvantages of systems that use margins instead
of winning votes. The website argues that using margins “destroys” some
information about majorities, so that the method can no longer honor
information about what majorities have determined and that consequently
margin-based systems cannot support a number of desirable voting
properties.

Ranked Pairs and Schulze are procedurally in some sense opposite
approaches:

  - Ranked Pairs (and variants) starts with the strongest information
    available and uses as much information as it can without creating
    ambiguity
  - Schulze (and variants) repeatedly removes the weakest ambiguous
    information until ambiguity is removed.

The text below describes (variants of) these methods in more
detail.

## Ranked Pairs, Maximize Affirmed Majorities (MAM), and Maximum Majority Voting (MMV)

In the Ranked Pairs (RP) voting method, as well as the variations
Maximize Affirmed Majorities (MAM) and Maximum Majority Voting (MMV),
pairs of defeats are ranked (sorted) from largest majority to smallest
majority. Then each pair is considered, starting with the defeat
supported by the largest majority. Pairs are “affirmed” only if they do
not create a cycle with the pairs already affirmed. Once completed, the
affirmed pairs are followed to determine the winner.

In essence, RP and its variants (such as MAM and MMV) treat each
majority preference as evidence that the majority's more preferred
alternative should finish over the majority's less preferred
alternative, the weight of the evidence depending on the size of the
majority.

The difference betweeen RP and its variants is in the details of the
ranking approach. Some definitions of RP use margins, while other
definitions use winning votes (not margins). Both MAM and MMV are
explicitly defined in terms of winning votes, not winning margins. In
MAM and MMV, if two defeat pairs have the same number of votes for a
victory, the defeat with the smaller defeat is ranked higher. If this
still doesn't disambiguate between the two, MAM and MMV perform slightly
differently. In MAM, information from a “tiebreaker” vote is used (which
could be a distinguished vote such as the vote of a “speaker”, but
unless there is a distinguished vote, a randomly-chosen vote is used).
In MMV all such conflicting matchups are ignored (though any
non-conflicting matchups of that size are still included).

## Schulze method

The [Schulze method](Schulze_method "wikilink") resolves votes as
follows:

1.  First, determine the Schwartz set (the innermost unbeaten set). If
    no defeats exist among the Schwartz set, then its members are the
    winners (plural only in the case of a tie, which must be resolved by
    another method).
2.  Otherwise, drop the weakest defeat information among the Schwartz
    set (i.e., where the number of votes favoring the defeat is the
    smallest). Determine the new Schwartz set, and repeat the procedure.

In other words, this procedure repeatedly throws away the narrowest
defeats, until finally the largest number of votes left over produce an
unambiguous decision.

## Related terms

Other terms related to the Condorcet method are:

  - **Condorcet loser**: the candidate who is less preferred than every
    other candidate in a pair wise matchup.
  - **weak Condorcet winner**: a candidate who beats or ties with every
    other candidate in a pair wise matchup. There can be more than one
    weak Condorcet winner.
  - **weak Condorcet loser**: a candidate who is defeated by or ties
    with every other candidate in a pair wise matchup. Similarly, there
    can be more than one weak Condorcet loser.

## An example

Imagine an election for the capital of Tennessee, a state in the United
States that is over 500 miles east-to-west, and only 110 miles
north-to-south. Let's say the candidates for the capital are Memphis (on
the far west end), Nashville (in the center), Chattanooga (129 miles
southeast of Nashville), and Knoxville (on the far east side, 114
northeast of Chattanooga). Here's the population breakdown by metro area
(surrounding county):

<div style="float:right;  padding:2px; text-align:center">

![CondorcetTennesee.png](CondorcetTennesee.png
"fig:CondorcetTennesee.png")

</div>

  - Memphis (Shelby County): 826,330
  - Nashville (Davidson County): 510,784
  - Chattanooga (Hamilton County): 285,536
  - Knoxville (Knox County): 335,749

Let's say that in the vote, the voters vote based on geographic
proximity. Assuming that the population distribution of the rest of
Tennessee follows from those population centers, one could easily
envision an election where the percentages of votes would be as follows:

<table border=1>

<tr>

<td>

**42% of voters (close to Memphis)**  
1\. Memphis  
2\. Nashville  
3\. Chattanooga  
4\. Knoxville

</td>

<td valign="top">

**26% of voters (close to Nashville)**  
1\. Nashville  
2\. Chattanooga  
3\. Knoxville  
4\. Memphis

</td>

<td>

**15% of voters (close to Chattanooga)**  
1\. Chattanooga  
2\. Knoxville  
3\. Nashville  
4\. Memphis

</td>

<td>

**17% of voters (close to Knoxville)**  
1\. Knoxville  
2\. Chattanooga  
3\. Nashville  
4\. Memphis

</td>

</tr>

</table>

The results would be tabulated as follows:

<table BORDER>

<caption>

Pairwise Election Results

</caption>

<tr>

<th colspan=2>

<th colspan=4 bgcolor="#c0c0ff">

A

</tr>

<tr>

<th colspan=2>

<th bgcolor="#c0c0ff">

Memphis

<th bgcolor="#c0c0ff">

Nashville

<th bgcolor="#c0c0ff">

Chattanooga

<th bgcolor="#c0c0ff">

Knoxville

</tr>

<tr>

<th  bgcolor="#ffc0c0" rowspan=4>

B

<th bgcolor="#ffc0c0">

Memphis

<td>

<td nowrap bgcolor="#e0e0ff">

\[A\] 58%  
\[B\] 42%  

<td nowrap bgcolor="#e0e0ff">

\[A\] 58%  
\[B\] 42%  

<td nowrap bgcolor="#e0e0ff">

\[A\] 58%  
\[B\] 42%  

</tr>

<tr>

<th bgcolor="#ffc0c0">

Nashville

<td nowrap bgcolor="#ffe0e0">

\[A\] 42%  
\[B\] 58%  

<td>

<td nowrap bgcolor="#ffe0e0">

\[A\] 32%  
\[B\] 68%  

<td nowrap bgcolor="#ffe0e0">

\[A\] 32%  
\[B\] 68%  

</tr>

<tr>

<th bgcolor="#ffc0c0">

Chattanooga

<td nowrap bgcolor="#ffe0e0">

\[A\] 42%  
\[B\] 58%  

<td nowrap bgcolor="#e0e0ff">

\[A\] 68%  
\[B\] 32%  

<td>

<td nowrap bgcolor="#ffe0e0">

\[A\] 17%  
\[B\] 83%  

</tr>

<tr>

<th bgcolor="#ffc0c0">

Knoxville

<td nowrap bgcolor="#ffe0e0">

\[A\] 42%  
\[B\] 58%  

<td nowrap bgcolor="#e0e0ff">

\[A\] 68%  
\[B\] 32%  

<td nowrap bgcolor="#e0e0ff">

\[A\] 83%  
\[B\] 17%  

<td>

</tr>

<tr>

<th colspan=2 bgcolor="#c0c0ff">

Ranking (by repeatedly removing Condorcet winner):

<td bgcolor="#ffffff">

4th

<td bgcolor="#ffffff">

1st

<td bgcolor="#ffffff">

2nd

<td bgcolor="#ffffff">

3rd

</table>

  - \[A\] indicates voters who preferred the candidate listed in the
    column caption to the candidate listed in the row caption
  - \[B\] indicates voters who preferred the candidate listed in the row
    caption to the candidate listed in the column caption

In this election, Nashville is the Condorcet winner and thus the winner
under all possible Condorcet methods.

## Use of Condorcet voting

Condorcet voting is not currently used in government elections. However,
it is starting to receive support in some public organizations.
Organizations which currently use some variant of the Condorcet method
are:

1.  The [Debian](http://www.debian.org/) project uses the [Schulze
    method](Schulze_method "wikilink").
2.  The [Software in the Public Interest (SPI)](http://www.spi-inc.org/)
    project uses the [Schulze method](Schulze_method "wikilink").
3.  The [Gentoo Linux](http://www.gentoo.org/) project uses the [Schulze
    method](Schulze_method "wikilink").
4.  The [UserLinux](http://www.userlinux.com/) project uses the [Schulze
    method](Schulze_method "wikilink").
5.  The Free State Project used a Condorcet method for choosing its
    target state
6.  The voting procedure for the uk.\* hierarchy of Usenet
7.  [Five-Second Crossword
    Competition](http://www.rsabey.pwp.blueyonder.co.uk/rpc/fscc/)

{{fromwikipedia}}

## External links

  - [Condorcet Voting Calculator](http://condorcet.ericgorr.net) by Eric
    Gorr
  - [Condorcet's Method](http://robla.net/1996/politics/condorcet.html)
    by Rob Lanphier
  - [Accurate Democracy](http://accuratedemocracy.com/) by Rob Loring
  - [Voting methods resource
    page](http://fc.antioch.edu/~james_green-armytage/voting.htm) by
    James Green-Armytage
  - [Maximum Majority
    Voting](http://radicalcentrism.org/majority_voting.html) by Ernest
    Prabhakar
  - [A New Monotonic and Clone-Independent Single-Winner Election
    Method](http://www.mcs.vuw.ac.nz/~ncj/comp303/schulze.pdf)
    ([PDF](Portable_Document_Format "wikilink")) by Markus Schulze
    ([mirror1](http://www.citizensassembly.bc.ca/resources/submissions/csharman-10_0409201706-143.pdf),
    [mirror2](http://lists.gnu.org/archive/html/demexp-dev/2003-09/pdflQW7IlpAfC.pdf))
  - [OpenSTV](http://www.OpenSTV.org/) -- Software for computing
    Condorcet methods and STV by Jeffrey O'Neill
  - [CIVS, a free web poll service using the Condorcet
    method](http://www5.cs.cornell.edu/~andru/civs/) by Andrew Myers
  - [Voting and Social
    Choice](http://www1.fee.uva.nl/creed/pdffiles/MoulinCh4Elferink.pdf)
    Demonstration and commentary on Condorcet method.
    ([PDF](Portable_Document_Format "wikilink")) By Herve Moulin
  - [Yahoo work group](http://groups.yahoo.com/group/Condorcet) Helping
    a WA state legislator to draft Condorcet election rules to replace
    recently nullified statute. Moderated by Jeffry R. Fisher

