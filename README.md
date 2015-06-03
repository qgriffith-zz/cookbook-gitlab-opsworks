## NOTE
This repository is no longer maintained and is deprecated.


This repository stores all the dependency cookbooks of the GitLab cookbook as required by AWS OpsWorks

#### Usage

* Create a custom stack
* Select the `Advanced` dropdown
* Set `Use custom chef coobooks` to Yes
* Under `Repository URL` supply the url to this repository: `https://gitlab.com/gitlab-com/cookbook-gitlab-opsworks.git` (no SSH key or branch/revision needed)
* Under `Custom Chef JSON` supply the JSON of the custom setting for your instance. You can find example in the [cookbook repository](https://gitlab.com/gitlab-org/cookbook-gitlab/blob/master/doc/production.md)
* Save the stack by pressing `Add Stack`
* Go to `Layers` and select `Add layer`
* Under `Layer type` select custom and save
* Select `edit` of newly created layer
* In `Custom Chef Recipes` section
* Under `Setup` write `gitlab::setup` and press the + sign to add
* Under `Deploy` write `gitlab::deploy` and press the + sign to add
* Save changes made to the layer (Scroll to the bottom of the page for the Save button)
* Go to Instances
* Create a new instance (we recommand a c3.large) and add the previously edited layer