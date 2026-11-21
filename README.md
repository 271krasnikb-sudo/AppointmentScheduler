# Appointment_Scheduler-Student
﻿SMART APPOINTMENT SCHEDULER - STUDENT STARTER
=============================================


CONTENTS (all in ONE folder when extracted)
  Appointment.java             - PROVIDED; do not edit
  AppointmentScheduler.java    - FIVE TODO methods to complete
  SchedulerMain.java           - PROVIDED console menu and startup/save I/O
  data/seed_schedule.txt       - starting schedule; do not edit
  BST_Appointment_Scheduler_Student_Directions.docx - assignment


SETUP
1. Extract this ZIP to a new folder.
2. In VS Code, File > Open Folder, and select THAT folder directly.
   The data folder must be in the same folder as the three .java files.
3. Run SchedulerMain.java (or in the terminal: javac *.java && java SchedulerMain).
4. Expected first message: Loaded 5 appointments from data/seed_schedule.txt


ONLY EDIT AppointmentScheduler.java.
The menu and initial file loading work before any TODO methods are completed.
Saving will not overwrite an earlier saved file until write() is implemented.
When working, save writes data/saved_schedule.txt; the next run loads that first.


ALL TIMES ARE 24-HOUR HH:MM. This is a single-day calendar, 08:00 to 17:00.

1. Explain how floor() and ceiling() allow your scheduling program to detect overlapping appointments. Why is checking these two appointments sufficient, rather than checking every appointment in the calendar? 

floor() returns the appointment with the start time before the requested and ceiling() returns the appointment with a start time after. Using these you can use check if the appointment before + duration of that appointment is greater than the start time of the requested and if the requested start time plus requested duration is greated than the start time of the one after. This is sufficient because the way that appointments are added is that they can't overlap so the only potential appoitnments that can overlap is the appointment directly before and directly after. So making sure these appointments don't overlap is good enough.
2. Why is a TreeSet (balanced binary search tree) more efficient than an unsorted ArrayList for finding the appointments immediately before and after a requested time? Compare their Big O time complexities and explain why this matters as the schedule grows. 
A TreeSet uses a binary search to find specific values instead of a linear search like an unsorted ArrayList. This makes the TreeSet for finding appointments before and after O(logn) while for the Arraylist it is O(n). 

3. Why is it unnecessary to save the exact shape of TreeSet’s internal tree?
It is unesseasary because a TreeSet can compare appointments by their start time so it only nees to save the first reference then off that reference it can use comparisons until it finds the value its looking for.

