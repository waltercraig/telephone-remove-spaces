# Telephone Remove Spaces
Remove ACF field spaces in Wordpress

PHP, ACF
```php
<?php 
  $telephone = get_field( 'telephone', 'option' ); 
  $telephone_nos = str_replace(' ', '', $telephone);    
?>
<a href="tel:<?php echo $telephone_nos; ?>"><?php echo $telephone; ?></a>
```

Or Javascript
```js
const telephoneRemoveSpaces = () => {
  const telephoneNumber = document.getElementsByClassName('tel-no');
  
  console.log(telephoneNumber);

  for(let x = 0; x < telephoneNumber.length; x++) {
    telephoneNumber[x].href = telephoneNumber[x].href.replace(/\s/g, '');
  }

}
telephoneRemoveSpaces();
```
