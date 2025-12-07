DIY SpaceMouse – Z-Lock RP2040 Version
A derivative work of the original diy-spacemouse by sb-ocr

This project is an enhanced version of the original open-source DIY SpaceMouse created by
sb-ocr / diy-spacemouse
.

It adds significantly expanded capability, improved navigation logic, and more intuitive 3D control behavior in Fusion 360.
This fork is published under the Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License (CC BY-NC-SA 4.0) in compliance with the original project’s license.

Major Improvements in This Fork
✔ Z-Lock Pan Mode

A new gesture control system using the TLV493D’s Z-axis magnetic field:

Pull upward (+Z) to enter Pan Mode

Pan mode stays locked regardless of tilt or drift

Push downward (–Z) to exit pan mode and return to orbit mode

Fully adjustable thresholds

This dramatically improves reliability and prevents accidental orbit/pan switching.

✔ Improved Orbit / Pan Separation

A lightweight state machine now decides:

When to remain in Orbit

When to switch into Pan

How to avoid flicker, jitter, and false mode changes

Orbiting is now smooth and natural, and panning feels controlled and predictable.

✔ Tilt-Based Navigation Refinements

X/Y tilt mapping corrected

Dead-zone tuning

Adjustable sensitivity

Swapped axes for intuitive Fusion 360 behavior

Smoothed output using Kalman filters

✔ Fusion 360 Workflow Enhancements

Orbit mode behaves consistently around object center once Fusion is configured

Pan mode matches expected viewport movement

Middle-mouse behavior improved

Hardware Used

Adafruit QT Py RP2040 (or equivalent RP2040 board)

TLV493D 3-axis magnetometer

Springs, magnets, printed shell, etc.

PCB or hand-wired breadboard (layout included)

Hardware diagrams and build documentation included in the /docs folder.

License

This project is licensed under the Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License (CC BY-NC-SA 4.0).

Because this is a derivative work of
sb-ocr’s diy-spacemouse
,
the same license must be applied.

You may:

Share the project

Modify it

Remix, improve, or extend it

You may NOT:

Use it commercially

Re-license it under MIT / GPL / BSD

Sell hardware based on it

Include it in a commercial product

Attribution is required in all forks and modifications.

Attribution

Original creator: sb-ocr
Original project: https://github.com/sb-ocr/diy-spacemouse

Derivative work by nsullivan44
Project repo: https://github.com/nsullivan44/DIYspacemouse-zlock-rp2040

This fork includes functional, structural, and ergonomic improvements but remains fundamentally based on the original author’s excellent foundation.

Installation & Upload

Upload the provided .ino file to the RP2040 board using Arduino IDE with:

Adafruit TinyUSB enabled

TLV493D library installed

RP2040 Board Support v5.x
