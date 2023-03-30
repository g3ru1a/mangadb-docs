---
title: Models
---

# MangaDB - All Endpoints <img src="https://img.shields.io/badge/Version-1.0.0-blue">

This list should have all the endpoints the api has to offer for both users and editors

## Bindings

**Binding data** refers to information about the physical construction of a book. This can include details about the cover
material, the type of binding used to hold the pages together, and any special features or embellishments.

Entries could be something like "Special Edition" or "Deluxe Edition" to denote a book that has unique or enhanced features beyond the standard paperback or hardback binding.

<swagger-ui src="./binding/openapi.yml"/>


## Languages

This table is used to reference the language of a book or series, which is a crucial aspect of organizing books within
the database. Each language in the table is identified by its name and ISO<sup>[1]</sup> code, providing a standardized system for
classifying languages. For example, English is identified as "en" and French is identified as "fr".

See Also:
- [1]: [Wikipedie ISO 639_1 Codes][iso_codes_wiki]

<swagger-ui src="./language/openapi.yml"/>


## Item Types

The **ItemType** table is used to store information about the type or genre of a book, such as Manga, Light Novels,
Novels, and Comic books. Each book in the database is associated with an **ItemType** entry that describes its specific type or genre.

The use of **ItemType** provides a standardized way to categorize books, making it easier for users to search and
filter books based on their interests. For example, a user interested in Manga can quickly search for books that
have been categorized as such using the **ItemType** field. By enabling users to easily find books based on their preferred
genre, the **ItemType** table helps to improve the user experience of searching and browsing through a large collection of books.


<swagger-ui src="./itemtype/openapi.yml"/>


## Publishers

The Publisher table in the book database API contains publisher information such as name, website URL, description, and logo.
Developers can use this table to retrieve and organize books by publisher, and to display additional information about publishers
to users. This enables users to discover new books and publishers more easily.

<swagger-ui src="./publisher/openapi.yml"/>

## Statuses

The status is used to denote the current state of a book or series. For example, a book that is currently being published
would have a status of "Ongoing", while a book that has been completed would have a status of "Completed".

<swagger-ui src="./status/openapi.yml"/>

## Staff

Staff data refers to information about the people who worked on a book, such as the author, illustrator, editor etc.

<swagger-ui src="./staff/openapi.yml"/>

## Series

Series contains all the variations of a title, such as manga, novels, light novels, special editions etc.

<swagger-ui src="./series/openapi.yml"/>

## SeriesType

SeriesType contains data about certain variations of a title. For example, a series could have a type of "Manga" or
"Light Novel" and all the books in that series-type would be of that type.

<swagger-ui src="./seriestype/openapi.yml"/>

## Book

Book contains all the information about a book, such as the title, author, publisher, ISBN, release date etc.

<swagger-ui src="./book/openapi.yml"/>

[iso_codes_wiki]: https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes