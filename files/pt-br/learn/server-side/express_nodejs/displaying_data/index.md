---
title: 'Express Tutorial Part 5: Displaying library data'
slug: Learn/Server-side/Express_Nodejs/Displaying_data
---

{{LearnSidebar}}{{PreviousMenuNext("Learn/Server-side/Express_Nodejs/routes", "Learn/Server-side/Express_Nodejs/forms", "Learn/Server-side/Express_Nodejs")}}

We're now ready to add the pages that display the [LocalLibrary](/pt-BR/docs/Learn/Server-side/Express_Nodejs/Tutorial_local_library_website) website books and other data. The pages will include a home page that shows how many records we have of each model type, and list and detail pages for all of our models. Along the way we'll gain practical experience in getting records from the database, and using templates.

<table class="learn-box standard-table">
  <tbody>
    <tr>
      <th scope="row">Pré-requisitos:</th>
      <td>
        Complete previous tutorial topics (including
        <a href="/en-US/docs/Learn/Server-side/Express_Nodejs/routes"
          >Express Tutorial Part 4: Routes and controllers</a
        >).
      </td>
    </tr>
    <tr>
      <th scope="row">Objetivo:</th>
      <td>
        To understand how to use the async module and Pug template language, and
        how to get data from the URL in our controller functions.
      </td>
    </tr>
  </tbody>
</table>

## Overview

In our previous tutorial articles we defined [Mongoose models](/pt-BR/docs/Learn/Server-side/Express_Nodejs/mongoose) that we can use to interact with a database and created some initial library records. We then [created all the routes](/pt-BR/docs/Learn/Server-side/Express_Nodejs/routes) needed for the LocalLibrary website, but with "dummy controller" functions (these are skeleton controller functions that just return a "not implemented" message when a page is accessed).

The next step is to provide proper implementations for the pages that _display_ our library information (we'll look at implementing pages featuring forms to create, update, or delete information in later articles). This includes updating the controller functions to fetch records using our models, and defining templates to display this information to users.

We will start by providing overview/primer topics explaining how to manage asynchronous operations in controller functions and how to write templates using Pug. Then we'll provide implementations for each of our main "read only" pages with a brief explanation of any special or new features that they use.

At the end of this article you should have a good end-to-end understanding of how routes, asynchronous functions, views, and models work in practice.

## Displaying library data tutorial subarticles

The following subarticles go through the process of adding the different features required for us to display the required website pages. You need to read and work through each one of these in turn, before moving on to the next one.

1. [Asynchronous flow control using async](/pt-BR/docs/Learn/Server-side/Express_Nodejs/Displaying_data/flow_control_using_async)
2. [Template primer](/pt-BR/docs/Learn/Server-side/Express_Nodejs/Displaying_data/Template_primer)
3. [The LocalLibrary base template](/pt-BR/docs/Learn/Server-side/Express_Nodejs/Displaying_data/LocalLibrary_base_template)
4. [Home page](/pt-BR/docs/Learn/Server-side/Express_Nodejs/Displaying_data/Home_page)
5. [Book list page](/pt-BR/docs/Learn/Server-side/Express_Nodejs/Displaying_data/Book_list_page)
6. [BookInstance list page](/pt-BR/docs/Learn/Server-side/Express_Nodejs/Displaying_data/BookInstance_list_page)
7. [Date formatting using moment](/pt-BR/docs/Learn/Server-side/Express_Nodejs/Displaying_data/Date_formatting_using_moment)
8. [Author list page and Genre list page challenge](/pt-BR/docs/Learn/Server-side/Express_Nodejs/Displaying_data/Author_list_page)
9. [Genre detail page](/pt-BR/docs/Learn/Server-side/Express_Nodejs/Displaying_data/Genre_detail_page)
10. [Book detail page](/pt-BR/docs/Learn/Server-side/Express_Nodejs/Displaying_data/Book_detail_page)
11. [Author detail page](/pt-BR/docs/Learn/Server-side/Express_Nodejs/Displaying_data/Author_detail_page)
12. [BookInstance detail page and challenge](/pt-BR/docs/Learn/Server-side/Express_Nodejs/Displaying_data/BookInstance_detail_page_and_challenge)

## Summary

We've now created all the "read-only" pages for our site: a home page that displays counts of instances of each of our models, and list and detail pages for our books, book instances, authors, and genres. Along the way we've gained a lot of fundamental knowledge about controllers, managing flow control when using asynchronous operations, creating views using _Pug_, querying the database using our models, how to pass information to a template from your view, and how to create and extend templates. Those who completed the challenge will also have learned a little about date handling using _moment_.

In our next article we'll build on our knowledge, creating HTML forms and form handling code to start modifying the data stored by the site.

## Veja mais

- [Async module](http://caolan.github.io/async/docs.html) (Async docs)
- [Using Template engines with Express](https://expressjs.com/en/guide/using-template-engines.html) (Express docs)
- [Pug](https://pugjs.org/api/getting-started.html) (Pug docs)
- [Moment](http://momentjs.com/docs/) (Moment docs)

{{PreviousMenuNext("Learn/Server-side/Express_Nodejs/routes", "Learn/Server-side/Express_Nodejs/forms", "Learn/Server-side/Express_Nodejs")}}
