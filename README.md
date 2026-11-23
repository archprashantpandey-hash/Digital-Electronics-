
Bit Lab — Sequential Logic

An interactive web project built for Lab 07 (Digital Electronics) that shows how basic memory circuits actually work in practice. Instead of just looking at truth tables, you can press buttons, toggle clocks, and test four working digital machines built from latches and flip-flops.
Live Demo: https://github.io

What's Inside


1. The Lockout Buzzer

A three-player quiz buzzer built with SR latches.
• How to play: Hit Start round, wait for GO, and press 1, 2, or 3 (or tap the buttons).
• The logic: The first player to press sets their SR latch, which triggers the LOCK line and blocks everyone else out until the host resets it.

2. Chronos Counter

A 4-bit binary ripple counter made from T flip-flops.
• How to play: Start the clock, adjust the speed (default is 2 Hz), or switch between counting up and down.
• The logic: Each flip-flop toggles whenever the one before it drops from 1 to 0, cutting the frequency in half at each stage and counting in binary.

3. The Vault

A digital combination lock with zero software—just a D flip-flop state machine.
• How to play: Enter the 4-digit passcode (hint: it starts like \(\pi \)) to reach State 4 and unlock it. You can also set your own custom code.
• The logic: Three D flip-flops keep track of your current state (Q2, Q1, Q0). Get a digit right and it moves to state + 1; get one wrong and it resets straight back to 0.

4. Silicon Dice

A hardware random-number generator using an 8-bit shift register (LFSR).
• How to play: Click Roll or step the clock manually to generate numbers, and watch the distribution bars even out over time.
• The logic: Eight D flip-flops shift bits to the left on every clock pulse while three XOR gates feed a new bit back in, cycling through 255 states before repeating.

Quick Reference

At the bottom of the page, there's a small field guide summarizing the five core building blocks used across the lab:
• SR Latch – Basic set/reset memory (level-sensitive).
• D Latch – Passes D through while the clock is high, then holds it.
• D Flip-Flop – Captures D right on the clock edge to store state.
• JK Flip-Flop – Can set, reset, hold, or toggle (J = K = 1).
• T Flip-Flop – Toggles on every clock tick and divides frequency by 2.

Running It Locally

No build tools or dependencies needed—everything runs in plain HTML, CSS, and JavaScript. Just download index.html and open it in any browser.
