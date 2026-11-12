# Orbit

Orbit is a personal start page with web search and device-local bookmarks.

## Google sign-in

Google sign-in is optional and only displays the signed-in email for the
current page session. It does not create an account, protect private data, or
sync bookmarks; bookmarks remain in this browser's local storage.

To enable the sign-in button:

1. Create a Google OAuth **Web application** client ID in Google Cloud.
2. Add the page's origin (for example, `http://localhost:8000`) to its
   authorized JavaScript origins.
3. Set `GOOGLE_CLIENT_ID` near the top of the script in `index.html` to that
   client ID. A client ID is public; never put a client secret in this page.
4. Serve the page from an authorized HTTP(S) origin. Google sign-in does not
   work when opening the file directly as `file://`.

Server-side token verification is required before using Google sign-in to
authorize access to private data.
