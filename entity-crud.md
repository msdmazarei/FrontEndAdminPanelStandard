# ENTITY CRUD

entity crud contain two main section with specific [url](/url.md) and [permissions](/permission.md):

1. **manage**
2. **save**

## manage

manage must have **grid** and **search**

- grid
  - pagination
  - sort
  - filter (optional)
  - actions
    - view
    - update
    - delete
- search
  - all entities searchable fields
  > each *search field type* matches that entites field and it can has it's own filter structure.
  > all filter should **AND** together as they send in a request.

manage must have a link to goto that entity create form, this can be done with:

- button (link)
- FLA (float action button)

## save (*not complete*)
