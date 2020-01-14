  # GRID COMPONENT

  ## Requirement
  Every Grid or List of data needs some items & actions

   ### Data
- Array of Data

   ### Actions
    - update
    - delete
    - create
    - filter (optional)
    - rating row(optional)

   ### View
    - pagination
    - sort
    - hidden or show culomn
    - select row
    - select all rows
    - theme(optional)


  ## SERVER
  - An Array Of data for Listing
  - An API for SEARCH in list(optional)
  - An API for Filter in list(optional)
  - An API for add new item to list(optional)
  - An API for delete an item from list(optional)
  - An API for edit an item of list(optional)
  - An API for pagination list 0r scrolling(optional)

  ## PROPS
  Every Grid Component needs some props:  
  - sort({sort:boolean, sortItem: Array of sortItem})
  - filter ({filter:boolean, filterItems:Array of itemFilter})
  - search ({search:boolean, methodForSearch})
  - viewCulomn (boolean)(optional)
  - select row 
  - select all rows
  - update(methodForEdit)
  - delete(methodForDelete)
  - create(methodForadd)
  - theme(optional)
  - rating row(boolean)
  