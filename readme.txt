=== btcpay-for-woocommerce ===
Contributors: btcpay, esky33, handymanJH
Donate link:https://main2-btc-ltc.forkbitpay.ninja/
Tags: bitcoin, payments, btcpay, cryptocurrency, payment
Requires at least: 4.3.1
Tested up to: 4.9.5
Requires PHP: 5.5
Stable tag: 2.2.24
License: MIT License (MIT)
License URI: https://opensource.org/licenses/MIT

BTCPay allows you to accept bitcoin payments on your WooCommerce store.

== Description ==

Use btcpay's plugin to accept Bitcoin payments from customers anywhere on earth.

Key features:

    Support all bitcoin wallets that support payment protocol
    Price in your local currency, let customers pay with bitcoin
    Have an overview of all your bitcoin payments in your btcpay merchant dashboard
    Refund your customers in bitcoin in your btcpay merchant dashboard

== Installation ==
This plugin requires Woocommerce. Please make sure you have Woocommerce installed.

    Get started by signing up for a [btcpay merchant account](https://btcpay-server-testnet.azurewebsites.net/Account/Register).
    Download the latest version of the btcpay plugin from the Wordpress site.
    Install the latest version of the btcpay plugin for Woocommerce:
        Navigate to your WordPress Admin Panel and select Plugins > Add New > Upload Plugin.
        Select the downloaded plugin and click "Install Now".
        Select "Activate Plugin" to complete installation.

For a video tutorial of installation and setup, go [here](https://www.youtube.com/watch?v=tTH3nLoyTcw)

== Connecting btcpay and Woocommerce ==
After you have installed the btcpay plugin, you can configure the plugin:

    Create a btcpay pairing code in your btcpay merchant dashboard:
        Login to your btcpay merchant account and select Payment Tools -> Manage API Tokens -> Add New Token -> Add Token
        Copy the 7 character pairing code
    Log in to your WordPress admin panel and select "Plugins" -> "Settings" link for the btcpay plugin.
        Paste the 7 character pairing code into the "Pairing Code" field in your btcpay plugin and click "Find"
        Click "Save changes" at the bottom

Pairing codes need to be used once and are only valid for 24 hours. If a code expires before you get to use it, you can always create a new one and pair with it.

Nice work! Your customers will now be able to check out with bitcoin on your WordPress site.

== Frequently Asked Questions ==

= How do I pay a btcpay invoice? =
You can pay a btcpay invoice with a Bitcoin wallet. You can either scan the QR code or copy/paste the payment link in your Bitcoin wallet.


= Does btcpay have a test environment? =
btcpay allows you to create a test merchant account and a testnet Bitcoin wallet.

More information about the test environment can be found [here](https://github.com/btcpayserver/btcpayserver-doc/blob/master/Getting-Started.md).

= The btcpay plugin does not work =
If btcpay invoices are not created, please check the following:

    The minimum invoice amount is USD 5. Please make sure you are trying to create a btcpay invoice for USD 5 or more (or your currency equivalent).
    Please make sure your btcpay merchant account is enabled for your transaction amounts. In your btcpay merchant account, go to Settings -> General -> Increase Processing Volume

= I need support from btcpay =
When contacting btcpay support, please describe your issue and attach screenshots and the btcpay logs.

btcpay logs can be retrieved in your Wordpress / Woocommerce environment:

    Enable logging in your btcpay plugin: Plugins -> Settings -> Debug Log -> Enable logging
    Download the logs from Plugins -> Logs

For support with this plugin, you can raise an issue on our [Github](https://github.com/btcpayserver/woocommerce-plugin/issues) or join us on [Slack](https://forkbitpay.slack.com).


== Changelog ==

= 2.2.24 =

    Bug: In some circumstances the auto update might crash the wordpress dashboard

= 2.2.23 =

    Setting Keep store level settings to transaction speed would still override store's setting
    Add low-medium transaction speed
    = 2.2.22 =
    Fix crash on some stores Cannot use object of type stdClass as array in... on the dashboard

= 2.2.21 =

    Add event_invoice_expiredPaidPartial handling

= 2.2.20 =

    Do not crash plugin page if update detection fails, be more resilient

= 2.2.19 =

    Can detect new update in plugin page

= 2.2.18 =

    Ignore IPN if another payment method for the order has been chosen (#2)
    Can detect new update in plugin page

= 2.2.17 =

    Fix a race condition if process_payment called twice
    Can decide to ignore a BTCPay event

= 2.2.16 =

    Handle 'expired' IPN
    Handle 'invoice_paidAfterExpiration' IPN event

= 2.2.15 =

    Wrong function call resulting in undefined wc_reduce_stock_levels() (#84)
    Syntax error in class-wc-gateway-bitpay.php (#80)
    Make sure that if redirect url is redefined, it has order information Added
    Redirect page displays 'payment successful' even for unpaid invoices (#81)

= 2.2.14 =

    (fixed via PHP package update) Price must be formatted as a float (#78)
    Fixed WC 2.5 compatibility, with get_billing_email() error (#83)

= 2.2.13 =

    Fixed wrong function call resulting in undefined wc_reduce_stock_levels() (#84)
    Fixed syntax error in class-wc-gateway-bitpay.php (#80)
    Fixed price must be formatted as a float (#78)
    Added redirect page, displaying 'payment successful' even for unpaid invoices (#81)

== Upgrade Notice ==


 
== Step-by-step guide with screenshots =

Having trouble setting it up? Check out the visual guide for installing the Bitcoin Payment Extension on a clean version of WooCommerce on our blog:
https://github.com/btcpayserver/woocommerce-plugin

Plugin not working? Most common plugin issues ?? all links for plugs need to be download from Wordpress

== Screenshots ==

   1. BTCPay payment form - cryptocurrency selection window
   2. Some of the 40+ cryptocurrencies supported by BTCPay
   3. BTCPay Bitcoin Payment Page - Invoice
   4. Merchant dashboard on BTCPay

