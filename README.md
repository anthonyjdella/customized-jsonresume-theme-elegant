# Customized JSON Resume Theme: Elegant

🖼️ This is a tweaked version of the [Elegant theme](https://github.com/mudassir0909/jsonresume-theme-elegant). Tweaked to fit my design preferences.

## Notable Changes

* 2 Page version in PDF/printable mode 
* Added sections for speaking and articles
* Style changes

## Prerequisites

To build and start the local server, it needs to use the cli command, which is custom cli I tweaked.

`npm i @anthonyjdella/customized-resume-cli`

## How to Start

To re-build HTML changes, execute: `grunt exec:compile_pug`

To re-build CSS changes, execute: `grunt less`

Then to start,

`npm run start` for localhost:4000 

or `grunt exec:run_server` for localhost:8080


## How to Change

* `index.js` is the order of the resume. Also make changes to `background-card.pug`
* `pug/` are the html files for each section. To re-build HTML changes, execute: `grunt exec:compile_pug`
* `assets/less` is the styling. To re-build CSS changes, execute: `grunt less`
* To make changes to the PDF/printable version, make changes in the `@print` section of `assets/less/print.less`
* Change version number in `package.json`
* Deploy the changes via `npm publish --access public`
* To see changes from `resume.anthonydellavecchia.com` you need to go to the [registry project](https://github.com/anthonyjdella/customized-registry-functions), then cd into `functions`, run `npm i` and `npm update`, then `firebase deploy`.

<details>
  <summary>Click to expand README.md of the source repository!</summary>

# Elegant Theme [![npm version](https://badge.fury.io/js/jsonresume-theme-elegant.svg)](http://badge.fury.io/js/jsonresume-theme-elegant)

Responsive theme for [JsonResume](https://jsonresume.org/) inspired by card layouts.

[Theme Preview](http://themes.jsonresume.org/theme/elegant)

### Markdown Supported
Supported in the following properties `resume.basics.summary`, `work[0].summary`, `work[0].highlights`, `projects[0].summary`, `projects[0].highlights`, `education[0].courses`, `volunteer[0].summary`, `volunteer[0].highlights`, `awards[0].summary`, `publications[0].summary`, `references[0].reference`, `skills[0].keywords`. If you have any other use case, please raise an issue

### Social Profiles
The profiles are shown in the order in which they are specified in the `basics.profiles` array. By default, only 5 profiles are shown & others are revealed on demand.

![Profile Section](https://raw.githubusercontent.com/mudassir0909/jsonresume-theme-elegant/master/screenshots/profile.png)

#### Supported Profiles
* angellist
* behance
* bitbucket
* blogger
* codepen
* dribbble
* dribble
* exercism
* facebook
* flickr
* foursquare
* github
* gitlab
* googleplus
* gratipay
* hackernews
* instagram
* lastfm
* linkedin
* medium
* meetup
* pinterest
* reddit
* skype
* soundcloud
* spotify
* stackexchange
* stackoverflow
* telegram
* tumblr
* twitter
* vimeo
* youtube

### Credits
* Thank you [contributors](https://github.com/mudassir0909/jsonresume-theme-elegant/graphs/contributors) for your pull requests
* Floating Menu: inspired by [Smart Fixed Navigation](http://codyhouse.co/demo/smart-fixed-navigation/index.html)

### Contributing
```
$ npm install -g grunt
$ npm install -g pug-cli
$ git clone https://github.com/mudassir0909/jsonresume-theme-elegant.git
$ cd jsonresume-theme-elegant
$ npm install
$ grunt watch // watches for file changes in *.pug & *.less
$ grunt exec:run_server // Do this in a new terminal tab to run node server
```

Visit [http://localhost:8888](http://localhost:8888) to see the theme in action.

[![Throughput Graph](https://graphs.waffle.io/mudassir0909/jsonresume-theme-elegant/throughput.svg)](https://waffle.io/mudassir0909/jsonresume-theme-elegant/metrics)

##### Testing JSON changes
You can test your changes by updating `resume.json` file inside `node_modules/resume-schema/` folder. You might want to rerun `grunt exec:run_server` whenever you make any changes to `resume.json`

##### Updating Styles
All the LESS files are organized under the folder `assets/less/`. Please go through the comments inside `theme.less` to find out which file to put your LESS changes. Grunt compiles `assets/less/theme.less` to `assets/css/theme.css` which is used eventually in the theme.

**_Please Do not make any changes inside `assets/css/theme.css`_**

##### Updating Javascript
All the javascript changes go into `index.js` which is responsible for rendering the theme.

##### Adding a new icon
Visit this [wiki page](https://github.com/mudassir0909/jsonresume-theme-elegant/wiki/Adding-a-new-icon)

### Roadmap

[https://github.com/mudassir0909/jsonresume-theme-elegant/labels/enhancement](https://github.com/mudassir0909/jsonresume-theme-elegant/labels/enhancement)
  
</details>
