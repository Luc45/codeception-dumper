# Codeception Dumper

### Goals
- Should allow to export a SQL database into a dump SQL file
- Should be a Codeception command
- Should read database credentials from Codeception `Db` module
- Should support modules that extend `Db
- Should write to the dump file specified in the `dump` parameter
- Should generate a dump for a given suite that has the `Db` module. See examples below.
- Should be extensible to provide methods that make it easier to export from specific frameworks
- The first extension will be for WordPress databases
- Adds an optional "dump_rules" parameter to the `Db` module, which receives a string as parameter, that must match a file in the `_support` folder. This file must be a class that extends `Codeception_Dumper_Rules`.

### Codeception_Dumper_Rules
- This is where a developer would specify rules for the creation of his dump, like clearing data that he don't need
- This is also where the usage of framework-specific dump extensions such as the "WordPress Dump Extension" is possible

### WordPress Dump Extension
- Possibly a decorator or similar that extends a main class
- Adds helper methods such as: (WIP)

### Scenarios
- I'm developing a plugin. The database settings and even structure might change often. I want to be able to quickly generate updated dumps for my tests.
- I'm developing a website. (WIP)

### Examples
Command: `codecept dump acceptance`

Parses the `Codeception_Dump_Rules`, if one is specified, which might use an extension such as the `WordPress Dump Extension` to help create dump rules.

Proceed to generate the dump as defined. If no Dump Rules are provided, just make a copy of the database as a dump file.

### Nice to haves
- Minimize third party dependencies
