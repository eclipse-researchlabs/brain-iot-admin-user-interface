# Admin User Interface

Provides a view of Smart Behaviours in marketplace and allows them to be installed/uninstalled.

## Implementation

The Brain-IoT Admin UI provides a REST server for an embedded Javascript UI by extending the Paremus UI server: https://github.com/paremus/ui_server.

It implements REST endpoints that link into the event-bus for:

* Behaviours
* Events
* Fabrics
* Hosts

The Javascript UI is unchanged from https://github.com/paremus/js_client.

## Testing

The app.test sub-project allows stand-alone testing of the UI. By default, `app.bndrun` is configured to use the security-light-marketplace:

```
# marketplace index for BMS
# (assumes marketplace is checked out next to this project)
mktplIndexes=file://${.}/../../marketplace/security-light-marketplace/target/marketplace/index.xml
```

To launch standalone UI:

```
bnd run app.test/app.bndrun
```

Now browse to http://localhost:8081 and login as admin (password: admin)



## end