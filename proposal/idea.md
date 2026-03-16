1. Project Title: Flight Genie

2. Team Members (names, emails): 
  - Melissa Andrade, maandra9@asu.edu
  - William Jones, whjones3@asu.edu
  - Gary Nez, gwnez@asu.edu
  - Janine Nelson, jenels19@asu.edu
  - Lariella Citron, lcitron@asu.edu

3. Problem Statement: Have you ever had your plans gone array because your flight got unexpectedly cancelled? Our nanoGPT model Flight Genie will calculate a probability of your flight getting cancelled or delayed, so you can plan your trip more accordingly to probable mishaps. 
  o Who is the user?
    Everyone who ever expects to fly on a commercial airline flight, and anyone who's plans can be impacted by flight delays or cancellations.
  o What problem or pain point do they experience today?
    Everyday flights get cancelled last minute. This can ruin the business, vacation, and family trips of expecting passengers. 

5. Why Now?:  AI models now have the capabilities to use more data to make more accurate predictions than ever before. Flight delays and cancellations 
  o Why does this problem matter in the next 3–5 years?
  o What changed (technology, regulations, culture) that makes this possible now?

This problem matters now because air travel demand is high, disruptions are common and costly, and travelers increasingly care about reliability before they book. At the same time, several changes make this product possible when it was not a few years ago. This is because aviation data infrastructure is improving, with the FAA modernizing how aeronautical data is collected and shared to support real-time operations, and AI tools are now strong enough to detect patterns across interacting variables like weather, route history, airport congestion, and airline performance

6. Proposed AI-Powered Solution
  o What does your product do for the user?
   Our model provides people insight on the probability of their flight being delayed or cancelled. By knowing that there's a higher chance of their flight being delayed, someone can accomodate their plans with that possibility in mind. For exmaple, a user could agree to pick up their friend from the airport at 10am and have plans to go to work at noon. Now, if that flight gets delayed, then that person has to choose between picking up their friend from the airport or going to work. To avoid this problem, the friend could've predicted that there was a high chance of their flight being delayed and therefore could've chosen someone with more leeway in theur schedule to pick them up from the airport. 
  o Where does AI/ML add unique value vs simple rules / heuristics?
   The reasons why flights get delayed will expand and change over time. The majority of flights are delayed or cancelled due to weather reasons. Climate change is making our planet warmer and our weather more severe, which will increasingly cause more flight delays and cancellations. Because of this, AI is the better than heauristics for the model because it can adapt over time to implement new data sets.  
 
7. Initial Technical Concept: 
  o What data would you need (or already have)?
    Our first data sets we'll use have information for millions of flights between the years 2018-2022. It includes the following information for each flight: date, airline, origin, destination, cancelled (true/false), diverted (true/false), CRS departure time, actual departure time, departure delay minutes, arrival time, arrival delay minutes, air time, CRS elapsed flight time, actual flight time, distance, day of the month, day of the week, operating airline, and more information.
   We are also adding data to our model that predicts storms on any day of the year and in any state. For this, we will use the data set from another d, which includes storm date, time, and state information from 1950-2015. 
  o What model(s) might you use (e.g., GPT-style text model, classifier,
    recommender, vision model)?
     Classifier models will be used for this project. The classifier model will predict the probability of a flight being on time, short delayed (< 30 minutes), long delayed (> 30 minutes), or cancelled. 
  o How could your nanoGPT work feed into this (e.g., custom generative
    component, fine-tuning, evaluation)?
9. Scope for MVP: 
  o What can you realistically build in ~6 weeks?
  o Define a very concrete v1 feature: “A user can ___ and our system returns ___.”

In about 6 weeks, a realistic MVP is a flight reliability ranking tool, which will not include a full booking or real-time disruption platform. A user enters an origin, destination, and travel date, and the system returns a ranked list of flight options by likelihood of delay or cancellation, using historical on-time performance plus a small set of current factors like route, airline, departure time, and weather forecast if available.

10. Risks and Open Questions
  o Top 3 unknowns (e.g., data availability, evaluation, user adoption).

  1: Timely Data: Past flight data is easy enough to procure but current data is hard to come by. The older the data, the less reliable it will be for modern flight calculations so this could potentially be a risk.
  2: Irregular Operations: Storms, strikes, and other irregular operations could make the algorithm less reliable. The AI will be trained on data that relates to normal operations and may not handle rarer events well.
  
12. Planned Data Sources
  o E.g., Kaggle, Hugging Face Datasets, public APIs, synthetic data.
We plan to use Kaggle to source our data sets. We have already downloaded data sets that include thousands of flight data from the years 2018-2022. This data includes information for each flight including: cancellation status, delayed departure/arrival time, flight origin and destination, airline, and more.
