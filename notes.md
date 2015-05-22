- Use cli to create records.
- Walk through the code for add
- `test_cli_classic.py` Resolve test case.
- `test_ut_cli.py`, ResolveUnitTestCase (unittest), TestMain, capsys for stdout
- Look into validator code
- `test_ut_validations.py`, `TestBaseValidator, TestAddValidator`
- `test_ut_prompt`, test for LamdaType
- `test_ut_ui`, TestDisplayField, pytest.fixture
- `test_ut_views` test_recursively_validate, mock ui.get, DummyValidator
- test_fetch_gravatar_and_store, `StubGravatar`, `FakeResponse`, `fake_get`, mock.patch, mock.patch.object, mock.patch context manager
- `test_ut_filestore`, test_store_image, refactor time.time to use datetime
- `test_it_db`, create_test_db, destroy_test_db, TestAdd(unittest), add_records (fixture), test_all, TestOne
