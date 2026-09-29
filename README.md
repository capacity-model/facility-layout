# :triangular_ruler: Proximity-Based Layout Evaluator

An interactive tool for declaring the qualitative proximity relationships between facility centers, laying the centers out, and scoring the layout against those relationships — then measuring what the layout actually costs in travel. Developed for **ISyE 6202 & 6335 — Supply Chain Facilities** at the Georgia Institute of Technology (Instructor: Prof. Benoit Montreuil).

- **Live app:** https://capacity-model.github.io/facility-layout/

## What it does

### Proximity relationships

- **Relationship table** — every field a dropdown: the pair of centers, importance, desired proximity, reason, and how the distance is measured. An I/O measurement names its stations explicitly, from the upstream center's output to the downstream center's input.
- **Importance scale** — rename levels, set each one's weight and drawn line width, add levels of your own, or mark one as an unscored feasibility constraint.
- **Satisfaction curves** — one curve per desired proximity, each editable; five ramps plus a bell for relationships that want an ideal separation, where closer is not always better.
- **Layout geometry** — drag centers to move or resize them and drag station markers along their walls. The relationship table decides which stations exist; the drawing follows as you drag.
- **Evaluation** — distance, satisfaction and contribution per relationship, with the design score. Everything recomputes live as the layout is dragged; there is no rescore step.

### Flow and travel

- **Flow estimation matrix** — loaded trips per period between centers. Empty trips are solved, not typed: a minimum-cost flow balances every center's arrivals against its departures at the least total empty travel.
- **Distance matrix** — measured on the layout, loaded trips from output station to input station and empty trips the other way round, along aisle shortest paths over the free space between blocks.
- **Flow graph and heatmap** — every trip drawn along the aisle route its distance was measured on, with independent layers for proximities, loaded trips and empty trips; the heatmap sums traffic per aisle cell.
- **Travel evaluation** — trips times distance, loaded and empty kept apart through every margin, plus total flow, total travel and average travel per center.

## Built with

Plain **HTML, CSS, and JavaScript** in a single self-contained file (`index.html`) — no frameworks and no build step.

## Usage

Open **https://capacity-model.github.io/facility-layout/** in any browser — nothing to install.

To run it locally, download `index.html` and open it directly, or serve the folder:

```bash
python -m http.server
```

Then visit http://localhost:8000.

## Contact Us

For any questions about this interactive tool, please contact Yinzhu Quan ([yquan9@gatech.edu](mailto:yquan9@gatech.edu)).
