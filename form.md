#Forms
All attributes mentioned below, should be passed to components as **props**.  
All Items cross referenced between mdn and w3c specs.

##Form Tag
Each From tag has some explicit *attributes* which should be defined on creation stage.

#### Mandatory Attributes
* id
    * The name of the form. 
* novalidate
    * Indicates that the form shouldn't be validated when submitted. 

#### Optional Attributs
* action
    * The URL that processes the form submission.
* name
    Deprecated as of HTML 4 (use id instead). Can be useful in some cases.
* class
    * Using **class** is not mandatory, this only used for some Styling purposes.
* autocapitalize
    * A nonstandard attribute used by iOS Safari that controls how textual form elements should be automatically capitalized. **autocapitalize** attributes on a form elements override it on **Form**.
* accept-charset
    * Space-separated character encodings the server accepts. The browser uses them in the order in which they are listed. The default value means the same encoding as the page.
* autocomplete
    * Indicates whether input elements can by default have their values automatically completed by the browser. autocomplete attributes on form elements override it on **form**.
* enctype
    * If the value of the method attribute is post, enctype is the **MIME** type of the form submission.
* ‌method
    * The HTTP method to submit the form with.
* target
    * Indicates where to display the response after submitting the form.
 
 
 
##Form Elements
Form Elements are components which we create to mimic pure/real html form elements with more functionality.

###Input
**Input** component will create an input with type **text**. Based on given type, functionality and validation may defer.
####Mandatory Attributes
* id
* type
    * defines functionality of the component, this will have direct impact on what would be rendered by component. Some of the types like number will render an input type text with validation for number, some other will only return their expected input type, like password so we can use native functionality specially on mobile devices.
        * data
        * datetime-local
        * email
        * hidden
        * month
        * number
        * password
        * search
        * tel
        * text
        * time
        * url
        * week
* autocomplete
    * Hint for form autofill feature
* autofocus
    * Automatically focus the form control when the page is loaded
* disabled
* name
    * Name of the input form control. Submitted with the form as part of a name/value pair.
* pattern(for password, text. tel)
    * Pattern the **value** must match to be valid
* palceholder(password, search, tel, text, url)
* readonly
* required
*  step(numeric types)
* tabindex
* title
* type
* value

####Optional Attributes
* class
* dirname 
    * Name of form field to use for sending the element's directionality in form submission
* form
* inputmode
    * Hint for selecting an input modality, such as the number keypad on dynamic keyboards.
* list
* max
* maxlength
* min
* minlength
* multiple(for email type)
* size(email, password, tel, text	)

###File-Input
####Mandatory Attributes  
* id
* accept

####Optional Attributes  
* class
* multiple
* capture

###selects
####Mandatory Attributes  
* disabled
* name
* required

####Optional Attributes
* autocomplete
* autofocus
* form
* multiple
* size
 
  

###Textarea
####Mandatory Attributes
* id 
* name
* disabled
* name 
* readonly
* required

####Optional Attributes  
* class
* autocomplete
* autofocus
* cols
* form
* maxlength
* minlength
* placeholder
* rows
* spellcheck
* wrap

###Radio and Checkbox
####Mandatory Attributes
* id
* checked
* value
* name
* required
* disabled

####Optional Attributes  
* class

###Range Slider
####Mandatory Attributes  
* id
* name

####Optional Attributes  
* class
* step
* min
* max
* list

###Date-Time Picker
####Mandatory Attributes  
####Optional Attributes
