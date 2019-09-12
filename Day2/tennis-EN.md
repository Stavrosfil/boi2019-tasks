# Tennis

Tournament

This year, Athens is preparing to host a tennis tournamentevent,
with no real winner, to support various non-profit organizations.
In order to raise as much money as possible, the organizers are planning
to invite famous tennis players from all over the world.

The organizers decided that the tournamentevent will consist of $K$ gamesmatches,
each between two different tennis players, and they asked your help to find
which $2K$ tennis players to invite to maximize the number of tickets
that will be sold in the tournamentevent.

Unfortunately, you are not that much of a tennis fan yourself.
So you searched the web and found a report from a famous international
tennis tournament with $N \ge 2K$ players, that was held recently
and lasted $N-1$ days.
Each day a single gamematch was held; the winner advanced and was eligible
to play during the following days, whereas the loser left the
tournament and did not play in any of the subsequent gamesmatches.
For each of the $N-1$ gamesmatches, the report states which pair of players
$(x_i, y_i)$ participated in the gamematch and how many people $w_i$ attended.
Since, you prefer not to rely on pure luck, you are only willing to select
which players to invite based on the $N-1$ pairs you have some information about.
However, to simplify your analysis, you make the assumption that selecting
each of these pairs ($x_i$, $y_i$) will result in the same number of people
$w_i$ attending the event.

You are asked to write a program that computes the maximum number of tickets
that can be sold onin the tournamentevent.

## Input

Your program must read from the standard input.

The first line will contain two space-separated integers $N$ and $K$:
the number of players in the past tournament and the number of gamesmatches that
you have to plan.

Each of the following $N-1$ lines will contain three space-separated
integers $x_i$, $y_i$ and $w_i$: the first player of the gamematch,
the second player of the gamematch and the number of people that attended the gamematch,
which result in the same number of tickets being sold.
Players will be numbered 1 to $N$.

Note that gamethe resultsmatches will be provided in arbitrary (and not chronological) order.

## Output

Your program must print a single line to the standard output,
consisting of a single integer: the maximum number of tickets
that can be sold onin the tournamentevent.
If you don't have enough information to select exactly $K$ pairs,
you will have to output $-1$ as your answer.

## Constraints

- $2 \le 2K \le N \le 10^6$
- $1 \le x_i < y_i \le N$
- $1 \le w_i \le 10^6$
- Time and memory limit: See the CMS.

## Subtasks

- Subtask 1 (11 points): $N \le 10^3$, $\quad K \le 100$  
  Furthermore, in the past tournament, no player participated in more than 3 gamesmatches.
- Subtask 2 (24 points): $N \le 10^4$, $\quad K \le 100$
- Subtask 3 (27 points): $N \le 1.5 \cdot 10^4$, $\quad K \le 7 \cdot 10^3$
- Subtask 4 (38 points): No further constraints.

## Example 1

### Input

    6 3
    1 2 9
    2 3 6
    3 4 6
    4 5 9
    5 6 2

### Output

    17

### Explanation

You select the pairs (1, 2), (3, 4) and (5, 6), as this is the only way
to select exactly 3 valid pairs given your constraints.
Selecting pairs (1, 2) and (4, 5) would result in more tickets being sold,
but there would be no way for you to select a third gamematch.

## Example 2

### Input

    7 3
    1 2 8
    1 3 15
    2 4 3
    2 7 2
    3 6 10
    4 5 6

### Output

    24

### Explanation

In this scenario, there are multiple ways to select exactly 3 pairs,
but you select the pairs (1, 2), (3, 6) and (4, 5) which will result
in the maximum amount of tickets being sold.

## Example 3

### Input

    9 3
    1 2 1
    1 3 1
    1 4 1
    1 5 1
    3 6 1
    3 7 1
    3 8 1
    3 9 1

### Output

    -1

### Explanation

In this scenario, there is no valid way to select more than 2 pairs of players
to invite, since at least one of players 1 and 3 participated in all of the gamesmatches.