## Convert Opta's tracking & event data from 2D to 3D

- Build upon the work of the Opta Forum 2023 submission.
- Combine Opta's tracking and event data to create one single data file.
- Then, use Godot Engine + GDScript + Blender to visualise the data in 3D.

### Ideas

- Test it on a single match first to reduce computational load.
- Processing data should be very easy, the hard part is converting from 2D to 3D.
- Have two camera angles:
  - Player's perspective -> changes based on who is controlling the ball.
  - Tactical perspective -> similar to Football Manager's sideway view (a bit elevated in height and covers the whole field).
- Field dimension should be 100x100 in Cartesian plane.
- Have the ability to pause at each action.

### Steps

1. [] Combine Opta's tracking and event data into a single df/csv file.
2. [] Import that csv file into GDScript (somehow...?).
3. [] Create a player model in Blender.
   - Doesn't have to be too specific (e.g. have accurate faces, detailed shirts, etc.).
   - One model can be copy+paste for the remaining 21 players.
   - Can have coloured shirts to distinguish the teams but don't add any specific details.
4. [] Add simple movements to the player model.
   - Running (ensure players don't teleport from one position to another!)
   - Passing/Shooting
   - Walking
5. [] Bring model to Godot Engine + put models onto a pitch.
6. [] Use the data and get the models to run based on the coordinates from the tracking data.
