# Better Friend Client
Better Friend automatically responds to activity on your Facebook feed, for
both users and organizations. It provides a way to feign interest in your
friends' inane memes and your customers' complaints. It won first place at
[CalgaryHacks 2017](http://calgaryhacks.com/) hackathon where the theme was
Automation and Optimization.

### Client
This is the ReactJS web app used to allows users to register their Facebook
accounts with Better Friend and configure their automatic replies and other
settings.

### [API](https://github.com/janclarin/better-friend-api)
To connect with
[Facebook Login](https://developers.facebook.com/docs/facebook-login) and
[Graph API](https://developers.facebook.com/docs/graph-api) to
manage users' Facebook accounts, we made a separate
API with Node.js.

### Hackathon team members
- [Andrew Zimmer](https://github.com/ajr-zimmer)
- [Jan Clarin](https://github.com/janclarin)
- [Jarrett Spiker](https://github.com/JarrettSpiker)
- [Jonathan Wan](https://github.com/jnthnwn)

## Screenshot
Landing page

<img src="https://raw.githubusercontent.com/ajr-zimmer/better-friend-client/master/screenshots/landing-page.jpg" width="400">

Sandra automatically replying to Ullrich's Facebook wall posts.

<img src="https://raw.githubusercontent.com/ajr-zimmer/better-friend-client/master/screenshots/example-replies.png" width="400">

## Inspiration
We found it difficult to keep up with all of the activity on social media.
It would save us a lot of time if we could automate our interactions with
friends and fans. That's why we made Better Friend.

## How we built it
We built the back-end with Node.js and stored our data in a MongoDB instance.
The front-end uses React.js. Our web server and API server are hosted using
Heroku.

We make use of the Facebook Graph and Facebook Login APIs to respond on a
user's behalf. Whenever new activity on a user's feed is detected, a webhook is
triggered and calls our API server, which uses the Facebook Graph API to make
an appropriate reply based on industry standards.

## Challenges we ran into
We had a lot of trouble dealing with the limitations of the Facebook APIs and
the large learning curve of React. As well, there were restrictions that
prevented us from allowing public Facebook accounts to work with the app. We
would have needed to submit a request to Facebook to allow us to ask users for
specific permissions that would allow us to post on their behalf.

**Because we do not have authorization from Facebook to enable certain
permissions needed to post on behalf of users, this currently only works with
our Facebook Test User accounts.**
