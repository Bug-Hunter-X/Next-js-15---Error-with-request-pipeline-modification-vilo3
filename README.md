# Next.js 15 - Unexpected Request Pipeline Behavior

This repository demonstrates a bug encountered in Next.js 15 when using a package that modifies the request pipeline. The bug causes unexpected behavior and prevents the application from rendering correctly.

## Bug Description

The core issue is that when package `example-package` intercepts and modifies the request, Next.js fails to properly handle the response, leading to an error.  The error may manifest as an unexpected 500 server error or a failure to render the page.

## Steps to Reproduce

1. Clone this repository.
2. Install the required dependencies: `npm install`
3. Run the development server: `npm run dev`
4. Observe the error in the browser's console or server logs.

## Solution

The solution involves ensuring the `example-package` correctly handles Next.js's internal request mechanisms, avoiding conflicts with the framework's pipeline.