# BridgeQL


`bridgeql` is part of VMware's support of open source development
and community.

A library which will add feature to serve your model over rest API
* This will allow users to make ORM query based on any models present in the django app
* This will ask user to provide request in defined format and will serve the API response as json data
* This will allow users to make filter, selection, ordering, slicing and count of model objects


## License

`bridgeql` is release under the BSD-2 license, see the LICENSE file.

SPDX-License-Identifier: BSD-2-Clause

## Usage

The bridgeql library can be integrated to the Django app by editing settings
file by including `bridgeql` in the `settings.INSTALLED_APPS` variable.
Another change required is to add a url to your existing project as

```
    projectname/projectname/settings.py
```

```python

INSTALLED_APPS = [
    ...
    'bridgeql'
    ...
    ]

```

On your project you can edit `urls.py`, to include the `bridgeql` urls.

```python
from bridgeql import urls as bridgeql_urls
...

urlpatterns = [
    ...
    path('bridgeql/', include(bridgeql_urls)),
    ...
]
...
```

## Management Commands

`bridgeql` includes few management commands (`bridgeql` needs to be
added to the `INSTALLED_APPS` to add these commands):

* `python manage.py create_test_data`: for testing purpose we can create some test data


### Build & Run

1. make test
2. tox
3. python3 -m pip install --upgrade build
4. python3 -m build

## Documentation

## Contributing

The bridgeql project team welcomes contributions from the community. Before you start working with bridgeql, please
read our [Developer Certificate of Origin](https://cla.vmware.com/dco). All contributions to this repository must be
signed as described on that page. Your signature certifies that you wrote the patch or have the right to pass it on
as an open-source patch. For more detailed information, refer to [CONTRIBUTING.md](CONTRIBUTING.md).


## Authors

Created and maintained by Piyus Kumar <piyusk@vmware.com>

Copyright © 2023, VMware, Inc.  All rights reserved.
