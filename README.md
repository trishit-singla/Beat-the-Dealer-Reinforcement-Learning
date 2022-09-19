# Beat-the-Dealer-Reinforcement-Learning

## **Introduction to BlackJack**

**BlackJack**, also know as Twenty One due to the special role of the number in the game, is arguably the oldest known casino game. The game played with 1 to 8 deck of cards allows the player to directly play against the casino and remains **one of the only mathematically beatable casino games.**

A small introduction of the rules can be found on the link: [Intro Video](https://www.youtube.com/watch?v=DwwaJGStuP0)

As seen a total of 5 actions can be taken by the player:


*   **Hit:** Draws a card
*   **Stand:** No more card to draw
*   **Double:** Doubles the bet and draws one card and stands
*   **Split:** Splits a value pair into two individual hands to play separately
*   **Surrender:** Forfiets the game by splitting the bet amount equally between the Casino and the Player.

## **Edward Thorp's Beat the Dealer**

In 1962, Edward Thorp published the first edition of his book ***Beat the Dealer*** solely dedicated to understanding the game of BlackJack and developing human strategies to excel at the game. As a result, the readers were able to earn great profits. Over the next few years, Casinos started taking measures to counter the so called *method players* including adding extra decks and shuffling very often to disrupt the strategies. 

In 1966, Thorp published a corrected and extended version of "Beat the Dealer" which to date proves to be the best human played strategy of the game.

Though the best method referred above is a Counting Cards strategy, Thorp also gave a basic strategy to provide a reference of actions in regular situations.
With the entire strategy learnt to heart, Thorp calculated a **long term return of +0.13%** which was the first time player advantage over the casino.

#### **Draw or Stand**
<center>

<br>

 ***Hard Totals*** 

You have ⬇ | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11
:--------:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:--:|:--:
17|S|S|S|S|S|**S**|**S**|**S**|**S**|**S**
16|S|S|S|S|S|D|D|D|**^**|D
15|S|S|S|S|S|D|D|D|D|D
14|S|S|S|S|S|D|D|D|*|D
13|**S**|**S**|S|S|S|D|D|D|D|D
12|D|D|**S**|**S**|**S**|D|D|D|D|D

<font size="2">
`^`➡ Draw if holding two cards and stand if holding more <br> </font>
<font size="2">
`*`➡ Stand if holding (7,7) </font>

<br>
<br>

***Soft Totals***


You have ⬇ | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11
:--------:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:--:|:--:
19|S|S|S|S|S|S|S|**S**|**S**|S
18|**S**|**S**|**S**|**S**|**S**|**S**|**S**|D|D|**S**

</center>

#### **Double**

<center>
<br>

***Hard Totals***

You have ⬇ | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11
:--------:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:--:|:--:
11|Y|Y|Y|Y|Y|Y|Y|Y|**Y**|**Y**
10|Y|Y|Y|Y|Y|**Y**|**Y**|**Y**|N|N
9|**Y**|**Y**|**Y**|**Y**|**Y**|N|N|N|N|N
8|N|N|N|*|*|N|N|N|N|N

<font size="2">
 `*` ➡ Double down except with (6,2)
 </font>
 <br>
 <br>

 ***Soft Totals***

 You have ⬇ | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11
:--------:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:--:|:--:
A,7|N|Y|Y|Y|Y|N|N|N|N|N
A,6|Y|Y|Y|Y|Y|N|N|N|N|N
A,5|N|N|Y|Y|Y|N|N|N|N|N
A,4|N|N|Y|Y|Y|N|N|N|N|N
A,3|N|N|Y|Y|Y|N|N|N|N|N
A,2|N|N|Y|Y|Y|N|N|N|N|N
A,A*|N|N|N|Y|Y|N|N|N|N|N

<font size="2">
`*`➡ Double down with (A,A) only if splitting isn't allowed.</center>
</font>

#### **Pair Splitting**

<center>

You have ⬇ | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11
:--------:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:--:|:--:
A,A|Y|Y|Y|Y|Y|Y|Y|Y|Y|Y
10,10|N|N|N|N|N|N|N|N|N|N
9,9|Y|Y|Y|Y|Y|N|Y|Y|N|N
8,8|Y|Y|Y|Y|Y|Y|Y|Y|Y|Y
7,7|Y|Y|Y|Y|Y|Y|Y|N|N|N
6,6|Y|Y|Y|Y|Y|Y|N|N|N|N
5,5|N|N|N|N|N|N|N|N|N|N
4,4|N|N|N|Y|N|N|N|N|N|N
3,3|Y|Y|Y|Y|Y|Y|N|N|N|N
2,2|Y|Y|Y|Y|Y|Y|N|N|N|N

</center>
