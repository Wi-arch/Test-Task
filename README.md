### CRUD operations on Books

#### Create a Book model:
* name
* author


#### Create a Author model:
* name

#### POST /api/books

```json
{
  "name": "Book Name",
  "author": {
    "name": "Author Name"
  }
}
```

#### Validation/Result
* If the book name is present in the database returns `BAD_REQUEST`
* If author not exist returns `BAD_REQUEST`
* If author name or book name blank returns `BAD_REQUEST`



#### GET /api/books/1234

#### Validation/Result

* The client is not present in the database returns `NOT_FOUND`
* If the client is present the returns `OK` with

```json
{
  "id": 1,
  "name": "Book Name",
  "author": {
    "name": "Author Name"
  }
}
```
