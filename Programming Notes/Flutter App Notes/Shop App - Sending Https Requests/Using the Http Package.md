# Using the Http Package #version-change 
-   Using the Http Package

-   The `http` package we added in the last lecture changed slightly with its last versions.

-   In the next lecture, we'll send a `POST` request to an API endpoint with a URL.

-   For this, in the lecture, I'll do this:

-   const url = '...'

-   http.post(url, ...)

-   As of version 0.13.0 or higher of the `http` package, url can't be a string (i.e. plain text) anymore.

-   You have two options:

-   1) Use an older version of the http package: E.g. set `http: 0.12.2` in your `pubspec.yaml` file

-   2) Convert url from a string to a "Url object" (and also change `const` to `final`):

-   final url = Uri.parse('')

-   http.post(url, ...)

-   For example, my code from the next lecture should look like this:

-   final url = Uri.parse('https://flutter-update.firebaseio.com/products.json')

-   http.post(url, ...)

-   Alternatively, you can also use this syntax:

-   final url = Uri.https('flutter-update.firebaseio.com', '/products.json')

-   http.post(url, ...)[](<- 2) Convert url from a string to a "Url object" (and also change ```dart
const
``` to ```dart final



```dart

    - final url = Uri.parse('%3Cyour-url%3E')
    - http.post(url, ...)
- For example, my code from the next lecture should look like this:
    - final url = Uri.parse('https://flutter-update.firebaseio.com/products.json')
    - http.post(url, ...)
- Alternatively, you can also use this syntax:
    - final url = Uri.https('flutter-update.firebaseio.com', '/products.json')
    - http.post(url, ...)
	
```

- Theory Continuation lectures for how to use http requests [[Sending POST Requests]]   
