# Pikmin 2 TAS Route
This document describes my route for my Tool Assisted Speedrun for the Pikmin 2 Pay off Dept category.
For the videos, see my [YouTube channel](https://www.youtube.com/channel/UCVSDjX4sC_Y7a6cmftkAkYQ).

## Splits
This TAS mostly follows the RTA route, and the section names follow the community conventions.

## 0. Beginning
TAS timing starts on console power-on. RTA timing starts on pressing A to continue without saving.
For precise timing, I use the "Input" number displayed in Dolphin's title bar.
This number increases at a constant 180Hz. Pikmin 2 mixes 30FPS and 60FPS, 
so the frames counter can't be used for abolute times.

The initial RNG seed is determined by the system clock when you start the 
emulator. This gets saved in the .dtm file.

The loading screens can take different amounts of time. The "(c) 2004 Nintendo"
can appear at frames 628 to 680. Almost a second of variance.

### 0.1 Day 1 Extinction
There are 2 spots for D1E: The classic one and [the Keisen spot](https://clips.twitch.tv/AnnoyingTsundereCucumberBrokeBack-HbURwx5vVTQ7n1Me).
The second one is 5 frames faster, because there is less distance to walk. 
![0.1 D1E faster spot.png]

Grab the Pikmin at the bulborb. Carrying it is about 20 frames faster than 
waiting for it to catch up.

The Moonwalk strategy allows for a faster death.
[Demonstration at 1:15](https://discord.com/channels/177495849100640256/698992259038838864/1172216267948703764)

The important thing here is to get a momontum throw, but backwards. The 
invisible ledge extends quite a bit out of bounds. Only a momentum throw 
clears that distance. For that, you need to moonwalk long enough so that the
cursor points behind Olimar. Release A two or three frames before Olimar 
thoughes the wall.
![0.1 D1E Pikmin chilling OOB.png]

On the Today's Report cutscene, mash A to get to the report 3sec faster.
(This is an easy thing to forget...)

### 0.2 Day 2
The pellet posies have a random spawn location, with collection times varying 
by about 130 frames. RNG can be manipulated on day 1, after throwing and before 
the fadeout, by walking around randomly.

Sadly, the fastest layouts are to fast. The bulborb doesn't die in time.
The fastes I got was taking 160f from red text over pellet to fadeout.
In my successful attempt it takes 187f. It should be possible with 177f.

The Pikmin can pick up the pellet with 0f, 10f or 20f of delay, depending on RNG.

The TAS can skip the pellet cutscene by ending the day on the same frame as the first pellet collects.
But you need to kill the bulborb beforehand, because otherwise you can never switch to Louie. 
The bulborb is dead when the health bar goes away completely, or when you hear
the ghost spawn sound in the day end cutscene.

Faster bulborb death animation:
> the turning on the spot animation makes it go at 60fps, you just need to kill it during that animation
> if it goes from turn straight to shake that can help since it maintains the 60fps while not turning
~ [PikHacker on Discord](https://discord.com/channels/177495849100640256/177496240035069962/903697188000006164), with video.

It's pretty easy to get here. Fast death takes 45f, normal death takes 90f.
Olimar punches faster when wiggling than when standing still.

### 0.3 Day 3
Manipulate RNG for the pellet posies again.

The cutscene for killing the bulborb happens here.
Aka cutscene timer storage. It has no use here.

Leaf Pikmin are slow, so throwing to the pellets is faster.
Carrying the Pikmin to near the first pellet is a few frames
faster than longthrowing. For the second pellet, I push
the Pikmin with Olimar and do a half-longthrow as soon
as it is throwable.

The throwing angle and distance is influenced for three
frames by the stick during the throwing animation.
By going in one direction for two frames and in a very
different direction on the third frame, I get a distance
that is between a short throw and a long throw.

Perform Louie skip by ending the day at the same time
as activating the Louie cutscene.

### 0.4 Day 4
Only the two grouped pellet posies and the eggs are RNG
dependent. All other pellets have a fixed spot.

The first thing you need to do is to get the 5-pellet moving.
The two 1-pellets won't work since 10 Pikmin are needed for mitites.
Plucking both sprouts with Olimar is faster, because Louie
lags so far behind.

#### Egg Push
All three eggs no to go down the slope. It is possible to
push all three eggs at the same time with one captain,
and still be faster than the 5-pellet.

First, push one egg slightly over the edge, otherwise it
will only move sideways later. Also punch it down to 1 hit.
Then run to the back egg and punch so that two eggs get hit.
It's easiest to punch them while on still being on the upper part.

Steering the eggs is very finnicy. It's like driving backwards
in a car with two trailers.
My technique is to pick a direction in the TAS Input window,
advance by ~5 frames, make a savestate, advance further to see
whether Olimar overshoots left or right of the egg,
load the savestate, adjust the direction, and repeat.
All three eggs shoud stay in a mostly straight line.
First all must go over the edge, then steer them towards the left edge.
On the slope it's sometimes neccessary to walk uphill.
That will slow you down though.

When the alignment is just perfect, you can switch to Louie about
two seconds before all eggs reach the bottom. Then whistle the
Pikmin from the 5-pellet. If you need to delay the whistling by a
few frames, then success! The egg push was faster than the 5-pellet.

#### Mitites Strategy
Before the second set of mitites can spawn, the first set needs to
fully collect. For that, you need all 10 available Pikmin. Otherwise it's very slow.
So pluck all 5 from the 5-pellet. RNG manipulate both the direction the sprouts
fall in (for a short walking distance) and how long they take to grow
(determined on the frame they land on the ground).

The first time you pluck, it's a slower pluck (38 frames), and then
if you are continuously pressing A to auto-pluck without walking to each
seed, then the 2nd pluck onward is fast (14 frames), until you fully stop plucking
and have movement control again. Between the plucks, the captain is in the
"pluck adjust" state, where they walk slower. So make sure the sprouts are
very near to each other.

The second captain will only start plucking when
* the current captain starts plucking
* there are sprouts that are fully grown
* the current captain isn't already targeting that sprout.
To make the second captain continue to pluck, he needs to
finish _before_ the current captain. Otherwise he will just stand around.
That's why it is very hard to make the second captain pluck
as many sprouts as the current captain.

For killing the mitites, not all 10 Pikmin must be available immediately,
since whistling isn't that slow (about 24 frames). For the first set,
you need to whistle once anyway.

Before the first set of mitites, collect the near 1-pellet. That will mean
that we have 12 Pikmin for the second set.
The far 1-pellet is to slow. It will not collect in time at all, and going for it
makes collecting the near 1-pellet 100 frames slower. Meaning we'd have only
6 Pikmin for killing the first set of mitites.


For the 10-pellet and third set of mitites, I'm investigating if they can be done
while CR moves. That would make it completely parallel. But doing both is very tight and
probably not enouth Pikmin are available. But one of the two can be done that late.



#### Gate Cutscene Skip
Break the gate to EC at the same time as Courage Reactor collects.
This skips a cutscene with dialog, and enables more things to happen in parallel.

The gate must start falling (meaning it reached 0 HP) in the fadeout to CR's treasure cutsene.
The gate cutscene would like to play as soon as the gate starts falling,
but since the treasure cutscene is already triggered, the gate cutscene
gets queued. But then the treasure collection cutscene queues the
find-first-treasure cutscene and that one takes priority. Thus the find-first-treasure
cutscene plays. In this one, Pikmin get processed, and thus the ones
from the gate join your party, and the gate-finished-falling-jingle plays.
Then the other day end cutscenes play and the gate cutscene never has a chance to play.

When done right, you can skip the find-first-treasure cutscenes on the first/second? frame.
Otherwise you need to wait in this cutscene for the gate falling animation to finish.
Compare [this video](https://youtu.be/Rc-e1xNW6rA?si=pOvkMM4unJkn7pie&t=213) with [this video](https://youtu.be/syHt7U5HuUc?si=zlvaGLxCLXhomQE1&t=465).

Note: Different cutscenes behave differently regarding which things get processed.
Eg. Pikmin can't deal damage to the gate in the treasure collection cutscene,
but can in the find-first-treasure cutscene.
See [PikHacker's Pikmin 2 Cutscene Documentation](https://docs.google.com/spreadsheets/d/10fIMMCDvYQ-v6UBLxkTATKAEysbJh4l63G728u7GSFk/edit?usp=sharing).



Cheats:
````
$Mitites die when trying to walk (US Final) [APerson13]
0436cd1c 38800004
0436cdac 38800000

$Mitites die when trying to walk (JPN) [APerson13]
0436d32c 38800004
0436d3bc 38800000

$Mitites die when trying to walk (PAL) [EpochFlame]
0436cf2c 38800004
0436cfbc 38800000
````

### 0.5 Day 5

## 1. Emergence Cage

## 2. Hole of Beasts

## 3. White Flower Garden

## 4. Snagret Hole

### 4.3 SH3
If you look closely at caveinfo, you can see that the level is not fully symmetrical. One spwan point (purple star) is slightly closer to the ship. I also did some time measurements to confirm that. (Those weren't very precise though.)
![4.3 SH3 caveinfo.png]

The second thing is how snagret spawning works:
A snagret has a fixed home point with an aggro range, which never varies between seeds, unlike other enemies. If a Pikmin enters that range, snagret pops up at a random location within that radius.
Here you can see that range with PikHacker's hitbox hack:
![4.3 HitblockHack WFG5.png]

### 4.6 SH6
Best known layout: [1:12.06 by Jack](https://www.youtube.com/watch?v=T0pGBGVPr5E&t=2162s)

## 5. Bulblax Kingdom

## 6. Subterrainian Complex

## 7. Frontier Cavern

## 8. Citadel of Spiders

## 9. Glutton's Kitchen


## Route Planning
Mostly, this is the RTA route. The above grounds are increadibly optimized.

In WFG3, the tape is skipped. This is the slowest treasure in the Pod route besides globes.
It takes 49sec or 1.6 pokos/sec.

Percent cutscene skips:
* After WFG it's barely not possible by 80pokos.
* 40%: Enter BK <=3999 and leave >5000. Though chance totem could be moved afterwards.
  This means that early game pokos don't matter that much actually. I just need to reach 3999.
* What to do in VoR? That's 760 pokos movable.

How many bugs?
This is the big question.


## References





