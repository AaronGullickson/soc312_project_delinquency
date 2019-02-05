# National Longitudinal Survey of Youth 1997

The data we are using comes from the [National Longitudinal Survey of Youth 1997](https://www.nlsinfo.org/content/cohorts/nlsy97) (NLSY97), conducted by the US Bureau of Labor Statistics. The first wave of the NLSY97 surveyed respondents who were aged 12-17 in 1997. These same individuals are re-interviewed each year, making this a *longitudinal* study. However, we will only be using the data from wave one in 1997.

I created an extract of the full NLSY97 data using the [NLS Investigator](https://www.nlsinfo.org/investigator/pages/login.jsp). Here is a full description of all variables in the dataset that we will use.

- **hard_times**: All household informants (typically the parents of respondents) were read the following: "Sometimes children go through hard times. For example, they live in a place without water or electricity, or in a homeless shelter. To the best of your knowledge, has [this youth] ever experienced such hard times?" This variable indicates whether the respondent answered yes or no to this question.
- **deliq_score**: The delinquency index is a score that ranges from 0 to 10 depending on the response to questions about the following: running away from home; carrying a gun; belonging to a gang; damaging or destroying property; stolen something from a store less than \$50. stolen something from a store work \$50 or more; other proper crimes like fencing; attacking someone with intent to seriouly hurt them; sold or helped sell drugs; ever arrested by police. The score indicates the number of "yes" responses given by the adolescent.
- **hh_income**: The household income for the respondent's household, measured in 1000's of US dollars.
- **hh_networth**: The net worth of the respondent's household, measured in 1000's of US dollars. Note that this value can be negative.
- **high_parent_ed**: the highest years of schooling reported by the respondent's resident parents and/or biological parents.
- **family_type**: What type of family does the respondent currently reside in? I have combined two biological and two adoptive parents into a single family type. The other types are a two parent household with one step-parent (bio + step), a single biological parent, and all other cases.
- **urbanicity**: Respondents are classified as living in either an urban or rural location. The NLSY97 did not distinguish sub-urban from rural.
- **school_type**: What kind of school did the respondent last attend. The choices are public, private, parochial (e.g. Catholic), or other.
- **drop_out**: is the student currently enrolled in school or did they drop out?
- **held_back**: has the student ever been held back a grade in school?

In the original data, there are missing values for some observations on some of these variables. To simplify our analysis, I have used some advanced techniques that are beyond the scope of our class to impute these missing values.
