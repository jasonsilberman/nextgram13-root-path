# NextGram with Root Path Bug Reproduction

This is a fork of the NextGram app built as a demo for Instagram style routes in Next.js 13 with Parallel and Intercepting routes. 

The original has a `/` root page that shows the grid of photos and then individual `/photos/:id` pages. However, for my use case, I would like to have the individual pages be at `/:id` without the `/photos` route segment. This is not currently possible as of Next.js 13.5.5. I have recorded two videos below showing the correct and incorrect behavior (you can see the URL changes in the Arc browser below).

## Working with `/photos/:id` pages
https://github.com/jasonsilberman/nextgram13-root-path/assets/1936396/3a2817b9-4730-4c93-9634-bb4b7ac2cf6e

## Not working with `/:id` pages
https://github.com/jasonsilberman/nextgram13-root-path/assets/1936396/e49f7baa-8240-40ec-b371-66dfcfe1d94a

## Other reports of this behavior
I found some other reports of this buggy behavior below:

- Reddit thread: [Root level dynamic routes with intercepting routes](https://www.reddit.com/r/nextjs/comments/13xq8wh/root_level_dynamic_routes_with_intercepting_routes/)

# Try it Yourself
I have also gone through and deployed this app to Vercel and updated the below instructions for this repo so you can see the issues for yourself.

## Demo

[https://nextgram.vercel.app](https://nextgram13-root-path.vercel.app)

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Fjasonsilberman%2Fnextgram13-root-path)

## Locally

```bash
git clone https://github.com/jasonsilberman/nextgram13-root-path.git
cd nextgram13-root-path/
yarn
yarn dev
```
