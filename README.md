# UTFT
Writing Unit tests and Functional Testing in Python

#### About Me

This is a command line interface for phonebook. From command line you will be
able to add new entry to phonebook, edit existing entry, view and delete. Yes, you can
also search for existing entries. That's about the application.

#### What you'll learn ?

As the name suggests, we'll learn how to write unit tests, functional tests in Python.
We will be using standard library unit test module, py.test, mock etc ...

We will learn how to assert basic types, objects, fixtures, mocking etc ...

Also writing tests will help you organize your code better.


#### How to read the source

The main entry for the program in `cli.py`, start jumping to the code from there on.

- `cli.py` - Handles initial invocation of the program and resolves the action, calls the function.
- `views.py` - Entry point for all actions.
- `validations.py` - All valdiation for user input and custom app validation.
- `ui.py` - All user handling input/displaying errors.
- `db.py` - SQLITE3 connection + all db operations.
- `prompt.py` - Cool way to get prompt depending on environment.
- `service.py` - Gravatar external service calls.
- `file_store.py` - Store image to the local file system.

All unit tests start with `test_ut_` and integration tests startwith `test_it_`.
All tests can be found in `test` branch.

#### Demo

```shell
(utft)➜  UTFT git:(master) ✗ cat phonebook.sql| sqlite3 phonebook.db
(utft)➜  UTFT git:(master) ✗ python cli.py
python cli.py ['add|display_one|display_all']
(utft)➜  UTFT git:(master) ✗ python cli.py add
Phone:89
First Name:Kracekumar
Last Name:Ramaraju
Email:me@kracekumar.com
Record added
(utft)➜  UTFT git:(master) ✗ python cli.py display_all
################################################################################
Id: 1
First Name: Kracekumar
Last Name: Ramaraju
Email: me@kracekumar.com
Thumbnail Path: /Users/krace/code/UTFT/2015-05-2322:32:30214588.jpeg
Phone: 89
################################################################################
(utft)➜  UTFT git:(master) ✗ python cli.py display_one
Id:1
################################################################################
Id: 1
First Name: Kracekumar
Last Name: Ramaraju
Email: me@kracekumar.com
Thumbnail Path: /Users/krace/code/UTFT/2015-05-2322:32:30214588.jpeg
Phone: 89
################################################################################
(utft)➜  UTFT git:(master) ✗ python cli.py display_one
Id:2
Record not found
(utft)➜  UTFT git:(master) ✗ python cli.py add
Phone:
First Name:
Last Name:
Email:
################################################################################
phone:['Value is missing']
first_name:['Value is missing']
################################################################################
Phone:4590
First Name:
################################################################################
first_name:['Value is missing']
################################################################################
First Name:Haris
Record added
(utft)➜  UTFT git:(master) ✗ python cli.py display_all
################################################################################
Id: 1
First Name: Kracekumar
Last Name: Ramaraju
Email: me@kracekumar.com
Thumbnail Path: /Users/krace/code/UTFT/2015-05-2322:32:30214588.jpeg
Phone: 89
################################################################################
Id: 2
First Name: Haris
Last Name:
Email:
Thumbnail Path: None
Phone: 4590
################################################################################
(utft)➜  UTFT git:(master) ✗
```

#### Concepts covered

- How to use unittest module
- How to use py.test and why py.test
- Writing simple functions as testcases
- Using different py.test command line features
- Capturing stdout with py.test
- Setting fixtures with py.test
- Writing Test classes which py.test can pick
- Using pytest.fixture
- Running specific test module/class/function etc ...
- Writing setup and teardown in pytest style
- How to mock expensive resources like network call, System Call.
- Patching modules/functions/classes.
- How to use Stubs/Fakes.

