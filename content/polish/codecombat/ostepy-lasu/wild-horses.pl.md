---
title: "Dzikie Konie"
date: 2019-01-06T19:52:31.411Z
translationKey: "wild-horses"
slug: "dzikie-konie"
order: 51
tags:
  - findFriends
  - distanceTo
  - friend.pos
---

> Z farmy uciekły konie. Zaprowadź wszystkie dzikie konie z powrotem do zagrody.

https://codecombat.com/play/level/wild-horses

Rozwiązanie

```javascript
while(true) {
    // How do you find the nearest friendly unit?
    // horse = ?
    var horse = hero.findNearest(hero.findFriends());
    if (horse) {
        var x1 = horse.pos.x - 7;
        var x2 = horse.pos.x + 7;
        if (x1 >= 1) {
            // Move to the horse's y position but use x1 for the x position.
            hero.moveXY(x1, horse.pos.y);
        } else if (x2 <= 79) {
            // Move to the horse's y position but use x2 for the x position.
             hero.moveXY(x2, horse.pos.y);
        }
        var distance = hero.distanceTo(horse);
        if (distance <= 10) {
            hero.say("Whoa");
            // Move to the red x to return the horse to the farm.
             hero.moveXY(27, 54);
            // Move back out into the pasture to begin looking for the next horse.
            //hero.moveXY(41, 18);
        }
    }
}

```

Potrzebne przedmioty z |
--- |
distanceTo |
moveXY |
findFriends |
findNearest |


