# [projects](http://ivans-innovation-lab.github.io/projects)/my-company-project-materialized-view [![CircleCI](https://circleci.com/gh/ivans-innovation-lab/my-company-project-materialized-view.svg?style=svg)](https://circleci.com/gh/ivans-innovation-lab/my-company-project-materialized-view) [![release](http://github-release-version.herokuapp.com/github/ivans-innovation-lab/my-company-project-materialized-view/release.svg?style=flat)](https://github.com/ivans-innovation-lab/my-company-project-materialized-view/releases/latest)

This component is an event-listener and processor. It listens for the Events and processes them in whatever way makes the most sense. In this case it just builds and maintains a **materialized view** which tracks the state of the 'Project' aggregate.

## Development

This project is driven using [Maven][mvn].

[mvn]: https://maven.apache.org/

### Run/Install locally
 
Make sure that you have this libraries installed in your local maven repsoitory:

 - [my-company-common](https://github.com/ivans-innovation-lab/my-company-common)

```bash
$ cd my-company-project-materialized-view
$ ./mvnw clean install
```

### Run tests

This component comes with tests. Use the following command to execute the tests using Maven:

```bash
$ ./mvnw test
```

---
Created by [Ivan Dugalic][idugalic]@[lab][lab].
Need Help?  [Join our Slack team][slack].

[idugalic]: http://idugalic.pro
[lab]: http://lab.idugalic.pro
[slack]: https://communityinviter.com/apps/idugalic/idugalic
[atomist]: https://www.atomist.com/
