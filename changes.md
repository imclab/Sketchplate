#Changes

##v0.1.7
-	bugfix `--server` hook now correctly responds with `404` status code when requesting
nonexistent resources.
-	minor corrections and improvements in readme

##v0.1.6
-	added `defaults/fetch.json` installation routine for new users and pre v0.1.6 users
-	bugfix `hooks` on `sketchplate template` not calling `process.exit()`

##v0.1.5
-	bugfix [default editor string](https://github.com/hapticdata/Sketchplate/pull/2)
-	added `sketchplate fetch` for automating resource retrieval in existing projects
-	made `hooks` consistent in all contexts ( such as between `sketchplate new`, `sketchplate template add`, `sketchplate hooks`)

##v0.1.4
-	added `sketchplate hooks` to allow for all of the creation hooks to be used on existing projects
-	added `initServer` hook to start a node.js + connect static file server for a project'
-	added all of the creation hooks to template creation and editing
-	bugfix `sketchplate template add`
-	merge pull request #1 to always provide options to wrench

##v0.1.3
-	added `lib/config.js` for managing configurations and easy-access to the users config file
-	editor configurations for launching vim, webstorm

##v0.1.2
-	`~/.sketchplate` folder for holding config and templates on a user-level
-	`sketchplate config restore` for restoring user config to defaults
-	`sketchplate config` and option `-e` fixed for editing config.json
-	added `colors` package

##v0.1.1
-	quick fix for config path not being correct after user setting it

##v0.1.0
-	multipe dual-level commands now complete, v0.1.0 api ready
-	`config.templateDirectory` is now `config.templatesPath`
-	"url" fetches are now referred to as "file" fetches
-	asks user to edit config when editor does not appear to be setup correctly
-	`sketchplate fetch jquery async three` fetch individual resources for a template by name
-	`sketchplate fetch -i` for fetching resources with interactive mode
-	`sketchplate template --new` for creating a new template
-	support for fetching zip archives
-	support for multiple targets with a fetched resource
-	properly checking for multiple targets
-	allowing errors to bubble up `bin/sketchplate` instead of throwing errors earlier
-	collecting and reporting of errors for failed git, zip or file fetches

##v0.0.4
-	started change log :)
-	updated readme
-	resolved issues where path to templates folder was incorrect
-	`lib/fetch.js` now cleans up after git repos that happen to fail during clone (such as if connection drops)
-	altered templates structure
-	added `--npminstall` to `sketchplate new`
-	added `--browse` to `sketchplate new`
-	added `mkdirp` for creating nested directories in fetch targets
-	throws an understandable error when trying to use a non-existant template