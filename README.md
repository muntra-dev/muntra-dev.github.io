Muntra react widget

# Placing a widget on a page

First, place the <div> tag in the site markup, with the following attributes:
  
  Required attributes:
  
  - `class`: "muntra-widget",
  - `key`: "id" (This is a unique id for each widget. If you place more than one widget, then you should assign them the corresponding unique id, for example, 0,1,2 ...),
  - `muntra_clinic_id`: "clinic_id" (Id of the clinic from which you'd like to get caregivers).
  
  Optional attributes: 
  
  - `muntra_caregiver_id`: "caregiver_id" (If you want to get only a specific caregiver for this clinic, then enter the caregiver id here),
  - `muntra_role_id`: "role_id" (Use it to filter out caregivers by role),
  - `muntra_procedure_id`: "procedure_id" (Use it to assign a default procedure),
  - `muntra_referral_source`: "referral_source" (Use if you want your booking to be made using a referral source),
  - `muntra_button_text`: "Booking button" (Use it to change the button text. The default button text is "Boka tid"),
  - `muntra_without_modal`: "true" (Use it to display a widget without a button and outside the modal window),
  
  Example: 
  
  ````
  <div class="muntra-widget" key="0" muntra_clinic_id="16" muntra_caregiver_id="2" muntra_referral_source="referral-link.se">
  ````
  
  Secondly, place a tag:
  ````
  <script type = "text/javascript" src = "https://muntra-dev.github.io/index.js"> </script>
  ````
  At the end of the body, to connect the widget to the page.
  
Expample of connecting widget to a page:

````
<body>
  <div class="auto-margin">
    <div class="flex-column right-align">
      <h2>Alla behandlare</h2>
      <div class="muntra-widget primary" key='1' muntra_clinic_id="16" muntra_referral_source="referral-link.se">
      </div>
    </div>
  </div>

  <script type="text/javascript" src="https://muntra-dev.github.io/index.js"></script>
</body>
````

# Styling a button
 
Styling "muntra-widget-button" class:
 
````
.muntra-widget-button {
   border-radius: 100px;
   color: #ffffff;
   font-size: 18px;
   font-weight: 700;
   line-height: 1.7em;
}
````

To style only certain buttons, use additional classes:

````
.secondary .muntra-widget-button {
    background-color: #fff;
    border-color: #52a8ff;
    color: #52a8ff;
}
````

# Styling a widget window

Styling "muntra-widget" class:
````
.muntra-widget {
  width: 100%;
  max-width: 720px;
  height: 500px;
  border: 1px solid lightgrey;
  border-radius: 15px;
}
````

To style only a specific widget, use additional classes:
````
.muntra-widget.without-modal {
  width: 100%;
  max-width: 720px;
  height: 500px;
  border: 1px solid lightgrey;
  border-radius: 15px;
}
````
