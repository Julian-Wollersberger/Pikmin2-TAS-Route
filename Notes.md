# Notes for TASing
These are my notes that I write during TASing,
or for ideas, that are probably not useful for other people.
This is my third TAS.

## Docs
Timing, poko route, fast seeds:
https://docs.google.com/spreadsheets/d/1KSQWQ4SKW3w6xR32oPBrn5pny-hm-H7AF0x4-Nce0ZM/edit?pli=1#gid=1274620090

ToolAssistedPikm's videos:
Start, EC: https://www.youtube.com/watch?v=8UCRR-mII9c
SH, BK:    https://www.youtube.com/watch?v=wSboKSiex7s
HoB, WFG:  https://www.youtube.com/watch?v=S8ecJVl7fQc


## Beginning
RTA time starts at:
TAP (JP): 0:18.60
my TAS-2: 0:18.74, input 3373
Standard_: 18.something
APerson13 (JP): input 3505, 0:19.47
That one setup for gate cutscene skip: input 3241, 18.01

Huh. Something takes varying time on the title screen.

Timing until title screen, without button presses:
F2: 4080
F3: 4136
F4: 4106

Timing until title screen, mashing START
My TAS-2: 654
F5: 680, 11.52
F6: 654
F7: 654
F8: 628, 10.66 (mixed Pikmin)
F2: 628 (many whites)
F9: 628 (few mixed Pikmin)
F10:628 (purple pound)

I'll go with F8.
And I managed to do a savestate on frame 0.
Funnily, the RNG seed here is 1. It gets initialized on frame 1.

F8: warning disappears at 161, Nintendo at 339, Dolby 460, 628
F5: 160, 339, Dolby 460, 680.
The time difference only comes from the load time. WTF?

Navigating the menues without button mashing:
Health and safety: Start at frame 127
Title loads slower now. WTF²?
Back to mashing.

No Memcard loads at:
F5: 973
F6: 970

A press on Yes happens at
frame 1037, input 3154 or 17.52sec.
That's 1.2sec faster than TAS-2.
But I have to hold A for 2 or 3 frames to register.
Does that count? I say yes.

Skip at 1076. 
Ship talks at 2063.

Text mashing:
When text is scrolling to make way for the next text box, every frame where B is not held loses one frame overall. So if you alternate B and not B, then you lose about 4 frames compared to holding B. I believe this is because holding B doubles the text scrolling speed, but I haven’t looked into code to confirm.
https://discord.com/channels/177495849100640256/698992259038838864/1151622366150008862
Can't remember the exact numbers but it's something like:
-Press B to fill text box
-14 frames later press A and start holding B on the same frame
-Hold B for a total of 9 frames
-Release B for one frame then press B to fill the next text box.
If it's the last text box just hold B until the text box is gone.
https://discord.com/channels/177495849100640256/698992259038838864/1151547617831026900

First try: 1 frame B (41), 15 frames nothing, 1 frame A (57).
Second try: B on 41, 14 frames doesn't work.
Third try: B on 41, 15 frames nothing, Press AB, hold B 9 frames, release B, press B. Works!
Again: B on 41, AB on 57, B until 67, nothing, B on 69
Again: B on 41, AB on 57, B until 66 -> works
Holding for 8 frames (9 frames including AB) is best.

F5: Camera changes at 2319.
F6: 2316
F7: Last at 61. Camera at 2315

Next dialog. First B at 2448.
Ends around 2530
F8: 2580
F9: 2582

Lockout ends at 2614. Good red positions.
F2: Red takes until 2641 to get up.
Always gets up at that time, no matter when I whistle.

TAP actually grabs the Pikmin.
Doesn't work with this RNG seed.
-> This was try 1. Let's try again with another console startup seed.

## Beginning, Take 2
F3: 628 copyright.
F4: Title screen fades at 832, no memcard at 970
F5: A at 985. Next text at 1020. Hold left.
F6: Hold left until 1036, Hold A on 1037. Input 3154
F7: Skip at 1076. Ship talks at 2063.

### D1E
F8: Camera switches at 2302
F9: Camera switches at 2301 -> even faster than take 1.
F2: First B at 2434. 
F3: Second dialog finished at 2565. Lockout ends at 2599
F4: Grab red at 2617.
F5: Grab red at 2618.

-> Continue with F4 and clean it up.
First do the Keisen strat, then try with moonwalking.

F5: Start running at 2605, grab at 2617.
F5: Skip at 2660
Lockout ends at 2722
F7: Made the OOB thorw at the Keisen spot
F7: Throw at 2803
F8: Dead at 2924. Pikmin whistled at 2838
F9: Dead at 2926. Pikmin whistled at 2840
F10: Start of RNG manip at frame 2890

#### Moonwalking
How to do it?

Joystick angles:
Below Y=186 and above Y=70 you down't move, but turn.
Y=187 and Y=69 are reduced speed of 130.
Y=188 and Y=68 have speed 133.

Ok now I get it:
https://clips.twitch.tv/LovelyPopularSnailFloof-1p2NSJP5gIba1M5O
Strategy:
Run most of the way normally. 
Then turn around.
Do moonwalking for <10 frames, until XZ speed is ~100.
Just as Olimar hits the wall, release A.

F3: Turn around starting at 2780
Start moonwalking at 2800
Collide at 2810
F4: Start moonwalk at 2830
F6: Successful throw, but not enouth momentum.
    LeftD, RightD, LD, RD, LD, RD, 0/53, nothing
F4: Start at 2804
F5: Successful clip, but not enouth momentum
    LeftD, RightD, LD, RD, LD, 255/48, 70/11 release,
F7: LD, RD, LD, RD, LD, 207/0, 14/75 release 
F8: LD, RD, LD, RD, 42/0, RD, nope
F8: LD, RD, LD, RD, LD, 255/90, 28/57
F9: WTF?!?! Played around with Freecam
F4: Clipped. It just doesn't throw wide enouth.
F3: New setup with a longer moonwalk.
    Cursor must be behind captain to do a 
	backwards momentum throw.
F4: YESSSSSS! It works!
    Backwards momentum throw past the OOB ledge!

F5 starts RNG manip at 2815.
Pikmin dead at 2881. That safes 45f over the normal strat :)

Standard_ is ~1sec slower in this section, with moonwalk 
on the normal spot, and not grabbing the Pikmin.
The Pikmin can catch up while Olimar turns around.

Walking to Keisen spot takes:
From 2565 to 2678 (hit wall, without Pikmin)
Walking to normal spot:
From 2565 to 2683 (hit wall, without Pikmin)
Keisen is only 5f faster.

How long does turning around take for moonwalk?
Moonwalk throws at 2813. Would hit wall at 2787.
-> turning + moonwalk takes 26f
Non-moonwalk throws at 2804. Would hit wall at 2788.
-> turning alone takes 16f.
-> moonwalk loses 10f

How long do you wait for Pikmin, when not grabbing?
Would hit wall at 2771. 16f faster.
Can press A at 2822 or throw at 2832.
So carrying Pikmin lets you throw faster.
Carrying loses 16f at beginning but gains >19f total.

I could optimize moonwalking a few more frames,
by turning around faster and moonwalking less distance.
Maybe 5 frames, 10 at most.
Not worth it for several hours of doing all that again.


Now investigate why my day1 "Ship starts talking" split is slower than in TAS-2.
In TAS-3, RTA start until stip stops talking:
1038 RTA timing start
1071 ( 33) Text invisible
1073 (  2) black
1077 (  4) START
1087 ( 10) Captain positions get reset
1105 ( 18) Text fades in
1307 (202) Captain positions are set
1329 ( 22) Cutscene starts
1666 (337) Fade to black
1679 ( 13) Fade in
1808 (129) Camera cut to landing
1943 (135) Camera cut to ejecting Olimar
2063 (120) Camera cut to ship starting to talk
2122 ( 59) Ship icon appears
2287 (165) Textbox away
2412 (125) Ship icon appears
2528 (116) Textbox away
2565 ( 37) black
(1527f total)

In TAS-2:
1066 RTA timing start (input 3241)
1098 ( 32, +1) Text invisible
1100 (  2,  0) black
1105 (  5, +1) propper START
1115 ( 10,  0) Captain positions get reset
1133 ( 18,  0) Text fades in
1336 (203, +1) Captain positions are set
1359 ( 23, +1) Cutscene starts
1696 (337,  0) Fade to black
1709 ( 13,  0) Fade in
1838 (129,  0) Camera cut to landing
1973 (135,  0) Camera cut to ejecting Olimar
2093 (120,  0) Camera cut to ship starting to talk
2154 ( 61, +2) Ship icon appears
2334 (180,+15) Textbox away
2466 (132, +7) Ship icon appears
2590 (124, +8) Textbox away
2632 ( 42, +5) black
(1566f total, that's +39f slower. Mostly textbox)

Actually, the reason is that I measured the start wrong!
My table said input 3373, but actually it's input 3241.
So the split time goes up from 33.08 to 33.82
So TAS-3 actually is faster. (By 4f at 60fps?)

### Day 2
Now: RNG manip for day 2.
RNG is called in: Extinction cutscene, second day end cutscene, 
a few times on today's report, a few times on landing.
So I need to frame-perfectly deal with only the first three cutscenes.

Timing Number over transporting pellet becomes red to cutscene start
F2: 6146 to 6315 => 169
F3: 4949 to 5111 => 162, sprout near leg
F4: 5124 to 5284 => 160, sprout in exact same spot
F5: 5063 to 5258 => 195 and 5023 to 5251 => 228
F6: 5047 to 5216 => 169 and 5135 to 5332 => 197
F7: 5056 to 5225 => 169
F8: 5146 to 5373 => 227

Cutscene timing:
START in extinction, day end, day end²; report x9; land: 
F3: 2890, 2927, 2964; 
    3003, 3042, 3095, 3097, 3164, 3166, 3290, 
    3314: down down A, 3355 (black 2409);
	3647, 3717, 4005
F4, F5, F6, F7: same

Go forward with F4.
5320 to 5480 => 160
That first sprout is always in the same position.

Textboxes: Starts at 4307.
B, 15x nothing, AB, 8x B, nothing, repeat
F2: 4399
F3: 4401
Holding B at the end makes it slower? what?

Pluck at 4481.
Skip at 4570.
Throw at 4632.

Pellet hit at:
F5: 4655 X=-158.5 or -268.6 at 4660 about 5f more walking
F6: 5649 X= -89.8 or -175.1 at 4660 about 24f walking
F7: 4659 X=-174.5 or -281.1 at 4660
F8: 4660 X=-185.2 or -290.2 at 4660 <-- chosen
F9: 4661 X=-185.2 or -291.8 at 4660

Two possible tactics here:
* Hit the pellet from as far away as possible.
  Means a lot more time to kill the bulborb.
* Hit the pellet from very close.
  Faster collection, but harder to kill bulborb in time.
Try with far throw first.
Edit: Other is impossible.

F3: Pikmin holds pellet at 4727, to 4887 => 160. Ok.
Start menu at 4870
F4: Spam A to kill. Can't switch captains though.
Frame perfect punching seems to be every 12 frames.
F9: Probably fast death animation.
  But still to slow. I think the pellet is way to fast.
  
Ok, slower pellet kill is needed.
When throwing at the side of the head, the Pikmin does one extra attack animation.
Nope, isn't actually slower.
F4: 4661 X=-210.4 or -317 at 4660
START at 4850. WTF, why even faster?
Probably because it behaves differently off-camera.
F5: 4661; X=-317
F6: First bulborb hit at 4697.
F7: Furthest I've gotten so far. Dies at 4862
F4: First hit at 4799. Dies at 4864.

This seed just doesn't work. The flower is to near. Fail.
About 20 to 30 frames slower would be fine.

### Day 2, second try
Cutscene timing: I improved by a frame! Press A on
2890, 2927, 2964; 
3003, 3042, 3095, 3097, 3164, 3166, 3290;
-> 3314 down, 3315 down + A, nothing, *3354* A (black 3408);
3646, 3716, 4004

Pellet transport
Old:5320 to 5480 => 160
F3: 5071 to 5270 => 199
It's even in a good position. I'll take it.

Textboxes: Starts at 4306. 
But at 4307 if I don't have TAS Input open. WTF?
B, 15x nothing, AB, 8x B, nothing, repeat
F4: 4449 dark
Holding B at the end is faster now. huh.
F4: Pluck at 4484.

F5: 4449 dark
Somehow I lost 3 frames over previous.

Previous, current:
4288, 4288 Ship appears
4312, 4311 text first textbox
4329, 4328 scroll first textbox
4335, 4334 blank first textbox
4338, 4337 text second textbox
4355, 4354 scroll second textbox
4359, 4358 blank second textbox
4364, 4363 text third textbox
4381, 4380 scroll third textbox
4387, 4386 blank third textbox
4391, 4392 textbox moves       <--- +2 timeloss
4399, 4400 moved out of screen 
4447, 4449 black               <--- +1 timeloss

Somehow I'm losing frames at the end of the textboxes.
Previous, Inputs from last AB press at 4376:
AB, 8x B until 4384, nothing, B, nothing, 
Current, Inputs from last AB press at 4375:
AB, 23x B until 4398

F5: Let's try the previous strat, from 4306.
Black at 4447. Mostly Success!
Now it only loses 1 frame instead of 3.
4386: blank third textbox (ok)
4390: textbox moves (no timeloss!)
4398: moved out of screen  (ok)
4447: black (+1 timeloss)
I don't understand that last frame of timeloss. But whatever.

Pluck at 4481.
F6: Skip at 4572. 2f timeloss to positioning.
222/43 until 4470, then 87/104
Pluck animation starts at 4489. Plucked at 4509.
(first frame where sprout is completely straight and clips through Olimar's nose)
Previous: 
226/37 until 4470, then 70,128 until 4481.
Pluck animation starts at 4487. Plucked at 4507.

F2: starts at 4488
Only loses 1 frame. Idk why I can't reproduce the previous thing.
Whistle at 4523.
Skip at 4571. Still 1 frame timeloss, but whatever.
Throw at 4633.
This time, there is enouth time to kill the bulborb! YAY!

Normal vs fast death animation:
0 HP, falling down, fallen over, no health bar
normal: 5222, 5230 (+8), 5278 (+56), 5311 (+89)
normal: 5343, 5351 (+8), 5399 (+56), 5432 (+89)
fast:   5390,          , 5417 (+27), 5434 (+44)
That really is double the speed. Nice.
Just kill the bulborb while it is turning on the spot.

Hit the pellet, Olimar X position at 4660, carry, START
F4: 4662, -267,     , 4909
F6: 4662, -292, 4709, 4891
F5: 4662, -292,     , 4899
F4: 4662, -288,     , 4889
(Previously, START was at 4870)

Bulborb kill (first hit, 0HP, no HP bar):
F4:       4868, 4912, ghost visible.
F5: 4702, 4865, nope, can't hear sound. This is probably a frame to late.
Louie is standing in the way. Go a bit to the right for a few frames.
Louie hits first at 4728. Misses two hits.
F7: 4702, 4873, nope.
F4: 4703, 4856, nope. Louie hits first at 4728. Misses one.
F6: 4702, 4860, YESSS, you hear the sound! Black at 4916
This might be frame-perect. Or the sound plays only in the cutscene fadeout, not in the menue fadeout.

4910 Menu R, 4943 Down, 4971 A, 4973 Up, 5001 Yes
5022 START, 5057 START
5103 makes text appear at 5111. Before and after is slower. Does before cause lag?
5122 A, 5175 A, 5177 A, 5244 A, 5246 A, 5370 A,
5394 Down, Down + A, 5434 A (black at 5488, input 28645)
F7 -> 0.2.3 bulborb killed just in time, day end at 5488.sav

Somehow my TAS-2 is faster on day2.
Timing stuff more precicely now.
4071 Black after area selection (spamming A)
4096 ( 25) Valley of Repose text
4266 (170) Ship appears
4290 ( 24) fadeout
4300 ( 10) text appears again
4387 ( 87) sprout lands
4547 (160) ship appears
4700 (153) black after text
4811 (111) black on first pikmin
4850 ( 39) after cutscene
4913 ( 63) Hit pellet. X pos: -346. Has way more running start.
5098 (185) bulborb 0 HP. Louie misses once, but starts late.
5142 ( 44) START, HP bar vanishes! There is lots of time.
5157 ( 15) black at cutscene skip
5327 (170) black after second ship cutscene.
The pellet takes from ~4956 to 5157 => 201.

And now, the current one.
3813 Black after area selection (spamming A)
3838 ( 25, same) Valley of Repose text
4008 (170, same) Ship appears
4032 ( 24, same) fadeout
4042 ( 10, same) text appears again
4129 ( 87, same) sprout lands
4288 (159, -1)   ship appears (looks different)
4447 (159, +6)   black after text
4560 (113, +2)   black on first pikmin
4599 ( 39, same) after cutscene
4662 ( 63, same) Hit pellet. X pos: -303
4860 (198, +13)  bulborb 0 HP. Louie misses once, but starts late.
4900 ( 40, -4)   START, still has HP bar.
4916 ( 16, +1)   black at cutscene skip
5085 (169, -1)   black after second ship cutscene.
The pellet takes 199.

Learnings:
Somehow, perfect text mashing is slower than alternating A and B.
The new bulborb kill is slower. Or the distance is more.
Distance should be 9 frames timeloss.

TODO:
New seed. Layout with ~200f collection time
and flower more to the left, for better throw angle.
Implement new Today's Report timesave.


### Day 2, third try
A press, text appears at:
3002: doesn't
3003: 3031
3004: 3031
3005: 3031
3006: 3031
3007: 3031
3008: 3031
3009: 3031
3010: 3031
3011: 3022 <--
3012: 3020 <--
3013: 3021
3014: 3022 (scene appears again)
Ok, so there is "a lot of lag" and "a little lag" and "no lag" or something.

Cutscene timing: Press later on fadeout, for 11f timesave.
2890, 2927, 2964; 
3012, 3031, 3084, 3086, 3153, 3155, 3279;
3303 down, 3315 down + A, 3343 A (black 3397);
3635, 3705, 3993

F7: pellet from 4769 to 4956 => 187; 
    To fast. But it can snipe pellet from X=-249. 
	About -338 when pellet hit. Almost as good as TAS-2.
    This seed might work out?

Textboxes: Start at 4295. 
B, 15x nothing, AB, 8x B, nothing, repeat
try 2: black at 4447, -11 = 4436.
F3: black at 4431, saved 5f somehow.


Try2: A at 4481, Straight sprout at 4488, 
    plucked at 4508, black at 560, skip at 4571, 
	throw at 4633, pellet hit at 4662 with X=-303.
F2: A at 4465 (-16), Straight sprout at 4473 (-15)
F2: A at 4465 (-16), Straight sprout at 4471 (-17), 
    plucked at 4491 (-17), black at 4543 (-17), skip at 4554 (-17), 
	throw at 4616 (-17).
    
The furthest away I can let go at full speed is X=-266. 
When hit X=-345. TAS-2 had X=-346, so this layout is just as good! Yay :)
F4: Adjust cursor until 4600. But can't moonwalk.
F4: Run up until 4600, adjust until 4611 (94|83), then down. To far by 7f.
F5: run 4593, adjust 4603 (82|93), adjust down, run down 4611.
F6: run up at 4619. Pellet hit at 4645 (-17), X=-344
    less walking by 8 frames.

Next: kill the bulborb.
F4: Lockout skip at 4881 or input 24997.
Would save time! yay!

First hit: 4677, then spam A.
F3: Success! Actually I have like 30f of possible timesave.
    How does that work?!
	RNG at 4670 = c68f...
	Dead at 4809, no health bar at 4853
F6: Ok, I can't really cahnge the RNG before the bulborb.
Dead at 4817, 4823, 
F6: RNG is 64ca... But hit is at 4678
F5: START at 4861.
F5: Dead at 4831, 4815. It worked! No health bar at 4859.
    Cutscene fadeout at frame 4878, input 24973
    (Try2 was 4916. 38f saved, of which 21 on better pellet)
F4: Dead at 4811, 4809, 4806
    It seems that wiggling the stick makes you punch faster.
    No health bar at 4850. START at 4861.

This could be another 10f faster. But not with this layout.
The Pikmin already grabs on as fast as possible.
F6: Same but more stylish.
Black at 4878, input 24973.

Try2: Black at 4916 (-38f). 
Now the times are:
4872 Menu R, 4905 Down, 4933 A, 4935 Up, 4963 Yes
4984 START, 5019 START
5065 makes text appear at 5073.
5084 A, 5137 A, 5139 A, 5206 A, 5208 A, 5332 A,
5356 Down, Down + A, 5396 A (black at 5450, input 28417)
5688 A, 5758 A, 6037 START (black at input 30937)


F4: Textbox away at 4975
F5: Textbox away at 4975

Spreadsheet inputs Try 2, Try 3, diff, split:
17314, 17242, 0.40s End of day 1
19882, 19816, 0.36s Landing cutscene (black after)
22378, 22282, 0.53s Extinction cutscene (black after)
25201, 24973, 1.27s Black on flower cutscene skip
28645, 28417, 1.27s End of day 2

### Day 3
RNG manipping pellets again. Best time is between 
bulborb kill and cutscene skip.

Near pellet, far pellet. Red 1|1 to grey 1|0.
(Day 2 has different timing method)
TAS-2: 163, 189
F3: 164, 184
F4: 158, 188 you can throw straight down.
F5: 176, 235
F6: 159, 188 -> F8

Let's do F4 -> F10.
Press A at 6137 and 6157. B at 6167. A at 6193.
Pellet hit, no health bar
F4: 6226, 6246
F5: 6222, 6255 no insta-kill
other pellet:
F6: 6217, 6237
F7: 6216, 6236

Last time it was faster to walk to the pellet 
instead of throwing.
Pellet hit, no health bar:
F6: 6218, 6238
F6: 6212, 6232
F7: 6212, 6232
F7: 6211, 6231

When picket up?
F5: 6271
None faster.
Cutscene skip at 6324.
Whistle at 6473 or 6475.
F4: C-Stick. Pick up at 6573.
F5: Throw. Pick up at 6559. Far away.
F5: Throw very near. 6551
F6: Louie skip black at 7067
F7: Skip at 7067, START at 7050

F7: START at 7049
7057 R, 7088 down, 7116 A, then up, 7146 A
7164 A, 7199 A, 7245 A, 7264 A, 
7317 A_A, 7386 A_A, 7512 A, 
7536 Down Down+A, 7576 A, black at 7630,
7868 A, 7938 A, 8217 START, 

A, Today's Report: 
7247: 7256
7246: 7255
7245: 7253
7244: 7255
7243: 7264

I'm at 3731 rerecords!
And 11 seconds faster than TAS-2!

### Day 4
There are 3 Pikmin in onion, 2 in ground.

#### Strategy
Old strategy in TAS-2:
Take out 3 from onion, pluck 2 with Olimar,
whistle Louie, throw 1 to 5-pellet, collect 5-pellet.
Push egg with Olimar
Push egg with Louie (pellet collects when down)
whistle Pikmin, throw 2 to far pellet, 2 to near pellet,
go up to egg with Louie. (Pikmin sprout in middle)
Pluck with Olimar.
Second pellet gets in on 4th Pikmin plucked.
Now I have 10 Pikmin. Mitites.

What can I do better?
I really need at least 10 Pikmin to collect mitites.
Get 1-pellets moving faster by not pushing second egg immediately.
Prioritize near 1-pellet?
Don't snipe far 1-pellet -> More time to get Louie up.
Get eggs down to 1 HP.
Do 10-pellet afterwards, when courage reactor is moving.
Snipe dwarf bulborb to get 1-pellet. Not body probably.
If I can get >10 Pikmin for mitites, less time would be wasted for whistling.

For egg push with both captains.
Possible to hug left wall?
Maybe switch to Louie on slope for better control?
If I manage a double egg push, I could redo day 2 and kill the bulborb after mitites.

What to do while waiting on CR?
There are ~26sec wasted in demonstration video. 
40sec total time from arriving at onion to collecting CR.
* 10-pellet. Takes 5 to 6 sec.
* far 1-pellet
* Write TAS with Pikmin like APerson.
* Third set of mitites: >30sec until sprouted. Nope.
  But with tripple egg push: <14sec to collect, 9sec to sprout
  Very viable! Probably even with 10-pellet.

Collection times:
near 1-pellet: 8809 to 9060 => 251f
far  1-pellet: 9509 to 9869 => 360f
5-pellet:    10301 to 10655 => 354f

Is there RNG here?
grouped posies: 138f and 179f. That's a lot nearer than on day 3!

Double and tripple egg push is actually pretty easy!
Just run along the right edge.
They even push themselves a bit.
Strat: Get 5-pellet collecting, run up with only Olimar,
Get eggs to push themselves down,
switch to Louie and get 1-pellets moving,
help push eggs with Olimar,
pluck with both captains, hopefully 12 Pikmin
(Right edge is easier than left edge)


#### Starting to TAS.
A under Onion on 8279.
8295 down _ down _ down+A
8309 B hold
8320 Louie whistled
8335 A to pluck
Alternatively: Pluck at 8337.
Plucking with Louie doesn't work.
When dismissing, his Pikmin either stays with him or dismisses too.
So pluck both with Olimar.

Collecting near red:
F6: 9132
F5: moves a bit earlier 
pellet after all pushes:
Done before sprouts pluckable. But 1-pellet not in time.

Now timing pellet before slope.
F4: Slope part takes from 8810 to 8980 => 170f
Switch+throw+switch takes 8810 to 9020 => 210f because waiting for 5-pellet.
Ok, doesn't work.

Switching back to Louie:
F3: 9021
F4: 8987
F8: 8978

Throwing, hit pellet:
F6: 9023, 9051
F7: 9019, 9050
F4: 9017, 9049

First Pik grabs, second, collects:
F2: 9103, 9126, 9360, 
F3: 9113, 9128, 9362, 

Opening egg:
F6: 9430
F7: 9430

Before I do mitites, I want to be sure I didn't miss anything.
* far 1-pellet will be done later.
* go through notes of TAS-2.

TODO:
Faster sprout growing. Wastes some time right now.
The first two sprouts should be as quick as possible.
The last two just not to slow.
Are the positions good enouth? Could be better.

old notes: 
* when you start plucking, there's a particular way to do it such that the first seed you pluck does the fast animation rather than the normal slow one
* getting your secondary captain to pluck first so they pluck on a better cycle for certain numbers of sprouts
* Timesave: Letting 10-pellet slide down the hill https://youtu.be/uMR9xyYrxV4?t=594


#### Posting my WIP on Discord:
There is much feedback :)
https://discord.com/channels/177495849100640256/698992259038838864/1232383264736411658

TODO Math out the strats.
Pikmin counts, timesave for extra Pikmin in AW,
timeloss for 1, 4 or 6 less Pikmin on gate,
what can be done between CR dig and collect


2 or 3 eggs at a time?
Standard_ does two amd starts mitites at 4:54 with day4 starting at 4:08 => 46sec
My WIP does three. (42868 - 49996) /180 = 39.6sec
Standard_'s 2eggs strat has 10 Pikmin for mitites, with both 1-pellets collected.
My 3eggs strat has 10 Pikmin with only one 1-pellet collected.

In Standard_'s video, first two eggs are pushed, then he collects both 1-pellets, then the third egg is pushed, then plucking. Mitites are spawned 46sec day start.
In my WIP, I push all three eggs down in one go, which takes longer. Then I collect only one 1-pellet and pluck. (The second wouldn't come in in time.) Mitites are spawned after 39.6sec.

That means all three eggs is about 6sec faster, at the cost of needing collect that last 1-pellet later. Probably after digging CR, where it shouldn't lose time. Also I can do the second set of mitites with at most 12 Pikmin. 14 would provide a small benefit.
Also, either the 3rd mitite set or the 10-pellet need to be collected before crushing the bags. The mitites would be the safe option, as I'm not sure there is time for that afterwards. The bigger timesave would be mitites later though, IF that even works.


Mitites after bags probably doesn't work, because to few Pikmin.
5 initial + 5 pellet + 3*2 pellet + 2*20 mitites = 56
+ 2 from far pellet is 58
+ 10 pellet + 20 mitites = 88
+ 4 dwarf bulborb + 2 pellet = 94 (with only 4 less Pikmin on gate; better than 5-pellet)

For bags and CR I need about 55 Pikmin.
Can't do all things after that, because no Pikmin are left.
So at least mitites or 10-pellet needs to happen before bags.
With mitites before, it's the safe option, since that takes the longest and grows 20.
With 10-pellet before, it's more risky: pluck 10, 4 from dwarf should be back, collect, sprout, pluck. All in under 40sec.


Check if I can do both far pellets before the first mitites.
Then I'd have 14 Pikmin for the second set.
Plucking there doesn't lose time, as long as I don't wait for the sprouts.

Near pellet: Pikmin free at 9361. Mitites at 9430.
Both pellets: Pikmin free at 9543, but ~20f optimizable.
That is 182f slower.
Sprouts happen at 9240. Captains arrive a second later.
-> Can I optimize the egg push by another second or two?
Pikmin at onion see captain at standing position for mitites. 
They could BARELY arrive in time for throwing.


Re-TASing from 5-pellet again. That carry is just perfect.
8490 DOWN to early. C:LEFT
8500 X
8515 R ANA 196,21
Collision version is 4 for a short moment, then XZ speed goes down to  100.
But the slippery geometry has collision 6. And the slowdown happens in the middle of the path too.

Re-TASing from a bit further up instead.
Egg push: First egg needs to be aligned a bit anyway. 
In that time, I can easily punch it to 1HP.
Aligning first egg takes at least 35 frames.
Last hit on first egg at:
F5: 8601
F4: 8603
F3: 8605
Pushing all three eggs on the flat part doesn't work. 
The furthest one just slides left but not over the slope.
Pushing one egg over edge first. Reaching collision 6 at:
F5: 8643, but turn around at 8625
F9: 8645, actually turns around at  8632
Collision 6 with all eggs:
F6: 8786
F9: 8813
F7: 8803
F4: 8787
When switching back (Louie visible)?
F7: 8898 (only 2 eggs down)
F9: 8978 (with zoom out)
F6: 8936
F8: 8962
F3: 8927 (2 eggs)
F3: 8939
F4: 8871 (2 eggs)
F3: 8929 (barely not 3 eggs)
F8: 8892 with 3 eggs! YAY!
F3: (8886) edited with zoom out.

TODO: Try to get all 3 eggs with F7
or redo F6 to take the better F7 egg path on the slope.
-> I saved 92f on the egg push :)


#### Getting Dolphin working under Linux, with Wine.
Installing wine:
https://wiki.winehq.org/Ubuntu
On Ubuntu 22.04:
sudo dpkg --add-architecture i386
sudo wget -O /etc/apt/keyrings/winehq-archive.key https://dl.winehq.org/wine-builds/winehq.key
sudo wget -NP /etc/apt/sources.list.d/ https://dl.winehq.org/wine-builds/ubuntu/dists/jammy/winehq-jammy.sources
sudo apt install libpoppler-glib8:{i386,amd64}=22.02.0-2ubuntu0.3
sudo apt install winehq-stable:amd64=9.0.0.0~jammy-1

On Ubuntu 24.04 it's just this to get wine 9.0:
sudo apt install wine

cd "/D/Dokumente/Pikmin2/TAS-3/Dolphin Lua Core v3.5.1/"
wine Dolphin.exe

Getting the controller to work:
https://www.reddit.com/r/wine_gaming/comments/hf5u14/wine_control_panel_controller_configuration/
https://selfmadepenguin.wordpress.com/2024/02/14/how-i-solved-my-gamecontroller-problems/

https://generalarcade.com/gamepadtool/
Mapping String:
03000000d620000011a7000011010000,Bensussen Deutsch & Associates Inc.(BDA) Core (Plus) Wired Controller,a:b1,b:b2,x:b0,y:b3,back:b8,guide:b12,start:b9,leftstick:b10,rightstick:b11,leftshoulder:b4,rightshoulder:b5,dpup:h0.1,dpdown:h0.4,dpleft:h0.8,dpright:h0.2,leftx:a0,lefty:a1,rightx:a2,righty:a3,lefttrigger:b6,righttrigger:b7,platform:Linux,
Version 2, with screenshot button:
03000000d620000011a7000011010000,Bensussen Deutsch & Associates Inc.(BDA) Core (Plus) Wired Controller,a:b1,b:b2,x:b0,y:b3,back:b8,guide:b12,start:b9,leftstick:b10,rightstick:b11,leftshoulder:b4,rightshoulder:b5,dpup:h0.1,dpdown:h0.4,dpleft:h0.8,dpright:h0.2,leftx:a0,lefty:a1,rightx:a2,righty:a3,lefttrigger:b6,righttrigger:b7,misc1:b13,platform:Linux,
Version 3, map screenshot as left stick press. misc1 isn't detected in Dolphin.
03000000d620000011a7000011010000,Bensussen Deutsch & Associates Inc.(BDA) Core (Plus) Wired Controller,a:b1,b:b2,x:b0,y:b3,back:b8,guide:b12,start:b9,leftstick:b13,rightstick:b11,leftshoulder:b4,rightshoulder:b5,dpup:h0.1,dpdown:h0.4,dpleft:h0.8,dpright:h0.2,leftx:a0,lefty:a1,rightx:a2,righty:a3,lefttrigger:b6,righttrigger:b7,platform:Linux,
Now I can use the screenshot button to save state 1! YAY!

The pro controller is different. Downloaded mapping vs. created one:
0500b7154c69632050726f20436f6e00,Nintendo Switch Pro Controller,crc:15b7,a:b1,b:b0,back:b8,dpdown:h0.4,dpleft:h0.8,dpright:h0.2,dpup:h0.1,guide:b12,leftshoulder:b4,leftstick:b10,lefttrigger:b6,leftx:a0,lefty:a1,misc1:b13,rightshoulder:b5,rightstick:b11,righttrigger:b7,rightx:a2,righty:a3,start:b9,x:b3,y:b2,hint:SDL_GAMECONTROLLER_USE_BUTTON_LABELS:=1,platform:Linux
0500b7154c69632050726f20436f6e00,Nintendo Switch Pro Controller,a:b0,b:b1,x:b2,y:b3,back:b8,guide:b12,start:b9,leftstick:b10,rightstick:b11,leftshoulder:b4,rightshoulder:b5,dpup:h0.1,dpdown:h0.4,dpleft:h0.8,dpright:h0.2,leftx:a0,lefty:a1,rightx:a2,righty:a3,lefttrigger:b6,righttrigger:b7,platform:Linux,crc:15b7,

sudo nano /etc/profile.d/sdl2-gamecontroller.sh
#!/bin/bash
export SDL_GAMECONTROLLERCONFIG="03000000d620000011a7000011010000,Bensussen Deutsch & Associates Inc.(BDA) Core (Plus) Wired Controller,a:b1,b:b2,x:b0,y:b3,back:b8,guide:b12,start:b9,leftstick:b13,rightstick:b11,leftshoulder:b4,rightshoulder:b5,dpup:h0.1,dpdown:h0.4,dpleft:h0.8,dpright:h0.2,leftx:a0,lefty:a1,rightx:a2,righty:a3,lefttrigger:b6,righttrigger:b7,platform:Linux,"

Then reboot.
wine reg add "HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\winebus" /v "DisableHidraw" /t REG_DWORD /d 1
wine reg add "HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\winebus" /v "Enable SDL" /t REG_DWORD /d 1
wine control

Only save state button is missing.

Dolphin can't overwrite its settings files for some reason.
Thus manually delete them before OK-ing the controller config.
/D/Dokumente/Pikmin2/TAS-3/Dolphin Lua Core v3.5.1/User/Config/
GCPadNew.ini  and  Hotkeys.ini

Creating a start menu shortcut:

nano "Dolphin.desktop"

[Desktop Entry]
Name=Dolphin TAS-3
Exec=wine "/D/Dokumente/Pikmin2/TAS-3/Dolphin Lua Core v3.5.1/Dolphin.exe"
Icon=/D/Dokumente/Pikmin2/TAS-3/Dolphin Lua Core v3.5.1/Sys/Resources/dolphin_logo.png
Path=/D/Dokumente/Pikmin2/TAS-3/Dolphin Lua Core v3.5.1/
Type=Application
Categories=Wine;Games;

Then drag&drop the file onto the task bar.


#### Asked about plucking:
> when you start plucking, there's a particular way to do it such that the first seed you pluck does the fast animation rather than the normal slow one

@curtis:
ok so the first time you pluck, from neutral, its a slower pluck, and then if youre continuously pressing A to auto-pluck without walking to each seed, then the 2nd pluck onward is fast, until you fully stop plucking and have movement control again
but sometimes you stop plucking and then start plucking again and the first pluck you do on the 2nd round is also the fast animation
for the longest time, we had no idea what could be causing that. i think jpep said recently that it might be because when youre doing 2-captain plucking, your 2nd captain can take the seed that the main captain tries to pluck, and then the main captain has to go to another seed, but still continues the fast-plucking animations on subsequent plucks. i think the idea is that if you get cut off by your second captain, and then you cancel plucking somehow around that time, the flag never gets set to go back to the slow pluck animation

Ok thanks. Does that mean you can't just get the fast plucking at the beginning?
as far as we know, no. like, theres no way to like start the run with the fast pluck animation


#### Plucking
Timing the first two plucks on day 4:
1 from 8330 to 8350 to 8368 => 20, 18 => 38f
2 from 8376 to 8382 to 8390 =>  6,  8 => 14f
Also 8f of "pluck adjust" inbetween.


Throwing to far pellet now.
Without whistling, Pikmin are throwable at 8942.
Whistle at 8898. But then pellet doesn't collect.
Whistle at 8904.
With whistling at 8927.

Throwing, hit:
F5: 8981, 9006
F6: 8976, 9003
F5: 8974, 9001
F6: 8974, 9001
Second throw at 8987.

RNG manip:
F5: throw at 9035
F6: throw at 9036 (same)
F6: stop at 9068 until 9078
F7: stop at 9088
F9: stop at 9086
F2: stop at 9083, long
F2: stop at 9086 until 9104
whistle Olimar at 9130.

TODO: Turn around camera before whistling.
I TASed 8sec today. Rerecords: 7758.

Ok, that worked.
Also I'm now TASing on Linux, on my new Framework laptop! YAY!

RNG manip for sprouts. When do come out?
F5: 9220, 9229, 9243, 9248 (glow 9279 => 59f)
F6: 9220, 9229, 9242, ???? (glow 9279 => 59f)
F6: 9212, 9219, 9237, ???? (glow 9270 => 58f)
F7: 9210, 9211, 9220, 9229 (glow 9269 => 59f)
F8: 9200, 9213, 9217, 9236 (glow 9258 => 58f)
F9: 9185, 9203, 9205, 9229
F4: 9178, 9201, 9203,
F5: 9221, 9224
F5: 9195, 9195, 9201
F6: 9197, 9201, 9226
F7: 9177, 9198, ????
F8: 9177, 9202, 9206
Sadly it's the second sprout that is so fast in F4, F7, F9.
I want the first two to be that fast.
Another session. Delete F3, F8, F9, F6, F5. Reassign F4, F7.
F3: 9177, 9194, 9201
F4: 9177, 9198, 9228
Run until, then measure:
F5 9162: 9220, 9230, 9237
F6 9160: same
F6 9158: 9198, 9220, 9223
F5 9159: 9220, 9220, 9229
F6 9157: 9194, 9220
F0 9156: 9220
F5 9155: 9196, 9220
F5 9153: 9184, 9220
F6 9151: 9177, 9203 right seed first
F7 9150: 9180, 9208 left seed first
F0 9149: 9201
Run until 9150, start again at
F8 9160: 9180, 9215
F8 9161: 9180, 9215
F8 9162: 9180, 9210
F0 9163: 9180, 9212
F8 9164: 9180, 9198
F8 9165: 9180, 9294
F0 9166: 9180, 9216
F0 9159: 9180, 9216
F9 9158: 9180, 9177 !!! YAY
I can barely see when the first one sprouts.
Might even be 9175 instead of all the 9180 above.
They are big at: 9234 and 9236.
Landing particles happen at 9159 and 9161.
So fastest surfacing is 16f and 75f until pluckable.

Now manipulating rest of the sprouts.
Landing, +75f pluckable:
#1: 9159, 9234, Louie +2+38 => 9274 finished, goto #4 (left)
#2: 9161, 9236, Olimar  +38 => 9274 finished, goto #3 (middle)
#3: 9176, 9251, must be ready at 9274
#4: 9195, 9270, must be ready at 9274, +50? => 9324
#5: 9212, 9297, must be ready at ~9324

Doable, but very tight.
Probably best to manip RNG for #3 and #4 with C-Stick.
Also adjust angle to stand on the right spot for
plucking as soon as possible.
For #3 and #4, Louie must pluck the farther one so
he finishes after Olimar, and Olimar gets to do #5.
Rerecords: 7977. That's two hundred for the first two sprouts.


Next session. Walk at a different angle.
F2: Before, at 9135.
F3: F9 but just after landing
F5: Just two frames of walking
Trying different angles. Run until 9150, start at 9158 for at least a frame.
When is Olimar below X=-80?
F6: 9196
F7: 9197
F0: 9208
F8: 9200  <-- let's use the more downwards angle.

Manipulating the third sprout. Run until, sprout appears:
F4: 9160, 9218
F0: 9161, 9218
F0: 9162, 9234
F0: 9163, 9234
F4: 9164, 9194, pluckable at 9253. Nice.
Can start tunning again at:
F5: 9173? Almost same timing.
F6: 9174
F7: 9174, but better angle.

Manipulating fourth sprout. Run until, sprout appears:
F8: 9174, 9224
F0: 9175, 9236
F8: 9176, 9211, pluckable at 9270.

Now position for plucking. Olimar must start first.
Fifth sprout doesn't matter much.
F9: Move again at 9193.
Can start plucking at: 9233.
Olimar is in pluck state at:
F3: 9246 (both)
F4: 9243
F5: 9242 (both)
F3: 9243 doesn't work.
F4: 9240 doesn't work.
F5: 9238 still doesn't work.
I think Olimar always goes to the farther one, even if Louie aborts plucking. Annoying.
Try with Louie on the other sprout first. Nope.

Ok, then do it with Louie plucking 3 Pikmin.
F6: Louie finishes at 9322, while Olimar is still plucking.
When do all captains pluck; finished
F6, F5: 9243
F4: 9246
F3: 9244
F3: 9242; 9325
F4: 9242; 9322
F0: 9242; Third sprout to slow.
F3: late; 9322
F3: 9241; 9320  <-- let's use this.

Next: Test mitites with the mitites hack.
Current rerecords: 8276.
Maybe C-stick Pikmin forwards before plucking? Doesn't really do anything.
Can throw again at 9327.

Egg breaks at:
F4: 9387
F4: 9371
F5: 9390 but mitites
F6: a bit better positioning
First mitite gets killed at 9427. When to throw?
I think this position is to near.
The first pellet is about a second to slow for those Pikmin to be useful.
I would need extra whistling.


#### Pellets & Plucking V2: The Plan
TODO: test how much exactly those Pikmin are to slow. => 55f
TODO: How much time does Louie take on plucking third sprout? => 19f
TODO: How much time does extra whistling cost on mitites? => 24f per whistle

The problem is that I only have 5 Pikmin to throw on the mitites.
Then I'd have to whistle and get some of those, plus two from pellet carry.
That will get back less than 5, so a third round of whistling is needed.

In TAS-2, on the second batch, I have 13 Pikmin.
1 on egg, 2 on pellets, 10 for mitites. Somehow that's 1 to few.
For third batch, I have 14 for mitites, of which 2 are left.

So for TAS-3, on second batch, 12 total Pikmin should be enouth.
1 on egg, 10 on mitites, 1 reserve. Will be a bit harder.
Pellets are not in the way.
I don't need the extra 2 from the far pellet.

New plan:
* Redo the part after switching to Louie
  and only get the near pellet. Bottelneck are the sprouts from 5-pellet
  and 2-pellet collecting.
  Then I have 9 Pikmin for first mitites.
* Better sprout pattern for plucking.
  I want Olimar to pluck 3 and Louie only 2.
  That wasn't possible with previous pattern.
  First two sprouts need to be reasonably far apart,
  but close enouth for Olimar to get to it before Louie.
  Third and forth must be in between first and second. Order doesn't matter.
  Olimar must finish first both times.


Timing previous:
Louie switch at 8877
Second pellet hit at 9057
Mitites appear at 9371, vulnerable at ~9427
First pellet collects at 9397
Would need more Pikmin at 9400
Can throw new Pikmin earliest at 9455. => 55f to slow.

When going for near pellet first, hit at: 8958  (F4)
That's 100f or 3.3sec faster. So ~1sec more faster than strictly needed.

Plucking third sprout with Louie: Takes from 9301 to 9320 => 19f

Extra whistling: Looking at TAS-2. Youtube frame-advance goes at 25 FPS. (WTF?)
First whistle: 19/25 sec
Second whistle: 20/25 sec = 0.8sec
Second batch, first whistle: 20/25 = 0.8sec  (would be 24f)

With the new plan I could save about 19f + 24f = 43f minimum.
Maybe ~67f if a fourth whistling is required.


Making a small video. Commands:
cd /D/Dokumente/Pikmin2/TAS-3/Dolphin\ Lua\ Core\ v3.5.1/User/Dump/Frames/
ffmpeg -i framedump0.avi -i ../Audio/dspdump.wav -map 0:v -map 1:a -c:v copy audiovideo.mp4
ffmpeg -i audiovideo.mp4 -filter:v scale=360:-1 -vcodec libx265 -crf 25 compressed.mp4


#### Pellets & Plucking V2: Just do it!
Press A at, throw at
F9: 8928, 8938
F3: 8928, 8935 good enouth.

RNG when Pikmin picks up pellet can be influenced
after the throw. Nice.

Angle: 206|23
Collect at:
F4: 9294 slow...
F5: 9287
F4: 9267
F5: 9274
F5: 9253 very good.
With that, the near pellet collects 144f faster
than with both pellets, instead of the estimated 100f.

Sprout RNG:
F4: good first three.
F5: All 5 good, but bad order.
F6: Might work out perfectly.
Nope! Olimar always uses the slow animation.
I think the second captain always uses the slow animation,
so my strat that Olimar plucks three can't work.
F7: 4 much more together, good order
F8: 4 perfect grouping
F4: Zooming
F4: 5 somewhat near
F4: Perfect grouping of all 5 sprouts :)

Sprout timings are the same as last try.
Louie spent 4+7+4=15f in pluck adjust state.
Sprouts enter the ground, +75f pluckable:
1: 9159, 9234, Louie  +38 => 9272 finished, goto 3
2: 9161, 9236, Olimar +38 => 9274 finished, goto 4; (actually finished at 9278 in last try)
3: 9178, 9253, Louie goto 5
4: 9194, 9269
5: 9212, 9285

I'm at 8819 rerecords.
Next time: RNG manip for growth time.

F3: Perfect grouping start.
left sprout, right sprout
Previous try: 9175, 9177
F4: 9199, 9200
F5: 9201, 9187
F6: third sprout at 9177
F7: 9175, 9209, 9217, RNG index: 896 on 9159; walk at 9153
F8: 9175, 9175. WTF?! That's better than last time!
How do sprout grow times actually work?
They are both pluckable at 9234.
So second sprout takes only 73f to be pluckable, and becomes visible after 14f.
Growing animation always takes 59f.

Anyway. Let's manip sprout 3.
It needs to be grown at 9272; thus visible at 9213.
F4: 9206; good enough.

Fourth sprout: Also needed at 9213.
F5: 9210

Fifth sprout: 9272 + 14f fast pluck => 9286 ready -59f => 9227 visible
Wait, that's impossible.
Measure in last try: Needed at 9301, visible at <9240
F6: 9234, Kinda good enough
F7: 9227; Wait I did the impossible
Hit ground at 9212 -> 15f in ground. Nice.

Rerecords: 8911
Next: Plucking. How few pluck adjust frames can I get?
Press A on 9231.
Louie in pluck state, walk state after third:
F9: 9241, 9320
F5: 9237, 9315 -> investigate
F4: 9244, 9341
F6: 9241, 9325
F8: 9241, 9349
F4: 9238, 9314
F8: 9238, 9311 (3, 1, 2) Pluck adjust frames
F4: 9236, 9311 (1, 4, 2)
F8: 9238, 9311 (3, 1, 2)
F6: 9236, 9309 (1, 2, 2) YESSSSS -> F3
That's 6 frames faster than last try :)

I'm at 8990 rerecords. Now: throw a Pikmin on eggs.
Can throw at 9316. Egg breaks:
F9: 9371
F4: 9358
F5: 9360 but left egg



