# join


Nombre de livre par auteur :

    mysql> SELECT name, COUNT(ab.book_id) FROM authors a LEFT JOIN authors_books ab ON (a.id = ab.author_id) GROUP BY a.id;
    +-----------------+-------------------+
    | name                | COUNT(ab.book_id)     |
    +-----------------+-------------------+
    | Dora Jimenez        |                 5     |
    | Isabella Cooper     |                 8     |
    | Molly Berg          |                 5     |
    | Abel Day            |                 5     |
    | Dai Beard           |                 5     |
    | Carissa Buck        |                 8     |
    | Justina Hull        |                 2     |
    | Avram Buckley       |                 4     |
    | Adria Banks         |                 4     |
    | Cara Bolton         |                 7     |
    | Shelley Ayers       |                 6     |
    | Hoyt Ruiz           |                 1     |
    | Karyn Ellison       |                 6     |
    | Ralph Petty         |                 3     |
    | Jason Sampson       |                 6     |
    | Iliana Pitts        |                 5     |
    | Quinn Cooke         |                 6     |
    | Lara Dixon          |                 5     |
    | Ella Mcknight       |                 6     |
    | Charissa Jacobs     |                 3     |
    +-----------------+-------------------+
    20 rows in set (0.00 sec)

Nombre de livre par auteur avec tous les titres: ?

    mysql> SELECT name, COUNT(ab.book_id), title FROM authors a LEFT JOIN authors_books ab ON (a.id = ab.author_id) RIGHT JOIN books b ON (ab.book_id = b.id) GROUP BY a.id;
    +-----------------+-------------------+---------------------------------------------------------------+
    | name            | COUNT(ab.book_id) | title                                                         |
    +-----------------+-------------------+---------------------------------------------------------------+
    | NULL            |                 0 | at risus.                                                     |
    | Dora Jimenez    |                 5 | eu tempor erat neque non quam. Pellentesque                   |
    | Isabella Cooper |                 8 | vestibulum. Mauris magna. Duis dignissim tempor arcu.         |
    | Molly Berg      |                 5 | Donec egestas. Aliquam nec enim.                              |
    | Abel Day        |                 5 | ullamcorper magna. Sed eu                                     |
    | Dai Beard       |                 5 | malesuada fringilla est.                                      |
    | Carissa Buck    |                 8 | vel sapien imperdiet                                          |
    | Justina Hull    |                 2 | ultricies ornare, elit elit fermentum risus,                  |
    | Avram Buckley   |                 4 | quis turpis vitae                                             |
    | Adria Banks     |                 4 | vestibulum. Mauris magna. Duis dignissim tempor arcu.         |
    | Cara Bolton     |                 7 | sodales. Mauris blandit enim consequat purus. Maecenas libero |
    | Shelley Ayers   |                 6 | lacus. Etiam bibendum fermentum metus.                        |
    | Hoyt Ruiz       |                 1 | ante. Nunc mauris sapien, cursus in,                          |
    | Karyn Ellison   |                 6 | gravida mauris ut                                             |
    | Ralph Petty     |                 3 | lacus. Etiam bibendum fermentum metus.                        |
    | Jason Sampson   |                 6 | convallis in, cursus et, eros.                                |
    | Iliana Pitts    |                 5 | eu tempor erat neque non quam. Pellentesque                   |
    | Quinn Cooke     |                 6 | non ante bibendum ullamcorper. Duis cursus, diam at           |
    | Lara Dixon      |                 5 | sodales. Mauris blandit enim consequat purus. Maecenas libero |
    | Ella Mcknight   |                 6 | non ante bibendum ullamcorper. Duis cursus, diam at           |
    | Charissa Jacobs |                 3 | iaculis quis, pede. Praesent                                  |
    +-----------------+-------------------+---------------------------------------------------------------+
    21 rows in set (0.00 sec)
