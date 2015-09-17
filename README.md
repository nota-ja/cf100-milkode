Milkode on Cloud Foundry (Proof of Concept)
====

Present status: NG.

## Usage

### Build Milkode Database

```
bundle install --path vendor/bundle
export export MILKODE_DEFAULT_DIR=${PWD}/.milkode
bundle exec milk init
bundle exec milk add <FILE_PATH_OR_REPOSITORY_URL>
```

### Deploy to Cloud Foundry

```
cf push milk -c 'bundle exec milk web -o $VCAP_APP_HOST -p $VCAP_APP_PORT --no-browser'
```

Note: You may need to specify additional options.
