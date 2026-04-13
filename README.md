# Assignment 6 - Bookstore Part 1
Author: Yuchen Shi 
NetId: YS6132

## Description
This set of code creates a small bookstore database in SQLite and then uses Python to interact with it through a command-line interface.
In addition to the original files, I added some more rows in the book table and implemented a function 'view_read_now_books' to return the books marked as read now. 
Specifically, this bookstore focuses on music-related books, including biographies, instrument learning books, music theory texts, scores, and collections.

## Files

- `createTables.sql` - creates the tables
- `insertRows.sql` - inserts sample categories and books
- `bookstore_cli.py` - Python CRUD program
- `bookstore.db` - database file you will create by running the commands below

## Create the database

Run these commands in the terminal:

```bash
python3 - <<'PY'
import sqlite3
sqlite3.connect('bookstore.db').close()
PY
```

Then load the SQL files using SQLite in Python or DB Browser for SQLite.

If your environment has the `sqlite3` shell installed, you can run:

```bash
sqlite3 bookstore.db < createTables.sql
sqlite3 bookstore.db < insertRows.sql
```

## Run the Python CLI

```bash
python3 bookstore_cli.py
```

## Notes

- This code uses parameterized queries in Python.
- The `image` field stores the filename only.
- The actual images can be reused later in the Flask web app.
