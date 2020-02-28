# Codeception Dumper

### Goals
- Should allow to export a SQL database into a dump SQL file
- Should be a Codeception command
- Should read database credentials from Codeception `Db` module
- Should write to the dump file specified in the `dump` parameter
- Should generate a dump for a given suite that has the `Db` module. See examples below.
- Should be extensible to provide methods that make it easier to export from specific frameworks
- The first extension will be for WordPress databases

### Nice to haves
- Minimize third party dependencies

### WordPress Dump Extension
- Possibly a decorator or similar from the Dump itself
- Adds helper methods such as: (WIP)

### Scenarios
- I'm developing a plugin. The database settings and even structure might change often. I want to be able to quickly generate updated dumps for my tests.
- I'm developing a website. (WIP)

### Examples
- codecept dump acceptance
