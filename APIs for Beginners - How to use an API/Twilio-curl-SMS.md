Attempted to install and run the following:

curl 'https://api.twilio.com/2010-04-01/Accounts/XXXXXXXX/Messages.json' -X POST \
--data-urlencode 'To=+XXXXXXXXXXX' \
--data-urlencode 'MessagingServiceSid=MGcXXXXXXXXXXXXXXX' \
--data-urlencode 'Body=TEST THROUGH CURL' \
-u XXXXXX:XXXXXXX

Encountered the following errors:

-U IS NOT RECOGNIZED AS AN INTERNAL OR EXTERNAL COMMAND

URL using bad/illegal format or missing url

Could not resolve host

400 Bad Request

  
Was able to overcome these issues by making the following changes:
  
  curl "https://api.twilio.com/2010-04-01/Accounts/XXXXXXXX/Messages.json" -X POST ^
--data-urlencode "To=+XXXXXXXXXXX" ^
--data-urlencode " MessagingServiceSid=MGcXXXXXXXXXXXXXXX" ^
--data-urlencode " Body=TEST THROUGH CURL" ^
-u XXXXXX:XXXXXXX

Needed to replace all single quotations to double quoatations, and the forward slashes to carets



⌨️ Video 2 - Using an API from the command line  (0:44:30​)


🎥 Course created by Craig Dennis, Developer Educator at Twilio
🐦 Craig on Twitter: @craigsdennis

