# Configuring an Editorial Project

Each Editorial Project has its own settings and a unique endpoint for Baker clients. Basically this means that a single PressRoom powered WordPress install could manage an unlimited number of *Editorial Projects*, and thus an unlimited number of Baker based Apps.

*[screenshot placeholder]*

Each editorial project has 4 to 6 sections that need configuration:

- **Basic:** the name and slug of the editorial project.
- **Visualization / Behaviour:** these are the ```book.json``` settings that are allowed on Baker. PressRoom supports all the available ```book.json``` parameters. For a comprehensive guide about the topic please head over [Book.json Baker extension parameters](https://github.com/bakerframework/baker/wiki/Book.json-Baker-extension-parameters) on the official Baker Framework repository.
- **TOC:** ```book.json``` settings for the table of contents. More info at [Adding an Index Bar to your publication](https://github.com/bakerframework/baker/wiki/Adding-an-Index-Bar-to-your-publication)
- **Push Notifications:** Insert your [Parse](https://parse.com/) or [Urban Airship](http://urbanairship.com/) api credentials.
