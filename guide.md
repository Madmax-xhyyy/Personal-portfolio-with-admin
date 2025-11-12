### Backend Suggested File Structure

api/
├── config.js                # Global configuration (env vars, CORS, sessions)
├── index.js                 # Entry point (starts the server)
├── setup.js                 # Database (MongoDB) connection initialization
├── package.json
├── .env                     # Environment variables

│
├── controllers/             # Request handlers (call services)
│   ├── auth.controller.js
│   ├── hero.controller.js
│   ├── about.controller.js
│   ├── skill.controller.js
│   ├── project.controller.js
│   ├── certification.controller.js
│   └── contact.controller.js
│
├── middleware/              # Middleware functions
│   ├── auth.middleware.js         # Cookie/session authentication
│   ├── error.middleware.js        # Centralized error handler
│   └── validate.middleware.js     # Joi validation middleware
│
├── models/                  # Mongoose schemas
│   ├── user.model.js
│   ├── hero.model.js
│   ├── about.model.js
│   ├── skill.model.js
│   ├── project.model.js
│   ├── certification.model.js
│   └── message.model.js
│
├── repositories/            # Direct DB operations (CRUD via Mongoose)
│   ├── user.repository.js
│   ├── hero.repository.js
│   ├── about.repository.js
│   ├── skill.repository.js
│   ├── project.repository.js
│   ├── certification.repository.js
│   └── message.repository.js
│
├── routes/                  # API route definitions
│   ├── auth.route.js
│   ├── hero.route.js
│   ├── about.route.js
│   ├── skill.route.js
│   ├── project.route.js
│   ├── certification.route.js
│   └── contact.route.js
│
├── services/                # Business logic (bridge between controller & repo)
│   ├── auth.service.js
│   ├── hero.service.js
│   ├── about.service.js
│   ├── skill.service.js
│   ├── project.service.js
│   ├── certification.service.js
│   └── contact.service.js
│
└── utils/                   # Helpers & utilities
    ├── cloudinary.util.js         # Cloudinary config
    ├── error.util.js              # Custom error handler classes
    ├── hash-password.util.js      # bcrypt password hashing
    ├── logger.util.js             # Winston logger config
    ├── paginate.util.js           # Pagination helper
    ├── token.util.js              # Cookie/session helpers
    └── validate-schema.util.js    # Joi schema definitions
