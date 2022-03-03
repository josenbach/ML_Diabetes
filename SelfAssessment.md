# SELF 
- **Presents a cohesive written analysis that describes the role(s) they played over the course of the project and their contribution to the project in that role.**
- **Presents a cohesive written summary of how they contributed to each of the roles they did not take on via team discussions, peer reviews, or other means.**
- **Additionally, the analysis should describe their greatest personal challenge over the course of the project, and how they overcame that challenge.**

Towards the first week, I helped look into various topics and searching for repositories. Ultimately my idea was not chosen, but we discussed as a team and decided diabetes was the best topic for us.

Towards the next week, my other teammates did a lot of work regarding the cleaning of the data and using random forest and ML models. I provided feedback and ideas but was not directly involved in the Jupyter notebook writing.

The week after, we already had a database within our Jupyter notebook so I exported the data to a csv file and began to play with the columns we wanted to keep which include medicine.

It was during that time our team met and discussed the confusion matrix which we discovered was not presenting the data the way we expected. We wanted to use the ML model to create a screen but it was not providing enough true negatives.  The accuracy was high but the confusion matrix showed a huge gap.

During that time there were a lot of conversations on how we could change data further. Such as removing some age bins, removing medicines, etc. and other items. This included input from myself as well as other team members. I pulled information on precision, recall and F1 score. This meant we changed the information in our database once more to which I exported it and created the dashboard we shared in the presentation. This was the biggest challenge because it meant all of the visuals I had created were now not relevant because we moved items like medicine which was a big piece. I had to wait on teammates who were cleaning and modifying data and could not start until they were finished which meant I had to hit the ground running once it was available to create visuals and dashboard.

With that I created a new dashboard and began to write about it in the slides and readme. Intisar and myself were both responsible for dashboards (Intisar created dashboards for the raw data and I explored database data). I made sure to include a screenshot in the slide deck and include the interactiveness and other requirements in the readme. Intisar kept our own chat on the side specifically talking about and reviewing each other’s dashboards and story boards.

# TEAM

**Presents a cohesive written analysis that describes their teamwork, including all of the following:**
- **Their communication protocol, including any challenges, how they were resolved, and what they would do differently next time**

  - We created a Slack chat with all 5 members which we utilized when we met every Tuesday and Thursday during class as well as during other times when each of us were working on the project and had updates/questions. Many of us had busy schedules that conflicted, aside from class time on Tuesdays and Thursdays, so we often spent the whole class time and extra time after working on our project together. I wish we could have met outside of class time, but it wasn’t bad. The only issues I would say is sometimes we were just sitting there while one person wrote code, or updated slides -  but we all provided information, feedback, pointed out spelling errors, or things we should mention so it was useful.
- **Their strengths as a team, including tips and tricks they would want to share with a new cohort kicking off the project**
  - One of the first things we did was discuss the different requirements and what we feel most comfortable doing. We all had different strengths so that played well into how we each split up the tasks. For example, Jae is great a github and was teaching us how complete a pull merge request for our branch. Jae and Julia were most comfortable with Python so we used that as our programing language. We did run into an issue and for whatever reason, even though the file was identical, we couldn’t merge the Jupyter notebook – so I do recommend mentioning to each other when you are working on the notebook and to use it. Or have your own versions and adding the codes that end up being relevant. I felt most comfortable with dashboards as I have work experience with it. Intisar is great at markdown and writing summaries, so she wrote most of the read me conclusions and thoughts and Karen put together the google slides and worked on animations for our presentation. We were all able to bounce of ideas off of one another and even point out mistakes in codes or dashboards. We were all open minded and honest with each other.

# SUMMARY
**Presents a cohesive, three- to four-sentence summary of the project that could be used on a LinkedIn profile, in an interview or cover letter, or as an elevator pitch, including all of the following: **
- **Topic addressed**
- **Machine module used**
- **Results of the analysis**

According to the CDC, 37.3 million people have diabetes (11.3% of the US population), and diabetes prevalence has grown significantly from 2004 to 2019. There is no known cure and medication, and monitoring devices are used by diabetics to control. We cleaned and prepared data available from UCI to potentially create a screener test. We used random forest and a neural network to be able to predict whether a patient may need their HbA1c to be checked. We had a high accuracy, but our confusion matrix showed our model was poor at classifying normal A1c. Given our limited time, we were not able to use multinomal or find a dataset that was better suited to create our screener and hopefully bypass unnecessary testing for HbA1c levels.
