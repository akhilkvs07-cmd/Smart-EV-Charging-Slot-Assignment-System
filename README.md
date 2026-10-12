# Smart EV Charging Slot Assignment System — VoltFlow

VoltFlow is a responsive, browser-based dashboard that mirrors the allocation logic in the project's C++ program. It is an educational simulator; it does not connect to physical chargers or use live telemetry.

## Open the dashboard

GitHub Pages: https://akhilkvs07-cmd.github.io/Smart-EV-Charging-Slot-Assignment-System/

You can also open `index.html` directly in a modern browser. No build tools, packages, API keys, or backend are required.

## What the dashboard demonstrates

- Add EV records with ID, battery percentage, waiting time, connector type, emergency flag, and reservation flag.
- Add charging stations with ID, connector type, power rating, and availability.
- Calculate the same priority score as the C++ program:
  `100 - battery + floor(wait / 5) + (reserved ? 20 : 0) + (emergency ? 100 : 0)`.
- Process EVs in priority order. Equal scores are broken by longer waiting time, then lower EV ID.
- Assign each EV to an available station with a matching connector, choosing the highest-power compatible station.
- Show final assignments, EVs still waiting, and station availability after allocation.
- Load a ready-made example, toggle dark/light theme, and print or save the dashboard as PDF.

## Data structures and algorithm concepts

- **Struct-like records:** EV and Station objects hold each item's data.
- **Priority queue:** EVs are ordered by priority, waiting time, then ID.
- **Greedy station selection:** for each EV, scan compatible available stations and select the one with the greatest power.
- **Waiting list:** EVs with no compatible available station remain unassigned.
- **State update:** a station becomes occupied once an EV is assigned to it.

## Important implementation note

The C++ source remains the reference implementation. The dashboard mirrors its current rules in JavaScript so that it can run in a browser without a server. Both are educational simulations, not validated real-world charging control software. Power is used only to choose between compatible stations; actual charging speed depends on the vehicle and charger hardware.
