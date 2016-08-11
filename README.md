# Angular-2-Instafeed
Make a personal Instagram Feed on a switchable grid with the Instagram API.

You will be creating a Instagram feed using the Instagram API and Angular 2. The feed will feature a switchable grid to change the layout of the photos on the page [see Style Guide below for details].

Before you start building out your Angular 2 web application, you will need to sign up to be an Instagram Developer:
1. First go [register as an Instagram Developer](https://instagram.com/developer/clients/manage/) to get your Client ID.
1. You will also need to get your user ID go run this program. To get your User ID, go to [this site](http://jelled.com/instagram/lookup-user-id) and enter your Instagram user name to get your user ID.
  1. Note: Your User ID is different than your User Name. Your User ID is a string that looks like `12345678`
  1. Note: If you do not have an Instagram account, find an account that you enjoy and use their photos for your feed.
1. This is the weird step - since we are making a client side web application, we need to get a [pre-approved access-token from Instagram](https://www.instagram.com/developer/authentication/). Here's how you do it:

  1. **Step One:** Direct your user to our authorization URL

        https://api.instagram.com/oauth/authorize/?client_id=CLIENT-ID&redirect_uri=REDIRECT-URI&response_type=token

    At this point, we present the user with a login screen and then a confirmation screen where they grant your app’s access to their Instagram data. Note that unlike the explicit flow the response type here is “token”.

  1. **Step Two:** Receive the access_token via the URL fragment

    Once the user has authenticated and then authorized your application, Instagram redirects them to your redirect_uri with the access_token in the url fragment. It will look like this:

        http://your-redirect-uri#access_token=ACCESS-TOKEN

    Simply grab the access_token off the URL fragment and you’re good to go. If the user chooses not to authorize your application, you’ll receive the same error response as in the explicit flow

1. Once you get your **user id** and your **access_token**, try hitting this route to get your most recent Instagram photos.

    https://api.instagram.com/v1/users/USER-ID/media/recent/?count=99&&callback=JSON_CALLBACK&access_token=ACCESS-TOKEN

1. Now, you're ready to starting building your Instagram Feed in Angular 2.0 :sparkles:

## Style Guide

Below is a guide for how you should layout your Instagram feed. There is a sample CSS for the header and the buttons in `styles.css`.

#### Grid Layout

![instafeed2 - Grid](https://cloud.githubusercontent.com/assets/4650739/17606157/ae6a1080-5fb9-11e6-8a71-3f06c8ea6a3f.png)

#### List Layout

![instafeed2 - List](https://cloud.githubusercontent.com/assets/4650739/17607299/a521ea1e-5fc0-11e6-8ce1-3b0e23e5d43f.png)

### Stretch Goals
- Add additional views
- Deploy your application to Github pages.
- Add a input so a user can select the user's photos.

## Additional Resources

#### Angular 2 Documentation
- Link: [Angular 2 Documentation](https://angular.io/)

#### Instagram API Documentation
- Link: [Instagram API Documentation](https://www.instagram.com/developer/endpoints/)

#### Instagram Client Registration
- Link: [Instagram Client Registration](https://www.instagram.com/developer/clients/manage/)

#### Lookup Your Instagram User ID
- Link: [Lookup Your Instagram User ID](http://jelled.com/instagram/lookup-user-id)
