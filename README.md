# The Web & Democracy: Working with an API

Hey there! This is a basic example of how to fetch JSON data from an API and display it on your own webpage.

In this example, we will:

1. Use HTML to create a basic layout for our data
2. Use Javascript (+ jQuery, a common Javascript library) to load JSON data from an external URL
3. Use a Javascript `for` loop to process that JSON data, one record at a time
4. Use jQuery to add our results to the HTML layout from step 1

## Instructions to get started

1. Click the green "Clone or download" button near the upper-right of this page, then choose "Download ZIP"
2. Un-zip the file you downloaded
3. Open `example.html` in your web browser
4. Open `example.html` in a text editor too, so that you can look at the source code and see how this example works

## A few suggested tools/resources

- A text editor like [Atom](https://atom.io/) or [Sublime Text](https://www.sublimetext.com/)
  - These are two common programs for working with HTML and Javascript files. You can use any kind of text editing program to write code, but these programs include some nice features like syntax highlighting that help make code easier to read and write.
- A JSON parser like http://json.parser.online.fr/beta/
  - This is a website that takes raw JSON data and prints it in an easier-to-read format.
  - Keep in mind that JSON parsing can be slow! If you paste in a JSON blob that's millions of characters long, this site (and most others) will take a long time to process it.
- The [API Docs](https://dev.socrata.com/foundry/data.providenceri.gov/vyz5-ii9r) for the Providence 2017 Motor Vehicle Tax Roll
  - The Providence Open Data website does a great job of providing basic API documentation for every data set that they offer. This particular API allows you to do things like filter your results (e.g. "only show me cars where `adjusted_net_value < 1000`"). For any API that you decide to work with, make sure to look at the documentation!

## Some notes for further work

#### Authentication

One nice thing about the Providence Open Data APIs is that it uses a very simple method for *authentication*.

Many APIs require authentication as a security check. For example, Facebook has an API, and you can use it to fetch a user's birthday. However, in order to do this you must (1) register your app with Facebook, and then (2) explicitly ask the user for permission to access their data. (You've probably seen step 2 before as a user, any time you connect a new app to Facebook.)

In today's example, we're doing some very basic (and totally optional) authentication using the `$$app_token` parameter. This parameter identifies your app to the Providence Open Data website, and this allows you to make a certain number of data requests per day. (If you request data from the API too many times, it will eventually cut you off.)

For other sites like Facebook and Twitter, authentication is often a complex, multi-step process, and unfortunately that's beyond the scope of what we'll be covering today. Auth can be confusing and frustrating even for experienced developers, so if this is your first time working with an API, I would generally encourage you to stick to "public" APIs that require minimal authentication.
