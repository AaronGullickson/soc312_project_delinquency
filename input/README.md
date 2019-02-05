# General Social Survey

The data we are using comes from the [General Social Survey](http://gss.norc.org/About-The-GSS) (GSS), conducted by the National Opinion Research Council. The GSS is a nationally representative survey of the US adult population that is conducted every two years.

We will only be using data from the 2012 and 2014 rounds of the GSS. I created an [extract](https://gssdataexplorer.norc.org/projects/56025) of the full GSS data using the GSS Explorer web application. I then subset the data to only include respondents who identified as male. Here is a full description of all variables in the dataset that we will use.

- **year**: year of the survey. Either 2012 or 2014.
- **birth_cohort**: year of birth for the respondent. survey year minus birth cohort year gives the respondent's age.
- **marstat**: current marital status of the respondent: never married, married, divorced/separated, widowed.
- **sex_orient**: Self-reported sexual orientation of the respondent. Because of small numbers, individuals who responded as gay or bisexual have been combined into a single category.
- **race**: self-reported race of the respondent. In the GSS, we only have the choices of white, black, or other. 
- **region**: region of the country: Northeast, Midwest, South, West.
- **women_nopolitics**: Response to a question abot whether women were as suited for politics as men. A value of 1 here means the respondent did not think women were as suited for politics as men, while a value of 0 means that the respondent did think women were as suited for politics as men. This variable is one of the three variables that make up the `women_attitude` variable.
- **workmom_nohealthy**: response to a question on whether a "working mother can establish just as warm and secure a relationship with her children as a mother who does not work." A value of 1 indicates that the respondent did not think a working mother could establish as warm and secure a relationship and a value of 0 indicates that the respondent though a working mother could. This variable is one of the three variables that make up the `women_attitude` variable.
- **breadwinnner_model**: response to a question on whether "it is much better for everyone involved if the man is the achiever outside the home and the woman takes care of the home and family." Respondents who said yes to this question are coded as 1 and respondents who said no are coded as 0. This variable is one of the three variables that make up the `women_attitude` variable.
- **women_attitude**: This variable sums up the values for `women_nopolitics`, `workmom_nohealthy`, and `breadwinner_model` to produce a summary score measure of attitudes toward gender equality. High values here indicate less support for gender equality.

In the original data, there are missing values for some observations on some of these variables. To simplify our analysis, I have used some advanced techniques that are beyond the scope of our class to impute these missing values.
