# Unhandled Exception in Asynchronous Dart Network Request

This repository demonstrates a common error in asynchronous Dart programming: neglecting to handle exceptions properly during network requests.  The provided code uses `http.get` to fetch data; however, it lacks comprehensive error handling, leading to potential crashes. The solution shows how to gracefully manage such situations. 

## Problem:
The initial `fetchData` function includes a `try-catch` block for error handling.  However, simply `rethrow`ing the exception might not be sufficient, depending on the application's architecture. Unhandled exceptions can lead to application crashes or unexpected behavior.  The lack of specific error handling might leave the user with a poor experience.

## Solution:
The improved `fetchData` function demonstrates more robust error handling. Specific checks are made for HTTP status codes, and a more informative exception is thrown for easier debugging. Additionally, error handling is improved to ensure the app doesn't crash unexpectedly.