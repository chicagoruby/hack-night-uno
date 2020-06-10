# Uno

Uno is a multiplayer card game where the object is to be the first person to discard all of their cards.

![Uno](https://ubistatic19-a.akamaihd.net/ubicomstatic/en-us/global/game-info/nakedbox_560x698_tablet_259523.jpg)

## Gameplay

Uno can be played by 2-10 players. We are building a two player version for our application, where it is either player vs player, player vs computer, or computer vs computer.


### Setup

The deck consists of 108 cards: four each of "Wild" and "Wild Draw Four," and 25 each of four different colors (red, yellow, green, blue). Each color consists of one zero, two each of 1 through 9, and two each of "Skip," "Draw Two," and "Reverse."

To get you started, there is a JSON file located at data/deck.json that contains each of the 108 cards. You can also challenge yourself by building a automated uno deck generator per the above stated rules.

To start the game, each player should be dealt 7 cards. The remaining cards are the draw pile and the top card from the draw pile is turned over and is the first card in the discard pile.


### Taking a turn

Each player will have a chance to take a turn. A turn can include one of 3 actions:

1. play one card matching the discard in color, number, or symbol
2. play a Wild card, or a playable Wild Draw Four card
3. draw the top card from the deck, then play it if possible

If the card the player discards is the last card in the player's hand, they win.

If the discard action leaves the player with only one remaining card, the player must declare "Uno". More on that in a bit.

If the player has more than one card remaining after discard, play moves to the next player.


#### Discarding

A player can only discard one card at a time. The top card of the discard pile is what the player is trying to match in either color, number, or symbol. For example, if a player discards a red 3, the next player can either discard a red card, a 3 card, or a wild card.

Wild cards can be played as any color. The player discarding the wild card must choose what color the wildcard will represent. For example, a player discards a green 4, the next player can discard a wild card and declare that card to be red, green, yellow or blue.

A second type of Wildcard, the Draw 4 Wildcard, follows the same rules as a regular wild card, but additionally, the next player must draw 4 cards and their turn concludes without a discard. The color that the wildcard represents will still need to be declared. This card can only be played if another card cannot be played, or they can risk a draw 4 challenge. See Draw 4 Challenge.

Another draw card in the deck is the draw 2 card. This card can only be played when the card's color matches the color of the top discarded card or if the discard is also a draw 2. The player drawing cards will not discard.

A skip card can be played if its color matches the most recent discard card or if the discard card is also a skip card. This card skips the next player's turn.

A reverse card can be played if its color matches the most recent discard card or if the discard is also a reverse card. This card reverses the direction of play. This rule only has an effect when a game is being played with more than 2 players. In a two player game, the reverse card acts as a skip card.


#### Drawing

If a player cannot discard a card from their hand, they must draw a card from the draw pile. If the card drawn can be played, they can discard it. Otherwise, the card is added to the player's hand.


### Special rules for first discarded card

The following rules apply if the first card discounted is not a numbered face card.

1. Skip - First player misses a turn
2. Reverse - Dealer gets first turn and play resumes counterclockwise
3. Draw 2 - First player draws 2 and does not discard
4. Wild - First player picks a color and plays a card of that color
5. Wild Draw 4 - Return card to draw pile, reshuffle draw pile, select new first discard card


### Declaring Uno

A player left with only one card after discarding must call out "Uno". If another player calls Uno before the discarding player, the discarding player must draw two cards as a penalty.


### Draw 4 Challenge

If a player plays a Wild Draw 4 card, the player who is drawing can challenge the player. As mentioned earlier, this card can only be played if no other cards in the player's hand can be played (no matching color, number, action, or regular wild). A player challenging the Draw 4 can secretly look at the discarder's hand to verify that no other cards were playable. If there is another playable card, the discarder must draw 4 cards. If the challenge proves that the discarder indeed did not have another card to play, then the challenger must draw 6 cards instead of the original 4.


## Application

Build an app that allows for creating a shuffled deck, dealing the cards, and playing a turn. You can design this for a player or a computer AI. Some of the game rules (like declaring "Uno") may be difficult to program, so save those for the end.


## Resources

* [Uno - Wikipedia](https://en.wikipedia.org/wiki/Uno_(card_game))
* [How to play Uno (video)](https://www.youtube.com/watch?v=dicgjskLVJc)
