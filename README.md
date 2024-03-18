The project is split up into two submodules:
- React Frontend that contains the jsx form.
- Rails backend that contain,
  - CRUD for /api/v1/fragrances
  - POST /api/v1/order to create an order to be pushed onto the users board_id

Done
### frontend
- [x] Build react jsx form out of monday vibe components
- [x] Add form validations/errors
- [x] Fetch current context to get `board_id` & current user id from the monday.com SDK.
- [x] Fetch fragrances from API to populate dropdown
- [x] Post order data on form submit

### backend
- [x] Create fragrance table
- [x] Seed db with some fragrances
- [x] Create `CRUD /fragrances`
- [x] Create `POST /orders`
- [x] Create service object to handle order creation logic (and to encapsulate any future order logic that we might want)
- [x] Create ruby monday API wrapper for the graphql API. 

Todo
### frontend
- [ ] Add tests to test basic form submission
- [ ] Clean up react code to include: add `./context/AppContext.js` to allow for context sharing across any component within the App, using react's `createContext`.
- [ ] Clean up styling


### backend
- [ ] Tests for rails app for: controller, model, service objects.
- [ ] Add JWT auth token to fragrance api.
- [ ] Add backend validations for first_name, last_name, and quantity of fragrances selected for a given order. Consider db level & model/business logic level.
- [ ] Consider placing the OrderService into a background job to improve performance (sidekiq)
- [ ] Improve error handling of API, to return approppriate status codes & messages (will they be presented to the user, and will we need to consider i18n internationalization/localization)
- [ ] For the requirement of "quantity" equating to number of orders, consider creating 1 order per quantity. Look into bulk insert options with the graphql mutation. If bulk option is not possiple, compare insterting both synch & async.

- [ ] For CRUD /fragrances, consider linking this to the optional "dropdown" labels. Similarly, would have to add webhooks to listen to when A user makes fragrance changes in the UI/monday.com side
- [ ] Consider organization <-> fragrance schema associations.
  
