release_assets
=========

Downloads all assets for a tagged release from a given repository.


Role Variables
--------------

Available variables are listed below (All variables are required):

`github_auth_token:` A [Github Personal Access Token](https://docs.github.com/en/github/authenticating-to-github/creating-a-personal-access-token).

**Note**: Be sure not to include `github_auth_token` directly in your playbooks!  Use `ansible-vault` or another secure method of storage to inject it in at runtime!

`release_tag:` The tag of the release from which to download the assets.

`github_repo_name:` The name of the repository.

`github_repo_owner:` The user or organization that owns the repository.

`assets_path:` Path where the assets should be downloaded. Will download to  `~/` by default.

Example Playbook
----------------

**Note**: `github_auth_token` is provided here as an example only. As mentioned above, this should be stored securely in `ansible-vault` or another secure storage.

    - hosts: servers
      roles:
         - { role: unstablereality.release_assets,
             github_auth_token: "abcde12345",
             release_tag: "v1.2.3",
             github_repo_name: "my-first-repo",
             github_repo_owner: "unstablereality",
             assets_path: "~/my-first-project/assets/" }

License
-------

[MIT](https://github.com/unstablereality/ansible-role-release-assets/blob/master/LICENSE)

Author Information
------------------

This role was created in 2020 by [Daniel Soskel](https://danielsoskel.dev)
