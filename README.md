=== Transmit to Slack ===
Contributors: shirgans
Tags: slack, woocommerce, orders, api
Donate link: https://www.paypal.me/shirgans
Requires at least: 4.5.0
Tested up to: 5.2
Requires PHP: 5.2.4
Stable tag: 3.6.4
License: GPLv3 or later
License URI: http://www.gnu.org/licenses/gpl-3.0.html

Instantly sends new orders from WooCommerce to your desired Slack channel.


= Screenshots =

- This is how new orders shows on Slack (Ver. 1.0)


== Getting Started ==

= Step 1: Create Slack App =

- Go to Slack APIs: https://api.slack.com/apps/ and login
- Create a new app
- Give it a name (WC Orders, for example)
- Choose the workspace you would like to integrate with
- Under “Building Apps for Slack” click on “Incoming Webhooks”
- At the top - Activate Incoming Webhooks
- Then, at the bottom, click on the button to add new webhook
- Choose the channel you wish the orders will show in
- You can create a new channel on slack and then refresh that page, so you can select the channel you just created
- Click Install
- You will see a new webhook URL, something that starts like this: https://hooks.slack.com/services/T8KD1LQ...... 
- Copy this URL

= Step 2: Add code =
- Add the following code to your functions.php.
- change "paste Webhook URL here" to the copied URL (from step 1)

add_filter('transmit_to_slack_webhook_url', 'slack_webhook_url');
function slack_webhook_url(){
    return 'paste Webhook URL here';
}

== Contribute on GitHub ==
You are welcome to contribute this open source project on GitHub:
https://github.com/shirgans/transmit-to-slack

== Changelog ==
= 1.0.0 - 2019-06-23 =
* First version