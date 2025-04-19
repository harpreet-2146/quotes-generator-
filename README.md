#quotes generator

JavaScript Functionality:

Fetching Quotes with fetch():

The JavaScript uses the fetch() method to make a request to the quotable.io API, which provides random quotes.

The API returns a JSON object containing the quote and author.

The quote and author are displayed inside the <blockquote> and <span> elements.


Disabling the Button:

The button is disabled during the fetching process to prevent multiple requests from being made while waiting for a response.

This is done using button.disabled = true at the start of the getquote() function.

After the quote is fetched (or if there's an error), the button is re-enabled with button.disabled = false.


Error Handling:

The try-catch block is used to handle any errors that may occur while fetching the quote (e.g., network issues, API failure).

If an error occurs, a fallback message is shown in place of the quote: "An error occurred, please try again."

The error is also logged to the browser's console for debugging purposes.

Displaying the Quote:

After successfully fetching the data, the content of the quote is placed inside the blockquote element using quote.innerHTML = data.content.

Similarly, the author's name is displayed in the span element with author.innerHTML = data.author.

Initial Quote Fetch:

When the page first loads, the getquote() function is automatically called to display an initial quote from the API.


Code Flow:

When the page is loaded:

The getquote() function is triggered automatically to display the first random quote.

The "New Quote" button is clicked:

The button calls getquote(api_url), fetching a new quote from the API.

The fetched quote and author are displayed in the respective elements on the page.

If an error occurs during the fetch process, an error message is displayed instead of the quote.


How to Use:

Open the index.html file in your browser.

A random quote will be displayed on the page.

Click the "New Quote" button to fetch and display a new random quote.


Technologies Used:

HTML: For the basic structure of the page.

CSS: For styling (you can create a quotes.css file for custom styles).

JavaScript: For fetching data from the API and handling the dynamic content on the page.

API: quotable.io for getting random quotes.
