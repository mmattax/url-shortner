# url-shortner

This is a plan for building a basic link shortner.

The backend will be a REST API, powered by [Echo](https://echo.labstack.com/), Postgres, and Memcache. 

The URL shortner will work by inserting a record for a URL, getting an integer id back (from a Postgres sequence) and then performing a base 62 encoding of that id to create a short URL slug. When a user navigates to the shortened URL, we'll look up the record to find the destination URL and insert a record into a `visits` table. This will allow us to provide some basic analytics.

The [MVP project](https://github.com/mmattax/url-shortner/projects/1) defines the tasks at a bit more granular level. Each item is prioritized with the goal of [getting one piece done](https://basecamp.com/shapeup/3.2-chapter-10) at a time: The dev environment, the redirection service, analytics, and then a production enviroment. Each of these are defined as [milestones](https://github.com/mmattax/url-shortner/milestones?direction=asc&sort=due_date&state=open).

