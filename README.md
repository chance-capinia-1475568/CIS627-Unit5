# Lane Transition Adjustment Score, an Analytics Innovation Project

## Project Overview
This project proposes a **Lane Transition Adjustment Score**. This metric tracks how much the oil pattern on a bowling lane breaks down over a match or tournament block and recommends when a bowler should change their line, ball surface, or equipment. As oil transitions from fresh to "burned up," the ball's reaction changes, and bowlers who adjust too late or too early lose pins they didn't need to lose.

## Decision Making Problem
Coaches and team captains need to decide, frame by frame or game by game, when a bowler should change their target line, switch balls, or adjust their release to match changing lane conditions. Right now, this decision relies almost entirely on the bowler's or coach's feel for the lane, which varies widely in consistency and can lag behind what's actually happening to the oil pattern.

## Proposed Analytics Approach
The score would combine three types of information.
- **Ball reaction data.** This compares the entry angle, breakpoint location, and pin carry from the previous several frames to the bowler's expected reaction on a new pattern.
- **Pattern decay indicators.** These include how many games or frames have been bowled on the pair, and how much oil is estimated to have been carried down or burned off based on shot volume and ball traffic in each zone of the lane.
- **Outcome trends.** These include strike percentage and pin count trends over the last two to three games compared with the bowler's season average on similar oil patterns.

This is a conceptual proposal only. No model or app is built here.

## Use by Decision Makers
A coach or team captain would look at the score between games or during breaks in the league or tournament schedule. When the score reached a point showing a significant break in the usual pattern, this would mean that it was probably necessary to make an adjustment, such as changing lines, altering the ball surface, or modifying the release, before the bowler took their next set of shots. Although the bowler and the coach still make the final decision, the tool provides an earlier, more consistent indication than relying solely on feel.

## Connection to Chapter 7
The idea is at the **creative phase** of the Chapter 7 innovation framework. Although the concept and the problem it aims to solve are clearly defined, no prototypes have been developed, no testing has been carried out on actual lane data, and no real coach or bowler has reviewed it. To proceed, prototyping and real feedback are necessary.

## Prototype Enhancement
**What is being changed.** The changes involve the original score considering the entire lane as one continuous oil pattern that breaks down evenly, whereas the improved version divides the lane into zones, such as those within the board range, the middle section of the lane, and those outside the board range, and monitors the breakdown separately for each zone. This is because more ball traffic on one side of the lane causes the oil to be used up more quickly there than in other areas. Additionally, the score includes a sensitivity weight for each bowler, since some bowlers' combinations of ball and release are more tolerant of a changing oil pattern than others.

**Why this could enhance decision making.** A single lane wide breakdown figure might not detect that the zone a bowler is bowling on has changed much more rapidly or slowly than the lane average, which is when a coach would ask for an adjustment. Because the tool includes a sensitivity weight for each bowler, it won't request an adjustment for a bowler whose game is naturally more tolerant of oil breakdown, and it will prompt an adjustment earlier for a bowler whose game isn't.

## Prototype Evaluation
**Should we integrate the prototype enhancement into the main project.**
In principle, that is correct. By using zone based tracking and setting sensitivity by bowler, the score more closely reflects how coaches see the lane rather than treating it as a uniform surface. Yet it should not be incorporated into the main project until it has been verified against actual coaching judgment, as the additional complexity is only worthwhile if it agrees with what experienced coaches and bowlers notice on the lanes.

**What feedback from decision makers would influence this decision.**
- It is unclear whether coaches agree that the zone breakdown matches what they see when observing the ball's reaction in person, or whether it complicates their existing read.
- It is unclear whether a sensitivity setting adjusted for each bowler is useful, or whether it confuses teammates when they discuss results.
- It is not clear whether the necessary data, such as the entry angle and breakpoint for each shot by lane zone, can realistically be recorded during league or tournament play without slowing things down.

## Reflection on Innovation and Version Control
**How branches support low-risk experimentation:** Creating the `prototype` branch made it possible to develop and document improvements to zones and bowler sensitivity without changing the original approach on `main`. It is like an analytics team testing a more detailed version of a metric without affecting the version coaches are currently using, so any change that doesn't work has no impact on the main workflow.

**How GitHub helps analytics ideas gain traction with decision makers:** The commit history shows how the idea developed, from the original concept through tested improvements and evaluation to the final decision to adopt it. This clear record makes it much easier for a coach or bowling program to trust the idea, since they can see the reasons behind each step rather than being given a finished tool with no record of how or why it was built that way.

**Alignment with the Chapter 7 innovation framework:** The different stages correspond directly to the creative phase, the prototyping phase, the engagement phase, and the build phase. The first entry in the README covered the creative phase, the prototype branch covered the prototyping phase, the evaluation section represented the engagement phase, and the merge (or the record of the decision not to merge) shows the build and implementation decision. Because of version control, each phase has a specific, traceable place in the project's history.
