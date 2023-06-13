# freshteam-connector
An example of a new Sesam component - a connector - to the Freshteam HR system.


## Notes and caveats:

The Freshteam api is documented here: https://developers.freshteam.com/api


## How to test

If you want to develop on this connector using the sesam-py tool you need to add a couple of files:

### .syncconfig
This file specifies which sesam subscription to test the connector in.
NOTE: all the config and data of this subscription will get wiped, so make sure you use a development subscription with no important data on.

```
    NODE=https://datahub-65da8bb4.sesam.cloud/api
    JWT=ey...
```

### .authconfig
This file contains the secrets needed to talk to the Freshteam api.

```
    API_KEY=DeMX...
    BASE_URL=https://sesam.freshteam.com
```

### test-env.json
This file contains the configuration needed to talk to the Freshteam api.

```
    {
      "base_url": "https://sesam.freshteam.com",
      "node-env": "prod"
    }
```

The API_KEY is created in the Freshteams web GUI.

