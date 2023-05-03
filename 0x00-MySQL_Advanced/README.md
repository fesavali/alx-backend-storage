Indexing is a powerful structure in MySQL which can be leveraged to get the fastest response times from common queries. MySQL queries achieve efficiency by generating a smaller table, called an index, from a specified column or set of columns. These columns, called a key, can be used to enforce uniqueness. Below is a simple visualization of an example index using two columns as a key.

+------+----------+----------+
| ROW | COLUMN_1 | COLUMN_2 |
+------+----------+----------+
| 1 | data1 | data2 |
+------+----------+----------+
| 2 | data1 | data1 |
+------+----------+----------+
| 3 | data1 | data1 |
+------+----------+----------+
| 4 | data1 | data1 |
+------+----------+----------+
| 5 | data1 | data1 |
+------+----------+----------+

This analogy compares MySQL indexing to indexing in the back of a book.
Queries utilize indexes to identify and retrieve the targeted data, even if they are a combination of keys. Without an index, running that same query results in an inspection of every row for the needed data. Indexing produces a shortcut, with much faster query times on expansive tables. A textbooks analogy may provide another common way to visualize how indexes function.

When to Enable Indexing?
Indexing is only advantageous for huge tables with regularly accessed information. For instance, to continue with our textbook analogy, it makes little sense to index a children’s storybook with only a dozen pages. It's more efficient to simply read the book to find each occurrence of the word “turtle” than it would be to set up and maintain indexes, query for those indexes, and then review each page provided. In the computing world, those extra tasks surrounding indexing represent wasted resourc