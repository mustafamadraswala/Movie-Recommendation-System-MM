# Movie-Recommendation-System-MM

### End to End Machine Learning Project | Movie-Recommendation-System | Front-end - Streamlit | Heroku Deployment 


### Anaconda Steps - 

1. Open anaconda prompt
2. Base environment - 
```
conda create -n <my_env_name> python=3.8.8 -y
```
```
conda activate <my_env_name>
```
3. Create a local Folder
4. Copy the path --> cd in anaconda prompt to the path (D:\)
```
 jupyter notebook
```

## OR

===========================================================================

### VS Code Steps - 

1. Create a local Folder
2. Create a Repo on github --> Add Readme.md - Select Python - Add a License
3. Open Cmd --> cd into local folder --> git clone github repo
4. Go to repo folder on local machine --> Right click - Git bash Here - code .
5. Vscode will open with the folder as working directory
6. Ctrl+Shift+P --> Select base pythn=3.8.8 interpreter --> Open Terminal
7. Select Cmd or Git ( or powershell)  according to the project
8. Create a new virtual environment

```
conda create -n <my_env_name> python=3.8.8 -y
conda create -n movierm python=3.8.8 -y
```
```
conda info --envs
```
```
conda activate <my_env_name>
conda activate movierm
```
===========================================================================

### Create and Install requirements.txt
```
pip install -r requirements.txt
```

### Setup your Github account
```
git config --global user.name "<your github username>"
```
```
git config --global user.email "<your github email id>"
```

### Push all the changes and code to Github -
Add all the files to github - 
```
git add .
```

Check status of your files -
```
git status
```

Commit all the files to github by pushing the fies from local to  thestaging environment -
```
git commit -m "This is my first commit includes requirement.txt and readme.md file"
```

Or do both the steps together -
```
git add . && git commit -m "This is my first commit"
```

Push everything to github -
```
git push origin main
```
=============================================================================

### Execute the Movie-Recommendation-System-MM.ipynb file to get 2 pickle files
1. movie_list.pkl 
2. similarity.pkl

### Create a python file for your streamlit application
```
touch app.py
````

### Use the streamlit library to make a simple front end page
### Execute the app.py file in vscode
```
streamlit run app.py
```

=============================================================================

### Deploy to Heroku
1. Create a Procfile in folder in VScode -
```
web: gunicorn app:app
```

If using Streamlit -
```
web: sh setup.sh && streamlit run app.py
```

2. Create a setup.sh file -
ps - Required for streamlit implementation

3. Add requirements.txt 
If deploying the app to heroku is not working, mostky it is a library version error.
Just add the names of the libraries and not the versions.
For eg - Streamlit, Flask, Requests

4. Go to Heroku - Create an app movie-recommendation-system-mm

#### In this project directly deploying to github will not work as you need to upload 2 pickle models -
1. movie_list.pkl 
2. similarity.pkl - This model file is more than 100 mb and it will not push to github.

###### So instead after step number 3, install heroku CLI on your local machine.
###### Close vscode and start the environment again after heroku installation and then perform the following steps.
###### Ps - These will be mentioned in your application on heroku -

```
>> heroku login
```
###### Create a new Git repository
######Initialize a git repository in a new or existing directory
```
>> cd my-project/
`````
```
>> git init
```
```
>> heroku git:remote -a movie-recommendation-system-mm
```

###### Deploy your application
###### Commit your code to the repository and deploy it to Heroku using Git.

```
>> git add .
```
```
>> git commit -am "first deployment"
```
```
>> git push heroku main (or master)
```
###### You can now change your main deploy branch from "master" to "main" for both manual and automatic deploys, please follow the instructions here.
###### Existing Git repository
###### For existing repositories, simply add the heroku remote

=======================================================================================
