# How to set up this project in local 

### If you are not using the database shared by me run the following commands
 - `git clone <repo>`
 - `ddev start`
 - `ddev composer install`
 - `ddev drush site:install -y`
 - `ddev drush config:set system.site uuid 09aa893d-74c2-47d3-9aa2-e1f81313a6e6 -y`
 - `ddev drush entity:delete shortcut`
 - `ddev drush entity:delete shortcut_set default`
 - `ddev drush cim -y && ddev drush cr`
 - `ddev drush uli`

### If you have the databse just
 - `git clone <repo>`
 - `ddev start`
 - `ddev composer install`
 - Please put the db in base project folder `ddev import-db --src db_dump.sql`
 - `ddev drush uli`


## Thanks for continue with the training now we are going to start the part 2, git PR's and drupal files revisions.

### Steps to submit changes of git
 - run `ddev drush cex` This command should be export your current local configuration to ./config directory.
 - Create a branch `git checkout -b [branch-name]` with some speciication of your work like feat-create-human-content-type.
 - Add your work in your branch with `git add -p`, with this command you can review your changes before you send to stash. Then run `git commit -m [messages]` try to set a short description in your messages like "feat: create a human content type to pop-human site"
 - Push you changes with `git push origin [branch-name]`, please make sure you have access to push into repository, ask me for this!
 - Create a Pull Request and compare with *Develop* and try to fill the steps of the Pull Request template.
 - We are going to have a activity like code reviewers and make sure the work made by for other groups it's fine and complete.

### Steps to get changes of git
 - First you need to fetch the branch that you want to review `git fetch`
 - Then `git checkout [branch-name]`, please make sure the branch is up to date with `git pull` or `git pull origin [branch-name]`.
 - After this you need to run `ddev drush cim`, this command should be import the current files in ./config directory to your project.
 - When the config was imported without errors, you need to follow the Pull Request Intructions of the other group to review the work.
 - At this point we're QA so try to be fussy with the review.
 - We are going to replicate a real work enviroment so I will give you some standards to considerer when you make the revision.


## Happy code review!
