# pylogger_unified

A python wrapper that handles web logging, standard application logging to different format: json (gelf), colored text, raw, gnome notifications

## Build manually (testing env for the moment)

Install testing envrionment here: <https://packaging.python.org/en/latest/tutorials/packaging-projects/>.

```bash
cd pylogger-unified/
rm ./dist/* -fr
python3 -m build
python3 -m twine upload --repository testpypi ./dist/*
```

You can test in a dev environment the packaging:

```bash
pip3 install -i https://test.pypi.org/simple/ pylogger_unified
```

When everything is ok on testpypi repo, you can publish it to prod:

```bash
python3 -m twine upload ./dist/*
```

## Install the lib

```bash
pip3 install pylogger-unified
```

## Start Using the lib

```python3
from pylogger_unified import logger as pylogger_unified
logger=pylogger_unified.init_logger()
logger.info("this is a test")
```
