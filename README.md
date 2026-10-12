# Smart EV Charging Slot Assignment System

A browser-based educational simulator for a data-structures-and-algorithms micro-project. It demonstrates how charging requests can be assigned to limited charging ports and how scheduling policy affects waiting time and utilisation.

## Run the simulator
Open **index.html** in a modern browser, or enable GitHub Pages to host it as a live website. No build tools, packages, API keys, or backend are required.

## Features
- Compare Smart Priority Scheduling with First Come, First Served (FCFS).
- Enter your own EV records (vehicle ID, battery level, arrival time, charging duration, and Normal/High/Emergency priority), or generate a sample workload.
- Select 2–6 charging stations and compare algorithms on the same manually entered scenario.
- Simulate emergency and low-battery requests; manual inputs are clearly distinguished from generated sample data.
- View station allocation, per-vehicle waiting time, queue order, average wait, longest wait, and station utilisation.
- Export per-vehicle results as CSV.
- Responsive dark/light interface and print-to-PDF support.

## Data structures and algorithm concepts
- **Queue / FCFS:** process requests in arrival order.
- **Priority queue concept:** emergency and low-battery vehicles are considered earlier in Smart mode.
- **Greedy best-fit assignment:** assign each request to a charger that becomes available earliest.
- **Performance analysis:** compare average waiting time, maximum wait and charger utilisation.

## Important note
This is a simplified academic simulation for explaining scheduling concepts. Generated sample vehicles are random demo data; manually entered values are user-provided scenario inputs. Charging durations and station availability are assumptions, and results are illustrative—not live EV telemetry or a validated real-world charging-network model. The interactive scheduling logic is implemented in JavaScript for this demo and can be mapped to C++ data structures and algorithms in the project implementation.
