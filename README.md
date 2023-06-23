# The Project

This purpose of this project is to simply display weather data on popular cities.

![image](https://github.com/hartgit/Svelte/assets/113650559/59503caf-6df7-451a-b862-1c6e4a023722)

![image](https://github.com/hartgit/Svelte/assets/113650559/0898dcca-e44b-4ab7-bc86-3967a1647caf)

### Mobile view:

![image](https://github.com/hartgit/Svelte/assets/113650559/306afd2f-dfce-4aef-af03-322e814bdaf1)

## Future Roadmap

In the future, I would like to randomize the the cities displayed on the cards. Currently, the cooridinates are hard coded. However as it is not really possible to randomize geocoordinates and still get a functioning location for the current api, this would have to be done by either using a database or a different api that has only relevant city information.

I would also like to turn the card component into a slider that allows the user to scroll through cities.

Currently all the images displayed on the cards are daytime ones, if I had more time I would adjust this to query a night image when the night weather icon is displayed.

## Run

Code is located on the `master` branch.

To run a local version of the website use:

```bash
npm run dev
```

## Known Bugs

* The card components load seperately on a slight delay as the location api only allows 2 requests per second. Very occasionally city names will remain on the `Loading...` display if the internet connection slows down and throws off the timing of the built-in delay.
* Sometimes Unsplash will load less relevant sponsored images when using a query, as they push these images to the top of the search results.
  


