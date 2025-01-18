# Next.js 404 Error on Refresh After Navigation

This repository demonstrates a common issue in Next.js applications where refreshing a page after navigating to it results in a 404 error.  The problem arises when the client-side routing doesn't properly handle initial page loads compared to subsequent requests.

## Bug Description

The application consists of two pages: `Home` and `About`.  Navigating from `Home` to `About` works correctly. However, refreshing the `About` page directly causes a 404 error because Next.js's file-system routing doesn't find a direct match for the request.

## Reproduction Steps

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm run dev` to start the development server.
4. Navigate to the About page.
5. Refresh the page; you should get a 404 error.

## Solution

This issue is addressed by ensuring that Next.js can handle requests to the About page either by using a custom server or by restructuring the application. See the solution in the `solutionContent` section.