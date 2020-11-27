# life-rpg
A (desktop) clone of life-rpg.

I couldn't really decide on how to implement this it sure feels like
one can can the same thing done with godot or with electron, or maybe
one can create a CLI for it. Even then one also has to decide how to 
implement a back-end. Should there be a daemon? What about backups? Etc.

With all there questions in mind I decided to first describe what 
I actually want from the app, and only then decide on the tech for it.


# Key features


## Task manager

Should have a basic functionality of a task manager.
One can create tasks, setup the date for when those should be done,
and mark them as done.


## Character profile

The gamification part - the tasks are assigned to certain skills,
and your character gets points for doing tasks.



# Design details


## Tasks

A task (optionally) has:
*Title* and *Description*, *Deadline*;
something about *Recurring* tasks;
*Subtasks* and *Notes*, also *Alarms*;
*Tags* (hashtag system would be more flexible than folder system, imho);

As well as things related to gamification part:
*Skills* - what skills are used for this task
*Rewards for completion*, such as *XP gain*, *Money gain*, etc;
*Complexity*, *Fear*, *Importance* etc. - params to estimate the rewards;


## Tasks handling

The overall structure for the tasks (maybe not obligatory, but as a default version).

Split tasks into short- and log-term plans
OR
Split tasks into having a deadline vs having none

Split routine daily tasks from other tasks for today


## UI

something something UI

Tabs with tasks for this day/week/month.

Ability to add icons to everything - I wonder if that should be
part of the data of the task itself though. If so, one has to implement
nice tech for media management (some designing); if not - one has to deal
with the way backups / task sharing is done (f.e. when migrating from one phone to another).


# Implementation details


## Tasks

Probably stored as json with some reference system.

