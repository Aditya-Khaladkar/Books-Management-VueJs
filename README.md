# books-management

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

Book Information Page
List Books, Each book will have (id, book name, author name, number of pages,issued/available)
List Books table will show id, name, author name, page count, status, operations [edit,delete]
Above List you will have a form to Create/ Update Book.
Create form will have Add Book Button & update Book form will have Update Book button.Update Book will show status drop-down/ radio button, this controle will not be visible inCreate Book.
Add Book : will create new entry of the book in the table
Update Book: Will update the details of the book if any changed
In table operation column if you click on edit, then that book information should be shownin update book form automatically.
In table operation column if you click on delete, then book should get deteted from thetable.
When you load page first time it should have atleast 3 books in the list.
