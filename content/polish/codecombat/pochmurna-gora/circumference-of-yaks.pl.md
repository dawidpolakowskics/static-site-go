---
title: "Obwód  Yaków"
date: 2019-01-26T22:39:25.203Z
translationKey: "circumference-of-yaks"
slug: "obwod-yakow"
order: 106
tags:
  - koło
---

> Yaki są jak duże kule futra

https://codecombat.com/play/level/circumference-of-yaks

Rozwiązanie

```javascript
// Calculate the circumference of yak circles.

// The first yak circle.
var yak1 = hero.findNearestEnemy();
// The distance to the yak is the radius.
var radius1 = hero.distanceTo(yak1);
// The circumference is calculated the following way:
var circumference1 = 2 * Math.PI * radius1;
// Let's say the result.
hero.say(circumference1);

// Move to the next mark.
hero.moveXY(60, 34);
// Find an yak from the second circle.
// Find the radius of the second circle.
var radius2 = hero.distanceTo(hero.findNearestEnemy());
// Calculate the circumference of the second circle:
// Say the result.
hero.say(2 * Math.PI * radius2);

```

Potrzebne przedmioty z |
--- |
findNearestEnemy |
distanceTo |
moveXY |


