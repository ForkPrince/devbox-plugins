# MongoDB Plugin

Plugin for the [`couchdb3`](https://www.nixhub.io/packages/couchdb3) package. This plugin configures CouchDB to run on the same machine as Devbox.

## How to Activate

To install CouchDB, run `devbox add couchdb3@latest`.

To activate this plugin, add the following reference to the `include` section of your `devbox.json` file.

```json

"include": [
    "github:forkprince/devbox-plugins?dir=couchdb"
],
```

## Services

* couchdb

Use `devbox services up couchdb` to start the CouchDB server.

## Files

This plugin creates the following helper files:

* **devbox.d/couchdb/mongod.conf** - CouchDB configuration file
* **.devbox/virtenv/couchdb/data** - empty directory for holding your CouchDB database
* **.devbox/virtenv/couchdb/process-compose.yaml** - Defines the process to start the CouchDB server

## Environment Variables

This plugin sets the following environment variables:

* **ERL_FLAGS** = {{.DevboxDir}}/mongod.conf
