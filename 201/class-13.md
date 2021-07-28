# The Different Types of Browser Storage
Modern web browsers offer different options for storing website data on users’ browsers, allowing this data to be retrieved based on the need. This enables website owners to persist the data for long-term storage, save website content or documents for offline use, store user preferences, apply states, and more.

![session](https://developer-chrome-com.imgix.net/image/admin/D0n4Y2LgEnwi2x98f4Su.png?w=964)
## Uses cases for browser storage
Personalizing site preferences
Persisting site activities
Storing the login state
Saving data and assets locally so a site will be quicker to download or usable without a network connection
Saving web application–generated documents locally for use offline
Improving website performance
Reducing requests to back-end servers
## Types of browser storage
Cookies
Local storage
Session storage
IndexedDB
Web SQL
Cache storage

## localStorage
The localStorage object stores the data with no expiration date. The data won’t be deleted when the browser is closed and will be available in the next day, week, or year — until deleted by the website or by the user.

# Local storage and Session storage
For the longest time cookies were the only way to maintain state. Then HTML5 came. HTML5 provides two more ways of storing data on the browser - localStorage and sessionStorage.

## Local storage
LocalStorage stores the data with no expiration date. It means the data will not be deleted when the browser is closed, and the data will be available the next day, next week, or even next year.

In chrome browser we can see the contents of localStorage by opening Developer tools > Application > Local Storage.

Setting, retrieving and deleting data from localStorage is pretty easy:
localStorage.setItem("favoriteColor", "black");
localStorage.favoriteColor;
localStorage.removeItem("favoriteColor");
Copy
Local storage provides at least 5MB of data storage across all major web browsers. This a lot more than the 4KB (maximum size) that we can store in cookies.

LocalStorage data can be read by any JavaScript code. If a hacker is able to execute JavaScript code on our web application then the hacker will be able to steal all the data stored in the localStorage.
