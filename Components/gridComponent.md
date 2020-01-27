  # GRID COMPONENT
   Version 1.0.0

  ## Requirement
  Every Grid or List of data needs some items & actions & View

  ## PROPS
  Every Grid Component needs some props:  
  - dataRow: Array<T>
  - colDef : Array <{title:string, icon: string, valueGetter:function, displayValue:function}>
  - cctions : Array <{title:string, icon: string, actionFn : (Row)=>void}>
  - footer : componentFooter
  - rowNumber : number
  
  ### Data: Array<T>
  Data for mapping is an array of objects which the type of that is recognised after add array to component, therefor we need  a generic type

  ### ColDef 
  colDef is a props which define for every column:
  - title: the title of col
  - icon : the icon of col
  - valueGetter: a function which get row value and return the value that is need for this col
  - displayValue : a function which get the value from the valueGetter function for every col and return the display value

  ### Actions 
  Actions is an array of action which define for every action
  - title: the title for action
  - icon: the icon for action
  - actionFn: is a function for every row which get the row value and return void

  ### Footer
  is a component for grid footer which has following props:
  - onNextPage function for pagination
  - onPrewPage function for paginamtion

  ### RowNumber
  RowNumber is recognised for number of row for every page