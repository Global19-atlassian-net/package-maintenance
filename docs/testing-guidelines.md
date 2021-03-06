# Testing

### Why?
Testing is awesome!

Testing is useful for developing new features, refactoring with confidence, and making sure new things don't break old things. When other people rely on your code for their own applications, testing helps you make sure things don't break for more than just yourself!

Testing is even more important when new maintainers take over a package. Sometimes when we work on a codebase for a long time we forget to articulate all the cognitive load to which we have become accustomed. Good test coverage can alleviate this burden.

### Updates
In order to indicate to your users that the module you made is intended to work correctly with the newer version of Node.js, it is a good practice to run your tests across multiple Node.js versions.

This can be done developing a CI pipeline. Check out our [CI guidelines](https://github.com/nodejs/package-maintenance/blob/master/README.md).

The minimum versions you should focus are:
* [LTS](https://nodejs.org/en/about/releases/) (long term support)
* [Current](https://nodejs.org/en/about/releases/)

Supporting older versions of Node.js is encouraged where practical.

For browser-based modules and modules that are designed to work equally both client and server side it is essential to test on various 
versions of your target browser and to publish which environments are supported.

### How?
It is a good idea to have unit tests, coverage that matches most use cases for the module, and make sure things work in all supported environments.

* **Unit Test**: test your code
* **Integration Test**: test your code with other applications dependencies
* **Acceptance Test**: test your application under a load

#### Unit Testing
The initial and fundamental start of any testing strategy should start with a unit testing strategy. For the JavaScript language
the unit test may be the first place to catch code that will not parse. It is also the way to define the expectation for a particular
function or code block. The unit test should describe what to expect from that code when given a defined set of inputs.

For a test to be considered a unit test it should consume no remote services.

It is generally considered good practice to run units as part of any commit or build strategy.

#### Integration Testing
Integration testing in general requires that the code under test be in a package.

For many packages integration testing requires that the built package be run via a testing tool upon several environments. The 
field of continuous integration and deployment (CI/CD) is complex. The package being built shall be run through
a CI/CD pipeline. Several integrations are available for GitHub based repositories. (There are also alternatives to GitHub.)
These include but are not limited to 
- [GitHub Actions](https://docs.github.com/en/actions)
- [GitLabs](https://about.gitlab.com/)
- [CircleCI](https://circleci.com/product/)
- [TravisCI](https://travis-ci.com/)

For many open-source projects on GitHub, free integration environments are available.

#### Acceptance Testing
Every package will have different criteria for acceptance. The maintenance committee has particular interest in making sure
that dependents of packages are not impacted by the release of a new version. We encourage liaison between both the
publisher and the dependents where possible.

### Links to some useful tools

* [c8](https://www.npmjs.com/package/c8)
* [citgm](https://www.npmjs.com/package/citgm)
* [Codecov](https://www.npmjs.com/package/codecov)
* [Coveralls](https://www.npmjs.com/package/coveralls)
* [Jest](https://www.npmjs.com/package/jest)
* [Mocha](https://www.npmjs.com/package/mocha)
* [Nock](https://www.npmjs.com/package/nock)
* [nyc](https://www.npmjs.com/package/nyc)
* [tape](https://www.npmjs.com/package/tape)
* [Github CICD](https://docs.github.com/en/actions/building-and-testing-code-with-continuous-integration/about-continuous-integration)
* [Gitlab](https://about.gitlab.com/)
* [Circle CI](https://circleci.com/product/)
* [Travis CI](https://travis-ci.com/)
