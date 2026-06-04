## First Thing First
All credits are to: https://github.com/samdemaeyer/codenames-pictures <br>
I only used Node.js to build the binaries provided in the [releases](https://github.com/Mohyoo/Codenames-Pictures-Binaries/releases) page.

The binaries are available for Windows, Linux, Mac and AIX operating systems. <br>
Though I could only test the Windows binaries, so please tell me if they don't work for you in other platforms.

---

## Codenames Pictures: Quick Guide
Two teams (**Red** and **Blue**) race to identify their secret agent cards on a grid based on clues given by their **Spymasters**.

---

## Can it be played locally (Offline - LAN - One Screen)?
Yes, that's how it's designed to be played, but there are limitations. <br>
The game doesn't automate everything, players should stay in the same room and agree to willingly respect the rules and roles as below:

1. First, they open the game web page in their devices (or just sit around one device. See `instructions.txt` for details). They add their names to the game via the menu button at bottom right.

2. One player (the Spymaster) opens the game and clicks the **Spy Master** button to look at the revealed cards (Spy now knows to which team a specific card belongs). Each team will have its Spy following this way.

3. The other players (the Operatives) look away from the screen when the Spy opens his key page; or they don't have to if they join via their devices (by typing the IP address plus the 3000 port as described in the `instructions.txt` file).

4. The Spymaster gives their clue out loud.

5. The Operatives discuss out loud and verbally tell the Spymaster which card they want to guess.

6. The Spymaster manually right-clicks that card on the screen to reveal its color, and everyone sees the result. 

The **Spymaster** page is designed only to let you see or search for the hidden key card layout. To actually click and mark the tiles as they are guessed, you need to be on the **Main/Player** page (on the screen showing the full grid of pictures, not on the Spy's special colored page).

So while it isn't an automated multiplayer game where two people can connect on separate devices locally, the interface acts perfectly as a digital game board for a group hanging out together in person.

---

## Notes
* **Rules & Trust:** Players must follow rules voluntarily. There is no automated enforcement.

* **Right-Clicking:** Anyone *can* right-click a card and reveal it technically, but by convention only the Spymaster should do it to reveal the identities since the Spy is the only one who knows its true belonging.

* **No Syncing On Multi-device:** This is a **static web build**. Changes do not sync across different devices over an LAN network. Also, attempting to open the server on multiple devices won't even show the same board cards. This is a limitation by the author, but it isn't that much trouble, you can just say it loudly, or write records to a paper for more fun :)

* **Search Function:** Think of the game as having a built-in booklet of 100 different map layouts. If the Spymaster types in "12" and hits submit, the game loads "Map #12". This ensures that if you want to replay the exact same map (board pre-set) later, or if two Spymasters need to look at the exact same solution grid on different screens, they can both just look up "12".

* **Paper Tracking:** The Spymaster must use the hidden key card page (the Spy page) to know what is correct or wrong. Right-clicking a tile simply cycles its color manually based on what the Spymaster believes, and so, marking it as blue gives a point to the blue team whether the blue or red team chose to reveal it, and vice-versa.

* **Turn Limits:** Players must manually stop guessing. The Spymaster reveals the true color on the screen after a verbal guess, which ends the turn if it's a wrong card. And the Spy is the one who announces that the guess was wrong for the team to stop guessing.


---

### Playing Possibilities
Because the app does not sync across devices, your only option is:

1. **Single Device:** Play entirely on one screen (like a laptop or TV).      Operatives look at the screen to guess. The Spymaster looks at the hidden key card on the web page, a piece of paper, their memory, or a completely separate screen (Operators should not look when the Spy is looking in the key card board), then right-clicks the main screen to reveal the cards.

The methods listed below have issues, such as sync lack (revealing cards, adding players, and other changes won't appear to other devices; also when you open the link http://host_ip_address:3000/#/play in other devices, the board cards will change sadly):

1. **Spies in one device, Operators in another device**: Though limited, since there is no sync for the changes, but it's still an option (see `instructions.txt' for details).

2. **Everyone on their device**: Same as above.

3. **Play the way you want**: There is no restriction to the way you and your friends/siblings can play, so find what fits your desire.

Unless you find a workaround, you may not be able to play that way. I apologize for the inconvenience (though it's by the author, not me hehe).

---

## Game Setup & Roles
* **The Key Card:** Spymasters click the **Spy Master** button to view the grid key. This key reveals which cards belong to **Red**, **Blue**, **Neutral (Bystanders)**, or the **Assassin (Game Over)**. Keep this hidden from operatives.
* **Starting Team:** Look at the lights on the sides of the key card. The starting team must guess **8 cards**; the other team must guess **7 cards**; for it to be fair.

---

## How to Play

### 1. Giving the Clue (Spymaster)
On your turn, give a clue consisting of exactly **one word** and **one number** (e.g., *Flying: 2*). 
* The **word** describes the visual elements of your team's pictures.
* The **number** tells your team how many pictures match that word.
* *Spymasters must maintain a straight face and cannot comment during the guessing phase.*

### 2. Guessing (Operatives)
Operatives discuss and point out their target card. Once a verbal choice is made, the Spymaster right-clicks the tile to reveal the identity:
* **Your Team's Agent:** The Spymaster marks it your color. You may guess again.
* **Innocent Bystander:** Marked as **Neutral**. **Your turn ends**.
* **Enemy Agent:** Marked with the opponent's color. **Your turn ends** and helps the enemy.
* **The Assassin:** Marked as **Game Over**. **Your team loses immediately**.

### 3. Number of Guesses & The "+1 Rule"
Your turn continues until you guess wrong, choose to stop, or run out of allowed guesses. 
> **The +1 Rule:** You can make a maximum number of guesses equal to the **clue number plus one**. This extra guess allows you to safely guess a missed card from a previous turn.

---

## Winning the Game
* **Normal Win:** The first team to successfully cover all of their color's pictures wins the game (even if the other team accidentally covers your last picture for you).
* **Instant Loss:** Whichever team uncovers the Assassin loses instantly.

---

## The Interface Controls
* **Zoom in on a picture:** Left-click the tile.
* **Mark a card's state (Red/Blue/Neutral/Game Over):** Right-click the tile.
* **Remove an accidental marking:** Double-click the tile.
* **Access the Master Grid:** Click the **Spy Master** button.
* **Load a specific Key Card Layout:** Click the **"insert card id"** field on the spymaster page, enter the Card ID, and click **"Search"**.
