# infinity-art-challenge

> Clone this repository to apply the challenge and when you're done, publish your project to your github account and share the link.

## Description

Create a little web application for display the art of [Art Institute of Chicago's](https://www.artic.edu/)

The application layout should be like [Infinity Art Layout App](https://www.figma.com/file/3jlSaJ8v0TBpJq3cQL3XrQ/Infinity-art?node-id=1%3A4) which consists of 3 screens.

- Welcome Screen (Static Content)
- Grid Screen (Infinity Scroll)
- Art Detail Screen (Modal)

For the **Welcome Screen** the content is static and the images you can found in [Cover Images](/resources/cover_images)

For populate infinity grid in **Grid Screen** you need consume the [Art Institute of Chicago API](https://api.artic.edu/docs/) and you must use pagination. Should be start with **page=1** and the **limit=15** when the scroll is at the end of the page, consume the API again increasing page value in 1.

    [GET]
    https://api.artic.edu/api/v1/artworks?page=1&limit=15

For get the images for each grid element you should use the [IIIF Image API 2.0](https://iiif.io/api/image/2.0/) you can use the following URL, replacing **image_id** with the value of each element of the first API..

    [GET]
    https://www.artic.edu/iiif/2/{image_id}/full/843,/0/default.jpg

For **Art Detail Screen** you need consume _"api_link": "https://api.artic.edu/api/v1/artworks/{id}"_ or reuse the data obtained in the first api. See [Screen Hints](https://www.figma.com/proto/3jlSaJ8v0TBpJq3cQL3XrQ/Infinity-art?node-id=23%3A101&scaling=min-zoom&page-id=1%3A4&starting-point-node-id=23%3A101)
[GET]
https://api.artic.edu/api/v1/artworks/{id}
