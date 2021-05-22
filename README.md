Keywords: Statistics, EDA, visualization, Bayes' theorem
 
# Do redhead people live shorter lives?

<img src="https://gingerparrot.co.uk/wp/wp-content/uploads/2018/06/group-of-redheads.jpeg" width="800"> 
I hope the headline of my first project is provocative enough to catch your attention.

Being a woman with red hair, during my 29-years long life I have heard millions of jokes, myths and precautions concerning myself and my health. Historically, red hair aroused the interest and, unfortunately, hateful biases. If in the mediveal times redhair women were automatically accused of being witches or soulless persons, in the XXI century redhair people are said to be more exposed to skin cancer or allergy, more pain sensitive and that redhair people will "go the way of the dinosaur" due to climate change. Even my tattoo master warned me that I might have some problems with tattoo because of my "different blood". Some of these statements are statistically proved facts and some are just myths.

**But do these aspects about redheads' health affect their life expectancy?**

Inspired by 2 sources:
- the article about correlation between health status and degree of hair redness: [Health status by gender, hair color, and eye color: Red-haired women are the most divergent](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5746253/);
- the DataCamp project designed by Madeleine Bonsma-Fisher: [Do Left-handed People Really Die Young?](https://learn.datacamp.com/projects/479);

I decided to explore this issue.

In this project I used 2 datasets:
- death distribution data for 2019 in Czech Republic [website of Czech Statistical Office](https://www.czso.cz/csu/czso/demographic-yearbook-of-the-czech-republic-2019);
- data collected for a survey on the RhD factor in relation to human health (answers for questionnaire were obtained from Czechs and Slovaks between 28/4/2014 and 12/09/2016, [dataset available here](https://figshare.com/s/6a02dd5cec0f90b69db9))

**DISCLAIMER:**
Even though the results seem to be very promising for me personally, I ask you not to take them too seriously because, as some of you might know, according to statistics the average longevity of swiss students in 19th century was 20.2 years (you can find this in the article: [The most dangerous profession: A note on nonsampling error.](https://psycnet.apa.org/doiLanding?doi=10.1037%2F1082-989X.4.3.250)).


# Notebooks
The project includes the following Notebook with detailed analysis and code:
- [Readhead people Project.ipynb](https://github.com/ElinaAizenberg/Readhead-people---Project/blob/main/Readhead%20people%20Project.ipynb)

# Conclusion

Average life expectancy of people in Czech Republic per gender and hair redness degree:

|	                | All hair colors |	Not red hair | Slightly red hair | Red hair |
| -------------   |:---------------:|:------------:|:-----------------:| --------:|
| Both genders	  |    75.74        |   74.92      |	      76.53      |	 77.61  |
| Females	        |    79.18	      |   78.39	     |        79.65	     |   80.78  |
| Males	          |    72.44        |	  71.28	     |        73.86	     |   74.26  |

Well, results look very promising for me. Despite all health problems, whether they are real or only mythical, female redheads seem to be longlivers. In all hair color categories females perform better than males.

Nevertheless, there are several issues about technical side of the project that should be considered while evaluating the results.

1. There is a 3-5 years gap between death distribution dataset and redhead people dataset. So, they are not aligned.

2. In redhead people dataset there were several ages without respondents. Also, for people aged 0-21 and 73-100 in 2019 there was lack of data about hair color rates. So, I extrapolated the existing rates using rolling mean. Although, I tried to catch trend during long time periods, I suppose, artificially calculated rates might differ substaintionally from real ones.

3. As I mentioned in the beginning, respondents in survey of health and hair color were from Czech Republic and Slovenia, while I used only czech death distribution data.
