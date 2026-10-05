# service-behaviour

The design for a service that runs the planner and the motion interactor together: one decides what a body does, the other how it moves.

## What it is for

In the design, the planner publishes intents onto a shared-memory ring, and the motion side reads them and publishes reference poses. Sharing the ring forces the two onto one machine. They stay two parts because a plan changes in seconds and a pose changes every tick, and a search on the tick path would make the tick as slow as the worst plan. Turning a pose into a body that moves against gravity and contact belongs to the zone service, not to this one.

## Build and run

The repository holds no code: it carries this description, its citation and its licence.

## Licence

MIT; see `LICENSE`.
