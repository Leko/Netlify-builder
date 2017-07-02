# Netlify build trigger
Trigger [Netlify](https://www.netlify.com/) build at a certain period.

This repository can be used for reservation posting on a static site, etc.

## Usage
### Setup account
Create those service's account

- [Netlify](https://www.netlify.com/)
- [Heroku](https://www.heroku.com/)

### Setup Netlify
Create build hooks in admin console.

![screenshot](https://raw.githubusercontent.com/Leko/Netlify-builder/master/screenshots/deployhook.png)

### Deploy trigger app
Click this button

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)

When deploy was finished, open Heroku scheduler admin.  
Click "Add net job" and 

|Label|Value|
|`$`|`curl -v -X POST -d '{"files": {}}' $BUILD_HOOK_URL`|
|DYNO SIZE|`Free`|
|FREQUENCY|Choose build interval you want|
|NEXT DUE|Choose build at you want|

![screenshot](https://raw.githubusercontent.com/Leko/Netlify-builder/master/screenshots/job.png)

### Setup done
Wait for about 1 hour.  
View your Netlify builds, 

![screenshot](https://raw.githubusercontent.com/Leko/Netlify-builder/master/screenshots/deploys.png)

It works fine.

## More information
- [NetlifyとHerokuで予約投稿機能を実現する](https://blog.leko.jp/post/automate-build-netlify-with-heroku)

## Contribution
1. Fork this repository
1. Create your branch
1. Write your code
1. Send pull request to `master` branch

## License
MIT
