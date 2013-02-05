# Professional iOS Network Programming
## Chapter 11: Inter-app Communication

The example code from Chapter 8 of my book, [Professional iOS Network Programming](http://www.wiley.com/WileyCDA/WileyTitle/productCd-1118362403,descCd-description.html "Professional iOS Network Programming: Connecting the Enterprise to the iPhone and iPad").  Further discussion is also available on the [Wiley P2P forum](http://p2p.wrox.com/book-professional-ios-network-programming-connecting-enterprise-iphone-ipad-708/).


### URL Schemes and Keychain

The three apps communicate and detect the presence of each other via URL schemes and utilize a single-sign-on (SSO) login via the iOS keychain.  

* Employee Directory - shows a SSO-protected list of employees and a few details about them.
* Employee Records - shows an SSO-protected list of employees and detailed Human Resources (salary, etc.) information about them.  It will also show an associated image, if any.
* Employee Records Image Adder - allows the user to add a W2 image to an employee's file in the Employee Records app, demonstrating how you can send any binary data via a URL scheme.


### Detecting Other Apps

Installation Detector asks you for birthday and saves it.  If it detects it has been installed previously on the current device, it prompts you to import your previous answer.  The app takes advantage of the fact that iOS keychain values are not wiped if an app is deleted.