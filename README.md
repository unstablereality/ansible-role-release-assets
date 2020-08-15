release_assets
=========

Downloads all assets for a tagged release from a given repository.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

Available variables are listed below (All variables are required):

`github_auth_token:` A [Github Personal Access Token](https://docs.github.com/en/github/authenticating-to-github/creating-a-personal-access-token).

`release_tag:` The tag of the release from which to download the assets.

`github_repo_name:` The name of the repository.

`github_repo_owner:` The user or organization that owns the repository.

`assets_path:` Path where the assets should be downloaded. Will download to  `~/` by default.


Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: unstablereality.release_assets,
             github_auth_token: "abcde12345",
             release_tag: "v0.21",
             github_repo_name: "my-first-repo",
             github_repo_owner: "unstablereality",
             assets_path: "~/my-first-project/assets/" }

License
-------

MIT

Author Information
------------------

This role was created in 2020 by [Daniel Soskel](danielsoskel.dev) 