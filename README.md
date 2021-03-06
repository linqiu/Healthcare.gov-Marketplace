What This Is
------------

This repository is an unofficial bug tracker and pull request target for fixes
to [healthcare.gov/marketplace](https://healthcare.gov/marketplace/global/en_US/registration),
the latest boondoggle from HHS & CGI Federal.

This repository attempts to be a working clone of the marketplace. You should be able to run this
on a local web server and access healthcare.gov in the same way.


What This Isn't
---------------

This is not an *official* repository. For all we know, nobody is listening.

I have created this in hopes that there are some concerned programmers at CGI Federal who want to see
the project succeed. Sourcing fixes from the users of healthcare.gov is one way to achieve that goal.

See [the pull request](https://github.com/CMSgov/healthcare.gov/pull/31) that started this idea.


How To Run
----------

```
git clone git@github.com:STRML/Healthcare.gov-Marketplace.git
cd Healthcare.gov-Marketplace
npm install -g grunt
npm install
grunt build # concat/minification step
node app.js # runs a webserver to view results & proxy the API. Go to http://localhost:8080
```

Tests
-----

There are no actual tests at this time. 


TODO
----

* ~~Redirect API calls to their actual destination so this fork works~~
* Add any missing JS/CSS from other sections of the site
* Add unit tests and TravisCI integration
* Pass JSHint (good luck)


Contributing
------------

If healthcare.gov frustrates you, please contribute! My hope is that this repository becomes large enough
to attract some real attention, not just from CGI Federal but from Health & Human Services. They have been thoroughly
embarassed by this boondoggle and with luck will be looking for a way to reform the system and save face.

See the TODO list above.

While the existing source does not pass jshint, please make sure that any contributions do (we have to start somewhere).
Unit tests would be greatly appreciated. Please place them inside the `test/` folder, prefixed by unit test framework
(qunit, jasmine). Please just make sure they pass, and feel free to use your favorite test framework. I will take care
of wiring them into Grunt and TravisCI.
