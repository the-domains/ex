---
inFeed: true
description: >-
  Normally we let Molly choose the font for our sites, and leave it at that..
  you can redesign a few times if you don’t like her choice, and she’ll come
  back with alternatives..
dateModified: '2017-09-10T10:20:54.112Z'
datePublished: '2017-09-10T10:20:54.632Z'
title: typography..
author: []
publisher: {}
via: {}
hasPage: true
sourcePath: _posts/2017-08-31-typography.md
starred: false
datePublishedOriginal: '2017-08-31T20:29:48.001Z'
url: typography/index.html
_type: Article

---
# typography..

Normally we let Molly choose the font for our sites, and leave it at that.. you can redesign a few times if you don't like her choice, and she'll come back with alternatives..

But what if you want a specific font say.. just for headings to articles ? ..trying to think of a reason, but what if you're a wedding business and want a more flamboyant heading..

Well we can do this.. we can do this through CSS and using an embedded html window.

For cross browser support, we've tried various methods, but the only way we have found that is consistent is by using fonts from [Google][0].

We would probably only use this for article headings, but here is an example, using an embedded window.. set the size to 100.. the same code can be used for any Google font.. note as we are using CSS on the grid site, the code needs to be within <style\>... </style\> tags..

Here is our code :

    <style>
    
    @import url('https://fonts.googleapis.com/css?family=Italianno');
    
    .fancy4 {
    font-family: 'Italianno', cursive;
    font-size: 80px;
    }
    </style>
    
    <div class="fancy4">The Wedding of Jon & Daenerys</div>

and the result.. would make a great wedding header to an article.. just never gonna happen when he finds out she is his Aunt... 😳

<iframe src="https://the-grid.github.io/ed-userhtml/?g=eJxFzrEKwjAUheE9T3HpYBW0cXCQNq0OLjoLziFN2kCahNy0GMV3Vyni_v2HwzAmIxtCjnrwLkQYg1nmfYweS0qVsxGLzrnOSO41FsINVCAeFB-0SfU5cqO5tS5fVYQUiluRdvAk324zmxLyv1qDGAPqSVYzQf2QJey3_l6RF2H0d4a1egJhOGKdzaNZc-0l3GTbatuBU3BxFhZw4tLKkJDRT9G8AYx0Rao" height="100" style=""></iframe>



[0]: https://fonts.google.com/