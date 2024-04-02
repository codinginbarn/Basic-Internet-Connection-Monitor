# Basic-Internet-Connection-Monitor

Here's how the code works:

Create a div element with the ID connectMessage that will be used to display the "Your connection to the internet is down..." message.

Define a checkConnection function that creates a new Image object and tries to load a small image file from a remote server (https://example.com/tiny.png). If the image loads successfully, it means the internet connection is available, and the "isConnected" variable is set to true. If the image fails to load, it means the internet connection is not available, and the isConnected variable is set to false, and the connectMessage div is displayed on the page.
We use setInterval to call the checkConnection function every 60 seconds (60000 milliseconds).

Use caution on setting the checkConnection function real low. Remember that this setting will poll the users internet connection each time fired. 15 seconds is about low as I would go and good middle ground is 30 seconds.

The connectMessage div is styled with CSS to be positioned in the center of the page, have a red background, white text color, rounded corners, and a drop shadow.

When the page loads, the checkConnection function will be fired immediately to check the initial internet connection status. If the connection is not available, the message will be displayed. The function will continue to run every 60 seconds, updating the connection status and showing or hiding the message accordingly.

Note: Make sure to replace https://example.com/tiny.png with the URL of a small image file hosted on a remote server that you can access. You can test with this image (https://i.ibb.co/H2gW8yr/1x1.png) but recommend you host your own 1x1.png which is included in this repo.
