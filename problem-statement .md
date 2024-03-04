# MD - Notion Sync App

## Problem Statement

I recently found a VS Code extension, "Notes", that allows one to write markdown inside it. I paired it with "MDX Preview" to view the file. I like the way it feels to write markdown. I use the vim extension, and I'm at a point where I'm using the keyboard to do just about everything in VS Code. For note-taking, I currently use Notion. I love Notion for viewing files, working with tables, trello boards -- but I don't like it for actual writing / text editing. Mainly because it doesn't support vim motions.

Vim has become such a big part of my life, that I can't imagine living without it. Coding and text editing has become so much faster. Picking up my hand and using the mouse to place my cursor in a specific place feels slow.

## Brainstorm

I have created a test.md file and used the "import" Notion function to manually import the test.md file. This imports it in the root Notion directory. I would love to be able to write a markdown file here, save it, and have it automatically:

1. Create and save the file in Notion, if that file does not exist.
2. If it exists, save that file.

This initial flow is great. Writing my notes in VS Code using Vim, then viewing those same notes in Notion would be awesome. Now, if there's something I don't like and I want to edit an existing file **in Notion**, I would like for it to automatically:

1. Save the updates
2. Open the same file on VS Code and be able to view those updates.
3. Edit and have it re-sync to Notion.

I want to have a continuous loop of being able to edit and sync. Regardless of where I'm writing (Notion or VS Code).

### Idea

Because I work at Dell, I don't want to give Notion or any application access to my computer and make updates to it. That's against the rules.

I could:

1. Create a GitHub repo to store my notes
2. On save, trigger a git commit and push to the repo.
3. Notion integrates with GitHub, so have Notion detect a change and store the notes in Notion.

This works publishing to Notion. What about the opposite?

Ideally, Notion should:

1. Detect a save
2. Push the updated note to GitHub repo

Then locally, I pull the changes. Rinse and repeat.

Not sure how this will work, or how to even start tbh but it's a start.
