# Pool Aim Assistant — Practice Guide

This guide is educational material for the app's offline practice features. It is not a substitute for the rules used by a particular venue or tournament.

## The table and balls
- The cue ball is the white ball struck by the cue.
- Object balls are numbered 1–15 in standard eight-ball: solids are 1–7, the 8-ball is black, and stripes are 9–15.
- Six pockets are positioned at the four corners and the middle of the two long rails.
- In a practice diagram, mark the cue ball, target ball, intended pocket, and the playable cushion boundaries before estimating a route.

## Basic eight-ball rules (common version)
1. The game starts with a break shot.
2. After groups are assigned, one player plays solids and the other stripes.
3. On a legal shot, the cue ball must contact a ball from the player's group first, subject to the applicable break/open-table rules.
4. After a legal contact, a ball must be pocketed or a ball must contact a cushion, according to the ruleset being used.
5. Pocketing the 8-ball is attempted only after the player's group has been cleared. Pocketing it early or pocketing it with a foul commonly loses the rack; confirm the local rules.
6. A scratch (cue ball pocketed) is commonly a foul and may give the opponent ball-in-hand.
7. Rules vary between leagues, venues, and mobile games. Follow the rules shown by the game or tournament you are playing.

## Geometry used by the practice overlay
- **Aim line:** the direction from the cue ball toward the intended contact point.
- **Ghost-ball estimate:** imagine the cue ball's center at the location where it would touch the target ball and send it toward the pocket.
- **Cut angle:** a larger off-center contact is generally harder to control than a near-full hit, all else being equal.
- **Cushion reflection:** a simple ideal model reflects the travel angle across the cushion normal. Real outcomes vary with speed, spin, cushion condition, and ball collision.
- **Distance:** longer paths typically increase sensitivity to alignment and speed errors.

## Important limitations
- A geometry overlay is an estimate, not a guaranteed shot or a measured success probability.
- Manual ball markers are not automatic vision. Automatic detection must be implemented and tested separately on representative screenshots.
- This project should not capture the screen until the user explicitly grants Android's screen-capture permission.
- Calibration feedback only becomes useful training data when shot outcomes and table coordinates are measured reliably; a success/miss counter alone does not prove that the model has learned the game's physics.

## Suggested validation checklist
- [ ] Confirm that all six pockets and the playable cushion boundaries are marked correctly.
- [ ] Test straight, thin-cut, and cushion-bank examples against hand-calculated reference cases.
- [ ] Verify that moving each marker updates the geometry without freezing the UI.
- [ ] Verify that shot feedback persists after restarting the app.
- [ ] Test on several screenshots with varied lighting, table colors, ball positions, and interface overlays before describing detection as reliable.
- [ ] Build and install the APK on a real device; a successful CI build alone does not verify runtime behavior.
