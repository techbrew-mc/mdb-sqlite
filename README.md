mdb-sqlite
==========

Provides automated conversion of MS Access 2000 databases to SQLite on any platform, utilizing Jackcess and SQLite Java libraries. No native driver required.

MDB-SQLite is used by Plausible Labs to read government-supplied Access databases.

This repository was created to fork and maintain the original abandoned code on https://code.google.com/p/mdb-sqlite/

Usage
=====
To compile, run:

    mvn package

This will create a standalone jar in target/mdb-sqlite-{#}.one-jar.jar

To convert a database file:

    java -jar target/mdb-sqlite-{#}.one-jar.jar source.mdb output.sqlite

Changes
=======
1.0.3 Release
- Moved to Maven project structure on github
- Updated dependencies
- Patched for explicit Float/Double support per https://code.google.com/p/mdb-sqlite/issues/detail?id=11
- Logging output added per https://code.google.com/p/mdb-sqlite/issues/detail?id=11#c11

1.0.2 Release
- Prefix index names with the table names to prevent name conflicts when converting indixes.

1.0.1 Release
- Work-around around the SQLite JDBC drivers lack of support for boolean values ( Issue #2 )

- Add support for converting indexes ( Issue #3 )

1.0 Release
- Initial Release
