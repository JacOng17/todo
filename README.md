# Prerequsites:

**Verify that you have a current version of Ruby *(v2.3.1 or later)*:**
``` 
ruby -v
```

**To install Rails, use the gem install command provided by RubyGems:**
```
gem install rails
```

**To verify that you have everything installed correctly, you should be able to run the following:**
```
rails --version
```



# 
**Navigate to the folder that you want to start your Rails App on:**
```
cd <file path>    (eg. cd ~/Workspace)
```

**To make the skeleton of your Rails App:**
```
rails new <App name>    (eg. rails new todo)
```

**"cd" into the project folder:**
```
cd todo
```

**Now run the Rails Server:**
```
rails server    [OR rails s] [You can check out your site on "localhost:3000/"]
```
*Ensure that you have "killed" the server by pressing "Ctrl + c"*

**Create a Repository on GitHub for this project:**
```
echo "# todo" >> README.md (optional)
git init
git add .     [you might also want to add a README.md page]
git commit -m "First commit"
git remote add origin https://github.com/<username>/<repo name>.git
[OR if ssh enabled]
git remote add origin git@github.com:<username>/<repo name>.git
[To check where your repo is pointing to: git remote -v]
git push -u origin master
```

#
**Create a "*scaffold*" *“Scaffolding in Ruby on Rails refers to the auto generation of a simple set of a model, views and controller usually for a single table. Would create a full CRUD (create, read, update, delete) web interface for the Users table”)* :**
```
rails g scaffold todo_list title:string description:text
```

**We did something to the model, the database, so now we’ve got to run a rake command:**
```
rake db:migrate
```

**Check your local server to see if everything worked:**
```
rails server    [OR rails s] [instead of "localhost:3000/", navigate to "localhost:3000/todo_lists/"]
```

#
**Use a text editor & open up the config/routes.rb file and make the root of the application the todo list controller:**
```
root "todo_lists#index"
```