# Omniauth Demo

We want to delegate authentication to a third party. Let them check the credentials (email and password), and then tell us that the user is who they say they are.

- [OmniAuth](https://github.com/intridea/omniauth)
- [The Auth Hash](https://github.com/intridea/omniauth/wiki/Auth-Hash-Schema
- [The Sign In Flow](https://dev.twitter.com/web/sign-in/desktop-browser)
- [Twitter OmniAuth Gem](https://github.com/arunagw/omniauth-twitter)
- [Twitter App Sign Up](https://apps.twitter.com/)
- [Figaro](https://github.com/laserlemon/figaro)

### Demo Steps
- Explain OAuth
- Show Twitter sign in flow
- Show Twitter OmniAuth gem
- Sign up as Twitter Application
- Setup API keys with Figaro
- Add link
- Create callback route
- Create callback controller action
- Fail and inspect auth object
- Create provider and uid migrations
- Find user by these fields in controller action
- Fallback create user by these fields
- Sign user in
- Redirect to backbone root
- Test in browser
- Refactor controller action to user model

# Backbone Auth Demo

This demo shows how to do a full session management in Backbone.js.

We attach a top level singleton currentUser object. Views can then listen to any `signIn` or `signOut` events on this object.

```
this.currentUser = new BackboneAuthDemo.Models.CurrentUser();
```

In the router we can use `_requireSignedIn` and `_requireSignedOut` functions to enforce the desired session state.

Files to check out:
- [backbone_auth_demo.js](./app/assets/javascripts/backbone_auth_demo.js)
- [user.js](./app/assets/javascripts/models/user.js)
- [sessions_controller.rb](./app/controllers/api/sessions_controller.rb)
- [users_router.js](./app/assets/javascripts/routers/users_router.js)
- [header.js](./app/assets/javascripts/views/shared/header.js)
- [sign_in.js](./app/assets/javascripts/views/shared/sign_in.js)

### OmniAuth Integration

View the [omniauth](https://github.com/jonathanlemuel/backbone-auth-demo/tree/omniauth) branch to see Twitter sign in integration.