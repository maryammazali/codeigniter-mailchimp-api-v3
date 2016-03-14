# CodeIgniter Mailchimp API v3 REST Client
A simple REST client for CodeIngniter for interacting with v3 of the MailChimp API.

## Requirements
1. CodeIgniter 3.0+

## Installation
Drag and drop the **application/libraries/Mailchimp.php** and **application/config/mailchimp.php** files into your application's directories.

Enter your API key in the **application/config/mailchimp.php** config file

## Making a Request
Making a request is simple. You can make a request to any of the endpoints supported by v3 of the MailChimp API. Simply pass the request type (GET,POST,PATCH,DELETE) and the Endpoint to the **call** function.

For example, to GET a list of your campaigns:

```php
$campaigns 	= $this->mailchimp->call('GET', 'campaigns');
```

## Passing API Key Manually
You can pass your API key directly when initializing the library. This is useful if you are working with multiple MailChimp accounts.

```php
$config['api_key'] = '<your-key>';
$this->load->library('mailchimp', $config);
```
