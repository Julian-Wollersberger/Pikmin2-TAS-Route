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


## References





