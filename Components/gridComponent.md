  # GRID COMPONENT
   Version 1.0.0

  ## Requirement
  Every Grid or List of data needs some items & actions & View

  ## PROPS
  Every Grid Component needs some props:  
  - dataRow: Array<T>
  - columnDef : Array <{title:string, icon: string, key: string, valueGetter:function, displayValue:function}>
  - actions : Array <{title:string, icon: string, actionFn : (Row)=>void}>
  
  ### dataRow: Array<T>
  dataRow for mapping is an array of objects which the type of that is recognised after add array to component, therefor we need  a generic type

  ### columnDef 
  columnDef is a props which define for every column:
  - title: the title of col
  - icon : the icon of col
  - key : the unique key for every column
  - valueGetter: a function which get row value and return the value that is need for this col
  - displayValue : a function which get the value from the valueGetter function for every col and return the display value

  ### actions 
  actions is an array of action which define for every action
  - title: the title for action
  - icon: the icon for action
  - actionFn: is a function for every row which get the row value and return void
