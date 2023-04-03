# Testing with Django

Django test framework
- build on `unittest` library that comes out of the box with python
- Django adds a test client- dummy web browser
- Allows simulate authentication
- Has temp. database

Django REST framework
- API test client, specifcly use to test API

## Where to put tests:
- Each app has tests.py
- tests subdirectory can be use as well. This allows spliting tests into multiple modules
- Keep in mind:
    - You need to decicde wheter you want to have a tests.py or tests folder
    - Test modules must start with `test_`
    - Test dir must contain `__init__.py`