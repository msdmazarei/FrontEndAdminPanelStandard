  # GRID COMPONENT
   Version 1.0.0

  ## Requirement
  Every Grid or List of data needs some items & actions & View

  ## PROPS
  Every Grid Component needs some props:  
  - dataRow: Array<T>
  - columnDef : Array <{title:string, icon: string, key: string, valueGetter:function, displayValue:function, sortable?:boolean>
  - actions ?: Array <{title:string, icon: string, actionFn : (Row)=>void}>
  -  message ?: string
  - onSort ?: a function for sort data
  - multiSort?: boolean
  
  ### dataRow: Array<T>
  dataRow for mapping is an array of objects which the type of that is recognised after add array to component, therefor we need  a generic type

  ### columnDef 
  columnDef is a props which define for every column:
  - title: the title of col
  - key : the unique key for every column
  - displayValue : a function which get the value from the valueGetter function for every col and return the display value
  - sortable?: is a boolean which allow onSort for this column. 

  ### actions 
  actions is an array of action which define for every action
  - title: the title for action
  - icon: the icon for action
  - actionFn: is a function for every row which get the row value and return void

  ### message
  this props is for costomize empty data row message.

  ### onSort
  there is a lot of senario for sorting data, however we introduce this senario which we need a permision for every column for sorting data and a function for adding event for evry sorting

  ### multiSort
   This is a boolean props which can allow for display multisort in cattod grid as icon 