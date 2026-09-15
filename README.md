# Lane Transition Adjustment Score — Analytics Innovation Project

## Project Overview
This project proposes a **Lane Transition Adjustment Score**. This metric tracks how much the oil pattern on a bowling lane breaks down over a match or tournament block and recommends when a bowler should change their line, ball surface, or equipment. As oil transitions from fresh to "burned up," the ball's reaction changes, and bowlers who adjust too late or too early lose pins they didn't need to lose.

## Decision-Making Problem
Coaches and team captains need to decide, frame by frame or game by game, when a bowler should change their target line, switch balls, or adjust their release to match changing lane conditions. Right now, this decision relies almost entirely on the bowler's or coach's feel for the lane, which varies widely in consistency and can lag behind what's actually happening to the oil pattern.

## Proposed Analytics Approach
The score would combine three types of information:
- **Ball reaction data**: This compares the entry angle, breakpoint location, and pin carry from the previous several frames to the bowler's expected reaction on a new pattern.
- **Pattern decay indicators**: These include how many games or frames have been bowled on the pair, and how much oil is estimated to have been carried down or burned off based on shot volume and ball traffic in each zone of the lane.
- **Outcome trends**: These include strike percentage and pin count trends over the last two to three games compared with the bowler's season average on similar oil patterns.
- 
This is a conceptual proposal only. No model or app is built here.

## Use by Decision Makers
A coach or team captain would look at the score between games or during breaks in the league or tournament schedule. When the score reached a point showing a significant break in the usual pattern, this would mean that it was probably necessary to make an adjustment, such as changing lines, altering the ball surface, or modifying the release, before the bowler took their next set of shots. Although the bowler and the coach still make the final decision, the tool provides an earlier, more consistent indication than relying solely on feel.

## Connection to Chapter 7
The idea is at the **creative phase** of the Chapter 7 innovation framework. Although the concept and the problem it aims to solve are clearly defined, no prototypes have been developed, no testing has been carried out on actual lane data, and no real coach or bowler has reviewed it. To proceed, prototyping and real feedback are necessary.

## Prototype Enhancement
**What is being changed:** The changes involve the original score considering the entire lane as one continuous oil pattern that breaks down evenly, whereas the improved version divides the lane into zones, such as those within the board range, the middle section of the lane, and those outside the board range, and monitors the breakdown separately for each zone. This is because more ball traffic on one side of the lane causes the oil to be used up more quickly there than in other areas. Additionally, the score includes a sensitivity weight for each bowler, since some bowlers' combinations of ball and release are more tolerant of a changing oil pattern than others.

**Why this could enhance decision-making:** A single lane-wide breakdown figure might not detect that the zone a bowler is bowling on has changed much more rapidly or slowly than the lane average, which is when a coach would ask for an adjustment. Because the tool includes a sensitivity weight for each bowler, it won't request an adjustment for a bowler whose game is naturally more tolerant of oil breakdown, and it will prompt an adjustment earlier for a bowler whose game isn't.
