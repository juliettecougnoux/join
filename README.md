# join

 >
mysql> SELECT name, COUNT(ab.book_id) FROM authors a LEFT JOIN authors_books ab ON (a.id = ab.author_id) GROUP BY a.id;
+-----------------+-------------------+
| name            | COUNT(ab.book_id) |
+-----------------+-------------------+
| Dora Jimenez    |                 5 |
| Isabella Cooper |                 8 |
| Molly Berg      |                 5 |
| Abel Day        |                 5 |
| Dai Beard       |                 5 |
| Carissa Buck    |                 8 |
| Justina Hull    |                 2 |
| Avram Buckley   |                 4 |
| Adria Banks     |                 4 |
| Cara Bolton     |                 7 |
| Shelley Ayers   |                 6 |
| Hoyt Ruiz       |                 1 |
| Karyn Ellison   |                 6 |
| Ralph Petty     |                 3 |
| Jason Sampson   |                 6 |
| Iliana Pitts    |                 5 |
| Quinn Cooke     |                 6 |
| Lara Dixon      |                 5 |
| Ella Mcknight   |                 6 |
| Charissa Jacobs |                 3 |
+-----------------+-------------------+
20 rows in set (0.00 sec)
