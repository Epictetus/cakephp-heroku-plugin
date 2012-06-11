# What is this?
This is CakePHP plugin for Heroku. You can run your app on Heroku environment with this plugin.

# How to use
Plugin source and config vars are required for using this plugin. if you already added shared-database addon, just skip that command.

	cd your_project
	git submodule add https://github.com/yandod/cakephp-heroku-plugin.git app/Plugin/Heroku
	touch app/Config/database.php
	heroku config:add salt=YOUR_SALT_HERE
	heroku config:add cipherSeed=YOUR_SEED_HERE
	heroku addons:add shared-database
	git add .
	git commit -m "add heroku plugin"
	git push heroku master

# Todo
- Schema migration.
- log availability from heroku log command.