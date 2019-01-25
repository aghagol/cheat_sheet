Install `pycodestyle` (e.g. using pip).

Configuration file for `pycodestyle` can be put in home directory. e.g. put the following in `~/setup.cfg`

```
[bdist_wheel]
universal = 1

[metadata]
license_file = LICENSE

[pycodestyle]
max_line_length = 100
```
