---
title: "BlackJack - Card Game"
date: 2024-11-08 12:45:00 +0800
image:
  path: /assets/img/blackjack/ingame.png
categories: ["Projects", "Web Development"]
tags: ["JavaScript", "HTML", "CSS", "Game"]
---

This project is a classic Blackjack card game built with vanilla JavaScript, HTML, and CSS. The goal is to create an interactive and engaging web-based gaming experience.

### Game Flow

The game starts with the player having an initial balance. They can then place a bid to start a round.

**1. Place Your Bid**

At the beginning of each round, you can place a bid. You start with a balance of $5000, and the minimum bid is $100.

![Start Screen](/assets/img/blackjack/start.png)

**2. Gameplay**

Once the bid is placed, the game begins. You are dealt two cards, and the dealer has one card. You can choose to "Hit" to take another card or "Stay" to end your turn.

![In-Game Screen](/assets/img/blackjack/ingame.png)

**3. Winning**

You win the round if your hand is closer to 21 than the dealer's without going over, or if the dealer busts. Winning doubles your bid amount.

![Win Screen](/assets/img/blackjack/win.png)

**4. Losing**

You lose if your hand exceeds 21 (a "bust") or if the dealer's hand is closer to 21. If you lose all your money, you'll have an option to reset your balance and play again.

![Lose Screen](/assets/img/blackjack/lose.png)

### Key Features

- **Interactive Gameplay:** Simple "Hit" and "Stay" controls.
- **Bidding System:** Players can bid money, adding a layer of strategy.
- **Dynamic UI:** The interface updates in real-time to show scores, cards, and player balance.
- **Game Logic:** Implements standard Blackjack rules for player and dealer actions.
- **Reset Functionality:** Allows players to reset their balance if they run out of money.

<a href="https://github.com/taste123/Ray-S-Web/tree/main/WEB5" target="_blank" class="btn btn-primary">
  <i class="fas fa-fw fa-code"></i>
  Source Code
</a>