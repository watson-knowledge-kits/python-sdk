# Watson Knowledge Kits

Python library for Watson Knowledge Kits (insert link here).

## Installation
Python 3.6 is required.

Install with either `pip` or `easy_install`:

`pip install knowledge_kits`

or

`easy_install knowledge_kits`

## Usage

Each kit has its own class with endpoints implemented as methods of the class. Here we use the `TravelKit` as an example:
```
from knowledge_kits import TravelKit


kit = TravelKit(api_key='YOUR_API_KEY', api_url='API_URL', instance_id='INSTANCE_ID')

# pass query parameters as keyword arguments
params = {
    'location': '37.7749,-122.4194',
    'category': 'landmarks'
}

data = kit.attractions(**params)
print(data)
```

## Development

Requirements can be installed into a virtual environment by running `tox -e
devenv`. Tox must be installed: `pip install tox`. When you setup your project
this way, changes to the code are automatically updated in the virtual
environment. To activate the virtual env, run `source venv/bin/activate`.

Create a new branch for your feature. Before pushing code, run `tox` to ensure
that all tests and linting passes.