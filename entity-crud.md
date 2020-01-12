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

## save

save refers to both create and update form.

save form must have form elements match all entitie's client property.

this form has action create or update depend on we create a record or update one (in create mode reset button is useful).

mainly save page permission is main action [permission](/permission.md):
   for example in create page page permission is ```<entity>-create```
   in update is ```<entity>-update```
   in view is ```<entity>-view```

> view page can be handled in save page only with view permission and no action (update or create).
