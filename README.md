# Ophelia
Project/Reoccurring task planner app with google calendar integration.
### Group Members:
- Cameron Nicholson
- Sean Shmulevich
- William Chapler
- Opeyemi Sanni

___
## Wireframe
- 🟥Red arrows are screen that link back to the Home Screen usually after finishing completing an action
- 🟩Green arrows link back and fourth between the Home Screen.
- ⬛️Black arrows are always "local" one screen jump
![WireframeAll](https://github.com/Sean-Shmulevich/Ophelia/blob/main/.images/WireframeAll.png)

___
## 1.  Create account
- Create a new account or account already exists and go to home screen
- Configure hours when you sleep &amp; hours when you dont want the app to schedule your <span style="color:red">*"freetime"*</span>
  - Drag between times to set times you do not want to be scheduled for projects in a per hour view of an entire generic week from monday-sunday
- Confirmation screen when you finish configuring new account.
![WireframeMakeAcct](https://github.com/Sean-Shmulevich/Ophelia/blob/main/.images/WireframeMakeAcct.png)

## 2.  Homescreen + Schedule navigator
- Single press day for week view
  - Single press day for hour by hour day view
- Access individual projects/tasks.
![WireframeMainNav](https://github.com/Sean-Shmulevich/Ophelia/blob/main/.images/WireframeMainNav.png)

## 3. View project/task
- the main view of scheduled events in this screen should very similar to the generated schedule -> pick schedule view
  - i.e. - the request of class should be the same 
  -( `list projectX = project.getListOfTimes()`Union `list otherThings = projectX.forEach(projectSessionDateTime => User.calendar.get(projectSessionDateTime)`) == set of times on this screen.
- View single task and configure project settings
- should this view be able to show everything thats happening on each individual day with a project scheduled or should it just show the times of each scheduled session
  - what if there are two sessions scheduled for one day?
- include other long term events/projects in this view or only imported google calendar events?
![WireframeViewTask](https://github.com/Sean-Shmulevich/Ophelia/blob/main/.images/WireframeViewTask.png)

## 4. Create new project/task
- Collect user information about their event to schedule. 
- Generate and show possible schedules within given paremeters
- Show individual schedules on single press possibly implement a calendar view as well.
  - Show confirmation on single press of 'set' button cancel button goes back to home screen
    - cancel button could possibly prompt to add this configuration to a list of unscheduled tasks that are acessable from settings to be planned later.
- Maybe?
  - maybe: before setting new events be prompted to resync with google calenders this will avoid schedule conflits before they happen. but it may mess up an existing one :/
  - Maybe add the option to add a link to a git repo or canvas or something
  - Maybe add the option checkbox to schedule on weekends (override free time)
  - Represent schedule with relative size of 7 rectangles representing relative time per day scheduled. 
  - What if no schedules could be make?
![WireframeMakeTask](https://github.com/Sean-Shmulevich/Ophelia/blob/main/.images/WireframeMakeTask.png)

## 5. Settings
- Configure FreeTime
- Configure Sleep
- Sync with google calendars 
  - upload events we planned to google calendars
  - or download new events from google calendars
  - or opt into sync with google calendars
- Turn on/off all notifications and timers
- Some kind of mission statement
- Logout

- lets say we implement automatic google calender sync:
-  this is a solution to some problems
   -  but what if a user schedules an event during another event through google calender and then comes back to the app. 
      -  how will the system know that this happened?
      -  how will will it react.
         -  one option is to prompt reschedule - too much work
         -  make the event 15 minutes after the event it has a conflict with - this is good but we should tell the user it was rescheduled
![WireframeSettings](https://github.com/Sean-Shmulevich/Ophelia/blob/main/.images/WireframeSettings.png)
