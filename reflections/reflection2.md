# Reflection #2

Pod Members: **Elias Arghand, William Huang, E Shayan Sarnevesht**

## Reflection Questions

* Name at least one successful thing this week.

One successful feature was getting the Google Maps API to show both the source and destination for the "More info" page when clicking on  event. This was difficult since we had to asynchronously wait for the GooogleMaps component to load, and also for the call to the backend to get the trip info (source and destination info).
Because of these calls, we made a sophisticated set of promises calls that were invoked when the resources were ready, and we set the markers on both locations and set the map to fit both.

 Add response here

* What were some challenges you and/or your group faced this week?

We had trouble with MaterialUI styling for the cards for each trip in the Bulletin Board and My Trip tabs. Because MaterialUI isn't super compatible with additional styling especially in there Card and CardContent components, we had trouble aligning everything exactly where it needed to be in each card. Also we couldn't link a regular stylesheet, instead using the useStyle's hook which was new to learn. 

 Add response here

* Did you finish all of your tasks in your sprint plan for this week? If you did not finish all of the planned tasks what were some factors that contributed to this?  (i.e over planned, did not know how to implement certain features, miscommunication from the team, had to pivot from original plans, etc.)

We had 5 core features (Github issues) that we need for the MVP and 5 stretch features, and our sprint was to finish the 5 core features, which we did. We created the ability to see all trips, create a profile with all necessary info, see deatiled information of rides, create a ride/post, and see/edit one's own profile info.

 Add response here

* Did the resources provided to you help prepare you in planning and executing your capstone project sprint this week? Be specific, what resources did you find particularly helpful or which tasks did you need more support on?

We watched the Y-combinator's video on how to plan an MVP and what features are most necessary to get done for an MVP with a tight deadline. Using Michael Seibel's talks MVP features, we decided which features would be most necessary for this sprint.

* Which features and user stories would you consider “at risk”? How will you change your plan if those items remain “at risk”?

We consider the live chatting feature within a trip group to be at risk since we learned that it will require specialized knowledge of networking concepts like WebSockets and WebRTC protocols. However, we are still up to the challenge once we eliminate all bugs from our core and "nice-to-have" features.
