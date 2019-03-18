# DBConTest
EFCore context auto tester and mocking framework

Goal:
Have an easy to setup tester that will run CRUDE tests on any EFCore context that you give to it.  It should be able through reflection or other methods find relationships and test those as well.

Tests should:
Create
Attempt to create with subsets
Create with children
Link children seperatley
Check for any missed attributes like length and not null
Read
Read fields seperatley
Read with all children
Try to lazy load
Eager load
Check for any SQL that is evaluated on the server
Update items
Update seperatley
Update single item
Update with children
Delete
Referential integrity
Delete by other lookups

*Do all of this in a transaction*

Second long term goal:
Create mocked database, possibly an in memory one or a file based one

Dream:
You can add this to your DB context to feed it anything that happens in it while it is running.  IE, add it to the DBContext and then let it run while you work on the frontend and it just adds anything that is processed.

Also possibly give it some type of easy to read csv or json based approach that will allow developers to just manually alter it if they want.  But make it a optimal compile once solution so that the tests are not slowed down.
