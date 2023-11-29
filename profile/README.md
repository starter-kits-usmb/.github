# Starter kits USMB

This organization is a collection of starter kits made by USMB students.

## 📚 Starter kits ready

A starter kit is ready when it has a all the requirements listed [here](#minimal-requirements-for-a-starter-kit). All starter can be used with any other starter kit of this organization. (e.g one `front-xxx` with one `back-xxx`)

| Name                                                                | Description                        |
| ------------------------------------------------------------------- | ---------------------------------- |
| [front-angular](https://github.com/starter-kits-usmb/front-angular) | A starter kit for angular projects |
| [back-nestjs](https://github.com/starter-kits-usmb/back-nestjs)     | A starter kit for nest js projects |
| [front-vue3](https://github.com/starter-kits-usmb/front-vue3)       | A starter kit for vue3 projects    |

## 📝 Starter kits in progress

| State | Name                                                                                | Description                                      |
| ----- | ----------------------------------------------------------------------------------- | ------------------------------------------------ |
| WIP   | [back-java-spring-boot](https://github.com/starter-kits-usmb/back-java-spring-boot) | A starter kit for java projects with spring boot |

## 🤝 Contributing

If you want to contribute to this organization, you can ask to a new starter kit by creating an issue with the `starter-kit` label [here](https://github.com/starter-kits-usmb/.github/issues).

You can also contribute to an existing starter kit by creating a pull request on the starter kit repository.

## Minimal requirements for a starter kit

### Frontend

- [ ] A `README.md` file with a description of the project and how to run it
- [ ] Scalable folder structure
- [ ] Linter and prettier
- [ ] Routing
- [ ] Authentification service with JWT
- [ ] Light design system and layout utilities see [files](https://github.com/starter-kits-usmb/.github/tree/main/minimal-design-system)
- [ ] Toast service (snackbar and loading screen)
- [ ] Modal service (support custom modals)
- [ ] Test setup
- [ ] docker compose file for development & production

### Backend

- [ ] A `README.md` file with a description of the project and how to run it
- [ ] Scalable folder structure
- [ ] Linter and prettier
- [ ] Authentification with JWT.
- [ ] Auth guard for routes (protected routes)
- [ ] Database setup (any)
- [ ] Swagger documentation available at `/api`
- [ ] Test setup
- [ ] docker compose file for development & production

### Authentification

Authentification should have at least 3 endpoints:

#### `POST /auth/login`

Login user with credentials and return a JWT token.

##### body

```json
{
  "login": "string",
  "password": "string"
}
```

##### response

```json
{
  "token": "string"
}
```

#### `POST /auth/register`

Register a new user. Return the user id and login.

##### body

```json
{
  "login": "string",
  "password": "string"
}
```

##### response

```json
{
  "id": "number",
  "login": "string"
}
```

#### `GET /auth`

Verify the token. Return 202 response if the token is valid and 401 if not.

##### headers

`Authorization: token`
