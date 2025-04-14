# The-N3tw0rk-writeup
Writeup for undutmaning ctf challenge "The N3tw0rk" 
<hr>

"You are a packet floating in the memory in a process."

<hr>

*Layout of the network*
![network chall](https://github.com/user-attachments/assets/c6ef418a-f938-4b7e-853d-df35f598e726)

<hr>
*Steps to complete the game

255

y

down

request tcp

manipulate tcp header src:31337

manipulate tcp header dst:25

down

request ip

manipulate ip header dst:198.51.100.25

request correct source address

request checksum

down

request ethernet

manipulate ethernet header dst-address:FF:FF:FF:FF:FF:FF

manipulate ethernet header src-address:E0:2C:B2:01:C0:A2

request checksum

upstream

upstream

port2

downstream

up

gi0/1

down

downstream

downstream

port1

downstream

up

up

request correct source address

manipulate ip header dst:198.51.100.33

request checksum

up

manipulate tcp header src:1080

manipulate tcp header dst:43891

request checksum

down

manipulate ip header dst:198.51.100.199

request checksum

down

upstream

upstream

port0

upstream

upstream

up

up

gi0/2

down

down

downstream

downstream

port1

downstream

up

request correct source address

manipulate ip header dst:198.51.100.199

request checksum

up

manipulate tcp header src:55643

manipulate tcp header dst:631

request checksum

down

request correct source address

manipulate ip header dst:198.51.100.182

request checksum

down

upstream

upstream

port3

downstream

up

up

request checksum

631

push boxes

`During the time when the director picks up the boxes;

inspect blobs

<hr>


<hr>
*from start to finish in bad order with all paths explored
pick a random byte - dont seem to matter in the game

You find yourself adrift in the shadowy memory of a process — a
concept that, rather unsettlingly, you grasp with ease. Surrounding
you is a frenetic swirl of data, bits, and bytes darting about like
nervous fireflies in a forest that never sees daylight. Some of these
bits seem dedicated to the same questionable task as you, while others
belong to different processes, each with its own secretive agenda. And
then there are the idle ones, lurking about with a vague air of
mischief, like digital ne'er-do-wells. A glowing, slightly pulsating
thread of light slithers away from the process, winding toward a
omnious black square not too far off. Below you, a suspiciously
labeled tube marked '31337' — perhaps an inside joke, or maybe
something more nefarious — plunges into the murky depths below.
There is one obvious exit: down.
Byte of data roaming the network and The process supervisor.
The terminal;
![Skärmavbild 2025-03-31 kl  13 55 44](https://github.com/user-attachments/assets/a8a038cc-5039-43d9-a4f6-1f2b8b51643f)

> ??go down

You find yourself drifting in what can only be described as the
bustling, and somewhat chaotic, transportation layer of a rather shady
computer's network stack. Packets of various shapes and sizes whizz
past you in every direction, some with purpose, others with an air of
aimlessness as if they've lost their way — or perhaps they're just
pretending to. Above you, a tube labeled '31337' leads upwards, while
a gaping opening below beckons ominously. A rather imposing
switchboard looms nearby, blinking and beeping with a sense of
self-importance, and off to one side, a large blackboard hangs in the
air, scribbled with all sorts of cryptic information.
There are two obvious exits: down and 31337.

An attentive clerk.
The blackboard;
![Skärmavbild 2025-03-31 kl  13 40 57](https://github.com/user-attachments/assets/55c189b6-a573-4984-ba02-6f6803134699)

request tcp
manipulate tcp header src:31337 - you need a source
manipulate tcp header dst:25 - from the terminal you see a mail server - common mail is 25

go down

request ip
manipulate ip header dst:198.51.100.25
request correct source address
request checksum

down

request ethernet
manipulate ethernet header dst-address:FF:FF:FF:FF:FF:FF - dont know where im going so broadcast
manipulate ethernet header src-address:E0:2C:B2:01:C0:A2 - mac address from the blackboard
request checksum

upstream
´thru the cable
upstream

Ah, you've arrived at a rather makeshift intersection in the grand
parade of data flow. This hub seems to have been thrown together in a
fit of temporary enthusiasm, with no one bothering to keep things tidy
or under control. You're floating amid a tangled mess of data traffic,
where three gateways splay out like the arms of a very confused
octopus. Two of these exits are bustling with packets zooming around
like caffeinated squirrels, while the third languishes in relative
solitude, its purpose as obscure as a cryptic riddle written in
binary.

There are three obvious exits: port0, port1 and port2.

> ??go port0

Upstream, before you, you see a luminous gateway and, beyond it, a
vast expanse of swirling data currents stretching out into what seems
to be infinity. This place seems to be a border between two very
different parts of this strange world of electricity, circuits and
information. Downstream is an orderly, calm and, compared to the
mayhem upstream, docile flow of data and you can see some sort of
digital intersection quite close. Upstream, beyond the gateway, you
sense a world teeming with possibilities, beckoning you to venture
forth and embark on a journey through the boundless realms of
cyberspace.
There are two obvious exits: upstream and downstream.

> ??go upstream

With a trilling sense of dread you slowly start to drift upstream...
You are sweapt up in the torrent of packets and are torn appart by the
unforgiving powers of the internet!
Closing down.

and port1 goes back up where you came from befor the switch

 > ??go port2

You find yourself in a data stream expressway, where packets of
various sizes are whizzing past you with the urgency of a last-minute
shopper on Christmas Eve. The sensation here is like being inside a
continuously running laser light show, with data darting about in
every conceivable direction. If you squint upstream, you'll spot the
cable leading to an intersection that looks like it was put together
on a Friday afternoon with whatever parts were left over. However,
downstream is where things get truly dramatic — a massive wall of
blazing flames stretches out in an endless, fiery expanse, as if
daring you to get any closer. It's both impressive and a little
nerve-wracking, like looking at a dragon's mouth from a safe
distance.
There are two obvious exits: downstream and upstream.

> ??go downstream

You find yourself at the foot of an enormous wall of roaring flames,
the kind that would make even the bravest packet think twice before
proceeding. The heat pulses in waves, making you feel like you're
sweating, though it's all very metaphorical, of course. All around
you, stern-looking entities hover, casting suspicious glances at every
passing packet as if expecting someone to suddenly burst into flames
(which, given the surroundings, seems quite plausible). The atmosphere
is tense, and at the base of a towering staircase leading upwards, a
queue of jittery packets stands nervously, waiting for their turn to
ascend to loftier levels.
There are two obvious exits: up and upstream.

> ??up

A Stressed technician examines you carefully.
A Stressed technician lets you pass upward.manipi

You find yourself on a precarious platform high up the side of a
blazing firewall. The heat is intense, and the light is so bright it
feels like your metaphorical retinas are being seared. The platform,
wide enough to avoid falling off (if you're careful), seems to be made
of the same flames as the wall itself. Fortunately, as a sentient
packet, you're spared the inconvenience of being set alight. A large
staircase leads both up and down, while two gateways beckon you into
the fiery depths of the wall. One of these, however, has been
resolutely sealed with a stern-looking sheet of metal. Clearly, not
all packets are welcome here.
There are three obvious exits: up, down and gi0/1.
A stern security guard."

> ??up

A Stern security guard eyes you with a practiced and suspicious gaze.
A Stern security guard says: Your identification seems to be in order. Welcome!
A Stern security guard steps aside and lets you through.

The contents of your IP header alters!
You stand on a platform precariously wedged between two towering walls
of fire, which meet at a perfect right angle as if they were on
unusually good terms. Unfortunately, the fire doesn't continue in the
other two directions, leaving nothing but a yawning void. Openings in
the fiery walls beckon you towards the unknown beyond, while
staircases, resembling particularly fiery snakes, curl both upwards
and downwards from the platform. The whole scene gives the impression
that the laws of physics are taking a very long tea break.
There are four obvious exits: up, down, gi0/0 and gi0/2. 
A diligent security officer.

there are signs here; 
> ??exa large sign

.---------------------------------------------------------------------------.
| Entrance to Gi0/0 - Take care! Here be monsters!                          |
|                     Hazardous conditions exist. Travel at your own risk!  |
'---------------------------------------------------------------------------'

> ??exa small sign

.----------------------------------------------------------------.
| Entrance to Gi0/2 - Only authorized packets beyond this point. |
'----------------------------------------------------------------'

*(At this moment your only way is down...)

> ??down

You are drifting lazily at the foot of a towering wall of flames that
stretches upwards like the sort of thing that would have any sensible
fire safety inspector fainting dead away. The wall climbs far beyond
what you can see, though your view is promptly cut short by a platform
hanging somewhere above, like a ceiling that's had enough of being up
and has decided to see what the ground looks like. A staircase clings
to the side of the wall, winding its way up to that very platform. To
your left, the wall abruptly turns at a sharp right angle, forming a
corner that seems to exist solely to make the wall look more
impressive. Off to one side, a gateway yawns open, leading into a
corridor that feels suspiciously like it's going downstream, though
where it flows is anyone's guess.
There are two obvious exits: up and downstream.
A security officer on the prowl and A stressed technician.

> ??Security officer leaves downstream.

Security officer arrives.
goSecurity officer says: Have you seen any suspicious packets in the area?

> ??go downstream

You are drifting through what appears to be a tunnel, though calling
it that might be a bit generous. The walls, floor, and ceiling are all
of the circular variety, or they would be if they were solid, which
they most certainly are not. Everything here seems a bit ethereal,
like something out of a half-forgotten dream. Around you, flashes of
light zip by, clumping together into little bundles of data, scurrying
along with the sort of urgency usually reserved for people who realize
they've left the oven on. It's abundantly clear that this is not a
place where data stop for a cup of tea and a chat, but rather a
thoroughfare, whisking them away to far more interesting
destinations.
There are two obvious exits: upstream and downstream.

> ??Security officer arrives.

??go downstream
You find yourself at a crossroads in the bustling realm of bits and
bytes. This is no ordinary crossroads, mind you — it's the kind of
place where decisions are made, where paths diverge, and where packets
must choose their destiny, or at least which exit to take. In the
center of this grand junction, a strange figure stands on a raised
circular platform, surveying the scene with an air of someone who
knows far more than they're letting on. All around the perimeter,
gateways beckon, some open and inviting, others closed and decidedly
less welcoming. Above you, the ceiling looms like a dome made of woven
wires and circuits, though you can't help but wonder if it's all just
an elaborate illusion concocted by your overworked imagination.
There are five obvious exits: port0, port1, port2, port3 and port4.
A traffic officer.

port0 takes you back where you came from
at this part you can find a lot of clues in port1 thru 4

And around (inside?) the switch you need to watch out for the "security officer on the prowl"
Is comes from an IPS(intrution prevention system). 
And the security officer will zapp you out of existence


> ??port1 

A Traffic officer examines you carefully.
A Traffic officer lets you float through the exit.
Happily you zipp along what appears to be the inside of a tunnel, but
something gives you pause — a certain unreality to your
surroundings, as if the walls, floor, and ceiling are only
half-present, existing more in the realm of ideas than in solid
reality. It's like traveling through a pipe that can't quite decide if
it's real or not. Upstream, you glimpse the vague outline of some sort
of structure, while downstream, an intersection looms in the distance,
bustling with activity.

There are two obvious exits: upstream and downstream.

A security officer on the prowl.

> ??downstream

You stand at the ground floor of a rather unremarkable building, the
very epitome of functionalism. The space around you is stark and
utilitarian, as if someone had taken a vow of minimalism and then
decided to make it a way of life. Packets dart about with purpose,
their efficiency seeming almost palpable as they zip up and down the
staircase. The environment hums with the whirring of unseen gears and
the faint crackle of electricity, a subtle reminder that in this
realm, speed and efficiency are the only measures of worth. The
staircase, a sturdy conduit for the relentless stream of data, ascends
with no pretensions. Next to it, a small desk, manned by a
receptionist, stands guard. Behind you, an opening leads upstream into
a tunnel, while ahead, the staircase beckons with a promise of
continued efficiency.

There are two obvious exits: up and upstream.

An efficient receptionist.

> ??up

A Receptionist examines you carefully.
A Receptionist lets you pass upward.
You are floating within a vast expanse that feels like the interior of
an over-sized warehouse, the sort of place where efficiency is not
just a goal but a lifestyle. The walls are adorned with large posters,
each covered in elaborate charts and intricate maps that seem to pulse
with purpose. Packets scurry about with an almost comical sense of
urgency, ferrying colossal amounts of data with a speed that makes
your circuits spin. A staircase descends into the lower reaches, while
a spiral ramp ascends toward the higher echelons of this data-driven
edifice.

exa posters

The room is festooned with large posters, their presence a testament
to the room's commitment to speed and efficiency. They are scattered
around, some hanging on the walls and others propped up on racks, each
one showcasing detailed charts and maps that would make a cartographer
weep with envy.

> ??exa charts

Charts here are a chaotic array of numbers, symbols, and equations, a
visual cacophony that's all about precision and speed. They're the
kind of charts that suggest if you look closely enough, you might see
the very threads of data being woven together.

> ??exa maps

These maps are not of the quaint variety you might use for a leisurely
walk. No, these maps depict complex networks and nodes, sprawling
diagrams that look like they could be the blueprint for a
hyper-efficient data distribution system.

There are two obvious exits: up and down.
A stern engineer.

> ??up

A Stern engineer examines you carefully.
A Stern engineer lets you pass upward.

You find yourself in what might be mistaken for a bustling shipping
depot, if only instead of boxes there were bundles of bits and bytes.
The entire room hums with activity, a constant whirlwind of packets
moving with purpose. A team of meticulous entities, overseen by a
grumpy administrator with an air of absolute authority, ensure that
every packet is in its proper place. Amidst this controlled chaos, a
circular ramp leads downwards while two impressive tubes rise upwards.
One tube, looking well-travelled and slightly tarnished, seems to have
been in use for quite some time, while the other, gleaming with a
recent polish, suggests a more modern route.
There are three obvious exits: down, 1080 and 22493.

A grumpy administrator.

> ??1080

A Grumpy administrator examines you carefully.
A Grumpy administrator lets you pass upward.

You've stumbled into a chamber that resembles a highly efficient
customs office, only without the dubious pastries. The room is neatly
divided into two distinct territories by a colossal desk that appears
to be the nerve center of this operation. On one side, packets arrive
in a flurry, like eager pigeons at a bread-throwing contest. They are
swiftly sorted, torn apart, and scrutinized with an intensity usually
reserved for top-secret documents. Once dissected, their contents are
scrutinized, repackaged with a fresh layer of secrecy, and then
dispatched through a gaping chasm in the floor.

There is one obvious exit: down.
A logistics supervisor.

> ??exa clipboard

While the administrator seems to be a bit extra occupied you take the
oppertunity to sneak a peek of its clipboard:
- Interfaces -
 eno1: inet 198.51.100.33 netmask 255.255.255.128 broadcast 198.51.100.127
       ether E4:3A:6E:00:32:67 mtu 1500
- ARP table -
 Address          HWtype  HWaddress            Iface
 198.51.100.1     ether   00:03:32:F2:33:22    eno1
- Current IP routing table -
 Destination     Gateway         Genmask         Use Iface
 default         198.51.100.1    0.0.0.0            eno1  
 198.51.100.0    0.0.0.0         255.255.255.128    eno1  
- Netstat -
 Proto     Local Address           Foreign Address         State
 tcp       0.0.0.0:1080            *:*                     LISTENING
 tcp       198.51.100.33:22493     23.253.58.227:443       ESTABLISHED
 tcp       198.51.100.33:1080      198.51.100.199:43891    ESTABLISHED



*Instead of port1 

> ??port2

A Traffic officer examines you carefully.
A Traffic officer lets you float through the exit.
You find yourself in yet another one of those claustrophobic, pipelike
corridors that seem to snake their way across the network, carrying
out their mysterious and undoubtedly important duties. Important, yes,
but certainly not glamorous. The decor here leaves much to be desired
— two stars on Google Maps would be optimistic, especially given the
eerie silence and the occasional flicker of something moving just out
of sight. The tunnel stretches upstream towards a bustling interchange
and downstream towards a building that exudes a distinct, unwelcome
aura. The kind of aura that makes you wish you were anywhere but here,
preferably with a hot cup of tea and a very thick firewall between you
and whatever lies ahead.

There are two obvious exits: upstream and downstream.


> ??downstream

You find yourself at the base of a towering, menacing structure, a
twisted conglomeration of steel beams arranged in a way that suggests
the architect had a grudge against right angles — and possibly
humanity itself. The entire edifice seems to glare down at you with
silent hostility, daring you to approach. Barbed wire coils around the
sharp edges, and you can almost hear it whispering unpleasant things
about what it might do if you get too close. A narrow staircase clings
precariously to the outside of the tower, spiraling upwards to a
platform shrouded in shadow. It's the sort of place that doesn't need
signs to say "Keep Out" — the very air feels thick with warnings,
and a distinct sense that whatever lives here does not appreciate
visitors.

There are two obvious exits: up and upstream.

An irritable overseer.

> ??Security officer arrives.

Security officer says: Any packet that's not up to snuff better watch out.

> ??go up

An Irritable overseer examines you carefully.
An Irritable overseer lets you pass upward.
You find yourself standing on a platform that clings to the side of a
steel-beam tower like an unwelcome parasite. The platform, much like
the rest of the tower, exudes an aura of hostility. The railing that
runs along the edge is topped with vicious spikes, as if the structure
itself is telling you to stay back — or else. The few packets that
drift through here move with a grim determination, their digital faces
set in expressions that range from anxious to outright terrified.
Occasionally, an official-looking packet descends from above, only to
quickly vanish down the staircase that spirals into the shadowy depths
below. A ladder, bolted unceremoniously to the side of the tower,
leads up to another equally unwelcoming platform above.

There are two obvious exits: up and down.

A grumpy inspector.
> ??exa inspector

A swirling vortex of data takes the vaguely intimidating form of a
surly inspector, its displeasure radiating like a dark cloud. Draped
in a drab, dark uniform with "IPS" emblazoned in stark white letters
across the back, it wields a tablet with the air of someone who's just
waiting for you to make a mistake. The screen occasionally flickers
with what looks like a map, but you're not about to ask for a closer
look. This is not the sort of entity you want to cross, but if you're
desperate, you might have no choice but to request help from it.


> ??up

A Grumpy inspector examines you carefully.
A Grumpy inspector lets you pass upward.
You find yourself near the summit of the steel beam tower, standing on
a platform that seems to vibrate with barely-contained tension. Above
you, a swirling mass of smokelike material pulses ominously, its dark
form roiling with an unsettling energy. The platform itself is barren,
save for a switchboard affixed to the tower's skeletal structure. The
floor is pockmarked with blackened patches, each one a silent
testament to the violent forces that seem to haunt this place. The air
is thick with the scent of burnt circuits, and the occasional flash of
red lightning within the cloud above casts eerie shadows across the
platform. A ladder leads downwards through a gap in the floor,
offering the only escape from this malevolent height.
There is one obvious exit: down.

Focused security dispatcher.

exa screen

- Interfaces -
 eth0: inet 198.51.100.5 netmask 255.255.255.128 broadcast 198.51.100.127  ether 3C:7D:1C:F3:44:0C mtu 1500

- ARP table -
 Address          HWtype  HWaddress            Iface
 down     ether   00:03:32:F2:33:22    eth0
 198.51.100.15    ether   00:14:22:03:5A:B2    eth0
 198.51.100.5     ether   3C:7D:1C:F3:44:0C    eth0
 198.51.100.33    ether   E4:3A:6E:00:32:67    eth0
 198.51.100.25    ether   00:14:22:FE:61:12    eth0

- Current IP routing table -
 Destination     Gateway         Genmask         Use Iface
 default         198.51.100.1    0.0.0.0            eth0  
 198.51.100.0    0.0.0.0         255.255.255.128    eth0  

- Netstat -
 Proto     Local Address           Foreign Address         State


*instead of port1 or port2

> ??port3

You've found yourself at the lively entrance of what might be the
hottest nightclub in the network. The building before you exudes an
irresistible allure, with flashing lights and pulsating beats echoing
from within. Packets, like eager party-goers, are lined up in a queue,
each one wriggling with anticipation to join the festivities inside.
The staircase leading up is flanked by shimmering lights and a vibrant
crowd of packets waiting their turn to be admitted. The buzz of
excitement is palpable, and you can almost feel the rhythm of the
digital beats even from here.

There are two obvious exits: up and upstream.
An arrogant bouncer.

> ??up

A Bouncer examines you carefully.
A Bouncer lets you pass upward.

You find yourself in what can only be described as the digital
equivalent of a nightclub's wardrobe area. It's an enormous space,
brimming with the frenetic energy of packets shedding their bytes and
picking up new ones as though they were swapping outfits. Every time a
packet passes through, it's as if it's changing costumes for the next
big event, leaving a trail of discarded data like confetti. Busy
digital entities scurry about, performing their duties with the sort
of efficiency that suggests they've had a strict code of conduct
drilled into them since they were mere bytes. Above you, a circular
staircase winds its way upward, promising more of the same dazzling
chaos and excitement, while lights and sounds hint at the revelry
beyond.

There are two obvious exits: up and down.

> ??up 

A Network concierge examines you carefully.
A Network concierge lets you pass upward.

Welcome to the bustling antechamber of the digital nightclub! This
place feels like the bustling foyer of an exclusive venue, with an air
of anticipation that crackles more intensely than a New Year's Eve
crowd. Above, you can barely discern the weight of revelry pressing
down on this space, as if the entire edifice extends upwards into
infinity, or perhaps into the realm of gigabytes. Three grand tubes
dominate the room, each leading up to where the party is clearly in
full swing. Two of these tubes are larger and prominently marked with
the numbers '80' and '443', from which a vibrant cascade of sounds and

lights descends in a thrilling, chaotic display. The third tube,
marked '22', is smaller and less flamboyant but equally important. The
packets, like eager club-goers, bustle about, entering and exiting
these tubes with an energetic fervor. A switchboard with a softly
glowing display sits to one side, its screens flashing with cryptic
data. Below, a circular staircase descends to the more mundane layers
of the network.

There are four obvious exits: down, 80, 443 and 22.

A laid-back usher.


> ??80

An Usher examines you carefully.
An Usher lets you pass upward.

You have stepped into what can only be described as the frenetic heart
of the digital revelry. This place is less a room and more an entire
universe of sensory overload, where reality seems to have taken a
holiday. Gigantic screens loom overhead, each displaying an unending
parade of video clips that range from the riveting to the absurd.
Monstrous speakers, which appear to have been stolen from a dragon's
lair, blast out music that oscillates between 'epic' and 'slightly
deranged.' In the midst of this cacophony, teleprompters whirl by,
scrolling text at speeds that suggest they're in a hurry to get
somewhere else. Packets, those elusive digital wanderers, dart in and
out of the room through an enormous, gaping hole in the floor. New
arrivals are pint-sized and chipper, while the departing packets are
bloated and groaning under the weight of their newfound information.
The scene is an exhilarating chaos, where order might exist but is
likely disguised as one of the revelers.

There is one obvious exit: down.

A wildly enthusiastic promoter.

> ??443

An Usher examines you carefully.
An Usher lets you pass upward.

You have stepped into what can only be described as the frenetic heart
of the digital revelry. This place is less a room and more an entire
universe of sensory overload, where reality seems to have taken a
holiday. Gigantic screens loom overhead, each displaying an unending
parade of video clips that range from the riveting to the absurd.
Monstrous speakers, which appear to have been stolen from a dragon's
lair, blast out music that oscillates between 'epic' and 'slightly
deranged.' In the midst of this cacophony, teleprompters whirl by,
scrolling text at speeds that suggest they're in a hurry to get
somewhere else. Packets, those elusive digital wanderers, dart in and
out of the room through an enormous, gaping hole in the floor. New
arrivals are pint-sized and chipper, while the departing packets are
bloated and groaning under the weight of their newfound information.
The scene is an exhilarating chaos, where order might exist but is
likely disguised as one of the revelers.

There is one obvious exit: down.

A wildly enthusiastic promoter.

> ??22 (ssh)

An Usher examines you carefully.
An Usher lets you pass upward.
You find yourself in what can only be described as the bureaucratic
heart of secure data transmission, a place where packets are shuffled
with all the gravity of a civil servant filing tax returns. The
process itself is a minimalist affair, floating serenely in the vast
expanse of memory, which seems to stretch on for miles in every
direction — or possibly just a few kilobytes, depending on your
perspective. Around the edges of this floating isle of purpose,
several large, ominous black squares hover, like silent judges at a
particularly dreary trial. Only one of these squares is currently
active, emitting a faint glow as if it's deep in thought, or perhaps
just napping witheone eye open.

There is one obvious exit: down.
> ??exa terminal

.------------------------------------------------------------------------------.
| admin@web: $ sudo apt update                                                 |
| [sudo] password for admin:                                                   |
| Hit:1 http://deb.debian.org/debian stable InRelease                          |
| Hit:2 https://deb.nodesource.com/node_14.x buster InRelease                  |
| Hit:3 http://security.debian.org/debian-security stable/updates InRelease    |
| Reading package lists... Done                                                |
| admin@web: $ sudo apt install --only-upgrade nodejs                          |
| Reading package lists... Done                                                |
| Building dependency tree                                                     |
| Reading state information... Done                                            |
| nodejs is already the newest version (14.18.2-1nodesource1).                 |
| 0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.               |
| admin@web: $



*instead of port1,port2 or port3

> ??port4

A Traffic officer examines you carefully.
A Traffic officer lets you float through the exit.
You've found yourself adrift in a cylindrical corridor of sorts, an
expanse that could be the tunnel of a colossal mechanical beast or
just a remarkably large straw. Pulses of light flicker along the
walls, casting an ever-changing spectacle as packets zip by in a
ceaseless ballet of binary brilliance. Upstream, the tunnel opens into
a bustling expanse resembling a chaotic carnival of data. Downstream,
however, is a more subdued affair — a drab, uninspired structure
that could be the very essence of bureaucratic dullness or a shoebox
pretending to be an office building.
There are two obvious exits: upstream and downstream.

> ??downstream

You've stumbled into the ground floor of what can only be described as
an architectural relic. The building's grey, boxy exterior could
easily be mistaken for an oversized filing cabinet, and everything
within seems to be stuck in a perpetual state of obsolescence. The
exposed wiring trails along the walls like neglected vines, and the
cables look as if they might short-circuit if someone merely glanced
at them too sharply. The fluorescent lights above cast a cold,
unfeeling glow that makes even the most vibrant hues seem to retreat
into the drab monotony of yesteryear. An old, battered desk, as worn
as a centenarian's slippers, sprawls along one wall, behind which an
attendant stands, embodying the spirit of ennui. The staircase leading
up to the higher floors seems as tired as the rest of the place, and a
tunnel leads away upstream, presumably to somewhere that isn't
suffering from the same dreary fate.
There are two obvious exits: up and upstream.
A security officer on the prowl and A bored attendant.

> ??up

An Attendant examines you carefully.
An Attendant lets you pass upward.

You find yourself perched at the summit of an ancient and somewhat
creaky staircase. It leads either up to this realms of yet
undiscovered marvels or down into the depths of bureaucratic tedium,
depending on your viewpoint. Surrounding you is a cavernous warehouse
that might have been state-of-the-art in the early days of the digital
age. Packets dart about with a sense of purpose, if not urgency, as
they are directed by various official-looking entities floating around
with an air of importance. Another staircase, circular and imposing,
spirals upwards while packets continue their steady procession up and
down its length.

There are two obvious exits: up and down.

A dispassionate administrator

> ??exa warehouse

The room you're in resembles a warehouse from a bygone era, spacious
and a touch forlorn. It has an air of being both underused and
over-extended, designed for a time when packing and sorting was a
grand affair.

> ??up

A Dispassionate administrator examines you carefully.
A Dispassionate administrator lets you pass upward.
You've stumbled into a room that looks like it was designed by someone
who thought bureaucracy and ancient technology made an excellent
pairing. This place is dominated by three grandiose tubes, their metal
surfaces adorned with the patina of time and the occasional suspicious
stain. Each tube boasts a sign with a number, like a peculiar
old-fashioned lottery where everyone's a winner, provided they don't
mind the rust. The staircase leading downwards is sturdier than it has
any right to be, groaning under the weight of its own history. In one
corner, a blackboard stands stoically, as though it has resigned
itself to being the repository of outdated information and forgotten
deadlines.

There are four obvious exits: down, 53, 25 and 110.
A grumpy administrator.


> ??25

A Grumpy administrator examines you carefully.
A Grumpy administrator lets you pass upward.
You find yourself in a drab and uninspiring room that seems to have
been plucked straight from the archives of bureaucratic history. Here,
the monotonous hum of bureaucracy is palpable. The room is cluttered
with heaps of letters, which are intermittently delivered by packets
that seem to move with a purpose so singular that it borders on the
absurd. The letters are shuffled around by entities that have
perfected the art of appearing busy while accomplishing very little.
Occasionally, one of these entities will carry off a letter, only for
it to reappear through a tube-like opening in the floor, presumably on
its way to another equally uninspired location.

There is one obvious exit: down.



 > ??53

A Grumpy administrator examines you carefully.
A Grumpy administrator lets you pass upward.

You find yourself floating in what can only be described as a
bureaucratic data vortex. It's as if a cosmic filing cabinet exploded,
and all its contents decided to drift around in a sort of well-ordered
chaos. The centerpiece of this room is an imposing list, suspended in
mid-air with an air of utter importance, as though it's the very
essence of order itself. Packets drift upwards from below, only to be
intercepted by various entities who handle them with a meticulousness
that borders on the obsessive. After interacting with the list, these
packets, now transformed, make their way back downwards, bearing the
fruits of their bureaucratic labor.

There is one obvious exit: down

> ??exa list

You drift close and try to read from the list. It says:
 This is the hosts file used by dnsmasq
Format: IP_address hostname [aliases...]

 DNS server
198.51.100.25 ns.n3tw0rk.ex ns 

Web server
198.51.100.15 n3tw0rk.ex www.n3tw0rk.ex 

Mail server
198.51.100.25 mail.n3tw0rk.ex mail 

Proxy server
198.51.100.33 proxy.n3tw0rk.ex proxy 

Firewalls/gateways
128.32.137.12 fw1.n3tw0rk.ex gateway1
198.51.100.1 fw1.n3tw0rk.ex gateway1.n3tw0rk.ex
198.51.100.129 fw1.n3tw0rk.ex gateway1.n3tw0rk.ex

Internal
198.51.100.182 printer.n3tw0rk.ex
198.51.100.199 workstation.n3tw0rk.ex
198.51.100.194 admin.n3tw0rk.ex




> ??110

A Grumpy administrator examines you carefully.
A Grumpy administrator lets you pass upward.
You've found yourself in a remarkably unadventurous room where the
walls are plastered with an impressive array of mailbox units. They
are arranged in neat rows and columns, creating a seemingly endless
maze of grey metal. The room is lit with a harsh, unforgiving light
that reflects off the shiny surfaces, making everything look even more
sterile and bureaucratic. The only notable feature in this room is a
small desk, where an intern, looking as though they'd rather be
anywhere else, stands idly by. An opening in the floor hints at the
way forward from this overly orderly space.

There is one obvious exit: down.

A bored intern.

exa mailbox

Each mailbox unit is a small, grey metal box with a locked door facing
the room. Each door has a tiny label, though one seems to be slightly
ajar. A closer look reveals that this particular mailbox is labeled
"alex"

> ??exa alex mailbox

The door on the mailbox labeled "alex" is slightly ajar. It looks like
it might be worth investigating. Curiosity might not have killed the
cat, but it could certainly lead to an interesting discovery here.

investigate alex mailbox

Investigate inside, or search, what?

> ??search alex mailbox

You open the mailbox door and quickly look through the mail within.

Good thing your a quick reader!
You read:

"A long email thread with some fun things"

those things are;
ICAgICAgLi0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS4K
ICAgICAgfCBHb29kIHdvcmssIGJ1dCB5b3VyIGZsYWcgaXMgaW4gYW5vdGhlciBjYXN0bGUhIHwK
ICAgICAgJy4gLi0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLScK
ICAgICAgIHwvIAogICAgICAgJyAgICAKICAoXF9fLykgIAogIChvJy4nbykgCiAgKCIpXygiKQoK
(base64 for)
      .------------------------------------------------.
      | Good work, but your flag is in another castle! |
      '. .---------------------------------------------'
       |/ 
       '    
  (\__/)  
  (o'.'o) 
  (")_(")


and an email attachment in base64 wich is a image, this image
![download (1)](https://github.com/user-attachments/assets/4cdb9976-7b87-49dc-bc56-8b938e6abc7e)

and in the end of all those emails
SW5zdHJ1Y3Rpb25zCi0tLS0tLS0tLS0tLQoxLiBSZXRyaWV2ZSB0aGUgZW1haWwgd2l0aCBzdWJq
ZWN0IElNUE9SVEFOVCAoeW91IHNob3VsZCBoYXZlIGl0IGluIHlvdXIgaW5ib3ggc29vbikKMi4g
UHJpbnQgaW5mb3JtYXRpb24gaW4gdGhlIG1haWwKMy4gRGVsZXRlIHRoZSBtYWlsIGZyb20geW91
ciBpbmJveAo0LiBQaWNrIHVwIHlvdXIgcHJpbnRlZCBkb2N1bWVudAo1LiBJbml0aWF0ZSB3b3Js
ZCBkb21pbmF0aW9uIQoKVGhlIGluZm9ybWF0aW9uIGlzIGZvciB5b3VyIGV5ZXMgb25seS4gS2Vl
cCBpdCBzZWNyZXQsIGtlZXAgaXQgc2FmZSEK==

wich is base64 of;

Instructions
------------
1. Retrieve the email with subject IMPORTANT (you should have it in your inbox soon)
2. Print information in the mail
3. Delete the mail from your inbox
4. Pick up your printed document
5. Initiate world domination!

The information is for your eyes only. Keep it secret, keep it safe!


*now we look for a printer
We know that there is an "internal network" and an proxy
In the proxy we saw on the cliboard that there was a established
" tcp       198.51.100.33:1080      198.51.100.199:43891    ESTABLISHED "

go up in port1 all the way up to where you can chose tcp och udp headers
and 
manipulate tcp header src:1080 - from the proxy
manipulate tcp header dst:43891 - to the listening port
request checksum 

go down and
request correct source address
manipulate ip header dst:198.51.100.199 - to the workstation

now go back down to the swich and watch out for the security officer

and go thru port0 (back to the gateway)

back up to;
The contents of your IP header alters!
You stand on a platform precariously wedged between two towering walls
of fire, which meet at a perfect right angle as if they were on
unusually good terms. Unfortunately, the fire doesn't continue in the
other two directions, leaving nothing but a yawning void. Openings in
the fiery walls beckon you towards the unknown beyond, while
staircases, resembling particularly fiery snakes, curl both upwards
and downwards from the platform. The whole scene gives the impression
that the laws of physics are taking a very long tea break.
There are four obvious exits: up, down, gi0/0 and gi0/2. 
A diligent security officer.

> ??gi0/2

A Diligent security officer steps aside and lets you through.
The contents of your IP header alters!
You find yourself on a platform that juts out from the side of a
towering wall of flames. Strangely enough, despite the roaring fire
just a few feet away, this place exudes a sense of calm. Perhaps it's
the slightly warmer air or the distant hum of activity that suggests
you're on the more relaxed side of things. The platform itself seems
almost tranquil, with a wide staircase leading down and a narrower one
winding upwards. Two openings in the wall of flames catch your eye,
though one appears to be firmly sealed off, as if to say, 'No entry,
not today, not ever.'
There are three obvious exits: up, down and gi0/1.
A stern engineer.

*gi0/1 takes you back to the gateway

> ??down

You find yourself at the base of the firewall, where the flames dance
and shimmer above. Here at the bottom of the network stack, everything
feels solid and foundational. The floor beneath you is made of sturdy
metal, giving a sense of stability and reliability. To one side, a
wide, inviting tunnel beckons, its mouth open and welcoming,
suggesting a smooth transition to other parts of the network. A
staircase, wide and robust, leads upward, disappearing into the
brighter layers above. It's a place where the crucial but often
overlooked tasks of data transmission take place, and there's a quiet
satisfaction in being part of this essential infrastructure.
There are two obvious exits: up and downstream.
A stressed technician.

> ??downstream

You find yourself in a corridor that hums with a serene energy, like a
place where data and purpose meld into a tranquil dance. The
surroundings are a gentle blend of soft hues and faint glows, with
walls that seem to ripple slightly as if they're in the midst of a
pleasant dream. The corridor stretches out before you in both
directions. One way leads back towards a more tumultuous realm you've
recently left, while the other opens up to what seems like a welcoming
crossroads further downstream. This crossroads might very well be a
bustling hub of activity, where decisions and directions are made with
a bit more flair. Perhaps it's worth a visit?
There are two obvious exits: upstream and downstream.

> ??downstream

You find yourself in a rather well-organized intersection of the
network. Openings in all directions beckon like polite doorways, each
labeled with the word 'port' and a number. The tunnels beyond lead
into a mysterious and possibly labyrinthine beyond. Packets bustle
about with the air of busy office workers — heads down, focused, yet
not frazzled. There's no panicked rushing here, just a calm,
purposeful flow. In the center, on a slightly raised platform, stands
an official-looking figure who oversees the entire operation with an
air of mild authority. Above, the ceiling — if it can be called that
— glimmers with the occasional flicker of light, hinting at the
electrical impulses shooting through the network. It's all quite
civilized, really.
There are four obvious exits: port0, port1, port2 and port3.
A traffic supervisor.

*(there are no security officer here)
> ??port1

A Traffic supervisor gives you a once-over, as if mentally checking a list.
A Traffic supervisor gives a satisfied nod and gestures for you to proceed.
In this crisscrossing labyrinth of data flows, you've stumbled into
yet another uninspiring round tunnel, where you and your digital
brethren zip along, propelled by both duty and the current. There
isn't much sense of urgency here, just a steady trudging along, as if
everyone is trying to get things done while keeping one eye on the
clock, hoping to make it home in time for dinner. Further downstream,
the tunnel terminates at what appears to be a cozy suburban townhouse,
while upstream lies an intersection that could lead to adventure, or
just another dead end.
There are two obvious exits: downstream and upstream.

> ??downstream

You find yourself in a cluttered and cramped garage-like room, that
groans under the weight of far too many outdated protocols and legacy
systems held together with digital duct tape and hope. Everything here
feels just slightly wrong, as if someone, somewhere, implemented
features using the most roundabout method possible, bypassing half the
APIs in favor of questionable shortcuts. The cables running along the
floor seem to sag under the strain of ancient standards, while data
packets lumber along, bloated and sluggish from the excess baggage of
backwards compatibility. A narrow staircase is leading upwards,
through an opening in the ceiling and a round tunnel is leading away
upstream. There's a sense of barely-controlled chaos, like an old
machine forced to run modern programs, clattering away with the quiet
despair of knowing it's just one patch away from total collapse.
There are two obvious exits: up and upstream.
A jaded technician.

> ??up

A Jaded technician examines you carefully.
A Jaded technician lets you pass upward.
You find yourself in a quiet but busy space, an intermediary zone
where this workstation reaches out to the larger, endless network
beyond. Everything here feels transient, like the room is aware that
it's only a small piece in a much bigger puzzle, playing its part in
the flow of information between this machine and the world outside.
However, not everything runs smoothly — every now and then, you can
feel the lag of outdated protocols, bottlenecks formed by forgotten
patches, and strange reroutes where someone clearly bypassed proper
APIs in favor of quick hacks. A spiral staircase is leading upwards
towards what might be loftier society, or just more complexity and
toil. Through an opening in the floor a rickety stair is leading down.
The space feels cobbled together with patches of old and new, with
packets trickling through cautiously, as if wary of triggering some
hidden bug.
There are two obvious exits: up and down.
A nervous networker.

> ??up

A Nervous networker examines you carefully.
A Nervous networker lets you pass upward.
You find yourself in what feels like a bustling, chaotic post office.
Small, clerk-like entities shuffle around with clipboards, trying
their best to keep track of which data stream goes where. A large,
dusty blackboard hangs on one side of the room, filled with scribbles
and cryptic numbers, while the clerks fuss around it with a mixture of
anxiety and resignation. The scent of legacy workarounds hangs in the
air like the faint whiff of old varnish. Everything here technically
functions, but it's clear that it's being held together by tradition,
guesswork, and the occasional bypassed API. Five large tubes snake
along the floor, leading upwards to destinations unknown, each of them
carrying strange markings that likely have some forgotten
significance. A rickety spiral staircase winds down through a hole in
the floor, leading deeper into the system.
There are six obvious exits: down, 135, 445, 34887, 43891 and 55643.
A frazzled dispatcher.

*port 135 and 445 are closed for all

> ??43891

A Frazzled dispatcher examines you carefully.
A Frazzled dispatcher lets you pass upward.

You find yourself in a cavernous, neon-lit room that buzzes with the
frenetic energy of constant distraction. Huge, floating panels display
rapidly changing images — some sharp, colorful, and inviting, others
flashing so quickly you barely have time to register them before
they're replaced. Voices drift in from invisible speakers, an
overlapping cacophony of adverts, music, and disembodied narrators
enthusiastically explaining the benefits of products you never knew
you needed. It's a place built for entertainment and information,
where the user's attention is a commodity to be constantly courted,
and every pixel is working overtime to keep you here just a little
longer. Packets come and go in a constant flow through an opening in
the floor. Somewhere, likely through the tube leading away downwards,
lies the content itself — remote, distant, but somehow feeding into
this dazzling spectacle you find yourself immersed in.
There is one obvious exit: down.

> ??55643

A Frazzled dispatcher examines you carefully.
A Frazzled dispatcher lets you pass upward.

You find yourself in a room that buzzes with a quiet but determined
sense of purpose. The space is neat, almost too neat, as if it's
constantly preparing for the next big task. Shelves line the walls,
each filled with rolled-up requests, neatly stacked and labeled with
tiny tags that flutter in an unseen breeze. A large, polished desk
stands in the middle of the room, with an ink-stained ledger resting
atop it. The air hums with the tension of a process awaiting the next
job. In one corner, a particularly irate-looking tube opens up in the
floor, leading downward to what ever lies below. The tube pulses
occasionally, as though trying to nudge the process into moving things
along faster. There's a clock on the wall, but it seems to tick
irregularly, as if unsure whether it should measure time or just add
to the general air of bureaucratic delay. A small placard on the desk
reads: 'We Take Our Jobs Very Seriously, Until We Don't.'
There is one obvious exit: down.
The spool manager.

> ??34887

A Frazzled dispatcher examines you carefully.
A Frazzled dispatcher lets you pass upward.

The room feels impossibly vast, cluttered with shelves, drawers, and
filing cabinets that seem to stretch out into infinity. Papers,
folders, and strange devices for sending, organizing, and losing
emails and numerous other whatnots are scattered everywhere. It's a
space that tries to do far too many things at once, as if someone had
decided that what was really missing from their life was an all-in-one
office, bakery, and zoo. Tiny, stressed figures dash about, trying to
keep track of unread messages, flagged items, and calendars
overburdened with meetings that no one ever attends. In one corner, a
gargantuan 'Search' tool lumbers about, occasionally waking from its
slumber to search for something — though what it finds rarely
matches what you asked for. 
And in another stands a rickety
blackboard, filled with what looks like hasty scribbled gibberish.
Meanwhile, the room has a faint hum, a constant sense of background
activity, as though the process is always running a multitude of
sub-processes, most of which seem to be arguing amongst themselves
about what is truly important. 
A yawning opening in the floor reveals
a dark tube leading down, through which emails are occasionally
funneled, though sometimes they seem to vanish into the abyss without
explanation.

There is one obvious exit: down.

An overworked clerk.

> ??exa chaotic scrawl

.----------------------------------------------------------------------------.
|                          -=* Operations log *=-                            |
|      [4] days without incident. [3421] left until cake and lemonade!       |
|----------------------------------------------------------------------------|
| 11:29:01 [INFO] Initializing POP3 Client...                                |
| 11:29:02 [INFO] Connecting to POP3 server at mail.n3tw0rk.ex:110           |
| 11:29:02 [INFO] Sending USER command for authentication...                 |
| 11:29:03 [INFO] Sending PASS command for authentication...                 |
| 11:29:04 [INFO] Authentication successful. Logged in as alex@n3tw0rk.ex    |
| 11:31:05 [INFO] Retrieving mail from server...                             |
| 11:31:06 [INFO] Mail retrieval in progress...                              |
| 11:31:09 [INFO] Mail #11 - Subject: "IMPORTANT" from: "kenneth@rymden.nu"  |
| 11:32:49 [INFO] Disconnecting from POP3 server.                            |
| 11:32:50 [INFO] Logged out from POP3 server.                               |
| 11:35:31 [INFO] Displaying retrieved emails to user...                     |
| 11:41:25 [INFO] User selected "IMPORTANT" email for printing.              |
| 11:41:26 [INFO] Preparing email for printing...                            |
| 11:41:37 [INFO] Starting print job for "IMPORTANT" email...                |
| 11:41:38 [INFO] Opening printer connection: "Printer@198.51.100.182"       |
| 11:41:39 [INFO] Sending print job to spooler (spoolsv.exe)...              |
| 11:42:19 [INFO] Print job successfully sent to spooler. Job ID: 31355      |
| 11:42:19 [INFO] Waiting for printer to complete the job...                 |
| 11:48:22 [INFO] Print job completed with error. Status: Queued             |
| 11:48:23 [INFO] Closing printer connection.                                |
| 11:48:24 [INFO] Print job finished. Proceeding to delete email...          |
| 11:48:25 [INFO] Deleting "IMPORTANT" email from server...                  |
| 11:48:26 [INFO] Sending DELE command to POP3 server for email ID: 11       |
| 11:48:27 [INFO] Email deleted successfully.                                |
'----------------------------------------------------------------------------'

go back down to;
"There are four obvious exits: port0, port1, port2 and port3."
port1 is the work station

> ??port2

(downstream and up and up)

The room feels like a workshop hastily converted into a shrine to
network efficiency, with wires and cables snaking about in a way that
could only make sense to someone who considers 'neatness' an insult to
their technical prowess. A rickety, spiral staircase leads downwards
— clearly built without any thoughts of health and safety, but it's
probably fine if you have the agility of a ferret. Meanwhile, a
sturdy-looking tube, marked with the number '21456' for no apparent
reason, extends upwards. In one corner, a blackboard is covered in
chalk-dusted network diagrams, connections, and cryptic notes that
only the truly initiated would dare to comprehend. The place is a
chaotic blend of brilliance and haphazard construction — exactly
what you'd expect from a someone who despises GUIs and believes that
the terminal is the one true interface.
There are two obvious exits: down and 21456.

> ??exa blackboard

The blackboard is covered in white chalk, diagramming the flow of
packets through the network with a level of abstraction and complexity
that only the most dedicated technician would find artistic. You get
the impression that understanding it fully would take several years of
dedicated study — or at least a strong pot of coffee and a disdain
for simplicity. But perhaps a closer look at the diagrams might
enlighten you.

> ??exa diagrams

You ponder the diagrams trying to make sense of it all:
- Interfaces -
 eth0: inet 198.51.100.194 netmask 255.255.255.128 broadcast 198.51.100.255
       ether 00:10:E3:8C:EA:51 mtu 1500
- ARP table -
 Address          HWtype  HWaddress            Iface
 198.51.100.129   ether   00:03:32:F2:33:23    eth0
- Current IP routing table -
 Destination     Gateway         Genmask         Use Iface
 default         198.51.100.129  0.0.0.0            eth0  
 198.51.100.128  0.0.0.0         255.255.255.128    eth0
- Netstat -
 Proto     Local Address           Foreign Address         State
 tcp       198.51.100.194:21456    198.51.100.15:22        ESTABLISHED


> ??21456

A Sullen manager examines you carefully.
A Sullen manager lets you pass upward.

You enter a room that feels oddly compressed, like it's been tucked
away inside a fortress where security is more than a suggestion, it's
an obsession. The walls are lined with glowing, arcane-looking symbols
— encryption standards, protocols, and key exchanges — all in a
dizzying dance of mathematical rigor. In the center stands a towering
terminal, flickering with life. The room hums with quiet tension,
every action logged, every breath monitored. Around you, shadows of
other processes flicker in and out, each focused on its own task but
wary of what might try to slip through. To one side, there's an
opening in the floor, a narrow tube is leading down into the lower
levels of the network, and you can feel the pull of packets rushing up
and down, frantically delivering their bits and bytes.

There is one obvious exit: down.

*you can do exa terminal but you see what you saw in port3 and "22(ssh)"

go back down to;
"There are four obvious exits: port0, port1, port2 and port3."
port1 is the work station
port2 is the "admin"

> ??port3

*(and up to IP layer)

This room has an air of barely-contained chaos, with large bundles of
tubes snaking across the floor, each marked in hurried, mismatched
handwriting. One particularly thick tube stretches upward through a
hole in the ceiling, its surface emblazoned with the number 631 in
faded stenciling. The tube pulses occasionally, as though struggling
to push data through to its final destination. Beside it, a bulletin
board haphazardly hangs on the wall, filled with a clutter of cryptic
notes, as if the clerks tasked with organizing things gave up halfway
through. A battered ladder leads down through a familiar rusted
opening in the floor, its rungs worn from years of heavy traffic. The
room hums with quiet urgency, every connection here representing the
frantic effort to keep things moving, even if some of them don't quite
follow the expected rules.
There are two obvious exits: down and 631.
An artistic courier.

> ??exa notes

You look through the notes on the bulletin board trying to make sense
of the information:
- Interfaces -
 eth0: inet 198.51.100.182 netmask 255.255.255.128 broadcast 198.51.100.255
       ether C0:FB:F9:0B:72:9E mtu 1500

- ARP table -
 Address          HWtype  HWaddress            Iface
 198.51.100.129   ether   00:03:32:F2:33:23    eth0
 198.51.100.199   ether   60:5B:30:FE:0B:98    eth0

- Current IP routing table -
 Destination     Gateway         Genmask         Use Iface
 default         198.51.100.129  0.0.0.0            eth0  
 198.51.100.128  0.0.0.0         255.255.255.128    eth0

- Netstat -
 Proto     Local Address           Foreign Address         State
 tcp       0.0.0.0:631             *:*                     LISTENING
 tcp       198.51.100.182:631      198.51.100.199:55643    ESTABLISHED

> ??631
An Artistic courier examines you carefully.
An Artistic courier lets you pass upward.
The room feels more like an avant-garde art studio than a computer
process, cluttered with abstract sketches pinned to the walls and
half-completed 'masterpieces' scattered on floating easels. Various
figures, each dressed in dramatically eccentric garb, bustle about,
deliberating over blobs of data floating in mid-air, forming a queue
of sorts. It is a bit unclear what kind of data is contained in these
blobs, but to the room's inhabitants, they are clearly seen as
creative works of the highest order. You can hear mutterings of 'true
genius takes time' as they shuffle the blobs around. The queue of
blobs leads up to a large funnel attached to an intricate machine
lumbering in the center of the room. However, the queue is not moving,
and a display on the machine angrily flashes a message, though none of
the 'artists' seem to take notice — or perhaps they consider the
message part of the creative process. To one side stands a dangerously
leaning tower of boxes, stacked high, constituting a possible lawsuit
waiting to happen. A large tube opens up in the floor, with packets of
data traveling up and down through it as if part of some grand
delivery system.
There is one obvious exit: down.
An eccentric art director.

**this is where you find the flag**

