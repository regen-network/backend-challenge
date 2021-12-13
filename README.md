# Back-end Code Challenge

This challenge consists of creating a RESTful API capable of managing users, their projects and monitoring data on [Regen Registry](http://registry.regen.network/).

The goal here is for us to get a basic understanding of how you code, so it's not meant to be very difficult. Ideally you shouldn't spend more than 4-6 hours on it.

This should be using TypeScript, [Express](https://expressjs.com/) and [PostgreSQL](https://www.postgresql.org/).

## Instructions

1. Set up database migrations with your desired tool to create a `user` and `project` table.
A user should have a unique id and a name.
A project should have a unique id, a name and a project developer that is an existing user from the `user` table.

Then provide an API that can:
- create a new user
- list all users
- query user by id
- create a new project
- list all projects
- query project by id

2. For a given project, we want to add some monitoring data. This can happen as part of multiple monitoring rounds.
Create a new `monitoring_round` table as part of your existing database migrations.
A monitoring round should have a unique id, a date, some metadata stored as JSON and a monitor that is an existing user from the `user` table.

Your API should be able to:
- create a new monitoring round
- list all monitoring rounds for a given project
- update an existing monitoring round

3. Complete **one of** the following tasks:

  a. In particular, monitoring round metadata can hold the following information:
   - sampling depth
   - list of soil samples with location and total carbon percentage for each of them

   This metadata is stored as [JSON-LD](https://json-ld.org/).
   Write down an example of such metadata in a new `metadata.json` file using the following properties:
   - `http://regen.network/samplingDepth`
   - `http://regen.network/soilSamples` 
   - `http://schema.org/latitude`
   - `http://schema.org/longitude`
   - `http://regen.network/totalCarbonPercentage`

  b. Add some tests for testing your API endpoints.

## Submission

For submission, please send us an email with a link to your project, ideally as a github repo. Oh, and don't forget to add a nice README.md so we know how to build & run it :)
