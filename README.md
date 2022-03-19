# A RealWorld Example App :woman_technologist:

This is a modified implementation of [RealWorld](https://realworld-docs.netlify.app/docs/intro), a project used to learn about frontend/backend frameworks by creating a blogging platform. Check out the [official demo](https://demo.realworld.io/#/).

### Short-term learning goals

- explore TailwindCSS
- get more comfortable with Next.js
- build proficiency in React
- learn about
  - implementing a backend using AWS
    - including DynamoDB, Lamba, API Gateway
    - and explore single-table design
  - caching strategies
  - pagination
  - authentication
- develop the habit of using [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)
- build proficiency with Git/GitHub version control
- deploy to Vercel

### Big hairy learning goals

- experiment with
  - Event-driven architecture
  - Micro-services
  - Micro-frontends
- implement
  - CI/CD
  - documentation
  - logging
  - analytics
  - i18n
  - TypeScript
  - Web3 version

## TODO

### User CRU[D] & Authentication

- [ ] User can register
- [ ] User can login
- [ ] User can update own profile (image, bio, email, password)
- [ ] Get user by username
- [ ] Get profile by username

### Article CRUD

- [ ] List all articles, ordered by most recent first
  - [ ] List articles by tag
  - [ ] List articles written by username
  - [ ] List articles favourited by username
- [ ] Personalized article feed
  - [ ] List articles written by followed users, ordered by most recent first
- [ ] Articles are paginated
- [ ] Get an article by slug
- [ ] User can create an article (using Markdown)
- [ ] User can update own articles (title, description, content)
- [ ] User can delete own articles

### Interactions

- [ ] List comments for an article
- [ ] Comments are paginated
- [ ] User can comment on an article
- [ ] User can update own comments (content)
- [ ] User can delete own comments
- [ ] User can un/favourite articles
- [ ] User can un/follow other users

### Bonus

- [ ] Admin dashboard
  - [ ] Admin can view activity insights for platform
- [ ] Author dashboard
  - [ ] Author can view activity insights for published articles (e.g. views)
- [ ] User can bookmark articles to read later
- [ ] User can view list of bookmarked articles, ordered by most recent(ly published) first
- [ ] User can delete their account

## Endpoints (as per [RealWorld Backend Specs](https://realworld-docs.netlify.app/docs/specs/backend-specs/endpoints))

```
POST /api/users/login - Authentication
POST /api/users - Registration
GET /api/user - Get current user
PUT /api/user - Update user
GET /api/profiles/:username - Get profile
POST /api/profiles/:username/follow - Follow user
DELETE /api/profiles/:username/follow - Unfollow user

GET /api/articles - List articles
GET /api/articles/feed - List feed articles
GET /api/articles/:slug - Get article
POST /api/articles - Create article
PUT /api/articles/:slug - Update article
DELETE /api/articles/:slug - Delete article

POST /api/articles/:slug/comments - Add comment to article
GET /api/articles/:slug/comments - Get comments from article
DELETE /api/articles/:slug/comments/:id - Delete comment

POST /api/articles/:slug/favorite - Favourite article
DELETE /api/articles/:slug/favorite - Unfavourite article

GET /api/tags - Get tags
```

## Resources

- [Introducing RealWorld 🙌](https://medium.com/@ericsimons/introducing-realworld-6016654d36b5) article by Eric Simons
- [RealWorld Project Docs](https://realworld-docs.netlify.app/docs/intro)
- [Conduit](https://demo.realworld.io/#/) - the RealWorld demo app

- Marcia Villalba's [7 Common DynamoDB Patterns for Modeling and Building an App](https://www.youtube.com/watch?v=Q6-qWdsa8a4) YouTube video with Alex De Brie
- The DynamoDB Book by Alex De Brie

- [Fullstack Authentication with Refresh Access Tokens](https://www.youtube.com/watch?v=xMsJPnjiRAc) YouTube tutorial by Florian Ludewig

---

This [Next.js](https://nextjs.org/) project was bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app). To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.
