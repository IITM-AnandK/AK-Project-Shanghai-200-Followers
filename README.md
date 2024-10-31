# AK-Project-Shanghai Users >200 Followers with Repositories

**Scrape / Data Collection Process:        **

-  To scrape/collect the required  data from GitHub, I leveraged the GitHub REST API to gather details about users in Shanghai with over 200 followers and their most recently pushed repositories with maximum limit to 500 repositories

-  I used my personal access token for authentication to access GITHUB API to avoid rate-limiting issues. The code includes error handling to pause execution in case rate limits are exceeded

-  To retrieve all relevant users, pagination was implemented to handle the API's limitation of returning a maximum of 100 users per request. The code iterates through pages of results until all matching users are obtained

-  For each identified user, a separate API call was made to retrieve detailed user information

-  The 'company' field was cleaned by removing leading/trailing spaces and any '@' symbol at the beginning.

-  Company names were then converted to uppercase

-  Additionally, all boolean fields were standardized to contain either 'true' or 'false' values

-  All extracted user and repository data were stored in separate CSV files named 'users.csv' and 'repositories.csv', respectively



**Some of the Interesting and surprising facts that I see in the data post analyzing are:     **   

-  While Shanghai's GitHub users are employed across various companies.  Among them users with over 200 followers who have provided company information, roughly 5% are affiliated with ByteDance, a leading Chinese internet technology company

-  While 29% of the 742 total users are open to hiring opportunities, the majority (71%) appear to be primarily using the platform for skill development and learning

-  Peng-zhihui leads in followers with 80,714 and 59 repositories, followed closely by ruanyf with 79,328 followers and 72 repositories

-  In contrast to Peng-zhihui and ruanyf, who have a large following, Hengle possesses the most repositories, with a remarkable count of 11,057

-  It is surprising to find that the stargazer and watcher counts are uniform across all users

-  Between 2008 and 2013, the number of repositories created by Shanghai users skyrocketed by over 95 times, from a mere 20 to a staggering 1900+. This reflects the rapid adoption of GitHub and a surge in open-source contributions from the Shanghai developer community

-  The year 2018 marked the peak of repository creation for Shanghai users, with more new repositories added. This suggests a high level of development activity and innovation within the community during that period.  In the past few years (2019-2024), there has been a noticeable decline in the number of new repositories created, dropping by nearly 39% from the 2018 peak. This trend might indicate a shift in development practices or a saturation point in repository creation



**Recommendation for developers basis my analysis:       **

-  Shanghai's developers initially favored JavaScript, Python, and Java, accounting for almost 44% of repositories where language data information exists. However, a clear shift is evident in the last two years, with Python and TypeScript gaining traction as the preferred languages for new projects, even amidst a diverse landscape of 87 different programming languages utilized by developers. Developers should consider learning and utilizing these languages in their projects. This can increase the visibility and relevance of their work within the developer community

-  Some of the most popular open sources licenses used by developers are MIT License and Apache License 2.0.  MIT and Apache licenses are permissive licenses and widely used in open-source projects. Key differences lie in their handling of patents and trademarks, where Apache has an advantage with more explicti protection

-  The vast majority of repositories (98%) have projects enabled, and a significant portion of those projects (86%) also include a wiki.  Developers should utilize these features to organize and document their work effectively to improve project clarity and make it easier for other to contribute

-  Repository names and descriptions play a cruicial role in discoverability and attach collaborators, so need to make it clear, concise, and relevant to the project's content

-  Only 29% of the Developers updated hiring preference.  Developers who are open to hiring should actively update their profiles and highlight their skills and experience to attract potential employers

-  Stay informed about emerging technologies, trends, and best practices within the developer community. Follow influential developers and organizations, participate in relevant discussions, and attend workshops or conferences
