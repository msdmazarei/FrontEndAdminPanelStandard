# URL

admin **CRUD** url should look like this:

## manage

```siteName/<entityName>/manage```

### nested manage

```siteName/<entityName>/manage/<parentEntityName>/<parentEntityId>```

## save

- **create** ```siteName/<entityName>/create```

- **update** ```siteName/<entityName>/update/<entityId>```

- **view** ```siteName/<entityName>/view/<entityId>```

> each page (route) need single or multiple [permission](/permission.md).
