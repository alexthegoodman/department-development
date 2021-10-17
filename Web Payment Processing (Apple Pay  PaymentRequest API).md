# Web Payment Processing (Apple Pay / PaymentRequest API)
### Browser APIs
* **ApplePaySession** 
	* Only used on Safari (iOS and MacOS)
	* If no card added: This opens the Wallet app at the Add Card screen, or it opens the Add Card screen on MacOS  (found in System Preferences -> Wallet & Apple Pay)
	* If card added: allows payment to proceed with that payment method
* **PaymentRequest API** 
	* Standard on all browsers (not just Safari)
	* Used by Stripe’s Payment Request Button ([Payment Request Button | Stripe Elements](https://stripe.com/docs/stripe-js/elements/payment-request-button))
	* Setting up new cards is not a part of the PaymentRequest API at this time, it must be done some other way
	* This means that Stripe’s Payment Request button does not help set up cards
	* So if Stripe (Payment Request API) is required (therefore Apple Pay JS (ApplePaySession API) cannot be used) then we may need to provide a “Set up Apple Pay” button which has a deep link to the Wallet app on iOS and a modal with instructions for the System Preferences panel on MacOS
	* Or we can hide the Payment Request Button completely if there is no card added

[Payment Request Button | Stripe Elements](https://stripe.com/docs/stripe-js/elements/payment-request-button)
[Deep Dive into the Payment Request API  |  Web Fundamentals](https://developers.google.com/web/fundamentals/payments/merchant-guide/deep-dive-into-payment-request)
[Apple Pay on the Web Demo](https://applepaydemo.apple.com) the docCustomizedSession js file here makes use of ApplePaySession (only available in Safari)

[[Stripe]]

#department/development