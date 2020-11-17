# Instauto
![tests](https://github.com/stanvanrooy/instauto/workflows/tests/badge.svg)
[![GitHub stars](https://img.shields.io/github/stars/stanvanrooy/instauto)](https://github.com/stanvanrooy/instauto/stargazers)
[![PyPI license](https://img.shields.io/pypi/l/instauto2)](https://pypi.python.org/project/instauto2/)
[![PyPI download month](https://img.shields.io/pypi/dw/instauto2)](https://pypi.org/project/instauto2/)
![coverage](https://github.com/stanvanrooy/instauto/blob/master/coverage.svg)


Instauto is a Python package for automating various parts of Instagram, making use of the private Instagram API.

Instauto is currently fairly limited, because it is under development. Progress can be tracked [here](https://github.com/stanvanrooy/instauto/projects/2).
Instauto in it's current state, should not be used for production systems.

For feature requests, ideas, comments, etc., please open an issue. 

## Installation
The package is still under development, but an alpha version has been published to PyPi. The package can be installed with the following pip command:
```pip install instauto2```

**Note:** due to a lost password, I temporarily lost access to my own PyPi account. Until that is resolved (see [pypi-support](https://github.com/pypa/pypi-support/issues/744)), `instauto` will be published to `instauto2` :).

## Usage
Here is a simple example that extracts all followers from an Instagram account: 

```python
from instauto.api.client import ApiClient
from instauto.api.actions import post as ps

if __name__ == '__main__':
    client = ApiClient("your_username", "your_password")
    client.login()
    
    like = ps.Like(
        media_id="1734612737423614055_6400760974"
    )
    client.post_like(like)
```
Other examples of how to use the package, can be found in the examples directory.

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)
