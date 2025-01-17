![VerticalX Banner](https://github.com/thisisashwinraj/VerticalX-Recommendation-System/blob/main/assets/VerticalX_Banner_Light.png#gh-light-mode-only)
![VerticalX Banner](https://github.com/thisisashwinraj/VerticalX-Recommendation-System/blob/main/assets/VerticalX_Banner_Dark.png#gh-dark-mode-only)

VerticalX is an information filtering system, that uses Natural Language Processing techniques to make content-based recommendations for 10k+ movies based on the user's interest. 
The project uses the [TMDb dataset](https://www.kaggle.com/datasets/juzershakir/tmdb-movies-dataset). The investigating dataset contains information for over 10,000+ movies collected from TMDb. This project is deployed using [StreamLit](https://tinyurl.com/verticalx-recommender-system).

Looking to get started with building a movie recommendation system? Look no further. Check out this [medium blog](https://ai.plainenglish.io/end-toend-tutorial-to-build-a-movie-recommendation-system-using-python-and-azure-cc6e640e0aab) by Ashwin Raj. With step-by-step instructions, and easy-to-follow code examples, this article covers everything you'll need to be well on your way to building your very first recommendation system. Download the pdf version from here

The project was developed in March 2022 as a standalone project & has been licensed under the [GNU Affero General Public License v3.0](https://github.com/thisisashwinraj/VerticalX-Recommendation-System/blob/main/LICENSE). All Pull Requests are maintained by [Ashwin](https://github.com/thisisashwinraj). Learn about VerticalX Recommendations System [here](https://github.com/thisisashwinraj/VerticalX-Recommendation-System#user-installation-and-source-code)

# SubDirectories and Constraints

### Dependencies
 - **Website:** StreamLit(front-end), Azure app service and Requests Library (for sending HTTP/1.1 requests in Python)
 - **Machine Learning Model:** Pandas, NumPy, Matplotlib, Seaborn, Natural Language Toolkit, Scikit-Learn and Pickle

### Files and Folders
- **Assets:** This directory contains Jupyter notebooks, required for building the NLP Model, & other visual resources
- **Data:** This sub-directory contains the entire dataset used for building the model. It contains 10,000+ data points
- **Pickle:** This directory contains the three serialized python-dump files. The similarity.pkl file, is not included in this
- **app.py:** This file is the generic entry point for this python application, and contains the complete py source code 
- **Procfile:** This file specifies all basic commands that are to be executed by the Heroku app during the app startup

All relevant updates, and stable versions are made available in the ~/stableVersion sub-directory. Some subdirectories may be sensitive for the project and may trigger 
review requests, when pull requests touch these files. Github handles with commit rights made available in the 
[~/Template Files/CODEOWNERS](https://github.com/thisisashwinraj/VerticalX-Recommendation-System/blob/main/templates/CODEOWNERS) are responsible for reviewing such changes

# User Installation and Source Code
The recommendation model is wrapped in a website, designed using streamlit and hosted over Heroku. The working demo can be found here: [verticalx.azurewebsites.net](https://verticalx.azurewebsites.net/). 
For a user to run this application on their local workstation, the user must first download all resources, and requirements. To recommend  movies, the users shall  select a movie from the dropdown list, and hit the recommend button. 5 similar movie selections will be recommended by the ml model.

To run the streamlit application on a local computer, open the terminal, install streamlit and then type the command:
```
streamlit run app.py
```
Command may take upto 30 sec before opening the streamlit app on the browser with local url: http://localhost:8501.

![Demo](https://github.com/ashwinraj-in/VerticalX-Recommendation-System/blob/main/assets/VerticalX_Demo.gif)

The working demo for the application hosted over heroku may sometimes crash with connection timed out message. This is because the program exceeds [Heroku's soft limit for slug size](https://devcenter.heroku.com/articles/slug-compiler#:~:text=The%20maximum%20allowed%20slug%20size,such%20as%20ls%20and%20du%20.) including
the program, and all it's dependencies.

### Directory Structure
VerticalX's development takes place on GitHub. Submit any bugs, that you may encounter to the issues tracker with a reproducible example, demonstrating the problem in accordance with the [issue template]() present in contributing files.
    
    ├── procfile
    ├── Assets                         // Contains image graphics and jupyter nbk
    │   └── VerticalXNotebook.ipynb
    ├── README.md                     
    ├── app.py                         // Entry point for the python applications
    ├── requirements.txt
    ├── setup.sh
    ├── Pickle                         // Contains serialized pickle python dumps
    │   ├── movies.pkl                    
    │   └── movie_dict.pkl             
    └── Data                           // Listing of all data source in the model
        └── tmdb_movies_data.csv
                             
To run the application, first download the required resources, or clone this repository. StreamLit must be pre-installed for this application to work. The files, and folders important for this website to run includes: app.py, procfile, setup.sh, pickle-dumps, the  datasets, and the Jupyter notebooks. Similarity.pkl file required [GitLFS](https://git-lfs.com/) to be hosted on GitHub as it exceeds GitHub's file size limit. However, the file can be re-generated by the user while running the Jupyter notebook


# Contribution Guidelines
To start contributing to the project, clone the repository into your local system subdirectory using the below git code:
```
https://github.com/thisisashwinraj/VerticalX-Recommendation-System.git
```
Before cloning the repository, make sure to navigate to the working subdirectory of your command line interface and ensure that no folder with same name exists. Other ways to clone the repository includes using a password protected SSH key, or by using Git CLI. The changes may additionally be performed by opening this repo using GitHub Desktop

### Edit the Source Code and Make Desired Changes
To be able to make changes to the source, you may need to install and use a python IDE such as PyCharm, Microsoft VisualStudio and/or any other python interpreter. You will also require a Jupyter notebook  for working with the code snippets. The movies posters are fetched using the [TMDb's API](https://developers.themoviedb.org/3). You may create your own API by logging into TMDb developers API-3. Ensure that you are strictly following the basic coding standards, while making the desired change

### Submitting a Pull Request
Before opening a Pull Request, it is recommended to have a look at the full contributing page to make sure your code complies with all the pull request guidelines. Please ensure that you satisfy the [~/checklist](https://github.com/thisisashwinraj/VerticalX-Recommendation-System/tree/main/Template%20Files/checklist) before submitting your PR.

Navigate to this subdirectory & check status of all files that were altered (red) by running the below code in Git Bash:
```
git status
```
Stage all your files that are to be pushed into your pull request. This can be done in two ways - stage all or some files:
```
git add .            // adds every single file that shows up red when running git status
```
```
git add <filename>   // type in the particular file that you would like to add to the PR
```

Commit all the changes that you've made and describe in brief the changes that you have made using this command:
```
git commit -m "<commit_message>"
```
Push all of your updated work into this GitHub repo in the form of a Pull Request by running the following command:
```
git push origin main
```
All pull requests are reviewed on a monthly rolling basis. Your understanding is appreciated during the review process

# License and Project Status
VerticalX and all its resources are distributed under the [GNU Affero General Public License v3.0](https://github.com/ashwinraj-in/VerticalX/blob/main/LICENSE). The site is compatible with all operating systems. The latest released version of VerticalX webapp is v1.0.1 and is available to be used on any local/remote system for general use through some web browsers. All new releases are logged in the [~Stable Versions](https://github.com/ashwinraj-in/Kiwi/tree/main/stableVersions)
