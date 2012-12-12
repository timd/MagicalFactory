MagicalFactory
==============

### tl;dr

MagicalFactory is a generator for creating test data in your Core Data model.


### The situation

You're diligently using a test-driven development approach to build your app. To develop with tests you need data;
and creating that data is a pain.  What you need is a generator that will create structured but distinct data on demand
to populate your Core Data stack.

### The approach

If you were building a Rails app, you'd use the FactoryGirl gem to create your dummy data.  But you're building an iOS app.

Damn.

MagicalFactory is inspired by the FactoryGirl approach.  You give it your model object, tell the generator what kind of
data you need, and how much you want.  MagicalFactory then creates it for you. Sorted.

### The process

- Create an instance of MagicalFactory.
- Pass it the object that you want to build, and a dictionary to tell MagicalFactory what to do.
- Optionally, get back an array of newly-created objects.  Alternatively, just carry on and use the newly-created objects direct from the database.

### Available data creators

- random names: first names, lastnames and combined names
- random email addresses
- random street addresses, zip codes and UK postcodes
- Random dates
- Random `NSNumber` values
- Lorem ipsum filler text

### Caveats

- It's a work-in-progress.
- Currently, it's built on top of Magical Record.

### Roadmap

- Remove direct dependency on Magical Record
- Extend with further data types
