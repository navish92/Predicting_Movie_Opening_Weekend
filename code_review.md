# Code Review: Project 2

### Name: Navish Agarwal

[X] README.md included
[X] Slides included
[X] Code included

## Clean Code:
- I like that you used separate notebooks for scraping, EDA, and modeling, helps make things things clean 
- You can just delete lines of earlier/unused code that's been commented out
- I'd recommend renaming plot axis labels to more easily understandable names than your defalut variable names 
- Code generally follows PEP-8

## Good Documentation:
- Great readme.md! Very descriptive and helps explain the motivations for and importance of the project, as well as a high-level explanation of results & work still to be done.  
- Good use of docstrings on your functions
- Excellent use of markdown cells throughout notebook describing your thought process and decicions, and separating sections; sparse inline comments where needed
- I'd love to see a markdown cell at the end of the notebook explaining your analysis of the final graphs and some conclusions/takeaways! 

## Proper Data Science: 
- Made great use of try/except to maximize data retention even when some rows missing, particularly in clean_soup_release function
- It was a good ideal to drop rows with nulls only if they fell in certain columns as you ackowledged you had a lot of null values. 
- Good pair plots -- I'd love to see a markdown cell with analysis/explanation
- Thorough EDA and treatment of missing values & encoding/thoughtful explanations as to why with graphs 
- I don't think you need both 'All Audience' and 'Adult Audience' as separate encoded columns -- you could keep just Adult Audience, a 1 represents adult audience, a 0 would hence represent all audience.
- Before you began on polynomial interactions & ridge, your statsmodelOLS summary indicated that your condition number was extremely high (9.61e+10) (even with a subset of features) -- this indicates strong multicollinearity, so features at this point should have been dropped first to reduce multicollinearity; polynomial interactions adds a great deal more and increases condition number. So in the future, feature engineer to drop columns first if you notice this! 
- It seems in your cross_val_kfold function you only scale the training data input to the ridge model, but not the simple linear regression model. Both should be scaled no matter what, but especially if you want to be able to directly compare the results. 

## Notes: 
- Great job on project 2! :) 
- Really thoughtful project and clear demonstration of industry knowledge informing nuanced decisions 
