# Hackathon.Zurich
# Verde Campus

*Small habits. Real rewards.*

Verde Campus is a mobile application concept that helps university students reduce their environmental footprint in everyday campus life. Sustainable actions earn points, wasteful ones cost points, and points are exchanged for tangible campus benefits.

> This is a fictional concept prototype created for a presentation. All data, NFC/QR validation, sensors and rewards are simulated.

---

## 1. Concept

Everyday campus activities feed one shared sustainability score:

| Area | What the app does |
|---|---|
| Study rooms | Find, book and access rooms; monitor and control heating, lights and equipment |
| Cafeteria | Show the environmental score of each dish; scan trays to measure food waste |
| Coffee machines | Reward students who bring a reusable mug |
| Vending and recycling | Deduct points for plastic bottles; return them to recover points |

The gamification is meant to motivate rather than patronise: a clear balance, honest feedback, and rewards with real value.

## 2. Points system

### Study rooms

| Student action | Points |
|---|---|
| Thermostat at 25°C or below | +2 |
| Thermostat above 25°C | −3 |
| Lights switched off when leaving | +2 |
| Lights left on when leaving | −2 |
| Monitors and projectors switched off when leaving | +2 |
| Equipment left running when leaving | −2 |

A full sustainable session earns **+6**. The 25°C threshold is the maximum setpoint that qualifies for a reward.

### Cafeteria, coffee and vending

| Action | Points |
|---|---|
| Vegetarian or plant-based, regional dish (score A) | +4 |
| Falafel wrap or similar (score B) | +3 |
| Standard dish (score C) | 0 |
| High-footprint dish (score E) | −2 |
| Tray returned with 10% leftover or less | +4 |
| Tray returned with more than 40% leftover | −3 |
| Reusable mug at the coffee machine | +2 |
| Plastic bottle purchased | −2 |
| Empty bottle returned to a deposit machine | +2 |

Dish scores (A to E) combine local sourcing, plant-based content, estimated footprint in kg CO₂e, and production sustainability.

### Rewards

| Reward | Points |
|---|---|
| Public transport day ticket | 300 |
| Free cafeteria lunch | 400 |
| Printing credit (CHF 10) | 600 |
| Student-fee reduction (CHF 25) | 1,500 |
| Semester pass discount (CHF 100) | 3,500 |

## 3. Application structure

Four sections in a bottom navigation bar.

1. **Home** – points balance (the most prominent element), points evolution chart, recent activity, progress to the next reward, recent achievements.
2. **Rewards** – unlocked and upcoming achievements, available rewards, progress bars, redemption history.
3. **Study rooms** – the central feature: discovery, booking, access, live room control, departure and scoring.
4. **Cafeteria** – menu with environmental scores, recommendations, tray-return validation, plus coffee and vending services.

## 4. Study rooms: user journey

1. **Find and book.** Browse rooms by day, check capacity, equipment and free slots, then confirm a reservation or book the next free slot.
2. **Access.** At the door, identify with the university card (NFC) or by scanning the door QR code. The app validates the reservation and unlocks the room.
3. **Manage energy.** View room status, adjust the thermostat, and control lights, monitors and projector. A live estimate shows the points the session would earn or lose, and the app gives immediate feedback when a setting crosses the 25°C threshold.
4. **Leave.** If anything is still running, the app prompts the student to switch it off before ending the session.
5. **Feedback.** A summary lists points earned or lost per item, the new balance and the estimated energy saving, and the session is added to the points history.

## 5. Hierarchical Task Analysis: use a study room sustainably

**Plan 0:** Do 1, then 2, then 3. When the session ends, do 4, then 5. If the reservation fails at step 1 or 2, repeat from the failing step or choose another room.

### 1. Find and book a study room
*Plan 1: do 1.1 to 1.3; if no suitable slot, change day or room (back to 1.2); then 1.4 and 1.5.*

- 1.1 Open the study room section
- 1.2 Browse available rooms
- 1.3 Check capacity, equipment and availability
- 1.4 Select a room and a time slot
- 1.5 Confirm the reservation

**Decision points:** slot free or taken; need the room now (book next free slot) or later (choose a date).
**Alternatives:** room full, so choose another day or room; booking changes, so cancel from My bookings.

### 2. Access the study room
*Plan 2: do 2.1; then 2.2 using NFC or QR; then 2.3 and 2.4.*

- 2.1 Arrive at the reserved room
- 2.2 Identify with the university card (NFC) or the door QR code
- 2.3 Validate the reservation
- 2.4 Unlock and enter the room

**Conditions:** a valid reservation exists for the current time.
**Alternatives:** NFC read fails, so switch to QR; no valid reservation, so the door stays locked and the student is offered a free slot.

### 3. Manage energy consumption during the session
*Plan 3: do 3.1; repeat 3.2 to 3.4 as needed during the session.*

- 3.1 Check the current room settings
- 3.2 Adjust the thermostat to a maximum of 25°C
- 3.3 Use lighting responsibly
- 3.4 Monitor the use of electronic equipment

**Decision points:** setpoint above 25°C (warn, projected −3) or at most 25°C (projected +2); lights needed or not.

### 4. Leave the room responsibly
*Plan 4: do 4.1 and 4.2 in any order; then 4.3; then 4.4.*

- 4.1 Turn off the lights
- 4.2 Turn off monitors and projectors
- 4.3 Check that all energy-consuming equipment is switched off
- 4.4 Validate the end of the session

**Alternatives:** equipment still on, so the app prompts "switch everything off and leave" or "leave as is" (points deducted); session ends early, so the slot is released.

### 5. Receive sustainability feedback
*Plan 5: do 5.1 to 5.4 in order (automatic).*

- 5.1 Calculate the points earned or lost
- 5.2 Display the energy-saving performance
- 5.3 Update the points balance
- 5.4 Record the activity in the history

## 6. Design principles

- Mobile-first, with a clear visual hierarchy and intuitive navigation.
- A contemporary but understated identity: warm off-white, deep forest green, and terracotta reserved for point losses and warnings.
- Serif numerals for points (Fraunces) with a clean sans-serif for interface text (Instrument Sans).
- Light and dark modes.
- Meaningful colour, restrained containers, few emojis, no childish gamification.
- Subtle motion: toasts, progress bars and transitions that confirm an action.

## 7. Prototype scope

Front end only. Simulated rather than implemented: database, NFC and QR validation, thermostat and lighting integration, payments and university authentication. Interactions rely on mock data and front-end state, and every control behaves coherently (booking updates availability and reservations; thermostat and light changes update the projected points).

## 8. Next steps

- Extend the Cafeteria, coffee and vending flows beyond simple simulations.
- Test the study-room journey with students against the HTA.
- Add campus-wide and group challenges to the Home screen.
