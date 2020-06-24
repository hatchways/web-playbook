# What is CORS? How does it work?

Cross-origin resource sharing (CORS) is a mechanism used to give a web browser the “OK” to allow a web application running on one origin to selectively access resources from another origin. In the context of CORS, an origin refers to the domain, protocol, and port used by a web app.

CORS is used in relation to the Single Origin Policy (SOP) that is implemented by most web browsers. The SOP only allows a site to make requests to its own origin, by default. SOP is a security measure used by browsers to address Cross-Site Request Forgery (CSRF) concerns. CSRF can occur when you visit a site that makes requests to a server on another origin using the user’s browser cookies containing authorization credentials, for example. With SOP, the site could not make such a request unless the server explicitly gave the “OK” to the browser via CORS.

If a server wants to allow requests from another origin via CORS, it can set certain headers in its responses. These headers are defined in the CORS spec, and are standardized across most browsers. A few of the main CORS headers are:

- Access-Control-Allow-Origin: specifies the origin that the server will allow requests from.
- Access-Control-Allow-Credentials: specifies whether credentials can be sent with the request to give permission to make the request.
- Access-Control-Allow-Methods: specifies the HTTP methods allowable when accessing the resource.

When a site wants to make a request to another server via CORS, the browser will first send a preflight request (with the exception of a few types of requests), asking the server of its CORS policy. The server will set its CORS headers in the response, which will tell the browser what permissions the site has. The site can then go ahead with the request.
