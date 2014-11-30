
This is a fork from: [https://github.com/mashery/iodocs](https://github.com/mashery/iodocs)

iodocs are used for the [live documention of the dxc4 API](http://apidocs.dxc4.com).
The api is available at [api.dxc4.com](http://api.dxc4.com)
A demo client is running here at [dxc4.com](http://dxc4.com)

BUILD/RUNTIME DEPENDENCIES
--------------------------
1. Node.js - server-side JS engine
2. npm - node package manager
3. Redis - key+value storage engine 

Build note: If you're not using a package manager, Node and some of the modules require compiler (like gcc). If you are on a Mac, you will need to install XCode. If you're on Linux, you'll need to install build-essentials, or something equivalent.

Redis note: Redis is considered a runtime dependency. It is used to store OAuth information server side. If you are not implementing OAuth, redis is not required. You can simply remove the redis block from config.json. However, if you do implement OAuth down the road, you will need to use Redis, otherwise you will see 500 errors during the auth dance.

INSTALLATION INSTRUCTIONS FOR NODE, NPM & REDIS
-----------------------------------------------
1. Node.js - [https://github.com/joyent/node/wiki/Installation](https://github.com/joyent/node/wiki/Installation)
2. npm (Node package manager) - [https://github.com/isaacs/npm](https://github.com/isaacs/npm)
(3. Redis - [http://redis.io/download](http://redis.io/download))

INSTALLATION INSTRUCTIONS FOR I/O DOCS
--------------------------------------
From the command line type in:
<pre>  git clone http://github.com/mashery/iodocs.git
  cd iodocs
  npm install
</pre>



RUNNING I/O DOCS
----------------
**Create your config** file by copying the default config:

```
cp config.json.sample config.json
```
The defaults will work, but feel free to change them.
IMPORTANT: If you do not use redis remove the corresponding settings from the config.

**Start I/O Docs**:

```
npm start (*nix, Mac OSX)
```

**Point your browser** to: [localhost:3000](http://localhost:3000)

CONFIGURING API DEFINITION LOCATION
-----------------------------------
API definitions are, by default, stored in `./public/data/` and described by `./public/data/"apiName".json` and referenced by `./public/data/apiconfig.json`. This can
be overridden in `config.json` by setting the `"apiConfigDir"` property.

SUPPORT
=======
If you need any help with I/O Docs, you can reach out to us via the GitHub Issues page at:
<code>[http://github.com/mashery/iodocs/issues](http://github.com/mashery/iodocs/issues)</code>
