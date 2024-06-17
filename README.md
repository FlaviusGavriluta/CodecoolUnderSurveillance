# Codecool under surveillance

## Story

You are soon to finish your studies at Codecool. You don't want to be uncool, so you're thinking about keeping an eye on the school's life. Twitter seems like a great platform to do it.

Also, since you'll be hunting jobs from now on, there are some financial information that can be useful as well, and you don't want to miss the fun either.

It is time to start a project that combines all of these together.

## What are you going to learn?

- how to communicate with multiple, different software systems
- what is `OAuth`
- how to design complex systems
- how to export data as a `PDF` file

## Tasks

1. Install the dependencies required by the project.
    - The `composer install` terminal command creates a `vendor` folder, which contains at least a `laravel` directory and an `autoload.php` file.

2. Sign up for Twitter Developer Account at [https://developer.twitter.com/](https://developer.twitter.com/)
    - The Twitter Developer account exists
    - The Twitter Developer account is available and can be logged in to

3. Create a `Twitter App` at [https://apps.twitter.com/](https://apps.twitter.com/)
    - The `Twitter App` appears under the `Projects` section
    - The keys and tokens are gathered and available
    - The `App` has `Read Only` permissions

4. Integrate a PDF export package with your application.
    - The `barryvdh/laravel-snappy` folder exists in the `vendor` directory, and is not empty

5. Draw a `sequence diagram` where you depict the required communication between different components (client, server, twitter-api, pdf-generator, mnb-service)
    - The `sequence diagram` exists in the `diagram` directory

6. Create the `/surveillance/pdf/{mode}` endpoint that returns a table containing the latest tweets of the `Codecool_global` Twitter Account.
    - The `/surveillance/pdf/{mode}` endpoint is defined and can be called
    - The returned tweets are listed in reverse chronological order
    - The `mode` parameter of the route can only be `fin` or `fun`
    - If the `mode` is not `fin` or `fun`, return a `Bad request` status
    - The `mode` parameter of the route is `fin` by default, meaning if `mode` isn't provided, `fin` is used
    - The route returns a `PDF` file
    - The endpoint does not leave the file on the server after returning it
    - If the `mode` is `fin`, every row of the table that is a fibonacci number and bigger than 2 is a random currency from the `MNB Webservice`
    - If the `mode` is `fun`, every row of the table that is a fibonacci number and bigger than 2 is a random joke from `ICNDb`
    - The fibonacci rows only add new information to the table, not replacing the tweets
    - The returned table has the following columns:
  - `Row number`: The number of the current row
  - `Source`: The source of the data (`Twitter`, `MNB`, or `ICNDb`)
  - `Text`: The tweet, the random currency, or the random joke
  - `Published`: The publish date of the tweet, empty for `MNB` and `ICNDb`

7. [OPTIONAL] Create the frontend of the application with the tool of your choice (notable mentions are `React` and `Postman`).
    - There is a frontend that can call the `/surveillance/pdf/{mode}` route and return the `PDF` file

## General requirements

None

## Hints

- None

## Background materials

- <i class="far fa-exclamation"></i> [What is Sequence Diagram?](https://www.visual-paradigm.com/guide/uml-unified-modeling-language/what-is-sequence-diagram/)
- <i class="far fa-exclamation"></i> [Twitter API - Get Tweet timelines](https://developer.twitter.com/en/docs/twitter-api/v1/tweets/timelines/overview)
- <i class="far fa-book-open"></i> [Twitter API - Tools and libraries](https://developer.twitter.com/en/docs/twitter-api/tools-and-libraries)
- <i class="far fa-exclamation"></i> [MNB Webservice](project/curriculum/materials/pages/web/mnb-webservice.md)
- <i class="far fa-exclamation"></i> [ICNDb API](http://www.icndb.com/api/)
- <i class="far fa-book-open"></i> [API Security](project/curriculum/materials/pages/web-security/api-security-auth-jwt.md)
- <i class="far fa-book-open"></i> [What is OAuth?](https://www.csoonline.com/article/3216404/what-is-oauth-how-the-open-authorization-framework-works.html)
- <i class="far fa-book-open"></i> [An introduction to XPath](https://www.zyte.com/blog/an-introduction-to-xpath-with-examples/)
- <i class="far fa-exclamation"></i> [Install wk**html**to**pdf** (Ubuntu)](https://computingforgeeks.com/install-wkhtmltopdf-on-ubuntu-debian-linux/)
- <i class="far fa-exclamation"></i> [Install wk**html**to**pdf** (macOS)](https://formulae.brew.sh/cask/wkhtmltopdf)
- <i class="far fa-exclamation"></i> [Snappy PDF/Image Wrapper for Laravel](https://laravel-news.com/snappy-laravel/)
- <i class="far fa-book-open"></i> [SimpleXML](https://riptutorial.com/php/example/27258/simplexml)
- <i class="far fa-book-open"></i> [SimpleXMLElement's xpath()](https://www.geeksforgeeks.org/php-simplexmlelement-xpath-function/)
- <i class="far fa-book-open"></i> [cURL examples](https://phpenthusiast.com/blog/five-php-curl-examples)
- <i class="far fa-book-open"></i> [Using GuzzleHttp with Laravel](https://medium.com/laravel-5-the-right-way/using-guzzlehttp-with-laravel-1dbea1f633da)
- <i class="far fa-candy-cane"></i> [TwitterOAuth](https://twitteroauth.com/)

