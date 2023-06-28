# Full-Stack React Example

This repo contains an example of a full-stack application with an express backend, a React frontend, and a postgres database. It's designed to be a starting point for a blue ocean project, or a reference for those wanting to get testing, CI, or docker working in their respective projects.

## Deployed setup
As of 5/26/2023 the website is deployed on https://instructor-hubmcsp19.onrender.com/ . This will stop being the case in about 2 months, as render's free services will expire

## Development Setup

The app can be started with two steps:

1. `cp .env.example .env` - Copy over required environment variables.
1. `npm install; npm install --prefix=api; npm install --prefix=client` - Install all dependencies.
1. `docker-compose up` - Run Project.

> **NOTE**: After installing a new npm dependency, you have to run `docker-compose up --build` to install the new dependencies on the container.

## npm Scripts

**`root`**

- `lint` - Checks code for style issues.
- `test` - Runs `test:client` and `test:api`.
- `ci` - Runs `lint` and `test`.
- `test:client` - Runs frontend tests.
- `test:api` - Runs backend tests.

**`/client`**

- `dev` - Hosts your assets (executed by docker-compose).
- `build` - Builds your assets for production.
- `test` - Runs tests.

**`/server`**

- `dev` - Runs the server in watch mode (executed by docker-compose).
- `start` - Starts the production server.
- `test` - Runs tests.

## Tech used

- [`vite`](https://vitejs.dev/) - Module bundler, transpiler and dev server.
- [`vitest`](https://vitest.dev/) - Test runner.
- [`prettier`](https://prettier.io/) - Code formatter/checker.
- [`react-testing-library`](https://testing-library.com/docs/react-testing-library/api/) - React component test helper.
- [`msw`](https://testing-library.com/docs/react-testing-library/api/) - Request mocking library for writing frontend tests.
- ['react-auth-kit] (https://authkit.arkadip.dev/) - Authentication kit used for react project to grant cookies for remembering users
- [`supertest`](https://github.com/ladjs/supertest) - HTTP request simulator for backend testing.
- [`docker`](https://www.docker.com/) - Containerization framework for dev and deployment.
- ['playwright'] (https://www.npmjs.com/package/playwright-testing-library) - used for scripting UI interactivity tests and the resulting changes to the site
- https://render.com/ - used for deploying the website production build

## Useful Docker Commands

- `docker exec <container_name_or_id> <command>` - Runs command in the context of a container.
- `docker inspect <container_name_or_id>` - Displays info (including IP address) of a container running in docker.

## Points of improvement for the next group to inherit this project

- playwright tests that involve adding new information thru interacting with the website should be made to have this info deleted upon deleting the volume
-  selecting individual assessments for the individual students, the list of members is based on their unique student_id, not their names. This should be rectified to displaying their names instead of number_ids 
- separate testing environment including a different ports for server, react site, database, so as to not influence the main project
- Assesments button needs to figure out routes that allow for selection of a student and a specfiic assessment, after assesment and student selected, the next button should take you to modal for grading 


