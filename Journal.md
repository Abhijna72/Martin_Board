# MartinBoard Build Log

This doc's the deep dive into the chaotic but fun journey of designing MartinBoard, a split keyboard that’s got Lockheed Martin vibes printed right on the PCB. From day one chaos to final routing bliss, everything’s logged here.

| Date       | Task Focus              | Hours Spent |
|------------|-------------------------|-------------|
| July 5     | Initial layout + ideas  | 3 hrs       |
| July 6     | Art + switch alignment  | 3 hrs       |
| July 7     | Traces + diodes         | 4 hrs     |
| July 8     | Styling + polish        | 3 hrs       |
| July 9     | 3D case & plate design  | 5 hrs       |
| July 10    | Final check + gerbers   | 2.5 hrs     |
| *Total*  |                         | *21.5 hrs*  |

---

## Log - July 5

Kicked off the MartinBoard project today with just vibes and a rough idea. I wanted something that looked different, felt comfy, and had that jet engine personality. Opened EasyEda and just started randomly dropping Pro Micro and switch footprints, honestly just to see how chaotic it would look. Layout looked like a toddler placed the keys but it’s fine, it’s a mood board for now. Spent time going through my folder of inspo keyboards, screenshotting anything that looked clean or edgy. Got hyped thinking about the jet logo on the copper layer. Not much wiring today, just kinda placing stuff until it made sense visually. Did try to space out rows evenly but the math wasn’t mathing. Told myself tomorrow I’ll actually measure things. Baby steps.

| Image | Description |
|-------|-------------|
|  <img width="759" height="390" alt="Screenshot 2025-07-11 224224" src="https://github.com/user-attachments/assets/217daa04-7e93-42d8-a039-4b1b57d9eb82" />                                                             | The absolute mess of an initial layout with unaligned keys and also i thought i will put knob on Top -_- |


| Image | Description |
|-------|-------------|
|<img width="1026" height="681" alt="Screenshot 2025-07-11 223221" src="https://github.com/user-attachments/assets/22d8e49e-c171-4cb6-85b4-89aaf1bd2f9c" /> | Schematic |







*Hours Spent*: 3 hrs

---

## Log - July 6

Switched gears today and focused on the aesthetics. Like yeah, it’s a keyboard, but if it’s not cool, why even bother? Imported the Lockheed Martin jet SVG and traced it with copper layers. Took a while ‘cause the vectors kept breaking but I managed to get it aligned to the top plate. Then back to layout — properly spaced the switches, fixed the tilt on the middle column and gave some thought to pinky reach. Deleted the entire left hand twice because mirroring didn’t work. It finally looked usable and not like an alien crab. Also figured out stabilizers wouldn’t fit if I didn’t leave clearance, so I had to shove things around again. It’s starting to look like something I’d want to actually use.

| Image | Description |
|-------|-------------|
| <img width="785" height="372" alt="image" src="https://github.com/user-attachments/assets/0c862861-69af-4646-b62d-6ee5ba898647" /> | Updated layout with jet art placed on top layer |

*Hours Spent*: 3 hrs

---

## Log - July 7

Today was trace spaghetti day. I finally got into routing and it was as cursed as I expected. Did all the rows first and they looked okay, but then the columns just wouldn’t fit without doing 90° turns everywhere. KiCad yelled at me for trace clearance like every two minutes. Also dropped in all the diode footprints, which felt like a massive win, except I forgot to rotate a bunch so current flow was wrong. Ripped and rerouted it all after lunch. Got to the point where I was zoomed in so far I could see individual electrons. Silkscreen labels are now readable, though a few might be under keycaps. Overall, everything is connected and ERC only shows one warning now. Progress.

| Image | Description |
|-------|-------------|
| <img width="701" height="387" alt="image" src="https://github.com/user-attachments/assets/0bd9c253-c889-44a9-8a8e-690d9a227e00" /> | Fully routed PCB with traces running like subway lines |

*Hours Spent*: 4 hrs

---

## Log - July 8

Focused on making things look way more polished today. I wanted the board to not only work but also feel premium. Filled copper zones, played with the edge cuts and added a few inner jokes on the silk just for me. That jet silhouette got some thickness added so it’s bolder and would show up in the final copper etch. Also made sure the Pro Micro footprint was rotated the right way and added vias for reset and raw pins. Double checked trace widths and spacing for 5V lines ‘cause I didn’t want it to fry the second I plug it in. Zoomed out and stared at it for a while, and yeah, it’s starting to look like a legit board. This thing’s gonna fly.

| Image | Description |
|-------|-------------|
| <img width="846" height="574" alt="Screenshot 2025-07-11 223120" src="https://github.com/user-attachments/assets/6d433de0-0943-4a01-9698-c85a0eda0efe" /> | Cleaned up board with final jet outline and via pass-throughs |

*Hours Spent*: 3 hrs

---

## Log - July 9

Shifted everything to Fusion 360 today to model the case and plate. Exported a DXF from KiCad, imported it into Fusion and immediately realized I forgot to offset the outer edge for the plate cuts. Fixed it, added 3mm thickness, and then designed cutouts for switches. Had to rewatch a Fusion tutorial ‘cause constraints kept snapping everything weird. Then designed the case base with screw holes and cutouts for the USB port and reset button. Dropped some placeholder switches and keycaps on the top to visualize the vibe. Rendered it with dark gray plastic and it actually looks fire. Might try printing it in matte black or even something translucent later. Super hyped.

| Image | Description |
|-------|-------------|
| <img width="721" height="388" alt="Screenshot 2025-07-11 223309" src="https://github.com/user-attachments/assets/c5470876-659d-428f-90aa-92c09303a464" /> | 3D model of the case and plate, keycaps placed for vibe-check |

*Hours Spent*: 5 hrs

---

## Log - July 10

Final push today. Double checked every trace, ran DRC and fixed a few small shorts I didn’t catch before. No more red lines anywhere. Set up fab layer stackups and cleaned up the edge cuts to remove some tiny fragments that could mess with production. Exported Gerbers, made sure the fab preview didn’t throw any errors, and zipped it all up for JLCPCB. Sent it for fab after a mini panic about naming files wrong. Also wrote the VIA JSON and outlined the QMK layout in my notebook. Gonna use layers for media and nav controls since it’s a split board. Feels surreal that it’s all done. Can’t wait to solder this beast and hear those switches click.

| Image | Description |
|-------|-------------|
| <img width="726" height="410" alt="Screenshot 2025-07-11 223325" src="https://github.com/user-attachments/assets/a8c289e1-3984-4310-a9d4-31cb64bc654e" /> | Gerbers exported, preview looks clean and jet is ready for takeoff |

*Hours Spent*: 2.5 hrs

---








