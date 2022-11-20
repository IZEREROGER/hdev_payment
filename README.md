
# HDEV PAYMENT GATEWAY

### HADEV PAYMENT. MIT license.

Use from a PHP script:


# INitiate payment
-- TEl : is a telephone with amount of money on momo
-- amount : is amount to pay
-- transaction_ref : is id of payment on your system
-- Calback : is a link that is hosted online where we can update that payment is done

```php
include 'pay_parse.php';

//REQUEST PAYMENT 

hdev_payment::api_id("Your Api ID");
hdev_payment::api_key("Your Api Key");
$pay = hdev_payment::pay($tel,$amount,$transaction_ref,$calback);

var_dump($pay);//to get payment server response
```

# Query Transaction 
```php
include 'pay_parse.php';

//REQUEST PAYMENT 

hdev_payment::api_id("Your Api ID");
hdev_payment::api_key("Your Api Key");
$result = hdev_payment::get_pay($tx_ref);

var_dump($result);//to get payment server response
```

*All of our response are objects for example to access the tx_ref in response you use
```php
	$transction_ref = $result->tx_ref;
```
