# Starter kits USMB

This organization is a collection of starter kits made by USMB students.

## 📚 Starter kits ready

| State | Name            | Description                        | Link                                                       |
| ----- | --------------- | ---------------------------------- | ---------------------------------------------------------- |
| ALPHA | `front-angular` | A starter kit for angular projects | [repo](https://github.com/starter-kits-usmb/front-angular) |
| ALPHA | `back-nestjs`   | A starter kit for netjs projects   | [repo](https://github.com/starter-kits-usmb/back-nestjs)   |

## 📝 Starter kits in progress

| State | Name                    | Description                                      | Link                                                    |
| ----- | ----------------------- | ------------------------------------------------ | ------------------------------------------------------- |
| TODO  | `back-java-spring-boot` | A starter kit for java projects with spring boot |                                                         |
| WIP   | `front-vue3`            | A starter kit for vue3 projects                  | [repo](https://github.com/starter-kits-usmb/front-vue3) |

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
- [ ] Auth guard for routes
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
