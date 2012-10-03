jquery-ujs-extended
===================

Extend usage of html5 data attributes of the jquery UJS gem in the context of Ajax calls.

#Work in Progress

These attributes need to be used in conjunction with the data-remote attribute that will be listened by the standard jquery-ujs library.

##Goals
Provide :
###Ajax
* data-ajax-update listener that automatically updates the DOM element
* data-ajax-delete listener that automatically deletes the DOM element
* data-ajax-append listener that automatically appends to the DOM element
* data-ajax-loader. Takes a DOM element. Will show the DOM element before sending the request, and hide it when the request is completed. This is best used to show a spinner image during a request.
* data-ajax-redirect. Takes a url. Redirects to the url on ajax success.
* data-ajax-input-url. Applies to form inputs. Calls the url whenever the field has changed. Compatible with data-method and all the above.

For all the above, DOM elements should be passed like this :
* ID : `data: {ajax: {update: 'dom_id'}}` or `data: {ajax: {update: '#dom_id'}}` or `data: {ajax: {update: :dom_id}}`
* Class : `data: {ajax: {update: '.dom_class'}}`

###Behaviour
* data-integer. If specified and applied to a text field, will prevent the field from being anything but an integer.Optional value: minimum value.
* data-float. If specified and applied to a text field, will prevent the field from being anything but a float.Optional value: minimum value.

