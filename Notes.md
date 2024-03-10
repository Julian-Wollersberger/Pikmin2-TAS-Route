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
F8: Camera switches at 2302
F9: Camera switches at 2301 -> even faster than take 1.
F2: First B at 2434. 
F3: Second dialog finished at 2565. Lockout ends at 2599
F4: Grab red at 1617.
F5: Grab red at 1618.

-> Continue with F4 and clean it up.