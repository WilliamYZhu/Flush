# Flush
from enum import Enum
from enum import IntEnmum

full_deck = []

#DECLARATION-------------------------

#Card Enumeration
class Card(IntEnum)
  TWO = 2
  THREE = 3
  FOUR = 4
  FIVE = 5
  SIX = 6
  SEVEN = 7
  EIGHT = 8
  NINE = 9
  TEN = 10
  JACK = 11
  QUEEN = 12
  KING = 13
  ACE = 14
  
#Suit Enumeration
class Suit(Enum):
  SPADES = 'spades'
  CLUBS = 'clubs'
  HEARTS = 'hearts'
  DIAMONDS = 'diamonds'
  
class PlayingCard:
  def __init__(self, card_value, card_suit):
    self.card = card_value
    self.suit = card_suit
    
    
#FUNCTION------------------

def create_deck():
  for suit in Suit:
    for card in Card:
      full_deck.append(PlayingCard(Card(card),Suit(suit)))
  return full_deck
  
def draw_cards(deck):
  rand_card = randint(0,len(deck),-1)
  return deck.pop(rand_card)
  
def draw_initial_cards(deck):
  for i in 4:
    draw_cards(deck)

  
#MAIN-------------------------
  
create_deck()

  
 
