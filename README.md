[![Dependency Status](https://david-dm.org/jdalrymple/node-gitlab-api/status.svg)](https://david-dm.org/jdalrymple/node-test#info=dependencies) [![devDependency Status](https://david-dm.org/jdalrymple/node-gitlab-api/dev-status.svg)](https://david-dm.org/jdalrymple/node-test#info=devDependencies)

node-gitlab-api
===============

--

[GitLab](https://github.com/gitlabhq/gitlabhq) API Nodejs library.
It wraps the HTTP v4 api library described [here](https://github.com/gitlabhq/gitlabhq/tree/master/doc/api).

Install
=======

```bash
# Install from npm
npm install gitlab
```

Usage
=====

URL to your GitLab instance should not include `/api/v4` path.

```javascript
// Connection
const GitlabAPI = require('gitlab-api')({
  url:   'http://example.com', // Defaults to http://gitlab.com
  token: 'abcdefghij123456'
})
  
// Listing users
let users = await gitlab.users.all();

console.log(users);

// Listing projects
let projects = await gitlab.projects.all();

console.log(projects);
```

Contributors
------------
This started off as a fork from [node-gitlab](https://github.com/node-gitlab/node-gitlab) but I ended up rewriting 90% of the code. Here are the original work's [contributers](https://github.com/node-gitlab/node-gitlab#contributors).


License
-------

MIT

Changelog
=========

[1.0.3](https://github.com/jdalrymple/node-gitlab-api/commit/fe5a5fbb8d01fb670b7c7b14ce2c5b7f30d71fe5) (2017-06-23)
------------------
- Updating problems within the Milestone API

[1.0.2](https://github.com/jdalrymple/node-gitlab-api/commit/a295d5a613efa13be79fec5fa2835076047cdcc5) (2017-06-22)
------------------
- Updating examples in readme
- Adding dependancy badges
- Removing unused test files

[1.0.1](https://github.com/jdalrymple/node-gitlab-api/commit/64a8f8c7720f5df9a67d3f26cc8712fc21eb3ac0) (2017-06-21)
------------------
- Initial release
- TODO: Tests, Examples

