# Reflection #1

Pod Members: **Elias Arghand, William Huang, Shayan Sarnevesht**

## Reflection Questions

* Name at least one successful thing this week.

We successfully created all the backend endpoints having anything to do with users and groups for going on a trip. A lot more functionality was needed for this than we initially thought. We had endpoints to register, login, find one’s self, update user info, get groups for user, get all groups, create group, add user to group, remove user from group, etc.



* What were some challenges you and/or your group faced this week?

We had trouble integrating the Google Maps API into the project. When creating a trip, we want a user to be able to type in a source and destination and be able to see visually on a map where that location is. 
At first we played around with the API in dummy project using google’s official documentation, which worked well, but we couldn’t use the same code in the React project unfortunately because it was not compatible.
Instead we had to use NPM modules for Google map API that were poorly maintained. It was frustrating because instead of having pristine documentation and full functionality with minimal effort with vanilla javascript, we had to use 3 separate npm modules to implement the autocomplete, distance/duration calculations, and the map itself.



* Did you finish all of your tasks in your sprint plan for this week? If you did not finish all of the planned tasks what were some factors that contributed to this?  (i.e over planned, did not know how to implement certain features, miscommunication from the team, had to pivot from original plans, etc.)

Yes. We planned on implementing our “in progress” issues on our project board on the backend by this week and starting on the frontend, which we did do.For example, we have endpoints to update user info, update group info, view one’s own profile (user details), create a profile with a school email, etc. To let the user interact with this logic we will finish up the frontend next week.

* Did the resources provided to you help prepare you in planning and executing your capstone project sprint this week? Be specific, what resources did you find particularly helpful or which tasks did you need more support on?

No, we did not use the resources here because we were mostly heads-down in working on our product, only consulting documentation for PERN related things or google maps api or materialUI



* Which features and user stories would you consider “at risk”? How will you change your plan if those items remain “at risk”?

The live chatting feature is definitely at risk because it will require a specialized knowledge of web sockets and webRTC which are frameworks of the networking area, which we are not well-acquainted with, but want to learn more about
