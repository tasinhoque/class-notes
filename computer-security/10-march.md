### Key Logger

### Locks and Safes

Master Key

Lockpicking

Safe Cracking

Side Channel Attack:

---

[Taken from Wikipedia]

In computer security, a side-channel attack is any attack based on information gained from the implementation of a computer system, rather than weaknesses in the implemented algorithm itself (e.g. cryptanalysis and software bugs). Timing information, power consumption, electromagnetic leaks or even sound can provide an extra source of information, which can be exploited.

Some side-channel attacks require technical knowledge of the internal operation of the system, although others such as differential power analysis are effective as black-box attacks. The rise of Web 2.0 applications and software-as-a-service has also significantly raised the possibility of side-channel attacks on the web, even when transmissions between a web browser and server are encrypted (e.g. through HTTPS or WiFi encryption), according to researchers from Microsoft Research and Indiana University.[1] Many powerful side-channel attacks are based on statistical methods pioneered by Paul Kocher.

---

[Taken from [Wired](https://www.wired.com/story/what-is-side-channel-attack/)]

MODERN CYBERSECURITY DEPENDS on machines keeping secrets. But computers, like poker-playing humans, have tells. They flit their eyes when they've got a good hand, or raise an eyebrow when they're bluffing—or at least, the digital equivalent. And a hacker who learns to read those unintended signals can extract the secrets they contain, in what's known as a "side channel attack."

Side channel attacks take advantage of patterns in the information exhaust that computers constantly give off: the electric emissions from a computer's monitor or hard drive, for instance, that emanate slightly differently depending on what information is crossing the screen or being read by the drive's magnetic head. Or the fact that computer components draw different amounts of power when carrying out certain processes. Or that a keyboard's click-clacking can reveal a user's password through sound alone.

"Usually when we design an algorithm we think about inputs and outputs. We don’t think about anything else that happens when the program runs," says Daniel Genkin, a computer scientist at the University of Michigan and a leading researcher in side channel attacks. "But computers don’t run on paper, they run on physics. When you shift from paper to physics, there are all sorts of physical effects that computation has: time, power, sound. A side channel exploits one of those effects to get more information and glean the secrets in the algorithm."

For a sufficiently clever hacker, practically any accidental information leakage can be harvested to learn something they're not supposed to. As computing gets more complicated over time, with components pushed to their physical limits and throwing off unintended information in all directions, side channel attacks are only becoming more plentiful and difficult to prevent. Look no further than the litany of bugs that Intel and AMD have struggled to patch over the last two years with names like Meltdown, Spectre, Fallout, RIDL, or Zombieload—all of which used side channel attacks as part of their secret-stealing techniques.

The most basic form of a side channel attack might be best illustrated by a burglar opening a safe with a stethoscope pressed to its front panel. The thief slowly turns the dial, listening for the telltale clicks or resistance that might hint at the inner workings of the safe's gears and reveal its combination. The safe isn't meant to give the user any feedback other than the numbers on the dial and the yes-or-no answer of whether the safe unlocks and opens. But those tiny tactile and acoustic clues produced by the safe's mechanical physics are a side channel. The safecracker can sort through that accidental information to learn the combination.

---

One-time password disadvantages
