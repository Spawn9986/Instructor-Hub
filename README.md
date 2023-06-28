<h1 align="center" id="title">Instructor Hub</h1>

<p align="center"><img src="https://socialify.git.ci/Spawn9986/Instructor-Hub/image?name=1&amp;theme=Auto" alt="project-image"></p>

<p id="description">Capstone project for Galvanize Full Stack Software Development Bootcamp.</p>

<p>Worked within a team of six utilizing Agile development practices and GIT workflows to deliver a PERN containerized application.
My part of the project consisted of leveraging React.js and CSS to design and implement captivating front-end functionality and styling as well as developing comprehensive unit and end-to-end tests.</p>

<h2>Project Screenshots:</h2>

<div align="center">
    <img src="https://github.com/Spawn9986/Instructor-Hub/blob/main/Project%20Screenshots/loginPage.png" alt="Project Screen Shot 1" width="700" height="370/">
    <img src="https://github.com/Spawn9986/Instructor-Hub/blob/main/Project%20Screenshots/registerPage.png" alt="Project Screen Shot 2" width="700" height="370/">
    <img src="https://github.com/Spawn9986/Instructor-Hub/blob/main/Project%20Screenshots/mainDashboard.png" alt="Project Screen Shot 3" width="700" height="370/">
    <img src="https://github.com/Spawn9986/Instructor-Hub/blob/main/Project%20Screenshots/projectsTab.png" alt="Project Screen Shot 4" width="700" height="370/">
    <img src="https://github.com/Spawn9986/Instructor-Hub/blob/main/Project%20Screenshots/addNewStudent.png" alt="Project Screen Shot 5" width="700" height="370/">
    <img src="https://github.com/Spawn9986/Instructor-Hub/blob/main/Project%20Screenshots/addNewCohort.png" alt="Project Screen Shot 6" width="700" height="370/">
</div>

<h2>💻 Built with</h2>

Technologies used in the project:

- [`PostgreSQL`](https://www.postgresql.org/) - Object-Relational Database
- [`Express`](https://expressjs.com/) - Fast, unopinionated, minimalist web framework for Node.js
- [`React`](https://react.dev/) - User interface library
- [`Node`](https://nodejs.org/en) - JavaScript runtime environment
- [`Asana`](https://app.asana.com/0/home/1204525778089563) - Project Management tool
- [`BCryptjs`](https://www.npmjs.com/package/bcryptjs) - Login/ Security (cryptographic hashing algorithm, recommended for password hashing)
- [`Vite`](https://vitejs.dev/) - Module bundler, transpiler and dev server
- [`Vitest`](https://vitest.dev/) - Test runner
- [`Prettier`](https://prettier.io/) - Code formatter/checker
- [`React-Testing-Library`](https://testing-library.com/docs/react-testing-library/api/) - React component test helper
- [`MSW`](https://testing-library.com/docs/react-testing-library/api/) - Request mocking library for writing frontend tests
- [`React-Auth-Kit`](https://authkit.arkadip.dev/) - Authentication kit used for react project to grant cookies for remembering users
- [`Supertest`](https://github.com/ladjs/supertest) - HTTP request simulator for backend testing
- [`Docker`](https://www.docker.com/) - Containerization framework for dev and deployment
- [`Playwright`](https://www.npmjs.com/package/playwright-testing-library) - Scripting UI interactivity tests and the resulting changes to the site
- [`Render`](https://render.com/) - Deploying the website production build

## Contributors

[`Billy Thomasello`](https://github.com/2000mato) 
[`Jesten Baez`](https://github.com/JesthenB)
[`David Ortiz`](https://github.com/Abellarr)
[`Tomas Corradini`](https://github.com/tomict23)
[`Shuyi Hoo`] 
[`Shawn Couch`](https://github.com/Spawn9986)


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

## Useful Docker Commands

- `docker exec <container_name_or_id> <command>` - Runs command in the context of a container.
- `docker inspect <container_name_or_id>` - Displays info (including IP address) of a container running in docker.

## Points of improvement for the next group to inherit this project

- playwright tests that involve adding new information thru interacting with the website should be made to have this info deleted upon deleting the volume
-  selecting individual assessments for the individual students, the list of members is based on their unique student_id, not their names. This should be rectified to displaying their names instead of number_ids 
- separate testing environment including a different ports for server, react site, database, so as to not influence the main project
- Assesments button needs to figure out routes that allow for selection of a student and a specfiic assessment, after assesment and student selected, the next button should take you to modal for grading 


