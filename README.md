# TestRail Python Library

This Python Library allows you to easily publish results and manage your TestRail instance.  

### Warning
This library is still in an alpha release.  This means little to no testing and future releases may break compatibility.  Please evaluate and report bugs/enhancements.

## Quick Start
```python
from testrail import TestRail

testrail = TestRail(project_id=1)
milestone = testrail.milestone('rel-2.3')
milestone.is_completed = True
testrail.update(milestone)
```

#### Configuration
Create '.testrail.conf' in your home directory with the following:
```
testrail:
    user_email: 'your email address'
    user_pass: 'your API key or password'
    url: 'domain for TestRail instance'
```

## Installation
The easiest and recommended way to install testrail is through [pip](https://pip.pypa.io):
```
$ pip install testrail
```

This will handle the client itself as well as any requirements.

## Usage
Full documentation will hopefully be available soon.  In the mean time, skimming over client.py should give you a good idea of how things work.

**Important:** For performance reasons, response content is cached for 30 seconds.  This can be adjusted by changing the timeout in api.py.  Setting it to zero is not recommended and will probably annoy you to no end!
