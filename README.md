The project is split up into two submodules:
- React Frontend that contains the jsx form.
- Rails backend that contain,
  - CRUD for /api/v1/fragrances
  - POST /api/v1/order to create an order to be pushed onto the users board_id



Todo
- [ ] Add JWT auth token to fragrance api
- [ ] Clean up react code to include: add `./context/AppContext.js` to allow for context sharing across any component within the App, using react's `createContext`.
- [ ] For CRUD /fragrances, consider linking this to the optional "dropdown" labels. Similarly, would have to add webhooks to listen to when A user makes fragrance changes in the UI/monday.com side
- [ ] Consider organization <-> fragrance schema associations.
  
