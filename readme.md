# Airbnb
### Practicing many to many relationships

Level: Easy

### Getting Started
- After you fork/clone this repo and `cd` into it, run `bundle`

- Take a look through the code and files that already exists to orient yourself.


#### Deliverables

You are building an app for an Airbnb competitor

your models are listings, guests, trips

a listing (i.e. a house or apartment) has many trips

a listing has a city attribute which is a string of a city name, e.g. 'Seattle'

a guest has many trips

a guest has a name attribute

a trip belongs to a listing and a guest

Write out the relationships using has_many, belongs_to and has_many_through. Create the necessary methods to connect these classes.

### Listing
1. `Listing#city`
returns a string of the city that listing belongs to
1. `Listing#guests`
returns an array of all guests who have stayed at a listing
1. `Listing#trips`
returns an array of all trips at a listing
1. `Listing#trip_count`
returns the number of trips that have been taken to that listing
1. `Listing.all`
returns an array of all listings
1. `Listing.find_all_by_city(city)`
takes an argument of a city name (as a string) and returns all the listings for that city
1. `Listing.most_popular`
finds the listing that has had the most trips

### Guest
1. `Guest#name`
returns the name of the guest
1. `Guest#listings`
returns an array of all listings a guest has stayed at
1. `Guest#trips`
returns an array of all trips a guest has made
1. `Guest#trip_count`
returns the number of trips a guest has taken
1. `Guest.all`
returns an array of all guests
1. `Guest.pro_traveller`
returns an array of all guests who have made over 1 trip
1. `Guest.find_all_by_name(name)`
takes an argument of a name (as a string), returns the all guests with that name

### Trip
1. `Trip#listing`
returns the listing object for the trip
1. `Trip#guest`
returns the guest object for the trip
1.`Trip.all`
returns an array of all trips