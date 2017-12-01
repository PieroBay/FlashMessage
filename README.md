# FlashMessage

Your can create a flash message.
This message will be destroy after it will be viewed.

The namespace :

`use KintoUn\libs\FlashMessage;`

init the class
`$FlashMessage  = new FlashMessage();`

To create a message :
`$FlashMessage->setFlash('error', 'Bad request');`

The first parameter is the type of the message and the second argument is the content message.
It will create a Session 

```php
$_SESSION['flash'] = array(
  'type' => $type,
  'message' => $message,
);
``` 

To get the message, use :
`$FlashMessage->flash();`

Il will return a html :

```html
<div class="flash flash-error">Bad request</div>
``` 
