# How it works behind the scenes

* When user tries to access the app, it will ask for JWT token
* It will be redirected to xsuaa
* It will ask for SAML token
* It will be redirected to IDP
* Using login screen, user will login
* Once XSUAA gets SAML if will check if its authorized to use it, and then give jwt token
*

    <figure><img src=".gitbook/assets/{9C992AEB-86C2-4395-8EF9-7897BD856401}.png" alt=""><figcaption></figcaption></figure>
