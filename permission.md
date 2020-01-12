# permission

all **actions**, **api** page (route) need one or more permission to be shown or enable.

permission has structure like this:

- ```<entity>-create```
- ```<entity>-retrieve```
- ```<entity>-update```
- ```<entity>-delete```

these are base crud permission per entity.

## check page permission

on page loading (component initing (mounting)):

- check page permission(s)
  - if not authorized: redirect to home (dahborad) and show no access [message](/message.md#UI).
- in link action, link (page or route) permission will be checked.

## check action permission

- in data grid **actions section** if user doesn't have a specific action, that action should not be visible.
  - if in some case **action visibility** is important it should be disable.

- in form
  - form's all buttons and link visibility depending on it's own permission(s).
