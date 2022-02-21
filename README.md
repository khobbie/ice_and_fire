# Ice & Fire PHP Package




## Overview ##

IceOnFire is php package wrapper for accessing [AnApiOfIceAndFire](https://anapioficeandfire.com/).

## Installation ##

The current production release of A-song-of-ice-and-fire-API is available through [npm](https://www.npmjs.com/package/asoiaf-api):

```
composer require ampahkwabena/ice-and-fire
```

## Usage ##

```php

> use AmpahKwabena\Anapioficeandfire;

> $ice_and_fire = new Anapioficeandfire();

> return $ice_and_fire->getAllBooks();

[ { url: 'http://www.anapioficeandfire.com/api/characters/583',
    name: 'Jon Snow',
    gender: 'Male',
    culture: 'Northmen',
    born: 'In 283 AC',
    died: '',
    titles: [ 'Lord Commander of the Night\'s Watch' ],
    aliases: 
     [ 'Lord Snow',
       'Ned Stark\'s Bastard',
       'The Snow of Winterfell',
       'The Crow-Come-Over',
       'The 998th Lord Commander of the Night\'s Watch',
       'The Bastard of Winterfell',
       'The Black Bastard of the Wall',
       'Lord Crow' ],
    father: '',
    mother: '',
    spouse: '',
    allegiances: [ 'http://www.anapioficeandfire.com/api/houses/362' ],
    books: [ 'http://www.anapioficeandfire.com/api/books/5' ],
    povBooks: 
     [ 'http://www.anapioficeandfire.com/api/books/1',
       'http://www.anapioficeandfire.com/api/books/2',
       'http://www.anapioficeandfire.com/api/books/3',
       'http://www.anapioficeandfire.com/api/books/8' ],
    tvSeries: [ 'Season 1', 'Season 2', 'Season 3', 'Season 4', 'Season 5' ],
    playedBy: [ 'Kit Harington' ] } ]
```

## API ##

### Characters ###

**getCharacterByID**

* Accepts: A string or number representing a character ID.
* Returns: An object containing the character's properties if the character exists.

**getCharacterByName**

* Accepts: A string representing full name of the character.
* Returns: An array of objects containing all the characters with given name.

**getCharactersByCulture**

* Accepts: A string representing the culture of Character.
* Returns: An array of objects containing all the characters with given culture.

**getCharactersByGender**

* Accepts: A string representing the gender of Character.
* Returns: An array of objects containing all the characters with given gender.

**getAllCharacters**

* Returns: An array of objects containing all the characters.

### Houses ###

**getHouseByID**

* Accepts: A string or number representing a house ID.
* Returns: An object containing the house's properties if the house exists.

**getHouseByName**

* Accepts: A string representing full name of the house.
* Returns: An array of objects containing all the houses with given name.

**getHouseByRegion**

* Accepts: A string representing the region of the house.
* Returns: An array of objects containing all the houses with given region.

**getHouseByWords**

* Accepts: A string representing the words/saying of the house.
* Returns: An array of objects containing all the houses with given words/saying.

**getAllHouses**

* Returns: An array of objects containing all the houses.

### Books ###

**getBookByID**

* Accepts: A string or number representing a book ID.
* Returns: An object containing the book's properties if the book exists.

**getBookByName**

* Accepts: A string representing full name of the book.
* Returns: An array of objects containing all the books with given name.

**getAllBooks**

* Returns: An array of objects containing all the books.

### FUN ###

**getRandomCharacter**

* Returns: An object containing the properties of a random character.

**getRandomHouse**

* Returns: An object containing the properties of a random house.

**getRandomCharacterOfHouse**

* Accepts: A string representing full name of the house.
* Returns: An object containing the properties of a random character from the given house
