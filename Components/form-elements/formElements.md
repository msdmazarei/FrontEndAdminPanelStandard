# form elements

## CatodFormElement

all **catod form elements** should extends from [CatodFormElement](CatodFormElement.md)

### input

- textarea, number, ... pattern, ...

- it's a textfield

### rating

- it's list of stars(or other symbol) and each star assigned to incremental value, that can be selected.

### tag

- in tag element we can add custom tag and as many as we want (unless it has validation).

### lookup

- should pick from autocomplete and it's searchable (http request needed).

### dropdownList

- list of prepared "label, value" data. 

### datePicker

- able to select date and return timestamp value.

## other form element

### BtnLoader

btn get action and show loader (like ladda btn).

### grid

### notify with action

modal notify

show msg

take action (cancel or confirm)

### toast msg

### content-loader

form on submit loader, grid loader, ...

### other

accordion, dropdowns, modal, tabs

navbar(small media toggleOpen btn)

overlays(popovers, tooltips)
