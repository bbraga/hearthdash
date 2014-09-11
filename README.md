# Hearthdash

Hearthdash is a card tracking application for Hearthstone.

<div style="float: left; width: 50%; text-align: center;">
	![Screenshot](images/game.png)
</div>
<div style="float: left; width: 50%; text-align: center;">
	![Deck editor](images/deck.png)
</div>
<br style="clear: both;">

## Features

* Uses packet capturing for foolproof tracking - fast and accurate. Cards appear in the tracker before your game even shows them!
* See your opponents play history broken down by turn.
* Sapped your opponents minion? Hearthdash will show it in their hand so you don't forget.
* Easy to use deck editor.

## Getting Started

Hearthdash isn't 100% ready yet, so there's some work needed to start using it.

### Requirements

* Mac OS X (Windows and Linux support coming soon)
* [atom-shell](https://github.com/atom/atom-shell/releases)
* [disunity](https://github.com/ata4/disunity/releases)
* nodejs v0.10
* coffee-script

Homebrew is the best way to install Node on OS X:

    ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
    brew install node
    npm install -g coffee

Extract the card data with disunity:

    disunity.sh -c extract /Applications/Hearthstone/Data/OSX/cardxml0.unity3d
	coffee tools/extract-card-data.coffee --card-dir=/Applications/Hearthstone/Data/OSX/cardxml0/TextAsset

Put `Atom.app` in the Hearthdash directory and run:

    ./Atom.app/Contents/MacOS/Atom .

Congratulations, you're now running Hearthdash.