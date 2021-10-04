# Puppet PDK Sync

PDK Sync is an efficient way to run a pdk update command against the various Puppet module repositories and is the successor of ModuleSync. This repository hold

In addition it can sync all the gihtub issue laabel defined in `labels.toml` to the repositories listet in `labeled_repos.yml`.

## Getting ready

Upon cloning this repo install the dependencies and clone all puppet modules listed in `managed_modules.yml`

    bundle install --path .bundle/gems/
    bundle exec rake git:clone_managed_modules

To verify the pdksync configuration (settings in pdksync.yml) run:

    bundle exec rake pdksync:show_config

To see the list of all available rake targets run `bundle exec rake -T`
