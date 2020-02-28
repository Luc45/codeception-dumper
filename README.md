# Codeception Dumper

### Goals
- Should allow to export a SQL database into a dump SQL file
- Should be a Codeception command
- Should have special methods for WordPress databases
- Should read database credentials from Codeception Db module
- Should generate the dump for a given suite, outputting to the given SQL dump file that the suite specifies

### Nice to haves
- Minimize third party dependencies

### Special methods for WordPress Databases
WIP

### Scenarios
- I'm developing a plugin. The database settings and even structure might change often. I want to be able to quickly generate updated dumps for my tests.
- I'm developing a website.
