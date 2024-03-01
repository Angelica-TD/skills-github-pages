---
title: "IMAGE-OPTIMISER-OPTIMAGE"
date: 2024-03-01
---

As a web developer, one of my main tasks is to optimise images for the web. This means that I have to resize and save each image manually. As you can imagine, this is tedious and takes up a lot of time.

I want to automate this using NodeJS, express, [sharp](https://sharp.pixelplumbing.com/) \(for image processing\) and [multer](https://www.npmjs.com/package/multer) to handle image upload. Note that this will be a private app.
Before I start coding, I like to list all my requirements:  

User interface
1. 'Select images' file input that accepts multiple selection
2. 'Destination folder absolute path' input field
3. 'Optimise images' button

Logic
1. GET /optimise render the UI
2. POST /optimise do 3-5
3. Get the destination folder value from user input. If empty, set a default value. Check if the folder exists, if not, create it.
4. Resize images to widths: 1200px, 800px and 300px while retaining their original aspect ratio
5. Save the images to the destination folder as .webp format
