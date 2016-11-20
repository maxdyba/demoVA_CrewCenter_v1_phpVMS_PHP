![demoVA](http://i.imgur.com/HSzEXHE.png)

### FOR THE *.TPL* VERSION [CLICK HERE!](http://www.github.com)

demoVA is the all in one FREE theme for CrewCenter by swan58 (Mark Swan) (This version comes with phpVMS 5.5.x.)

demoVA is preloaded with...
  - demoVA Welcome Page Skin
  - phpVMS which comes pre-installed with CrewCenter
  - Mark Swan's CrewCenter

More features...
  - Fully Customisable if you have a general knowledge of HTML, CSS & Basic PHP
  - CrewCenter is Licenced under the MIT Licence!
  - demoVA is licenced under the Attribution-NonCommercial-ShareAlike 
CC BY-NC-SA

    [![CC BY-NC-SA](https://licensebuttons.net/l/by-nc-sa/3.0/88x31.png)](https://nodesource.com/products/nsolid)



## Installation

##### YOU'RE GOING TO NEED TO MAKE A SUBDOMAIN!
Here's a guide on how to make one for cPanel
[CLICK ME!](https://documentation.cpanel.net/display/ALD/Subdomains)

Set the subdomain to crew.yourva.com or fly.yourva.com etc.


Upload the entire .zip onto your webserver (* ONLY if you are using cPanel or any other online FTP service with an extract function*) if not, extract all the files there or on your desktop and upload each file manually via. a FTP program such as [FileZilla](https://filezilla-project.org) or [CyberDuck](https://cyberduck.io/?l=en)

Shove the phpVMS installation into the subdomains folder and leave all other folders out of there and in the main directory (public_html).

phpVMS Installation is pretty straight forward... Once the files are up there just head to crew.yourva.com and follow through with the steps.

If you need to know how to make an SQL database via. cPanel [CLICK HERE!](https://documentation.cpanel.net/display/ALD/MySQL+Databases)

After CrewCenter is installed, if you head to your main domain (yourva.com) you should see the site. A lot of links will need to be changed (This is the part where you need that general knowledge of HTML, if you can't be bothered... Get a mate who has that knowledge to help you out)



```sh
$ cd dillinger
$ npm install -d
$ node app
```

For production environments...

```sh
$ npm install --production
$ npm run predeploy
$ NODE_ENV=production node app
```

### Plugins

Dillinger is currently extended with the following plugins

* Dropbox
* Github
* Google Drive
* OneDrive

Readmes, how to use them in your own application can be found here:

* [plugins/dropbox/README.md] [PlDb]
* [plugins/github/README.md] [PlGh]
* [plugins/googledrive/README.md] [PlGd]
* [plugins/onedrive/README.md] [PlOd]

### Development

Want to contribute? Great!

Dillinger uses Gulp + Webpack for fast developing.
Make a change in your file and instantanously see your updates!

Open your favorite Terminal and run these commands.

First Tab:
```sh
$ node app
```

Second Tab:
```sh
$ gulp watch
```

(optional) Third:
```sh
$ karma start
```
#### Building for source
For production release:
```sh
$ gulp build --prod
```
Generating pre-built zip archives for distribution:
```sh
$ gulp build dist --prod
```
### Docker
Dillinger is very easy to install and deploy in a Docker container.

By default, the Docker will expose port 80, so change this within the Dockerfile if necessary. When ready, simply use the Dockerfile to build the image.

```sh
cd dillinger
npm run-script build-docker
```
This will create the dillinger image and pull in the necessary dependencies. Moreover, this uses a _hack_ to get a more optimized `npm` build by copying the dependencies over and only installing when the `package.json` itself has changed.  Look inside the `package.json` and the `Dockerfile` for more details on how this works.

Once done, run the Docker image and map the port to whatever you wish on your host. In this example, we simply map port 8000 of the host to port 80 of the Docker (or whatever port was exposed in the Dockerfile):

```sh
docker run -d -p 8000:8080 --restart="always" <youruser>/dillinger:latest
```

Verify the deployment by navigating to your server address in your preferred browser.

```sh
127.0.0.1:8000
```

#### Kubernetes + Google Cloud

See [KUBERNETES.md](https://github.com/joemccann/dillinger/blob/master/KUBERNETES.md)


#### docker-compose.yml

Change the path for the nginx conf mounting path to your full path, not mine!

### N|Solid and NGINX

More details coming soon.


### Todos

 - Write Tests
 - Rethink Github Save
 - Add Code Comments
 - Add Night Mode

License
----

MIT


**Free Software, Hell Yeah!**

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)


   [dill]: <https://github.com/joemccann/dillinger>
   [git-repo-url]: <https://github.com/joemccann/dillinger.git>
   [john gruber]: <http://daringfireball.net>
   [@thomasfuchs]: <http://twitter.com/thomasfuchs>
   [df1]: <http://daringfireball.net/projects/markdown/>
   [markdown-it]: <https://github.com/markdown-it/markdown-it>
   [Ace Editor]: <http://ace.ajax.org>
   [node.js]: <http://nodejs.org>
   [Twitter Bootstrap]: <http://twitter.github.com/bootstrap/>
   [keymaster.js]: <https://github.com/madrobby/keymaster>
   [jQuery]: <http://jquery.com>
   [@tjholowaychuk]: <http://twitter.com/tjholowaychuk>
   [express]: <http://expressjs.com>
   [AngularJS]: <http://angularjs.org>
   [Gulp]: <http://gulpjs.com>

   [PlDb]: <https://github.com/joemccann/dillinger/tree/master/plugins/dropbox/README.md>
   [PlGh]:  <https://github.com/joemccann/dillinger/tree/master/plugins/github/README.md>
   [PlGd]: <https://github.com/joemccann/dillinger/tree/master/plugins/googledrive/README.md>
   [PlOd]: <https://github.com/joemccann/dillinger/tree/master/plugins/onedrive/README.md>
