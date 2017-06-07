# my-company-project-materialized-view [![CircleCI](https://circleci.com/gh/ivans-innovation-lab/my-company-project-materialized-view.svg?style=svg)](https://circleci.com/gh/ivans-innovation-lab/my-company-project-materialized-view) [![release](http://github-release-version.herokuapp.com/github/ivans-innovation-lab/my-company-project-materialized-view/release.svg?style=flat)](https://github.com/ivans-innovation-lab/my-company-project-materialized-view/releases/latest)

This component is an event-listener and processor. It listens for the Events and processes them in whatever way makes the most sense. In this case it just builds and maintains a **materialized view** which tracks the state of the 'Project' aggregate.

## Running instructions / Installation
 
Make sure that you have this libraries installed in your local maven repsoitory:

 - [my-company-common](https://github.com/ivans-innovation-lab/my-company-common)

```bash
$ cd my-company-project-materialized-view
$ ./mvnw clean install
```
