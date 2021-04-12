<img src="./assets/alteri_logo.jpg" alt="Alteri Logo" width="1200"/>

`Alteri` is a platform connecting users in need of basic necessities with donors in their area. The app's mission is to spread compassion through helping the less fortunate.

Requires [Alteri front end](https://github.com/jeffreyc86/alteri-frontend) and [Alteri back end](https://github.com/jeffreyc86/alteri-backend).

## Live Link & Demo

Visit the [Live Link](https://alteri-client.netlify.app/) 

Watch the [Demo](https://www.loom.com/share/471914886e254936afc0976c14b0b3c2)

## Technologies Used

`Alteri` is built with a `React` front end, a `Ruby on Rails` & `PostgreSQL` back end, `Redux` for universal state management, and `ActionCable` to integrate WebSockets. All styling was done with custom CSS. The live link for `Alteri` is deployed on [Netlify](https://www.netlify.com/) with [Heroku](https://www.heroku.com/) for the back end.

## Features

The word ***alteri*** itself comes from the root of the word **altruism**, which was the basis for the app. Users are both able to create requests for basic necessity items and fulfill requests. Once a recipient is connected with a donor, a live chat is set up to figure out the exchange logistics. Compassion included.

### User Authentication

Users are able to sign up or login. There are validations when creating an account. Users may also register using their Google account. Upon a successful account creatation/login attempt, a `JWT Token` is issued to store the user's session.

Once logged in, the user is brought to their profile page where they'll see all their past requests and donations. 

<img src="./assets/login.gif" alt="login" width="800"/>

### Creating Requests

When creating requests, users may select from a set list of items. The items are separated by category and users may filter items by name. Certain food and clothing items allow the user to specify a quantity and/or preference. All other items default to a quantity of one.

<img src="./assets/create-request.gif" alt="create request" width="800"/>

There is a limit of 10 items per request. Once exceeded, an alert appears. Users may also remove items from their request by clicking remove.

<img src="./assets/request-limit.gif" alt="create request 2" width="800"/>

Once a request is complete, the user is brought back to their profile page where they'll see the newly created request with a pending status.

<img src="./assets/complete-request.gif" alt="create request 3" width="800"/>

### Fulfilling Requests

Users are able to view all the current pending requests and filter them by distance away. If they have all the items requested, they may accept the request. Once accepted a chat will be assigned to the recipient and the donor.

<img src="./assets/accept-request.gif" alt="accept request" width="800"/>

Once accepted, the status for the request will now show as accepted for both the recipient and donor.

<img src="./assets/accepted-request.gif" alt="accepted request" width="800"/>

Within each chat, users are able to see the items requested, as well as a map showing the distance between the two users. The map uses [GoogleMap](https://developers.google.com/maps)'s API and pinpoints both users' geolocations.

<img src="./assets/chat-features.gif" alt="chat features" width="800"/>

The recipient and donor are able to chat in real-time due to WebSocket integration. They may also send emojis. 

<img src="./assets/chat.gif" alt="chat" width="800"/>

Once the exchange has been made, either user can mark the request as fulfilled. Doing so will be reflected for both the recipient and donor. The status of the request on their profile pages will be updated to fulfilled.

<img src="./assets/fulfilled-request.gif" alt="fulfilled request" width="800"/>

### Logging Out

When a user is complete with their session, they're able to log out. Once logged out, the stored `JWT Token` is deleted and they're brought back to the home page.

<img src="./assets/logout.gif" alt="log out" width="800"/>

### Accessibility

Alteri was created with all custom CSS and the use of media queries, making the app is mobile friendly. The sizing of all elements adjust depending on the window size.

<img src="./assets/mobile.gif" alt="mobile friendly" width="800"/>

## License

The [MIT](https://choosealicense.com/licenses/mit/) License

Copyright (C) 2021 - [Jeffrey Chiu](https://github.com/jeffreyc86) 