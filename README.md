# api documentation for  [mongodb (v2.2.25)](https://github.com/mongodb/node-mongodb-native)  [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-mongodb.svg)](https://travis-ci.org/npmdoc/node-npmdoc-mongodb)
#### The official MongoDB driver for Node.js

[![NPM](https://nodei.co/npm/mongodb.png?downloads=true)](https://www.npmjs.com/package/mongodb)

[![apidoc](https://npmdoc.github.io/node-npmdoc-mongodb/build/screen-capture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-mongodb_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-mongodb/build..beta..travis-ci.org/apidoc.html)

![package-listing](https://npmdoc.github.io/node-npmdoc-mongodb/build/screen-capture.npmPackageListing.svg)



# package.json

```json

{
    "author": {
        "name": "Christian Kvalheim"
    },
    "bugs": {
        "url": "https://github.com/mongodb/node-mongodb-native/issues"
    },
    "dependencies": {
        "es6-promise": "3.2.1",
        "mongodb-core": "2.1.9",
        "readable-stream": "2.1.5"
    },
    "description": "The official MongoDB driver for Node.js",
    "devDependencies": {
        "JSONStream": "^1.0.7",
        "betterbenchmarks": "^0.1.0",
        "bluebird": "3.4.6",
        "bson": "latest",
        "cli-table": "^0.3.1",
        "co": "4.6.0",
        "colors": "^1.1.2",
        "coveralls": "^2.11.6",
        "eslint": "^3.8.1",
        "event-stream": "^3.3.2",
        "gleak": "0.5.0",
        "integra": "0.1.8",
        "jsdoc": "3.4.0",
        "ldjson-stream": "^1.2.1",
        "mongodb-extended-json": "1.7.1",
        "mongodb-topology-manager": "1.0.x",
        "mongodb-version-manager": "github:christkv/mongodb-version-manager#master",
        "nyc": "^8.1.0",
        "optimist": "0.6.1",
        "rimraf": "2.5.4",
        "semver": "5.3.0",
        "worker-farm": "^1.3.1"
    },
    "directories": {},
    "dist": {
        "shasum": "d3b25dad00eda2bdfcbc996210ba082ac686a6b6",
        "tarball": "https://registry.npmjs.org/mongodb/-/mongodb-2.2.25.tgz"
    },
    "engines": {
        "node": ">=0.10.3"
    },
    "gitHead": "915d5c8a765151fb14942445a92d92a0e9e9c942",
    "homepage": "https://github.com/mongodb/node-mongodb-native",
    "keywords": [
        "mongodb",
        "driver",
        "official"
    ],
    "license": "Apache-2.0",
    "main": "index.js",
    "maintainers": [
        {
            "name": "christkv",
            "email": "christkv@gmail.com"
        }
    ],
    "name": "mongodb",
    "nyc": {
        "include": [
            "lib/**/*.js"
        ]
    },
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+ssh://git@github.com/mongodb/node-mongodb-native.git"
    },
    "scripts": {
        "coverage": "nyc node test/runner.js -t functional && node_modules/.bin/nyc report --reporter=text-lcov | node_modules/.bin/coveralls",
        "lint": "eslint lib",
        "test": "node test/runner.js -t functional -l"
    },
    "version": "2.2.25"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module mongodb](#apidoc.module.mongodb)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>Admin (db, topology, promiseLibrary)](#apidoc.element.mongodb.Admin)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>BSONRegExp (pattern, options)](#apidoc.element.mongodb.BSONRegExp)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>Binary (buffer, subType)](#apidoc.element.mongodb.Binary)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>Chunk (file, mongoObject, writeConcern)](#apidoc.element.mongodb.Chunk)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>Code (code, scope)](#apidoc.element.mongodb.Code)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>Collection (db, topology, dbName, name, pkFactory, options)](#apidoc.element.mongodb.Collection)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>CoreConnection (messageHandler, options)](#apidoc.element.mongodb.CoreConnection)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>CoreServer (options)](#apidoc.element.mongodb.CoreServer)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>Cursor (bson, ns, cmd, options, topology, topologyOptions)](#apidoc.element.mongodb.Cursor)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>DBRef (namespace, oid, db)](#apidoc.element.mongodb.DBRef)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>Db (databaseName, topology, options)](#apidoc.element.mongodb.Db)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>Decimal128 (bytes)](#apidoc.element.mongodb.Decimal128)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>Double (value)](#apidoc.element.mongodb.Double)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>GridFSBucket (db, options)](#apidoc.element.mongodb.GridFSBucket)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>GridStore (db, id, filename, mode, options)](#apidoc.element.mongodb.GridStore)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>Int32 (value)](#apidoc.element.mongodb.Int32)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>Logger (className, options)](#apidoc.element.mongodb.Logger)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>Long (low, high)](#apidoc.element.mongodb.Long)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>Map ()](#apidoc.element.mongodb.Map)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>MaxKey ()](#apidoc.element.mongodb.MaxKey)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>MinKey ()](#apidoc.element.mongodb.MinKey)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>MongoClient ()](#apidoc.element.mongodb.MongoClient)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>MongoError (message)](#apidoc.element.mongodb.MongoError)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>Mongos (servers, options)](#apidoc.element.mongodb.Mongos)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>ObjectID (id)](#apidoc.element.mongodb.ObjectID)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>ObjectId (id)](#apidoc.element.mongodb.ObjectId)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>ReadPreference (mode, tags, options)](#apidoc.element.mongodb.ReadPreference)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>ReplSet (servers, options)](#apidoc.element.mongodb.ReplSet)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>Server (host, port, options)](#apidoc.element.mongodb.Server)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>Symbol (value)](#apidoc.element.mongodb.Symbol)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>Timestamp (low, high)](#apidoc.element.mongodb.Timestamp)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>aggregation_cursor (bson, ns, cmd, options, topology, topologyOptions)](#apidoc.element.mongodb.aggregation_cursor)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>apm (core, options, callback)](#apidoc.element.mongodb.apm)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>command_cursor (bson, ns, cmd, options, topology, topologyOptions)](#apidoc.element.mongodb.command_cursor)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>connect (url, options, callback)](#apidoc.element.mongodb.connect)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>instrument (options, callback)](#apidoc.element.mongodb.instrument)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>metadata (name, object, stream)](#apidoc.element.mongodb.metadata)
1.  object <span class="apidocSignatureSpan">mongodb.</span>Admin.define
1.  object <span class="apidocSignatureSpan">mongodb.</span>Admin.prototype
1.  object <span class="apidocSignatureSpan">mongodb.</span>Binary.prototype
1.  object <span class="apidocSignatureSpan">mongodb.</span>Chunk.prototype
1.  object <span class="apidocSignatureSpan">mongodb.</span>Code.prototype
1.  object <span class="apidocSignatureSpan">mongodb.</span>Collection.define
1.  object <span class="apidocSignatureSpan">mongodb.</span>Collection.prototype
1.  object <span class="apidocSignatureSpan">mongodb.</span>CoreConnection.prototype
1.  object <span class="apidocSignatureSpan">mongodb.</span>CoreServer.prototype
1.  object <span class="apidocSignatureSpan">mongodb.</span>Cursor.define
1.  object <span class="apidocSignatureSpan">mongodb.</span>Cursor.prototype
1.  object <span class="apidocSignatureSpan">mongodb.</span>DBRef.prototype
1.  object <span class="apidocSignatureSpan">mongodb.</span>Db.define
1.  object <span class="apidocSignatureSpan">mongodb.</span>Db.prototype
1.  object <span class="apidocSignatureSpan">mongodb.</span>Decimal128.prototype
1.  object <span class="apidocSignatureSpan">mongodb.</span>Double.prototype
1.  object <span class="apidocSignatureSpan">mongodb.</span>GridFSBucket.prototype
1.  object <span class="apidocSignatureSpan">mongodb.</span>GridStore.define
1.  object <span class="apidocSignatureSpan">mongodb.</span>GridStore.prototype
1.  object <span class="apidocSignatureSpan">mongodb.</span>Int32.prototype
1.  object <span class="apidocSignatureSpan">mongodb.</span>Logger.prototype
1.  object <span class="apidocSignatureSpan">mongodb.</span>Long.prototype
1.  object <span class="apidocSignatureSpan">mongodb.</span>MongoClient.define
1.  object <span class="apidocSignatureSpan">mongodb.</span>Mongos.define
1.  object <span class="apidocSignatureSpan">mongodb.</span>Mongos.prototype
1.  object <span class="apidocSignatureSpan">mongodb.</span>ObjectID.prototype
1.  object <span class="apidocSignatureSpan">mongodb.</span>ReadPreference.prototype
1.  object <span class="apidocSignatureSpan">mongodb.</span>ReplSet.define
1.  object <span class="apidocSignatureSpan">mongodb.</span>ReplSet.prototype
1.  object <span class="apidocSignatureSpan">mongodb.</span>Server.define
1.  object <span class="apidocSignatureSpan">mongodb.</span>Server.prototype
1.  object <span class="apidocSignatureSpan">mongodb.</span>Symbol.prototype
1.  object <span class="apidocSignatureSpan">mongodb.</span>Timestamp.prototype
1.  object <span class="apidocSignatureSpan">mongodb.</span>aggregation_cursor.prototype
1.  object <span class="apidocSignatureSpan">mongodb.</span>apm.prototype
1.  object <span class="apidocSignatureSpan">mongodb.</span>command_cursor.prototype
1.  object <span class="apidocSignatureSpan">mongodb.</span>metadata.prototype
1.  object <span class="apidocSignatureSpan">mongodb.</span>topology_base
1.  object <span class="apidocSignatureSpan">mongodb.</span>utils

#### [module mongodb.Admin](#apidoc.module.mongodb.Admin)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>Admin (db, topology, promiseLibrary)](#apidoc.element.mongodb.Admin.Admin)
1.  object <span class="apidocSignatureSpan">mongodb.Admin.</span>define

#### [module mongodb.Admin.define](#apidoc.module.mongodb.Admin.define)
1.  boolean <span class="apidocSignatureSpan">mongodb.Admin.define.</span>stream
1.  [function <span class="apidocSignatureSpan">mongodb.Admin.define.</span>object (db, topology, promiseLibrary)](#apidoc.element.mongodb.Admin.define.object)
1.  object <span class="apidocSignatureSpan">mongodb.Admin.define.</span>instrumentations
1.  string <span class="apidocSignatureSpan">mongodb.Admin.define.</span>name

#### [module mongodb.Admin.prototype](#apidoc.module.mongodb.Admin.prototype)
1.  [function <span class="apidocSignatureSpan">mongodb.Admin.prototype.</span>addUser (username, password, options, callback)](#apidoc.element.mongodb.Admin.prototype.addUser)
1.  [function <span class="apidocSignatureSpan">mongodb.Admin.prototype.</span>authenticate (username, password, options, callback)](#apidoc.element.mongodb.Admin.prototype.authenticate)
1.  [function <span class="apidocSignatureSpan">mongodb.Admin.prototype.</span>buildInfo (callback)](#apidoc.element.mongodb.Admin.prototype.buildInfo)
1.  [function <span class="apidocSignatureSpan">mongodb.Admin.prototype.</span>command (command, options, callback)](#apidoc.element.mongodb.Admin.prototype.command)
1.  [function <span class="apidocSignatureSpan">mongodb.Admin.prototype.</span>listDatabases (callback)](#apidoc.element.mongodb.Admin.prototype.listDatabases)
1.  [function <span class="apidocSignatureSpan">mongodb.Admin.prototype.</span>logout (callback)](#apidoc.element.mongodb.Admin.prototype.logout)
1.  [function <span class="apidocSignatureSpan">mongodb.Admin.prototype.</span>ping (options, callback)](#apidoc.element.mongodb.Admin.prototype.ping)
1.  [function <span class="apidocSignatureSpan">mongodb.Admin.prototype.</span>profilingInfo (callback)](#apidoc.element.mongodb.Admin.prototype.profilingInfo)
1.  [function <span class="apidocSignatureSpan">mongodb.Admin.prototype.</span>profilingLevel (callback)](#apidoc.element.mongodb.Admin.prototype.profilingLevel)
1.  [function <span class="apidocSignatureSpan">mongodb.Admin.prototype.</span>removeUser (username, options, callback)](#apidoc.element.mongodb.Admin.prototype.removeUser)
1.  [function <span class="apidocSignatureSpan">mongodb.Admin.prototype.</span>replSetGetStatus (callback)](#apidoc.element.mongodb.Admin.prototype.replSetGetStatus)
1.  [function <span class="apidocSignatureSpan">mongodb.Admin.prototype.</span>serverInfo (callback)](#apidoc.element.mongodb.Admin.prototype.serverInfo)
1.  [function <span class="apidocSignatureSpan">mongodb.Admin.prototype.</span>serverStatus (callback)](#apidoc.element.mongodb.Admin.prototype.serverStatus)
1.  [function <span class="apidocSignatureSpan">mongodb.Admin.prototype.</span>setProfilingLevel (level, callback)](#apidoc.element.mongodb.Admin.prototype.setProfilingLevel)
1.  [function <span class="apidocSignatureSpan">mongodb.Admin.prototype.</span>validateCollection (collectionName, options, callback)](#apidoc.element.mongodb.Admin.prototype.validateCollection)

#### [module mongodb.BSONRegExp](#apidoc.module.mongodb.BSONRegExp)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>BSONRegExp (pattern, options)](#apidoc.element.mongodb.BSONRegExp.BSONRegExp)

#### [module mongodb.Binary](#apidoc.module.mongodb.Binary)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>Binary (buffer, subType)](#apidoc.element.mongodb.Binary.Binary)
1.  number <span class="apidocSignatureSpan">mongodb.Binary.</span>BUFFER_SIZE
1.  number <span class="apidocSignatureSpan">mongodb.Binary.</span>SUBTYPE_BYTE_ARRAY
1.  number <span class="apidocSignatureSpan">mongodb.Binary.</span>SUBTYPE_DEFAULT
1.  number <span class="apidocSignatureSpan">mongodb.Binary.</span>SUBTYPE_FUNCTION
1.  number <span class="apidocSignatureSpan">mongodb.Binary.</span>SUBTYPE_MD5
1.  number <span class="apidocSignatureSpan">mongodb.Binary.</span>SUBTYPE_USER_DEFINED
1.  number <span class="apidocSignatureSpan">mongodb.Binary.</span>SUBTYPE_UUID
1.  number <span class="apidocSignatureSpan">mongodb.Binary.</span>SUBTYPE_UUID_OLD

#### [module mongodb.Binary.prototype](#apidoc.module.mongodb.Binary.prototype)
1.  [function <span class="apidocSignatureSpan">mongodb.Binary.prototype.</span>length ()](#apidoc.element.mongodb.Binary.prototype.length)
1.  [function <span class="apidocSignatureSpan">mongodb.Binary.prototype.</span>put (byte_value)](#apidoc.element.mongodb.Binary.prototype.put)
1.  [function <span class="apidocSignatureSpan">mongodb.Binary.prototype.</span>read (position, length)](#apidoc.element.mongodb.Binary.prototype.read)
1.  [function <span class="apidocSignatureSpan">mongodb.Binary.prototype.</span>toJSON ()](#apidoc.element.mongodb.Binary.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">mongodb.Binary.prototype.</span>toString (format)](#apidoc.element.mongodb.Binary.prototype.toString)
1.  [function <span class="apidocSignatureSpan">mongodb.Binary.prototype.</span>value (asRaw)](#apidoc.element.mongodb.Binary.prototype.value)
1.  [function <span class="apidocSignatureSpan">mongodb.Binary.prototype.</span>write (string, offset)](#apidoc.element.mongodb.Binary.prototype.write)

#### [module mongodb.Chunk](#apidoc.module.mongodb.Chunk)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>Chunk (file, mongoObject, writeConcern)](#apidoc.element.mongodb.Chunk.Chunk)
1.  number <span class="apidocSignatureSpan">mongodb.Chunk.</span>DEFAULT_CHUNK_SIZE

#### [module mongodb.Chunk.prototype](#apidoc.module.mongodb.Chunk.prototype)
1.  [function <span class="apidocSignatureSpan">mongodb.Chunk.prototype.</span>buildMongoObject (callback)](#apidoc.element.mongodb.Chunk.prototype.buildMongoObject)
1.  [function <span class="apidocSignatureSpan">mongodb.Chunk.prototype.</span>eof ()](#apidoc.element.mongodb.Chunk.prototype.eof)
1.  [function <span class="apidocSignatureSpan">mongodb.Chunk.prototype.</span>getc ()](#apidoc.element.mongodb.Chunk.prototype.getc)
1.  [function <span class="apidocSignatureSpan">mongodb.Chunk.prototype.</span>length ()](#apidoc.element.mongodb.Chunk.prototype.length)
1.  [function <span class="apidocSignatureSpan">mongodb.Chunk.prototype.</span>read (length)](#apidoc.element.mongodb.Chunk.prototype.read)
1.  [function <span class="apidocSignatureSpan">mongodb.Chunk.prototype.</span>readSlice (length)](#apidoc.element.mongodb.Chunk.prototype.readSlice)
1.  [function <span class="apidocSignatureSpan">mongodb.Chunk.prototype.</span>rewind ()](#apidoc.element.mongodb.Chunk.prototype.rewind)
1.  [function <span class="apidocSignatureSpan">mongodb.Chunk.prototype.</span>save (options, callback)](#apidoc.element.mongodb.Chunk.prototype.save)
1.  [function <span class="apidocSignatureSpan">mongodb.Chunk.prototype.</span>write (data, callback)](#apidoc.element.mongodb.Chunk.prototype.write)

#### [module mongodb.Code](#apidoc.module.mongodb.Code)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>Code (code, scope)](#apidoc.element.mongodb.Code.Code)

#### [module mongodb.Code.prototype](#apidoc.module.mongodb.Code.prototype)
1.  [function <span class="apidocSignatureSpan">mongodb.Code.prototype.</span>toJSON ()](#apidoc.element.mongodb.Code.prototype.toJSON)

#### [module mongodb.Collection](#apidoc.module.mongodb.Collection)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>Collection (db, topology, dbName, name, pkFactory, options)](#apidoc.element.mongodb.Collection.Collection)
1.  object <span class="apidocSignatureSpan">mongodb.Collection.</span>define

#### [module mongodb.Collection.define](#apidoc.module.mongodb.Collection.define)
1.  boolean <span class="apidocSignatureSpan">mongodb.Collection.define.</span>stream
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.define.</span>object (db, topology, dbName, name, pkFactory, options)](#apidoc.element.mongodb.Collection.define.object)
1.  object <span class="apidocSignatureSpan">mongodb.Collection.define.</span>instrumentations
1.  string <span class="apidocSignatureSpan">mongodb.Collection.define.</span>name

#### [module mongodb.Collection.prototype](#apidoc.module.mongodb.Collection.prototype)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>aggregate (pipeline, options, callback)](#apidoc.element.mongodb.Collection.prototype.aggregate)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>bulkWrite (operations, options, callback)](#apidoc.element.mongodb.Collection.prototype.bulkWrite)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>count (query, options, callback)](#apidoc.element.mongodb.Collection.prototype.count)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>createIndex (fieldOrSpec, options, callback)](#apidoc.element.mongodb.Collection.prototype.createIndex)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>createIndexes (indexSpecs, callback)](#apidoc.element.mongodb.Collection.prototype.createIndexes)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>deleteMany (filter, options, callback)](#apidoc.element.mongodb.Collection.prototype.deleteMany)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>deleteOne (filter, options, callback)](#apidoc.element.mongodb.Collection.prototype.deleteOne)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>distinct (key, query, options, callback)](#apidoc.element.mongodb.Collection.prototype.distinct)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>drop (options, callback)](#apidoc.element.mongodb.Collection.prototype.drop)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>dropAllIndexes (options, callback)](#apidoc.element.mongodb.Collection.prototype.dropAllIndexes)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>dropIndex (indexName, options, callback)](#apidoc.element.mongodb.Collection.prototype.dropIndex)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>dropIndexes (options, callback)](#apidoc.element.mongodb.Collection.prototype.dropIndexes)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>ensureIndex (fieldOrSpec, options, callback)](#apidoc.element.mongodb.Collection.prototype.ensureIndex)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>find ()](#apidoc.element.mongodb.Collection.prototype.find)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>findAndModify (query, sort, doc, options, callback)](#apidoc.element.mongodb.Collection.prototype.findAndModify)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>findAndRemove (query, sort, options, callback)](#apidoc.element.mongodb.Collection.prototype.findAndRemove)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>findOne ()](#apidoc.element.mongodb.Collection.prototype.findOne)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>findOneAndDelete (filter, options, callback)](#apidoc.element.mongodb.Collection.prototype.findOneAndDelete)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>findOneAndReplace (filter, replacement, options, callback)](#apidoc.element.mongodb.Collection.prototype.findOneAndReplace)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>findOneAndUpdate (filter, update, options, callback)](#apidoc.element.mongodb.Collection.prototype.findOneAndUpdate)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>geoHaystackSearch (x, y, options, callback)](#apidoc.element.mongodb.Collection.prototype.geoHaystackSearch)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>geoNear (x, y, options, callback)](#apidoc.element.mongodb.Collection.prototype.geoNear)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>group (keys, condition, initial, reduce, finalize, command, options, callback)](#apidoc.element.mongodb.Collection.prototype.group)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>indexExists (indexes, callback)](#apidoc.element.mongodb.Collection.prototype.indexExists)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>indexInformation (options, callback)](#apidoc.element.mongodb.Collection.prototype.indexInformation)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>indexes (callback)](#apidoc.element.mongodb.Collection.prototype.indexes)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>initializeOrderedBulkOp (options)](#apidoc.element.mongodb.Collection.prototype.initializeOrderedBulkOp)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>initializeUnorderedBulkOp (options)](#apidoc.element.mongodb.Collection.prototype.initializeUnorderedBulkOp)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>insert (docs, options, callback)](#apidoc.element.mongodb.Collection.prototype.insert)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>insertMany (docs, options, callback)](#apidoc.element.mongodb.Collection.prototype.insertMany)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>insertOne (doc, options, callback)](#apidoc.element.mongodb.Collection.prototype.insertOne)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>isCapped (callback)](#apidoc.element.mongodb.Collection.prototype.isCapped)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>listIndexes (options)](#apidoc.element.mongodb.Collection.prototype.listIndexes)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>mapReduce (map, reduce, options, callback)](#apidoc.element.mongodb.Collection.prototype.mapReduce)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>options (callback)](#apidoc.element.mongodb.Collection.prototype.options)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>parallelCollectionScan (options, callback)](#apidoc.element.mongodb.Collection.prototype.parallelCollectionScan)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>reIndex (options, callback)](#apidoc.element.mongodb.Collection.prototype.reIndex)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>remove (selector, options, callback)](#apidoc.element.mongodb.Collection.prototype.remove)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>removeMany (filter, options, callback)](#apidoc.element.mongodb.Collection.prototype.removeMany)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>removeOne (filter, options, callback)](#apidoc.element.mongodb.Collection.prototype.removeOne)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>rename (newName, opt, callback)](#apidoc.element.mongodb.Collection.prototype.rename)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>replaceOne (filter, doc, options, callback)](#apidoc.element.mongodb.Collection.prototype.replaceOne)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>save (doc, options, callback)](#apidoc.element.mongodb.Collection.prototype.save)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>stats (options, callback)](#apidoc.element.mongodb.Collection.prototype.stats)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>update (selector, document, options, callback)](#apidoc.element.mongodb.Collection.prototype.update)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>updateMany (filter, update, options, callback)](#apidoc.element.mongodb.Collection.prototype.updateMany)
1.  [function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>updateOne (filter, update, options, callback)](#apidoc.element.mongodb.Collection.prototype.updateOne)

#### [module mongodb.CoreConnection](#apidoc.module.mongodb.CoreConnection)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>CoreConnection (messageHandler, options)](#apidoc.element.mongodb.CoreConnection.CoreConnection)
1.  [function <span class="apidocSignatureSpan">mongodb.CoreConnection.</span>connections ()](#apidoc.element.mongodb.CoreConnection.connections)
1.  [function <span class="apidocSignatureSpan">mongodb.CoreConnection.</span>disableConnectionAccounting ()](#apidoc.element.mongodb.CoreConnection.disableConnectionAccounting)
1.  [function <span class="apidocSignatureSpan">mongodb.CoreConnection.</span>enableConnectionAccounting ()](#apidoc.element.mongodb.CoreConnection.enableConnectionAccounting)
1.  [function <span class="apidocSignatureSpan">mongodb.CoreConnection.</span>super_ ()](#apidoc.element.mongodb.CoreConnection.super_)

#### [module mongodb.CoreConnection.prototype](#apidoc.module.mongodb.CoreConnection.prototype)
1.  [function <span class="apidocSignatureSpan">mongodb.CoreConnection.prototype.</span>connect (_options)](#apidoc.element.mongodb.CoreConnection.prototype.connect)
1.  [function <span class="apidocSignatureSpan">mongodb.CoreConnection.prototype.</span>destroy ()](#apidoc.element.mongodb.CoreConnection.prototype.destroy)
1.  [function <span class="apidocSignatureSpan">mongodb.CoreConnection.prototype.</span>isConnected ()](#apidoc.element.mongodb.CoreConnection.prototype.isConnected)
1.  [function <span class="apidocSignatureSpan">mongodb.CoreConnection.prototype.</span>resetSocketTimeout ()](#apidoc.element.mongodb.CoreConnection.prototype.resetSocketTimeout)
1.  [function <span class="apidocSignatureSpan">mongodb.CoreConnection.prototype.</span>setSocketTimeout (value)](#apidoc.element.mongodb.CoreConnection.prototype.setSocketTimeout)
1.  [function <span class="apidocSignatureSpan">mongodb.CoreConnection.prototype.</span>toJSON ()](#apidoc.element.mongodb.CoreConnection.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">mongodb.CoreConnection.prototype.</span>toString ()](#apidoc.element.mongodb.CoreConnection.prototype.toString)
1.  [function <span class="apidocSignatureSpan">mongodb.CoreConnection.prototype.</span>unref ()](#apidoc.element.mongodb.CoreConnection.prototype.unref)
1.  [function <span class="apidocSignatureSpan">mongodb.CoreConnection.prototype.</span>write (buffer)](#apidoc.element.mongodb.CoreConnection.prototype.write)

#### [module mongodb.CoreServer](#apidoc.module.mongodb.CoreServer)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>CoreServer (options)](#apidoc.element.mongodb.CoreServer.CoreServer)
1.  [function <span class="apidocSignatureSpan">mongodb.CoreServer.</span>disableServerAccounting ()](#apidoc.element.mongodb.CoreServer.disableServerAccounting)
1.  [function <span class="apidocSignatureSpan">mongodb.CoreServer.</span>enableServerAccounting ()](#apidoc.element.mongodb.CoreServer.enableServerAccounting)
1.  [function <span class="apidocSignatureSpan">mongodb.CoreServer.</span>servers ()](#apidoc.element.mongodb.CoreServer.servers)
1.  [function <span class="apidocSignatureSpan">mongodb.CoreServer.</span>super_ ()](#apidoc.element.mongodb.CoreServer.super_)

#### [module mongodb.CoreServer.prototype](#apidoc.module.mongodb.CoreServer.prototype)
1.  [function <span class="apidocSignatureSpan">mongodb.CoreServer.prototype.</span>auth (mechanism, db)](#apidoc.element.mongodb.CoreServer.prototype.auth)
1.  [function <span class="apidocSignatureSpan">mongodb.CoreServer.prototype.</span>command (ns, cmd, options, callback)](#apidoc.element.mongodb.CoreServer.prototype.command)
1.  [function <span class="apidocSignatureSpan">mongodb.CoreServer.prototype.</span>connect (options)](#apidoc.element.mongodb.CoreServer.prototype.connect)
1.  [function <span class="apidocSignatureSpan">mongodb.CoreServer.prototype.</span>connections ()](#apidoc.element.mongodb.CoreServer.prototype.connections)
1.  [function <span class="apidocSignatureSpan">mongodb.CoreServer.prototype.</span>cursor (ns, cmd, cursorOptions)](#apidoc.element.mongodb.CoreServer.prototype.cursor)
1.  [function <span class="apidocSignatureSpan">mongodb.CoreServer.prototype.</span>destroy (options)](#apidoc.element.mongodb.CoreServer.prototype.destroy)
1.  [function <span class="apidocSignatureSpan">mongodb.CoreServer.prototype.</span>equals (server)](#apidoc.element.mongodb.CoreServer.prototype.equals)
1.  [function <span class="apidocSignatureSpan">mongodb.CoreServer.prototype.</span>getConnection ()](#apidoc.element.mongodb.CoreServer.prototype.getConnection)
1.  [function <span class="apidocSignatureSpan">mongodb.CoreServer.prototype.</span>getDescription ()](#apidoc.element.mongodb.CoreServer.prototype.getDescription)
1.  [function <span class="apidocSignatureSpan">mongodb.CoreServer.prototype.</span>getServer ()](#apidoc.element.mongodb.CoreServer.prototype.getServer)
1.  [function <span class="apidocSignatureSpan">mongodb.CoreServer.prototype.</span>insert (ns, ops, options, callback)](#apidoc.element.mongodb.CoreServer.prototype.insert)
1.  [function <span class="apidocSignatureSpan">mongodb.CoreServer.prototype.</span>isConnected ()](#apidoc.element.mongodb.CoreServer.prototype.isConnected)
1.  [function <span class="apidocSignatureSpan">mongodb.CoreServer.prototype.</span>isDestroyed ()](#apidoc.element.mongodb.CoreServer.prototype.isDestroyed)
1.  [function <span class="apidocSignatureSpan">mongodb.CoreServer.prototype.</span>lastIsMaster ()](#apidoc.element.mongodb.CoreServer.prototype.lastIsMaster)
1.  [function <span class="apidocSignatureSpan">mongodb.CoreServer.prototype.</span>logout (dbName, callback)](#apidoc.element.mongodb.CoreServer.prototype.logout)
1.  [function <span class="apidocSignatureSpan">mongodb.CoreServer.prototype.</span>remove (ns, ops, options, callback)](#apidoc.element.mongodb.CoreServer.prototype.remove)
1.  [function <span class="apidocSignatureSpan">mongodb.CoreServer.prototype.</span>unref ()](#apidoc.element.mongodb.CoreServer.prototype.unref)
1.  [function <span class="apidocSignatureSpan">mongodb.CoreServer.prototype.</span>update (ns, ops, options, callback)](#apidoc.element.mongodb.CoreServer.prototype.update)
1.  string <span class="apidocSignatureSpan">mongodb.CoreServer.prototype.</span>parserType

#### [module mongodb.Cursor](#apidoc.module.mongodb.Cursor)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>Cursor (bson, ns, cmd, options, topology, topologyOptions)](#apidoc.element.mongodb.Cursor.Cursor)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.</span>super_ (options)](#apidoc.element.mongodb.Cursor.super_)
1.  number <span class="apidocSignatureSpan">mongodb.Cursor.</span>CLOSED
1.  number <span class="apidocSignatureSpan">mongodb.Cursor.</span>GET_MORE
1.  number <span class="apidocSignatureSpan">mongodb.Cursor.</span>INIT
1.  number <span class="apidocSignatureSpan">mongodb.Cursor.</span>OPEN
1.  object <span class="apidocSignatureSpan">mongodb.Cursor.</span>define

#### [module mongodb.Cursor.define](#apidoc.module.mongodb.Cursor.define)
1.  boolean <span class="apidocSignatureSpan">mongodb.Cursor.define.</span>stream
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.define.</span>object (bson, ns, cmd, options, topology, topologyOptions)](#apidoc.element.mongodb.Cursor.define.object)
1.  object <span class="apidocSignatureSpan">mongodb.Cursor.define.</span>instrumentations
1.  string <span class="apidocSignatureSpan">mongodb.Cursor.define.</span>name

#### [module mongodb.Cursor.prototype](#apidoc.module.mongodb.Cursor.prototype)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>_find (callback)](#apidoc.element.mongodb.Cursor.prototype._find)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>_getmore (callback)](#apidoc.element.mongodb.Cursor.prototype._getmore)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>_killcursor (callback)](#apidoc.element.mongodb.Cursor.prototype._killcursor)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>_next (callback)](#apidoc.element.mongodb.Cursor.prototype._next)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>_read ()](#apidoc.element.mongodb.Cursor.prototype._read)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>addCursorFlag (flag, value)](#apidoc.element.mongodb.Cursor.prototype.addCursorFlag)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>addQueryModifier (name, value)](#apidoc.element.mongodb.Cursor.prototype.addQueryModifier)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>batchSize (value)](#apidoc.element.mongodb.Cursor.prototype.batchSize)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>bufferedCount ()](#apidoc.element.mongodb.Cursor.prototype.bufferedCount)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>clone ()](#apidoc.element.mongodb.Cursor.prototype.clone)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>close (callback)](#apidoc.element.mongodb.Cursor.prototype.close)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>collation (value)](#apidoc.element.mongodb.Cursor.prototype.collation)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>comment (value)](#apidoc.element.mongodb.Cursor.prototype.comment)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>count (applySkipLimit, opts, callback)](#apidoc.element.mongodb.Cursor.prototype.count)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>cursorBatchSize ()](#apidoc.element.mongodb.Cursor.prototype.cursorBatchSize)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>cursorLimit ()](#apidoc.element.mongodb.Cursor.prototype.cursorLimit)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>cursorSkip ()](#apidoc.element.mongodb.Cursor.prototype.cursorSkip)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>destroy (err)](#apidoc.element.mongodb.Cursor.prototype.destroy)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>each (callback)](#apidoc.element.mongodb.Cursor.prototype.each)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>explain (callback)](#apidoc.element.mongodb.Cursor.prototype.explain)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>filter (filter)](#apidoc.element.mongodb.Cursor.prototype.filter)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>forEach (iterator, callback)](#apidoc.element.mongodb.Cursor.prototype.forEach)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>hasNext (callback)](#apidoc.element.mongodb.Cursor.prototype.hasNext)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>hint (hint)](#apidoc.element.mongodb.Cursor.prototype.hint)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>isClosed ()](#apidoc.element.mongodb.Cursor.prototype.isClosed)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>isDead ()](#apidoc.element.mongodb.Cursor.prototype.isDead)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>isKilled ()](#apidoc.element.mongodb.Cursor.prototype.isKilled)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>isNotified ()](#apidoc.element.mongodb.Cursor.prototype.isNotified)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>kill (callback)](#apidoc.element.mongodb.Cursor.prototype.kill)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>limit (value)](#apidoc.element.mongodb.Cursor.prototype.limit)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>map (transform)](#apidoc.element.mongodb.Cursor.prototype.map)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>max (max)](#apidoc.element.mongodb.Cursor.prototype.max)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>maxAwaitTimeMS (value)](#apidoc.element.mongodb.Cursor.prototype.maxAwaitTimeMS)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>maxScan (maxScan)](#apidoc.element.mongodb.Cursor.prototype.maxScan)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>maxTimeMS (value)](#apidoc.element.mongodb.Cursor.prototype.maxTimeMS)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>maxTimeMs (value)](#apidoc.element.mongodb.Cursor.prototype.maxTimeMs)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>min (min)](#apidoc.element.mongodb.Cursor.prototype.min)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>next (callback)](#apidoc.element.mongodb.Cursor.prototype.next)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>nextObject (callback)](#apidoc.element.mongodb.Cursor.prototype.nextObject)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>project (value)](#apidoc.element.mongodb.Cursor.prototype.project)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>readBufferedDocuments (number)](#apidoc.element.mongodb.Cursor.prototype.readBufferedDocuments)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>returnKey (value)](#apidoc.element.mongodb.Cursor.prototype.returnKey)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>rewind ()](#apidoc.element.mongodb.Cursor.prototype.rewind)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>setCursorBatchSize (value)](#apidoc.element.mongodb.Cursor.prototype.setCursorBatchSize)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>setCursorLimit (value)](#apidoc.element.mongodb.Cursor.prototype.setCursorLimit)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>setCursorOption (field, value)](#apidoc.element.mongodb.Cursor.prototype.setCursorOption)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>setCursorSkip (value)](#apidoc.element.mongodb.Cursor.prototype.setCursorSkip)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>setReadPreference (r)](#apidoc.element.mongodb.Cursor.prototype.setReadPreference)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>showRecordId (value)](#apidoc.element.mongodb.Cursor.prototype.showRecordId)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>skip (value)](#apidoc.element.mongodb.Cursor.prototype.skip)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>snapshot (value)](#apidoc.element.mongodb.Cursor.prototype.snapshot)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>sort (keyOrList, direction)](#apidoc.element.mongodb.Cursor.prototype.sort)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>stream (options)](#apidoc.element.mongodb.Cursor.prototype.stream)
1.  [function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>toArray (callback)](#apidoc.element.mongodb.Cursor.prototype.toArray)
1.  object <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>namespace
1.  object <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>readPreference

#### [module mongodb.DBRef](#apidoc.module.mongodb.DBRef)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>DBRef (namespace, oid, db)](#apidoc.element.mongodb.DBRef.DBRef)

#### [module mongodb.DBRef.prototype](#apidoc.module.mongodb.DBRef.prototype)
1.  [function <span class="apidocSignatureSpan">mongodb.DBRef.prototype.</span>toJSON ()](#apidoc.element.mongodb.DBRef.prototype.toJSON)

#### [module mongodb.Db](#apidoc.module.mongodb.Db)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>Db (databaseName, topology, options)](#apidoc.element.mongodb.Db.Db)
1.  [function <span class="apidocSignatureSpan">mongodb.Db.</span>super_ ()](#apidoc.element.mongodb.Db.super_)
1.  object <span class="apidocSignatureSpan">mongodb.Db.</span>define
1.  string <span class="apidocSignatureSpan">mongodb.Db.</span>SYSTEM_COMMAND_COLLECTION
1.  string <span class="apidocSignatureSpan">mongodb.Db.</span>SYSTEM_INDEX_COLLECTION
1.  string <span class="apidocSignatureSpan">mongodb.Db.</span>SYSTEM_JS_COLLECTION
1.  string <span class="apidocSignatureSpan">mongodb.Db.</span>SYSTEM_NAMESPACE_COLLECTION
1.  string <span class="apidocSignatureSpan">mongodb.Db.</span>SYSTEM_PROFILE_COLLECTION
1.  string <span class="apidocSignatureSpan">mongodb.Db.</span>SYSTEM_USER_COLLECTION

#### [module mongodb.Db.define](#apidoc.module.mongodb.Db.define)
1.  boolean <span class="apidocSignatureSpan">mongodb.Db.define.</span>stream
1.  [function <span class="apidocSignatureSpan">mongodb.Db.define.</span>object (databaseName, topology, options)](#apidoc.element.mongodb.Db.define.object)
1.  object <span class="apidocSignatureSpan">mongodb.Db.define.</span>instrumentations
1.  string <span class="apidocSignatureSpan">mongodb.Db.define.</span>name

#### [module mongodb.Db.prototype](#apidoc.module.mongodb.Db.prototype)
1.  [function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>addChild (db)](#apidoc.element.mongodb.Db.prototype.addChild)
1.  [function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>addUser (username, password, options, callback)](#apidoc.element.mongodb.Db.prototype.addUser)
1.  [function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>admin ()](#apidoc.element.mongodb.Db.prototype.admin)
1.  [function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>authenticate (username, password, options, callback)](#apidoc.element.mongodb.Db.prototype.authenticate)
1.  [function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>close (force, callback)](#apidoc.element.mongodb.Db.prototype.close)
1.  [function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>collection (name, options, callback)](#apidoc.element.mongodb.Db.prototype.collection)
1.  [function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>collections (callback)](#apidoc.element.mongodb.Db.prototype.collections)
1.  [function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>command (command, options, callback)](#apidoc.element.mongodb.Db.prototype.command)
1.  [function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>createCollection (name, options, callback)](#apidoc.element.mongodb.Db.prototype.createCollection)
1.  [function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>createIndex (name, fieldOrSpec, options, callback)](#apidoc.element.mongodb.Db.prototype.createIndex)
1.  [function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>db (dbName, options)](#apidoc.element.mongodb.Db.prototype.db)
1.  [function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>dropCollection (name, options, callback)](#apidoc.element.mongodb.Db.prototype.dropCollection)
1.  [function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>dropDatabase (options, callback)](#apidoc.element.mongodb.Db.prototype.dropDatabase)
1.  [function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>ensureIndex (name, fieldOrSpec, options, callback)](#apidoc.element.mongodb.Db.prototype.ensureIndex)
1.  [function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>eval (code, parameters, options, callback)](#apidoc.element.mongodb.Db.prototype.eval)
1.  [function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>executeDbAdminCommand (selector, options, callback)](#apidoc.element.mongodb.Db.prototype.executeDbAdminCommand)
1.  [function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>indexInformation (name, options, callback)](#apidoc.element.mongodb.Db.prototype.indexInformation)
1.  [function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>listCollections (filter, options)](#apidoc.element.mongodb.Db.prototype.listCollections)
1.  [function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>logout (options, callback)](#apidoc.element.mongodb.Db.prototype.logout)
1.  [function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>open (callback)](#apidoc.element.mongodb.Db.prototype.open)
1.  [function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>removeUser (username, options, callback)](#apidoc.element.mongodb.Db.prototype.removeUser)
1.  [function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>renameCollection (fromCollection, toCollection, options, callback)](#apidoc.element.mongodb.Db.prototype.renameCollection)
1.  [function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>stats (options, callback)](#apidoc.element.mongodb.Db.prototype.stats)
1.  [function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>unref ()](#apidoc.element.mongodb.Db.prototype.unref)

#### [module mongodb.Decimal128](#apidoc.module.mongodb.Decimal128)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>Decimal128 (bytes)](#apidoc.element.mongodb.Decimal128.Decimal128)
1.  [function <span class="apidocSignatureSpan">mongodb.Decimal128.</span>fromString (string)](#apidoc.element.mongodb.Decimal128.fromString)

#### [module mongodb.Decimal128.prototype](#apidoc.module.mongodb.Decimal128.prototype)
1.  [function <span class="apidocSignatureSpan">mongodb.Decimal128.prototype.</span>toJSON ()](#apidoc.element.mongodb.Decimal128.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">mongodb.Decimal128.prototype.</span>toString ()](#apidoc.element.mongodb.Decimal128.prototype.toString)

#### [module mongodb.Double](#apidoc.module.mongodb.Double)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>Double (value)](#apidoc.element.mongodb.Double.Double)

#### [module mongodb.Double.prototype](#apidoc.module.mongodb.Double.prototype)
1.  [function <span class="apidocSignatureSpan">mongodb.Double.prototype.</span>toJSON ()](#apidoc.element.mongodb.Double.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">mongodb.Double.prototype.</span>valueOf ()](#apidoc.element.mongodb.Double.prototype.valueOf)

#### [module mongodb.GridFSBucket](#apidoc.module.mongodb.GridFSBucket)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>GridFSBucket (db, options)](#apidoc.element.mongodb.GridFSBucket.GridFSBucket)
1.  [function <span class="apidocSignatureSpan">mongodb.GridFSBucket.</span>super_ ()](#apidoc.element.mongodb.GridFSBucket.super_)

#### [module mongodb.GridFSBucket.prototype](#apidoc.module.mongodb.GridFSBucket.prototype)
1.  [function <span class="apidocSignatureSpan">mongodb.GridFSBucket.prototype.</span>delete (id, callback)](#apidoc.element.mongodb.GridFSBucket.prototype.delete)
1.  [function <span class="apidocSignatureSpan">mongodb.GridFSBucket.prototype.</span>drop (callback)](#apidoc.element.mongodb.GridFSBucket.prototype.drop)
1.  [function <span class="apidocSignatureSpan">mongodb.GridFSBucket.prototype.</span>find (filter, options)](#apidoc.element.mongodb.GridFSBucket.prototype.find)
1.  [function <span class="apidocSignatureSpan">mongodb.GridFSBucket.prototype.</span>openDownloadStream (id, options)](#apidoc.element.mongodb.GridFSBucket.prototype.openDownloadStream)
1.  [function <span class="apidocSignatureSpan">mongodb.GridFSBucket.prototype.</span>openDownloadStreamByName (filename, options)](#apidoc.element.mongodb.GridFSBucket.prototype.openDownloadStreamByName)
1.  [function <span class="apidocSignatureSpan">mongodb.GridFSBucket.prototype.</span>openUploadStream (filename, options)](#apidoc.element.mongodb.GridFSBucket.prototype.openUploadStream)
1.  [function <span class="apidocSignatureSpan">mongodb.GridFSBucket.prototype.</span>openUploadStreamWithId (id, filename, options)](#apidoc.element.mongodb.GridFSBucket.prototype.openUploadStreamWithId)
1.  [function <span class="apidocSignatureSpan">mongodb.GridFSBucket.prototype.</span>rename (id, filename, callback)](#apidoc.element.mongodb.GridFSBucket.prototype.rename)

#### [module mongodb.GridStore](#apidoc.module.mongodb.GridStore)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>GridStore (db, id, filename, mode, options)](#apidoc.element.mongodb.GridStore.GridStore)
1.  [function <span class="apidocSignatureSpan">mongodb.GridStore.</span>exist (db, fileIdObject, rootCollection, options, callback)](#apidoc.element.mongodb.GridStore.exist)
1.  [function <span class="apidocSignatureSpan">mongodb.GridStore.</span>list (db, rootCollection, options, callback)](#apidoc.element.mongodb.GridStore.list)
1.  [function <span class="apidocSignatureSpan">mongodb.GridStore.</span>read (db, name, length, offset, options, callback)](#apidoc.element.mongodb.GridStore.read)
1.  [function <span class="apidocSignatureSpan">mongodb.GridStore.</span>readlines (db, name, separator, options, callback)](#apidoc.element.mongodb.GridStore.readlines)
1.  [function <span class="apidocSignatureSpan">mongodb.GridStore.</span>unlink (db, names, options, callback)](#apidoc.element.mongodb.GridStore.unlink)
1.  number <span class="apidocSignatureSpan">mongodb.GridStore.</span>IO_SEEK_CUR
1.  number <span class="apidocSignatureSpan">mongodb.GridStore.</span>IO_SEEK_END
1.  number <span class="apidocSignatureSpan">mongodb.GridStore.</span>IO_SEEK_SET
1.  object <span class="apidocSignatureSpan">mongodb.GridStore.</span>define
1.  string <span class="apidocSignatureSpan">mongodb.GridStore.</span>DEFAULT_CONTENT_TYPE
1.  string <span class="apidocSignatureSpan">mongodb.GridStore.</span>DEFAULT_ROOT_COLLECTION

#### [module mongodb.GridStore.define](#apidoc.module.mongodb.GridStore.define)
1.  boolean <span class="apidocSignatureSpan">mongodb.GridStore.define.</span>stream
1.  [function <span class="apidocSignatureSpan">mongodb.GridStore.define.</span>object (db, id, filename, mode, options)](#apidoc.element.mongodb.GridStore.define.object)
1.  object <span class="apidocSignatureSpan">mongodb.GridStore.define.</span>instrumentations
1.  string <span class="apidocSignatureSpan">mongodb.GridStore.define.</span>name

#### [module mongodb.GridStore.prototype](#apidoc.module.mongodb.GridStore.prototype)
1.  [function <span class="apidocSignatureSpan">mongodb.GridStore.prototype.</span>chunkCollection (callback)](#apidoc.element.mongodb.GridStore.prototype.chunkCollection)
1.  [function <span class="apidocSignatureSpan">mongodb.GridStore.prototype.</span>close (callback)](#apidoc.element.mongodb.GridStore.prototype.close)
1.  [function <span class="apidocSignatureSpan">mongodb.GridStore.prototype.</span>collection (callback)](#apidoc.element.mongodb.GridStore.prototype.collection)
1.  [function <span class="apidocSignatureSpan">mongodb.GridStore.prototype.</span>destroy ()](#apidoc.element.mongodb.GridStore.prototype.destroy)
1.  [function <span class="apidocSignatureSpan">mongodb.GridStore.prototype.</span>eof ()](#apidoc.element.mongodb.GridStore.prototype.eof)
1.  [function <span class="apidocSignatureSpan">mongodb.GridStore.prototype.</span>getc (callback)](#apidoc.element.mongodb.GridStore.prototype.getc)
1.  [function <span class="apidocSignatureSpan">mongodb.GridStore.prototype.</span>open (callback)](#apidoc.element.mongodb.GridStore.prototype.open)
1.  [function <span class="apidocSignatureSpan">mongodb.GridStore.prototype.</span>puts (string, callback)](#apidoc.element.mongodb.GridStore.prototype.puts)
1.  [function <span class="apidocSignatureSpan">mongodb.GridStore.prototype.</span>read (length, buffer, callback)](#apidoc.element.mongodb.GridStore.prototype.read)
1.  [function <span class="apidocSignatureSpan">mongodb.GridStore.prototype.</span>readlines (separator, callback)](#apidoc.element.mongodb.GridStore.prototype.readlines)
1.  [function <span class="apidocSignatureSpan">mongodb.GridStore.prototype.</span>rewind (callback)](#apidoc.element.mongodb.GridStore.prototype.rewind)
1.  [function <span class="apidocSignatureSpan">mongodb.GridStore.prototype.</span>seek (position, seekLocation, callback)](#apidoc.element.mongodb.GridStore.prototype.seek)
1.  [function <span class="apidocSignatureSpan">mongodb.GridStore.prototype.</span>stream ()](#apidoc.element.mongodb.GridStore.prototype.stream)
1.  [function <span class="apidocSignatureSpan">mongodb.GridStore.prototype.</span>tell (callback)](#apidoc.element.mongodb.GridStore.prototype.tell)
1.  [function <span class="apidocSignatureSpan">mongodb.GridStore.prototype.</span>unlink (callback)](#apidoc.element.mongodb.GridStore.prototype.unlink)
1.  [function <span class="apidocSignatureSpan">mongodb.GridStore.prototype.</span>write (data, close, callback)](#apidoc.element.mongodb.GridStore.prototype.write)
1.  [function <span class="apidocSignatureSpan">mongodb.GridStore.prototype.</span>writeFile (file, callback)](#apidoc.element.mongodb.GridStore.prototype.writeFile)

#### [module mongodb.Int32](#apidoc.module.mongodb.Int32)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>Int32 (value)](#apidoc.element.mongodb.Int32.Int32)

#### [module mongodb.Int32.prototype](#apidoc.module.mongodb.Int32.prototype)
1.  [function <span class="apidocSignatureSpan">mongodb.Int32.prototype.</span>toJSON ()](#apidoc.element.mongodb.Int32.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">mongodb.Int32.prototype.</span>valueOf ()](#apidoc.element.mongodb.Int32.prototype.valueOf)

#### [module mongodb.Logger](#apidoc.module.mongodb.Logger)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>Logger (className, options)](#apidoc.element.mongodb.Logger.Logger)
1.  [function <span class="apidocSignatureSpan">mongodb.Logger.</span>currentLogger ()](#apidoc.element.mongodb.Logger.currentLogger)
1.  [function <span class="apidocSignatureSpan">mongodb.Logger.</span>filter (type, values)](#apidoc.element.mongodb.Logger.filter)
1.  [function <span class="apidocSignatureSpan">mongodb.Logger.</span>reset ()](#apidoc.element.mongodb.Logger.reset)
1.  [function <span class="apidocSignatureSpan">mongodb.Logger.</span>setCurrentLogger (logger)](#apidoc.element.mongodb.Logger.setCurrentLogger)
1.  [function <span class="apidocSignatureSpan">mongodb.Logger.</span>setLevel (_level)](#apidoc.element.mongodb.Logger.setLevel)

#### [module mongodb.Logger.prototype](#apidoc.module.mongodb.Logger.prototype)
1.  [function <span class="apidocSignatureSpan">mongodb.Logger.prototype.</span>debug (message, object)](#apidoc.element.mongodb.Logger.prototype.debug)
1.  [function <span class="apidocSignatureSpan">mongodb.Logger.prototype.</span>error (message, object)](#apidoc.element.mongodb.Logger.prototype.error)
1.  [function <span class="apidocSignatureSpan">mongodb.Logger.prototype.</span>info (message, object)](#apidoc.element.mongodb.Logger.prototype.info)
1.  [function <span class="apidocSignatureSpan">mongodb.Logger.prototype.</span>isDebug ()](#apidoc.element.mongodb.Logger.prototype.isDebug)
1.  [function <span class="apidocSignatureSpan">mongodb.Logger.prototype.</span>isError ()](#apidoc.element.mongodb.Logger.prototype.isError)
1.  [function <span class="apidocSignatureSpan">mongodb.Logger.prototype.</span>isInfo ()](#apidoc.element.mongodb.Logger.prototype.isInfo)
1.  [function <span class="apidocSignatureSpan">mongodb.Logger.prototype.</span>isWarn ()](#apidoc.element.mongodb.Logger.prototype.isWarn)
1.  [function <span class="apidocSignatureSpan">mongodb.Logger.prototype.</span>warn (message, object)](#apidoc.element.mongodb.Logger.prototype.warn)

#### [module mongodb.Long](#apidoc.module.mongodb.Long)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>Long (low, high)](#apidoc.element.mongodb.Long.Long)
1.  [function <span class="apidocSignatureSpan">mongodb.Long.</span>fromBits (lowBits, highBits)](#apidoc.element.mongodb.Long.fromBits)
1.  [function <span class="apidocSignatureSpan">mongodb.Long.</span>fromInt (value)](#apidoc.element.mongodb.Long.fromInt)
1.  [function <span class="apidocSignatureSpan">mongodb.Long.</span>fromNumber (value)](#apidoc.element.mongodb.Long.fromNumber)
1.  [function <span class="apidocSignatureSpan">mongodb.Long.</span>fromString (str, opt_radix)](#apidoc.element.mongodb.Long.fromString)
1.  number <span class="apidocSignatureSpan">mongodb.Long.</span>TWO_PWR_16_DBL_
1.  number <span class="apidocSignatureSpan">mongodb.Long.</span>TWO_PWR_24_DBL_
1.  number <span class="apidocSignatureSpan">mongodb.Long.</span>TWO_PWR_31_DBL_
1.  number <span class="apidocSignatureSpan">mongodb.Long.</span>TWO_PWR_32_DBL_
1.  number <span class="apidocSignatureSpan">mongodb.Long.</span>TWO_PWR_48_DBL_
1.  number <span class="apidocSignatureSpan">mongodb.Long.</span>TWO_PWR_63_DBL_
1.  number <span class="apidocSignatureSpan">mongodb.Long.</span>TWO_PWR_64_DBL_
1.  object <span class="apidocSignatureSpan">mongodb.Long.</span>INT_CACHE_
1.  object <span class="apidocSignatureSpan">mongodb.Long.</span>MAX_VALUE
1.  object <span class="apidocSignatureSpan">mongodb.Long.</span>MIN_VALUE
1.  object <span class="apidocSignatureSpan">mongodb.Long.</span>NEG_ONE
1.  object <span class="apidocSignatureSpan">mongodb.Long.</span>ONE
1.  object <span class="apidocSignatureSpan">mongodb.Long.</span>TWO_PWR_24_
1.  object <span class="apidocSignatureSpan">mongodb.Long.</span>ZERO

#### [module mongodb.Long.prototype](#apidoc.module.mongodb.Long.prototype)
1.  [function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>add (other)](#apidoc.element.mongodb.Long.prototype.add)
1.  [function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>and (other)](#apidoc.element.mongodb.Long.prototype.and)
1.  [function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>compare (other)](#apidoc.element.mongodb.Long.prototype.compare)
1.  [function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>div (other)](#apidoc.element.mongodb.Long.prototype.div)
1.  [function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>equals (other)](#apidoc.element.mongodb.Long.prototype.equals)
1.  [function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>getHighBits ()](#apidoc.element.mongodb.Long.prototype.getHighBits)
1.  [function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>getLowBits ()](#apidoc.element.mongodb.Long.prototype.getLowBits)
1.  [function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>getLowBitsUnsigned ()](#apidoc.element.mongodb.Long.prototype.getLowBitsUnsigned)
1.  [function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>getNumBitsAbs ()](#apidoc.element.mongodb.Long.prototype.getNumBitsAbs)
1.  [function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>greaterThan (other)](#apidoc.element.mongodb.Long.prototype.greaterThan)
1.  [function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>greaterThanOrEqual (other)](#apidoc.element.mongodb.Long.prototype.greaterThanOrEqual)
1.  [function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>isNegative ()](#apidoc.element.mongodb.Long.prototype.isNegative)
1.  [function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>isOdd ()](#apidoc.element.mongodb.Long.prototype.isOdd)
1.  [function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>isZero ()](#apidoc.element.mongodb.Long.prototype.isZero)
1.  [function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>lessThan (other)](#apidoc.element.mongodb.Long.prototype.lessThan)
1.  [function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>lessThanOrEqual (other)](#apidoc.element.mongodb.Long.prototype.lessThanOrEqual)
1.  [function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>modulo (other)](#apidoc.element.mongodb.Long.prototype.modulo)
1.  [function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>multiply (other)](#apidoc.element.mongodb.Long.prototype.multiply)
1.  [function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>negate ()](#apidoc.element.mongodb.Long.prototype.negate)
1.  [function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>not ()](#apidoc.element.mongodb.Long.prototype.not)
1.  [function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>notEquals (other)](#apidoc.element.mongodb.Long.prototype.notEquals)
1.  [function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>or (other)](#apidoc.element.mongodb.Long.prototype.or)
1.  [function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>shiftLeft (numBits)](#apidoc.element.mongodb.Long.prototype.shiftLeft)
1.  [function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>shiftRight (numBits)](#apidoc.element.mongodb.Long.prototype.shiftRight)
1.  [function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>shiftRightUnsigned (numBits)](#apidoc.element.mongodb.Long.prototype.shiftRightUnsigned)
1.  [function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>subtract (other)](#apidoc.element.mongodb.Long.prototype.subtract)
1.  [function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>toInt ()](#apidoc.element.mongodb.Long.prototype.toInt)
1.  [function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>toJSON ()](#apidoc.element.mongodb.Long.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>toNumber ()](#apidoc.element.mongodb.Long.prototype.toNumber)
1.  [function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>toString (opt_radix)](#apidoc.element.mongodb.Long.prototype.toString)
1.  [function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>xor (other)](#apidoc.element.mongodb.Long.prototype.xor)

#### [module mongodb.Map](#apidoc.module.mongodb.Map)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>Map ()](#apidoc.element.mongodb.Map.Map)

#### [module mongodb.MaxKey](#apidoc.module.mongodb.MaxKey)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>MaxKey ()](#apidoc.element.mongodb.MaxKey.MaxKey)

#### [module mongodb.MinKey](#apidoc.module.mongodb.MinKey)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>MinKey ()](#apidoc.element.mongodb.MinKey.MinKey)

#### [module mongodb.MongoClient](#apidoc.module.mongodb.MongoClient)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>MongoClient ()](#apidoc.element.mongodb.MongoClient.MongoClient)
1.  [function <span class="apidocSignatureSpan">mongodb.MongoClient.</span>connect (url, options, callback)](#apidoc.element.mongodb.MongoClient.connect)
1.  object <span class="apidocSignatureSpan">mongodb.MongoClient.</span>define

#### [module mongodb.MongoClient.define](#apidoc.module.mongodb.MongoClient.define)
1.  boolean <span class="apidocSignatureSpan">mongodb.MongoClient.define.</span>stream
1.  [function <span class="apidocSignatureSpan">mongodb.MongoClient.define.</span>object ()](#apidoc.element.mongodb.MongoClient.define.object)
1.  object <span class="apidocSignatureSpan">mongodb.MongoClient.define.</span>instrumentations
1.  string <span class="apidocSignatureSpan">mongodb.MongoClient.define.</span>name

#### [module mongodb.MongoError](#apidoc.module.mongodb.MongoError)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>MongoError (message)](#apidoc.element.mongodb.MongoError.MongoError)
1.  [function <span class="apidocSignatureSpan">mongodb.MongoError.</span>create (options)](#apidoc.element.mongodb.MongoError.create)

#### [module mongodb.Mongos](#apidoc.module.mongodb.Mongos)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>Mongos (servers, options)](#apidoc.element.mongodb.Mongos.Mongos)
1.  [function <span class="apidocSignatureSpan">mongodb.Mongos.</span>super_ ()](#apidoc.element.mongodb.Mongos.super_)
1.  object <span class="apidocSignatureSpan">mongodb.Mongos.</span>define

#### [module mongodb.Mongos.define](#apidoc.module.mongodb.Mongos.define)
1.  boolean <span class="apidocSignatureSpan">mongodb.Mongos.define.</span>stream
1.  [function <span class="apidocSignatureSpan">mongodb.Mongos.define.</span>object (servers, options)](#apidoc.element.mongodb.Mongos.define.object)
1.  object <span class="apidocSignatureSpan">mongodb.Mongos.define.</span>instrumentations
1.  string <span class="apidocSignatureSpan">mongodb.Mongos.define.</span>name

#### [module mongodb.Mongos.prototype](#apidoc.module.mongodb.Mongos.prototype)
1.  [function <span class="apidocSignatureSpan">mongodb.Mongos.prototype.</span>auth ()](#apidoc.element.mongodb.Mongos.prototype.auth)
1.  [function <span class="apidocSignatureSpan">mongodb.Mongos.prototype.</span>capabilities ()](#apidoc.element.mongodb.Mongos.prototype.capabilities)
1.  [function <span class="apidocSignatureSpan">mongodb.Mongos.prototype.</span>close (forceClosed)](#apidoc.element.mongodb.Mongos.prototype.close)
1.  [function <span class="apidocSignatureSpan">mongodb.Mongos.prototype.</span>command (ns, cmd, options, callback)](#apidoc.element.mongodb.Mongos.prototype.command)
1.  [function <span class="apidocSignatureSpan">mongodb.Mongos.prototype.</span>connect (db, _options, callback)](#apidoc.element.mongodb.Mongos.prototype.connect)
1.  [function <span class="apidocSignatureSpan">mongodb.Mongos.prototype.</span>connections ()](#apidoc.element.mongodb.Mongos.prototype.connections)
1.  [function <span class="apidocSignatureSpan">mongodb.Mongos.prototype.</span>cursor (ns, cmd, options)](#apidoc.element.mongodb.Mongos.prototype.cursor)
1.  [function <span class="apidocSignatureSpan">mongodb.Mongos.prototype.</span>insert (ns, ops, options, callback)](#apidoc.element.mongodb.Mongos.prototype.insert)
1.  [function <span class="apidocSignatureSpan">mongodb.Mongos.prototype.</span>isConnected ()](#apidoc.element.mongodb.Mongos.prototype.isConnected)
1.  [function <span class="apidocSignatureSpan">mongodb.Mongos.prototype.</span>isDestroyed ()](#apidoc.element.mongodb.Mongos.prototype.isDestroyed)
1.  [function <span class="apidocSignatureSpan">mongodb.Mongos.prototype.</span>lastIsMaster ()](#apidoc.element.mongodb.Mongos.prototype.lastIsMaster)
1.  [function <span class="apidocSignatureSpan">mongodb.Mongos.prototype.</span>logout ()](#apidoc.element.mongodb.Mongos.prototype.logout)
1.  [function <span class="apidocSignatureSpan">mongodb.Mongos.prototype.</span>remove (ns, ops, options, callback)](#apidoc.element.mongodb.Mongos.prototype.remove)
1.  [function <span class="apidocSignatureSpan">mongodb.Mongos.prototype.</span>unref ()](#apidoc.element.mongodb.Mongos.prototype.unref)
1.  [function <span class="apidocSignatureSpan">mongodb.Mongos.prototype.</span>update (ns, ops, options, callback)](#apidoc.element.mongodb.Mongos.prototype.update)

#### [module mongodb.ObjectID](#apidoc.module.mongodb.ObjectID)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>ObjectID (id)](#apidoc.element.mongodb.ObjectID.ObjectID)
1.  [function <span class="apidocSignatureSpan">mongodb.ObjectID.</span>ObjectId (id)](#apidoc.element.mongodb.ObjectID.ObjectId)
1.  [function <span class="apidocSignatureSpan">mongodb.ObjectID.</span>createFromHexString (string)](#apidoc.element.mongodb.ObjectID.createFromHexString)
1.  [function <span class="apidocSignatureSpan">mongodb.ObjectID.</span>createFromTime (time)](#apidoc.element.mongodb.ObjectID.createFromTime)
1.  [function <span class="apidocSignatureSpan">mongodb.ObjectID.</span>createPk ()](#apidoc.element.mongodb.ObjectID.createPk)
1.  [function <span class="apidocSignatureSpan">mongodb.ObjectID.</span>isValid (id)](#apidoc.element.mongodb.ObjectID.isValid)
1.  number <span class="apidocSignatureSpan">mongodb.ObjectID.</span>index

#### [module mongodb.ObjectID.prototype](#apidoc.module.mongodb.ObjectID.prototype)
1.  [function <span class="apidocSignatureSpan">mongodb.ObjectID.prototype.</span>equals (otherId)](#apidoc.element.mongodb.ObjectID.prototype.equals)
1.  [function <span class="apidocSignatureSpan">mongodb.ObjectID.prototype.</span>generate (time)](#apidoc.element.mongodb.ObjectID.prototype.generate)
1.  [function <span class="apidocSignatureSpan">mongodb.ObjectID.prototype.</span>getInc ()](#apidoc.element.mongodb.ObjectID.prototype.getInc)
1.  [function <span class="apidocSignatureSpan">mongodb.ObjectID.prototype.</span>getTimestamp ()](#apidoc.element.mongodb.ObjectID.prototype.getTimestamp)
1.  [function <span class="apidocSignatureSpan">mongodb.ObjectID.prototype.</span>get_inc ()](#apidoc.element.mongodb.ObjectID.prototype.get_inc)
1.  [function <span class="apidocSignatureSpan">mongodb.ObjectID.prototype.</span>inspect (format)](#apidoc.element.mongodb.ObjectID.prototype.inspect)
1.  [function <span class="apidocSignatureSpan">mongodb.ObjectID.prototype.</span>toHexString ()](#apidoc.element.mongodb.ObjectID.prototype.toHexString)
1.  [function <span class="apidocSignatureSpan">mongodb.ObjectID.prototype.</span>toJSON ()](#apidoc.element.mongodb.ObjectID.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">mongodb.ObjectID.prototype.</span>toString (format)](#apidoc.element.mongodb.ObjectID.prototype.toString)

#### [module mongodb.ReadPreference](#apidoc.module.mongodb.ReadPreference)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>ReadPreference (mode, tags, options)](#apidoc.element.mongodb.ReadPreference.ReadPreference)
1.  [function <span class="apidocSignatureSpan">mongodb.ReadPreference.</span>isValid (_mode)](#apidoc.element.mongodb.ReadPreference.isValid)
1.  string <span class="apidocSignatureSpan">mongodb.ReadPreference.</span>NEAREST
1.  string <span class="apidocSignatureSpan">mongodb.ReadPreference.</span>PRIMARY
1.  string <span class="apidocSignatureSpan">mongodb.ReadPreference.</span>PRIMARY_PREFERRED
1.  string <span class="apidocSignatureSpan">mongodb.ReadPreference.</span>SECONDARY
1.  string <span class="apidocSignatureSpan">mongodb.ReadPreference.</span>SECONDARY_PREFERRED

#### [module mongodb.ReadPreference.prototype](#apidoc.module.mongodb.ReadPreference.prototype)
1.  [function <span class="apidocSignatureSpan">mongodb.ReadPreference.prototype.</span>isValid (mode)](#apidoc.element.mongodb.ReadPreference.prototype.isValid)
1.  [function <span class="apidocSignatureSpan">mongodb.ReadPreference.prototype.</span>toJSON ()](#apidoc.element.mongodb.ReadPreference.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">mongodb.ReadPreference.prototype.</span>toObject ()](#apidoc.element.mongodb.ReadPreference.prototype.toObject)

#### [module mongodb.ReplSet](#apidoc.module.mongodb.ReplSet)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>ReplSet (servers, options)](#apidoc.element.mongodb.ReplSet.ReplSet)
1.  [function <span class="apidocSignatureSpan">mongodb.ReplSet.</span>super_ ()](#apidoc.element.mongodb.ReplSet.super_)
1.  object <span class="apidocSignatureSpan">mongodb.ReplSet.</span>define

#### [module mongodb.ReplSet.define](#apidoc.module.mongodb.ReplSet.define)
1.  boolean <span class="apidocSignatureSpan">mongodb.ReplSet.define.</span>stream
1.  [function <span class="apidocSignatureSpan">mongodb.ReplSet.define.</span>object (servers, options)](#apidoc.element.mongodb.ReplSet.define.object)
1.  object <span class="apidocSignatureSpan">mongodb.ReplSet.define.</span>instrumentations
1.  string <span class="apidocSignatureSpan">mongodb.ReplSet.define.</span>name

#### [module mongodb.ReplSet.prototype](#apidoc.module.mongodb.ReplSet.prototype)
1.  [function <span class="apidocSignatureSpan">mongodb.ReplSet.prototype.</span>auth ()](#apidoc.element.mongodb.ReplSet.prototype.auth)
1.  [function <span class="apidocSignatureSpan">mongodb.ReplSet.prototype.</span>capabilities ()](#apidoc.element.mongodb.ReplSet.prototype.capabilities)
1.  [function <span class="apidocSignatureSpan">mongodb.ReplSet.prototype.</span>close (forceClosed)](#apidoc.element.mongodb.ReplSet.prototype.close)
1.  [function <span class="apidocSignatureSpan">mongodb.ReplSet.prototype.</span>command (ns, cmd, options, callback)](#apidoc.element.mongodb.ReplSet.prototype.command)
1.  [function <span class="apidocSignatureSpan">mongodb.ReplSet.prototype.</span>connect (db, _options, callback)](#apidoc.element.mongodb.ReplSet.prototype.connect)
1.  [function <span class="apidocSignatureSpan">mongodb.ReplSet.prototype.</span>connections ()](#apidoc.element.mongodb.ReplSet.prototype.connections)
1.  [function <span class="apidocSignatureSpan">mongodb.ReplSet.prototype.</span>cursor (ns, cmd, options)](#apidoc.element.mongodb.ReplSet.prototype.cursor)
1.  [function <span class="apidocSignatureSpan">mongodb.ReplSet.prototype.</span>insert (ns, ops, options, callback)](#apidoc.element.mongodb.ReplSet.prototype.insert)
1.  [function <span class="apidocSignatureSpan">mongodb.ReplSet.prototype.</span>isConnected (options)](#apidoc.element.mongodb.ReplSet.prototype.isConnected)
1.  [function <span class="apidocSignatureSpan">mongodb.ReplSet.prototype.</span>isDestroyed ()](#apidoc.element.mongodb.ReplSet.prototype.isDestroyed)
1.  [function <span class="apidocSignatureSpan">mongodb.ReplSet.prototype.</span>lastIsMaster ()](#apidoc.element.mongodb.ReplSet.prototype.lastIsMaster)
1.  [function <span class="apidocSignatureSpan">mongodb.ReplSet.prototype.</span>logout ()](#apidoc.element.mongodb.ReplSet.prototype.logout)
1.  [function <span class="apidocSignatureSpan">mongodb.ReplSet.prototype.</span>remove (ns, ops, options, callback)](#apidoc.element.mongodb.ReplSet.prototype.remove)
1.  [function <span class="apidocSignatureSpan">mongodb.ReplSet.prototype.</span>unref ()](#apidoc.element.mongodb.ReplSet.prototype.unref)
1.  [function <span class="apidocSignatureSpan">mongodb.ReplSet.prototype.</span>update (ns, ops, options, callback)](#apidoc.element.mongodb.ReplSet.prototype.update)

#### [module mongodb.Server](#apidoc.module.mongodb.Server)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>Server (host, port, options)](#apidoc.element.mongodb.Server.Server)
1.  [function <span class="apidocSignatureSpan">mongodb.Server.</span>super_ ()](#apidoc.element.mongodb.Server.super_)
1.  object <span class="apidocSignatureSpan">mongodb.Server.</span>define

#### [module mongodb.Server.define](#apidoc.module.mongodb.Server.define)
1.  boolean <span class="apidocSignatureSpan">mongodb.Server.define.</span>stream
1.  [function <span class="apidocSignatureSpan">mongodb.Server.define.</span>object (host, port, options)](#apidoc.element.mongodb.Server.define.object)
1.  object <span class="apidocSignatureSpan">mongodb.Server.define.</span>instrumentations
1.  string <span class="apidocSignatureSpan">mongodb.Server.define.</span>name

#### [module mongodb.Server.prototype](#apidoc.module.mongodb.Server.prototype)
1.  [function <span class="apidocSignatureSpan">mongodb.Server.prototype.</span>auth ()](#apidoc.element.mongodb.Server.prototype.auth)
1.  [function <span class="apidocSignatureSpan">mongodb.Server.prototype.</span>capabilities ()](#apidoc.element.mongodb.Server.prototype.capabilities)
1.  [function <span class="apidocSignatureSpan">mongodb.Server.prototype.</span>close (forceClosed)](#apidoc.element.mongodb.Server.prototype.close)
1.  [function <span class="apidocSignatureSpan">mongodb.Server.prototype.</span>command (ns, cmd, options, callback)](#apidoc.element.mongodb.Server.prototype.command)
1.  [function <span class="apidocSignatureSpan">mongodb.Server.prototype.</span>connect (db, _options, callback)](#apidoc.element.mongodb.Server.prototype.connect)
1.  [function <span class="apidocSignatureSpan">mongodb.Server.prototype.</span>connections ()](#apidoc.element.mongodb.Server.prototype.connections)
1.  [function <span class="apidocSignatureSpan">mongodb.Server.prototype.</span>cursor (ns, cmd, options)](#apidoc.element.mongodb.Server.prototype.cursor)
1.  [function <span class="apidocSignatureSpan">mongodb.Server.prototype.</span>insert (ns, ops, options, callback)](#apidoc.element.mongodb.Server.prototype.insert)
1.  [function <span class="apidocSignatureSpan">mongodb.Server.prototype.</span>isConnected ()](#apidoc.element.mongodb.Server.prototype.isConnected)
1.  [function <span class="apidocSignatureSpan">mongodb.Server.prototype.</span>isDestroyed ()](#apidoc.element.mongodb.Server.prototype.isDestroyed)
1.  [function <span class="apidocSignatureSpan">mongodb.Server.prototype.</span>lastIsMaster ()](#apidoc.element.mongodb.Server.prototype.lastIsMaster)
1.  [function <span class="apidocSignatureSpan">mongodb.Server.prototype.</span>logout ()](#apidoc.element.mongodb.Server.prototype.logout)
1.  [function <span class="apidocSignatureSpan">mongodb.Server.prototype.</span>remove (ns, ops, options, callback)](#apidoc.element.mongodb.Server.prototype.remove)
1.  [function <span class="apidocSignatureSpan">mongodb.Server.prototype.</span>unref ()](#apidoc.element.mongodb.Server.prototype.unref)
1.  [function <span class="apidocSignatureSpan">mongodb.Server.prototype.</span>update (ns, ops, options, callback)](#apidoc.element.mongodb.Server.prototype.update)

#### [module mongodb.Symbol](#apidoc.module.mongodb.Symbol)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>Symbol (value)](#apidoc.element.mongodb.Symbol.Symbol)

#### [module mongodb.Symbol.prototype](#apidoc.module.mongodb.Symbol.prototype)
1.  [function <span class="apidocSignatureSpan">mongodb.Symbol.prototype.</span>inspect ()](#apidoc.element.mongodb.Symbol.prototype.inspect)
1.  [function <span class="apidocSignatureSpan">mongodb.Symbol.prototype.</span>toJSON ()](#apidoc.element.mongodb.Symbol.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">mongodb.Symbol.prototype.</span>toString ()](#apidoc.element.mongodb.Symbol.prototype.toString)
1.  [function <span class="apidocSignatureSpan">mongodb.Symbol.prototype.</span>valueOf ()](#apidoc.element.mongodb.Symbol.prototype.valueOf)

#### [module mongodb.Timestamp](#apidoc.module.mongodb.Timestamp)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>Timestamp (low, high)](#apidoc.element.mongodb.Timestamp.Timestamp)
1.  [function <span class="apidocSignatureSpan">mongodb.Timestamp.</span>fromBits (lowBits, highBits)](#apidoc.element.mongodb.Timestamp.fromBits)
1.  [function <span class="apidocSignatureSpan">mongodb.Timestamp.</span>fromInt (value)](#apidoc.element.mongodb.Timestamp.fromInt)
1.  [function <span class="apidocSignatureSpan">mongodb.Timestamp.</span>fromNumber (value)](#apidoc.element.mongodb.Timestamp.fromNumber)
1.  [function <span class="apidocSignatureSpan">mongodb.Timestamp.</span>fromString (str, opt_radix)](#apidoc.element.mongodb.Timestamp.fromString)
1.  number <span class="apidocSignatureSpan">mongodb.Timestamp.</span>TWO_PWR_16_DBL_
1.  number <span class="apidocSignatureSpan">mongodb.Timestamp.</span>TWO_PWR_24_DBL_
1.  number <span class="apidocSignatureSpan">mongodb.Timestamp.</span>TWO_PWR_31_DBL_
1.  number <span class="apidocSignatureSpan">mongodb.Timestamp.</span>TWO_PWR_32_DBL_
1.  number <span class="apidocSignatureSpan">mongodb.Timestamp.</span>TWO_PWR_48_DBL_
1.  number <span class="apidocSignatureSpan">mongodb.Timestamp.</span>TWO_PWR_63_DBL_
1.  number <span class="apidocSignatureSpan">mongodb.Timestamp.</span>TWO_PWR_64_DBL_
1.  object <span class="apidocSignatureSpan">mongodb.Timestamp.</span>INT_CACHE_
1.  object <span class="apidocSignatureSpan">mongodb.Timestamp.</span>MAX_VALUE
1.  object <span class="apidocSignatureSpan">mongodb.Timestamp.</span>MIN_VALUE
1.  object <span class="apidocSignatureSpan">mongodb.Timestamp.</span>NEG_ONE
1.  object <span class="apidocSignatureSpan">mongodb.Timestamp.</span>ONE
1.  object <span class="apidocSignatureSpan">mongodb.Timestamp.</span>TWO_PWR_24_
1.  object <span class="apidocSignatureSpan">mongodb.Timestamp.</span>ZERO

#### [module mongodb.Timestamp.prototype](#apidoc.module.mongodb.Timestamp.prototype)
1.  [function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>add (other)](#apidoc.element.mongodb.Timestamp.prototype.add)
1.  [function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>and (other)](#apidoc.element.mongodb.Timestamp.prototype.and)
1.  [function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>compare (other)](#apidoc.element.mongodb.Timestamp.prototype.compare)
1.  [function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>div (other)](#apidoc.element.mongodb.Timestamp.prototype.div)
1.  [function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>equals (other)](#apidoc.element.mongodb.Timestamp.prototype.equals)
1.  [function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>getHighBits ()](#apidoc.element.mongodb.Timestamp.prototype.getHighBits)
1.  [function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>getLowBits ()](#apidoc.element.mongodb.Timestamp.prototype.getLowBits)
1.  [function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>getLowBitsUnsigned ()](#apidoc.element.mongodb.Timestamp.prototype.getLowBitsUnsigned)
1.  [function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>getNumBitsAbs ()](#apidoc.element.mongodb.Timestamp.prototype.getNumBitsAbs)
1.  [function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>greaterThan (other)](#apidoc.element.mongodb.Timestamp.prototype.greaterThan)
1.  [function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>greaterThanOrEqual (other)](#apidoc.element.mongodb.Timestamp.prototype.greaterThanOrEqual)
1.  [function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>isNegative ()](#apidoc.element.mongodb.Timestamp.prototype.isNegative)
1.  [function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>isOdd ()](#apidoc.element.mongodb.Timestamp.prototype.isOdd)
1.  [function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>isZero ()](#apidoc.element.mongodb.Timestamp.prototype.isZero)
1.  [function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>lessThan (other)](#apidoc.element.mongodb.Timestamp.prototype.lessThan)
1.  [function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>lessThanOrEqual (other)](#apidoc.element.mongodb.Timestamp.prototype.lessThanOrEqual)
1.  [function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>modulo (other)](#apidoc.element.mongodb.Timestamp.prototype.modulo)
1.  [function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>multiply (other)](#apidoc.element.mongodb.Timestamp.prototype.multiply)
1.  [function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>negate ()](#apidoc.element.mongodb.Timestamp.prototype.negate)
1.  [function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>not ()](#apidoc.element.mongodb.Timestamp.prototype.not)
1.  [function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>notEquals (other)](#apidoc.element.mongodb.Timestamp.prototype.notEquals)
1.  [function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>or (other)](#apidoc.element.mongodb.Timestamp.prototype.or)
1.  [function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>shiftLeft (numBits)](#apidoc.element.mongodb.Timestamp.prototype.shiftLeft)
1.  [function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>shiftRight (numBits)](#apidoc.element.mongodb.Timestamp.prototype.shiftRight)
1.  [function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>shiftRightUnsigned (numBits)](#apidoc.element.mongodb.Timestamp.prototype.shiftRightUnsigned)
1.  [function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>subtract (other)](#apidoc.element.mongodb.Timestamp.prototype.subtract)
1.  [function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>toInt ()](#apidoc.element.mongodb.Timestamp.prototype.toInt)
1.  [function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>toJSON ()](#apidoc.element.mongodb.Timestamp.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>toNumber ()](#apidoc.element.mongodb.Timestamp.prototype.toNumber)
1.  [function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>toString (opt_radix)](#apidoc.element.mongodb.Timestamp.prototype.toString)
1.  [function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>xor (other)](#apidoc.element.mongodb.Timestamp.prototype.xor)

#### [module mongodb.aggregation_cursor](#apidoc.module.mongodb.aggregation_cursor)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>aggregation_cursor (bson, ns, cmd, options, topology, topologyOptions)](#apidoc.element.mongodb.aggregation_cursor.aggregation_cursor)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.</span>super_ (options)](#apidoc.element.mongodb.aggregation_cursor.super_)
1.  number <span class="apidocSignatureSpan">mongodb.aggregation_cursor.</span>CLOSED
1.  number <span class="apidocSignatureSpan">mongodb.aggregation_cursor.</span>INIT
1.  number <span class="apidocSignatureSpan">mongodb.aggregation_cursor.</span>OPEN
1.  object <span class="apidocSignatureSpan">mongodb.aggregation_cursor.</span>define

#### [module mongodb.aggregation_cursor.prototype](#apidoc.module.mongodb.aggregation_cursor.prototype)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>_find (callback)](#apidoc.element.mongodb.aggregation_cursor.prototype._find)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>_getmore (callback)](#apidoc.element.mongodb.aggregation_cursor.prototype._getmore)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>_killcursor (callback)](#apidoc.element.mongodb.aggregation_cursor.prototype._killcursor)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>_next (callback)](#apidoc.element.mongodb.aggregation_cursor.prototype._next)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>_read ()](#apidoc.element.mongodb.aggregation_cursor.prototype._read)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>addCursorFlag (flag, value)](#apidoc.element.mongodb.aggregation_cursor.prototype.addCursorFlag)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>addListener (ev, fn)](#apidoc.element.mongodb.aggregation_cursor.prototype.addListener)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>addQueryModifier (name, value)](#apidoc.element.mongodb.aggregation_cursor.prototype.addQueryModifier)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>batchSize (value)](#apidoc.element.mongodb.aggregation_cursor.prototype.batchSize)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>bufferedCount ()](#apidoc.element.mongodb.aggregation_cursor.prototype.bufferedCount)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>clone ()](#apidoc.element.mongodb.aggregation_cursor.prototype.clone)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>close (callback)](#apidoc.element.mongodb.aggregation_cursor.prototype.close)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>collation (value)](#apidoc.element.mongodb.aggregation_cursor.prototype.collation)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>comment (value)](#apidoc.element.mongodb.aggregation_cursor.prototype.comment)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>count (applySkipLimit, opts, callback)](#apidoc.element.mongodb.aggregation_cursor.prototype.count)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>cursorBatchSize ()](#apidoc.element.mongodb.aggregation_cursor.prototype.cursorBatchSize)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>cursorLimit ()](#apidoc.element.mongodb.aggregation_cursor.prototype.cursorLimit)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>cursorSkip ()](#apidoc.element.mongodb.aggregation_cursor.prototype.cursorSkip)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>destroy (err)](#apidoc.element.mongodb.aggregation_cursor.prototype.destroy)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>each (callback)](#apidoc.element.mongodb.aggregation_cursor.prototype.each)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>emit (type)](#apidoc.element.mongodb.aggregation_cursor.prototype.emit)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>eventNames ()](#apidoc.element.mongodb.aggregation_cursor.prototype.eventNames)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>explain (callback)](#apidoc.element.mongodb.aggregation_cursor.prototype.explain)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>filter (filter)](#apidoc.element.mongodb.aggregation_cursor.prototype.filter)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>forEach (iterator, callback)](#apidoc.element.mongodb.aggregation_cursor.prototype.forEach)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>geoNear (document)](#apidoc.element.mongodb.aggregation_cursor.prototype.geoNear)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>get (callback)](#apidoc.element.mongodb.aggregation_cursor.prototype.get)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>getMaxListeners ()](#apidoc.element.mongodb.aggregation_cursor.prototype.getMaxListeners)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>group (document)](#apidoc.element.mongodb.aggregation_cursor.prototype.group)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>hasNext (callback)](#apidoc.element.mongodb.aggregation_cursor.prototype.hasNext)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>hint (hint)](#apidoc.element.mongodb.aggregation_cursor.prototype.hint)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>isClosed ()](#apidoc.element.mongodb.aggregation_cursor.prototype.isClosed)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>isDead ()](#apidoc.element.mongodb.aggregation_cursor.prototype.isDead)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>isKilled ()](#apidoc.element.mongodb.aggregation_cursor.prototype.isKilled)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>isNotified ()](#apidoc.element.mongodb.aggregation_cursor.prototype.isNotified)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>isPaused ()](#apidoc.element.mongodb.aggregation_cursor.prototype.isPaused)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>kill (callback)](#apidoc.element.mongodb.aggregation_cursor.prototype.kill)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>limit (value)](#apidoc.element.mongodb.aggregation_cursor.prototype.limit)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>listenerCount (type)](#apidoc.element.mongodb.aggregation_cursor.prototype.listenerCount)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>listeners (type)](#apidoc.element.mongodb.aggregation_cursor.prototype.listeners)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>lookup (document)](#apidoc.element.mongodb.aggregation_cursor.prototype.lookup)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>map (transform)](#apidoc.element.mongodb.aggregation_cursor.prototype.map)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>match (document)](#apidoc.element.mongodb.aggregation_cursor.prototype.match)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>max (max)](#apidoc.element.mongodb.aggregation_cursor.prototype.max)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>maxAwaitTimeMS (value)](#apidoc.element.mongodb.aggregation_cursor.prototype.maxAwaitTimeMS)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>maxScan (maxScan)](#apidoc.element.mongodb.aggregation_cursor.prototype.maxScan)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>maxTimeMS (value)](#apidoc.element.mongodb.aggregation_cursor.prototype.maxTimeMS)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>maxTimeMs (value)](#apidoc.element.mongodb.aggregation_cursor.prototype.maxTimeMs)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>min (min)](#apidoc.element.mongodb.aggregation_cursor.prototype.min)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>next (callback)](#apidoc.element.mongodb.aggregation_cursor.prototype.next)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>nextObject (callback)](#apidoc.element.mongodb.aggregation_cursor.prototype.nextObject)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>on (ev, fn)](#apidoc.element.mongodb.aggregation_cursor.prototype.on)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>once (type, listener)](#apidoc.element.mongodb.aggregation_cursor.prototype.once)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>out (destination)](#apidoc.element.mongodb.aggregation_cursor.prototype.out)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>pause ()](#apidoc.element.mongodb.aggregation_cursor.prototype.pause)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>pipe (dest, pipeOpts)](#apidoc.element.mongodb.aggregation_cursor.prototype.pipe)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>prependListener (type, listener)](#apidoc.element.mongodb.aggregation_cursor.prototype.prependListener)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>prependOnceListener (type, listener)](#apidoc.element.mongodb.aggregation_cursor.prototype.prependOnceListener)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>project (document)](#apidoc.element.mongodb.aggregation_cursor.prototype.project)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>push (chunk, encoding)](#apidoc.element.mongodb.aggregation_cursor.prototype.push)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>read (n)](#apidoc.element.mongodb.aggregation_cursor.prototype.read)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>readBufferedDocuments (number)](#apidoc.element.mongodb.aggregation_cursor.prototype.readBufferedDocuments)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>redact (document)](#apidoc.element.mongodb.aggregation_cursor.prototype.redact)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>removeAllListeners (type)](#apidoc.element.mongodb.aggregation_cursor.prototype.removeAllListeners)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>removeListener (type, listener)](#apidoc.element.mongodb.aggregation_cursor.prototype.removeListener)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>resume ()](#apidoc.element.mongodb.aggregation_cursor.prototype.resume)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>returnKey (value)](#apidoc.element.mongodb.aggregation_cursor.prototype.returnKey)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>rewind ()](#apidoc.element.mongodb.aggregation_cursor.prototype.rewind)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>setCursorBatchSize (value)](#apidoc.element.mongodb.aggregation_cursor.prototype.setCursorBatchSize)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>setCursorLimit (value)](#apidoc.element.mongodb.aggregation_cursor.prototype.setCursorLimit)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>setCursorOption (field, value)](#apidoc.element.mongodb.aggregation_cursor.prototype.setCursorOption)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>setCursorSkip (value)](#apidoc.element.mongodb.aggregation_cursor.prototype.setCursorSkip)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>setEncoding (enc)](#apidoc.element.mongodb.aggregation_cursor.prototype.setEncoding)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>setMaxListeners (n)](#apidoc.element.mongodb.aggregation_cursor.prototype.setMaxListeners)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>setReadPreference (r)](#apidoc.element.mongodb.aggregation_cursor.prototype.setReadPreference)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>showRecordId (value)](#apidoc.element.mongodb.aggregation_cursor.prototype.showRecordId)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>skip (value)](#apidoc.element.mongodb.aggregation_cursor.prototype.skip)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>snapshot (value)](#apidoc.element.mongodb.aggregation_cursor.prototype.snapshot)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>sort (document)](#apidoc.element.mongodb.aggregation_cursor.prototype.sort)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>stream (options)](#apidoc.element.mongodb.aggregation_cursor.prototype.stream)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>toArray (callback)](#apidoc.element.mongodb.aggregation_cursor.prototype.toArray)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>unpipe (dest)](#apidoc.element.mongodb.aggregation_cursor.prototype.unpipe)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>unshift (chunk)](#apidoc.element.mongodb.aggregation_cursor.prototype.unshift)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>unwind (field)](#apidoc.element.mongodb.aggregation_cursor.prototype.unwind)
1.  [function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>wrap (stream)](#apidoc.element.mongodb.aggregation_cursor.prototype.wrap)
1.  object <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>namespace
1.  object <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>readPreference
1.  undefined <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>domain

#### [module mongodb.apm](#apidoc.module.mongodb.apm)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>apm (core, options, callback)](#apidoc.element.mongodb.apm.apm)
1.  [function <span class="apidocSignatureSpan">mongodb.apm.</span>super_ ()](#apidoc.element.mongodb.apm.super_)

#### [module mongodb.apm.prototype](#apidoc.module.mongodb.apm.prototype)
1.  [function <span class="apidocSignatureSpan">mongodb.apm.prototype.</span>uninstrument ()](#apidoc.element.mongodb.apm.prototype.uninstrument)

#### [module mongodb.command_cursor](#apidoc.module.mongodb.command_cursor)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>command_cursor (bson, ns, cmd, options, topology, topologyOptions)](#apidoc.element.mongodb.command_cursor.command_cursor)
1.  [function <span class="apidocSignatureSpan">mongodb.command_cursor.</span>super_ (options)](#apidoc.element.mongodb.command_cursor.super_)
1.  number <span class="apidocSignatureSpan">mongodb.command_cursor.</span>CLOSED
1.  number <span class="apidocSignatureSpan">mongodb.command_cursor.</span>INIT
1.  number <span class="apidocSignatureSpan">mongodb.command_cursor.</span>OPEN
1.  object <span class="apidocSignatureSpan">mongodb.command_cursor.</span>define

#### [module mongodb.command_cursor.prototype](#apidoc.module.mongodb.command_cursor.prototype)
1.  [function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>_find (callback)](#apidoc.element.mongodb.command_cursor.prototype._find)
1.  [function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>_getmore (callback)](#apidoc.element.mongodb.command_cursor.prototype._getmore)
1.  [function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>_killcursor (callback)](#apidoc.element.mongodb.command_cursor.prototype._killcursor)
1.  [function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>_next (callback)](#apidoc.element.mongodb.command_cursor.prototype._next)
1.  [function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>batchSize (value)](#apidoc.element.mongodb.command_cursor.prototype.batchSize)
1.  [function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>bufferedCount ()](#apidoc.element.mongodb.command_cursor.prototype.bufferedCount)
1.  [function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>close (callback)](#apidoc.element.mongodb.command_cursor.prototype.close)
1.  [function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>each (callback)](#apidoc.element.mongodb.command_cursor.prototype.each)
1.  [function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>explain (callback)](#apidoc.element.mongodb.command_cursor.prototype.explain)
1.  [function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>forEach (iterator, callback)](#apidoc.element.mongodb.command_cursor.prototype.forEach)
1.  [function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>get (callback)](#apidoc.element.mongodb.command_cursor.prototype.get)
1.  [function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>isClosed ()](#apidoc.element.mongodb.command_cursor.prototype.isClosed)
1.  [function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>isDead ()](#apidoc.element.mongodb.command_cursor.prototype.isDead)
1.  [function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>isKilled ()](#apidoc.element.mongodb.command_cursor.prototype.isKilled)
1.  [function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>isNotified ()](#apidoc.element.mongodb.command_cursor.prototype.isNotified)
1.  [function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>kill (callback)](#apidoc.element.mongodb.command_cursor.prototype.kill)
1.  [function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>maxTimeMS (value)](#apidoc.element.mongodb.command_cursor.prototype.maxTimeMS)
1.  [function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>next (callback)](#apidoc.element.mongodb.command_cursor.prototype.next)
1.  [function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>readBufferedDocuments (number)](#apidoc.element.mongodb.command_cursor.prototype.readBufferedDocuments)
1.  [function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>rewind ()](#apidoc.element.mongodb.command_cursor.prototype.rewind)
1.  [function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>setCursorBatchSize (value)](#apidoc.element.mongodb.command_cursor.prototype.setCursorBatchSize)
1.  [function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>setReadPreference (r)](#apidoc.element.mongodb.command_cursor.prototype.setReadPreference)
1.  [function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>toArray (callback)](#apidoc.element.mongodb.command_cursor.prototype.toArray)

#### [module mongodb.metadata](#apidoc.module.mongodb.metadata)
1.  [function <span class="apidocSignatureSpan">mongodb.</span>metadata (name, object, stream)](#apidoc.element.mongodb.metadata.metadata)

#### [module mongodb.metadata.prototype](#apidoc.module.mongodb.metadata.prototype)
1.  [function <span class="apidocSignatureSpan">mongodb.metadata.prototype.</span>classMethod (name, options)](#apidoc.element.mongodb.metadata.prototype.classMethod)
1.  [function <span class="apidocSignatureSpan">mongodb.metadata.prototype.</span>generate ()](#apidoc.element.mongodb.metadata.prototype.generate)
1.  [function <span class="apidocSignatureSpan">mongodb.metadata.prototype.</span>staticMethod (name, options)](#apidoc.element.mongodb.metadata.prototype.staticMethod)

#### [module mongodb.topology_base](#apidoc.module.mongodb.topology_base)
1.  [function <span class="apidocSignatureSpan">mongodb.topology_base.</span>ServerCapabilities (ismaster)](#apidoc.element.mongodb.topology_base.ServerCapabilities)
1.  [function <span class="apidocSignatureSpan">mongodb.topology_base.</span>Store (topology, storeOptions)](#apidoc.element.mongodb.topology_base.Store)

#### [module mongodb.utils](#apidoc.module.mongodb.utils)
1.  [function <span class="apidocSignatureSpan">mongodb.utils.</span>assign ()](#apidoc.element.mongodb.utils.assign)
1.  [function <span class="apidocSignatureSpan">mongodb.utils.</span>checkCollectionName (collectionName)](#apidoc.element.mongodb.utils.checkCollectionName)
1.  [function <span class="apidocSignatureSpan">mongodb.utils.</span>debugOptions (debugFields, options)](#apidoc.element.mongodb.utils.debugOptions)
1.  [function <span class="apidocSignatureSpan">mongodb.utils.</span>decorateCommand (command, options, exclude)](#apidoc.element.mongodb.utils.decorateCommand)
1.  [function <span class="apidocSignatureSpan">mongodb.utils.</span>filterOptions (options, names)](#apidoc.element.mongodb.utils.filterOptions)
1.  [function <span class="apidocSignatureSpan">mongodb.utils.</span>formatSortValue (sortDirection)](#apidoc.element.mongodb.utils.formatSortValue)
1.  [function <span class="apidocSignatureSpan">mongodb.utils.</span>formattedOrderClause (sortValue)](#apidoc.element.mongodb.utils.formattedOrderClause)
1.  [function <span class="apidocSignatureSpan">mongodb.utils.</span>getReadPreference (options)](#apidoc.element.mongodb.utils.getReadPreference)
1.  [function <span class="apidocSignatureSpan">mongodb.utils.</span>getSingleProperty (obj, name, value)](#apidoc.element.mongodb.utils.getSingleProperty)
1.  [function <span class="apidocSignatureSpan">mongodb.utils.</span>handleCallback (callback, err, value1, value2)](#apidoc.element.mongodb.utils.handleCallback)
1.  [function <span class="apidocSignatureSpan">mongodb.utils.</span>isObject (arg)](#apidoc.element.mongodb.utils.isObject)
1.  [function <span class="apidocSignatureSpan">mongodb.utils.</span>mergeOptions (target, source)](#apidoc.element.mongodb.utils.mergeOptions)
1.  [function <span class="apidocSignatureSpan">mongodb.utils.</span>normalizeHintField (hint)](#apidoc.element.mongodb.utils.normalizeHintField)
1.  [function <span class="apidocSignatureSpan">mongodb.utils.</span>parseIndexOptions (fieldOrSpec)](#apidoc.element.mongodb.utils.parseIndexOptions)
1.  [function <span class="apidocSignatureSpan">mongodb.utils.</span>shallowClone (obj)](#apidoc.element.mongodb.utils.shallowClone)
1.  [function <span class="apidocSignatureSpan">mongodb.utils.</span>toError (error)](#apidoc.element.mongodb.utils.toError)
1.  [function <span class="apidocSignatureSpan">mongodb.utils.</span>translateOptions (target, source)](#apidoc.element.mongodb.utils.translateOptions)
1.  number <span class="apidocSignatureSpan">mongodb.utils.</span>MAX_JS_INT



# <a name="apidoc.module.mongodb"></a>[module mongodb](#apidoc.module.mongodb)

#### <a name="apidoc.element.mongodb.Admin"></a>[function <span class="apidocSignatureSpan">mongodb.</span>Admin (db, topology, promiseLibrary)](#apidoc.element.mongodb.Admin)
- description and source-code
```javascript
Admin = function (db, topology, promiseLibrary) {
  if(!(this instanceof Admin)) return new Admin(db, topology);

  // Internal state
  this.s = {
      db: db
    , topology: topology
    , promiseLibrary: promiseLibrary
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.BSONRegExp"></a>[function <span class="apidocSignatureSpan">mongodb.</span>BSONRegExp (pattern, options)](#apidoc.element.mongodb.BSONRegExp)
- description and source-code
```javascript
function BSONRegExp(pattern, options) {
  if(!(this instanceof BSONRegExp)) return new BSONRegExp();

  // Execute
  this._bsontype = 'BSONRegExp';
  this.pattern = pattern || '';
  this.options = options || '';

  // Validate options
  for(var i = 0; i < this.options.length; i++) {
    if(!(this.options[i] == 'i'
      || this.options[i] == 'm'
      || this.options[i] == 'x'
      || this.options[i] == 'l'
      || this.options[i] == 's'
      || this.options[i] == 'u'
    )) {
      throw new Error('the regular expression options [' + this.options[i] + "] is not supported");
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Binary"></a>[function <span class="apidocSignatureSpan">mongodb.</span>Binary (buffer, subType)](#apidoc.element.mongodb.Binary)
- description and source-code
```javascript
function Binary(buffer, subType) {
  if(!(this instanceof Binary)) return new Binary(buffer, subType);

  this._bsontype = 'Binary';

  if(buffer instanceof Number) {
    this.sub_type = buffer;
    this.position = 0;
  } else {
    this.sub_type = subType == null ? BSON_BINARY_SUBTYPE_DEFAULT : subType;
    this.position = 0;
  }

  if(buffer != null && !(buffer instanceof Number)) {
    // Only accept Buffer, Uint8Array or Arrays
    if(typeof buffer == 'string') {
      // Different ways of writing the length of the string for the different types
      if(typeof Buffer != 'undefined') {
        this.buffer = new Buffer(buffer);
      } else if(typeof Uint8Array != 'undefined' || (Object.prototype.toString.call(buffer) == '[object Array]')) {
        this.buffer = writeStringToArray(buffer);
      } else {
        throw new Error("only String, Buffer, Uint8Array or Array accepted");
      }
    } else {
      this.buffer = buffer;
    }
    this.position = buffer.length;
  } else {
    if(typeof Buffer != 'undefined') {
      this.buffer =  new Buffer(Binary.BUFFER_SIZE);
    } else if(typeof Uint8Array != 'undefined'){
      this.buffer = new Uint8Array(new ArrayBuffer(Binary.BUFFER_SIZE));
    } else {
      this.buffer = new Array(Binary.BUFFER_SIZE);
    }
    // Set position to start of buffer
    this.position = 0;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Chunk"></a>[function <span class="apidocSignatureSpan">mongodb.</span>Chunk (file, mongoObject, writeConcern)](#apidoc.element.mongodb.Chunk)
- description and source-code
```javascript
Chunk = function (file, mongoObject, writeConcern) {
  if(!(this instanceof Chunk)) return new Chunk(file, mongoObject);

  this.file = file;
  var mongoObjectFinal = mongoObject == null ? {} : mongoObject;
  this.writeConcern = writeConcern || {w:1};
  this.objectId = mongoObjectFinal._id == null ? new ObjectID() : mongoObjectFinal._id;
  this.chunkNumber = mongoObjectFinal.n == null ? 0 : mongoObjectFinal.n;
  this.data = new Binary();

  if(typeof mongoObjectFinal.data == "string") {
    var buffer = new Buffer(mongoObjectFinal.data.length);
    buffer.write(mongoObjectFinal.data, 0, mongoObjectFinal.data.length, 'binary');
    this.data = new Binary(buffer);
  } else if(Array.isArray(mongoObjectFinal.data)) {
    buffer = new Buffer(mongoObjectFinal.data.length);
    var data = mongoObjectFinal.data.join('');
    buffer.write(data, 0, data.length, 'binary');
    this.data = new Binary(buffer);
  } else if(mongoObjectFinal.data && mongoObjectFinal.data._bsontype === 'Binary') {
    this.data = mongoObjectFinal.data;
  } else if(!Buffer.isBuffer(mongoObjectFinal.data) && !(mongoObjectFinal.data == null)){
    throw Error("Illegal chunk format");
  }

  // Update position
  this.internalPosition = 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Code"></a>[function <span class="apidocSignatureSpan">mongodb.</span>Code (code, scope)](#apidoc.element.mongodb.Code)
- description and source-code
```javascript
function Code(code, scope) {
  if(!(this instanceof Code)) return new Code(code, scope);
  this._bsontype = 'Code';
  this.code = code;
  this.scope = scope;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Collection"></a>[function <span class="apidocSignatureSpan">mongodb.</span>Collection (db, topology, dbName, name, pkFactory, options)](#apidoc.element.mongodb.Collection)
- description and source-code
```javascript
Collection = function (db, topology, dbName, name, pkFactory, options) {
  checkCollectionName(name);

  // Unpack variables
  var internalHint = null;
  var slaveOk = options == null || options.slaveOk == null ? db.slaveOk : options.slaveOk;
  var serializeFunctions = options == null || options.serializeFunctions == null ? db.s.options.serializeFunctions : options.serializeFunctions
;
  var raw = options == null || options.raw == null ? db.s.options.raw : options.raw;
  var promoteLongs = options == null || options.promoteLongs == null ? db.s.options.promoteLongs : options.promoteLongs;
  var promoteValues = options == null || options.promoteValues == null ? db.s.options.promoteValues : options.promoteValues;
  var promoteBuffers = options == null || options.promoteBuffers == null ? db.s.options.promoteBuffers : options.promoteBuffers;
  var readPreference = null;
  var collectionHint = null;
  var namespace = f("%s.%s", dbName, name);

  // Get the promiseLibrary
  var promiseLibrary = options.promiseLibrary;

  // No promise library selected fall back
  if(!promiseLibrary) {
    promiseLibrary = typeof global.Promise == 'function' ?
      global.Promise : require('es6-promise').Promise;
  }

  // Assign the right collection level readPreference
  if(options && options.readPreference) {
    readPreference = options.readPreference;
  } else if(db.options.readPreference) {
    readPreference = db.options.readPreference;
  }

  // Set custom primary key factory if provided
  pkFactory = pkFactory == null
    ? ObjectID
    : pkFactory;

  // Internal state
  this.s = {
    // Set custom primary key factory if provided
      pkFactory: pkFactory
    // Db
    , db: db
    // Topology
    , topology: topology
    // dbName
    , dbName: dbName
    // Options
    , options: options
    // Namespace
    , namespace: namespace
    // Read preference
    , readPreference: readPreference
    // SlaveOK
    , slaveOk: slaveOk
    // Serialize functions
    , serializeFunctions: serializeFunctions
    // Raw
    , raw: raw
    // promoteLongs
    , promoteLongs: promoteLongs
    // promoteValues
    , promoteValues: promoteValues
    // promoteBuffers
    , promoteBuffers: promoteBuffers
    // internalHint
    , internalHint: internalHint
    // collectionHint
    , collectionHint: collectionHint
    // Name
    , name: name
    // Promise library
    , promiseLibrary: promiseLibrary
    // Read Concern
    , readConcern: options.readConcern
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.CoreConnection"></a>[function <span class="apidocSignatureSpan">mongodb.</span>CoreConnection (messageHandler, options)](#apidoc.element.mongodb.CoreConnection)
- description and source-code
```javascript
CoreConnection = function (messageHandler, options) {
  // Add event listener
  EventEmitter.call(this);
  // Set empty if no options passed
  this.options = options || {};
  // Identification information
  this.id = _id++;
  // Logger instance
  this.logger = Logger('Connection', options);
  // No bson parser passed in
  if(!options.bson) throw new Error("must pass in valid bson parser");
  // Get bson parser
  this.bson = options.bson;
  // Grouping tag used for debugging purposes
  this.tag = options.tag;
  // Message handler
  this.messageHandler = messageHandler;

  // Max BSON message size
  this.maxBsonMessageSize = options.maxBsonMessageSize || (1024 * 1024 * 16 * 4);
  // Debug information
  if(this.logger.isDebug()) this.logger.debug(f('creating connection %s with options [%s]', this.id, JSON.stringify(debugOptions
(debugFields, options))));

  // Default options
  this.port = options.port || 27017;
  this.host = options.host || 'localhost';
  this.keepAlive = typeof options.keepAlive == 'boolean' ? options.keepAlive : true;
  this.keepAliveInitialDelay = options.keepAliveInitialDelay || 0;
  this.noDelay = typeof options.noDelay == 'boolean' ? options.noDelay : true;
  this.connectionTimeout = options.connectionTimeout || 0;
  this.socketTimeout = options.socketTimeout || 0;

  // If connection was destroyed
  this.destroyed = false;

  // Check if we have a domain socket
  this.domainSocket = this.host.indexOf('\/') != -1;

  // Serialize commands using function
  this.singleBufferSerializtion = typeof options.singleBufferSerializtion == 'boolean' ? options.singleBufferSerializtion : true
;
  this.serializationFunction = this.singleBufferSerializtion ? 'toBinUnified' : 'toBin';

  // SSL options
  this.ca = options.ca || null;
  this.crl = options.crl || null;
  this.cert = options.cert || null;
  this.key = options.key || null;
  this.passphrase = options.passphrase || null;
  this.ssl = typeof options.ssl == 'boolean' ? options.ssl : false;
  this.rejectUnauthorized = typeof options.rejectUnauthorized == 'boolean' ? options.rejectUnauthorized : true;
  this.checkServerIdentity = typeof options.checkServerIdentity == 'boolean'
    || typeof options.checkServerIdentity == 'function' ? options.checkServerIdentity : true;

  // If ssl not enabled
  if(!this.ssl) this.rejectUnauthorized = false;

  // Response options
  this.responseOptions = {
    promoteLongs: typeof options.promoteLongs == 'boolean' ?  options.promoteLongs : true,
    promoteValues: typeof options.promoteValues == 'boolean' ? options.promoteValues : true,
    promoteBuffers: typeof options.promoteBuffers == 'boolean' ? options.promoteBuffers: false
  }

  // Flushing
  this.flushing = false;
  this.queue = [];

  // Internal state
  this.connection = null;
  this.writeStream = null;

  // Create hash method
  var hash = crypto.createHash('sha1');
  hash.update(f('%s:%s', this.host, this.port));

  // Create a hash name
  this.hashedName = hash.digest('hex');

  // All operations in flight on the connection
  this.workItems = [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.CoreServer"></a>[function <span class="apidocSignatureSpan">mongodb.</span>CoreServer (options)](#apidoc.element.mongodb.CoreServer)
- description and source-code
```javascript
CoreServer = function (options) {
  options = options || {};

  // Add event listener
  EventEmitter.call(this);

  // Server instance id
  this.id = id++;

  // Internal state
  this.s = {
    // Options
    options: options,
    // Logger
    logger: Logger('Server', options),
    // Factory overrides
    Cursor: options.cursorFactory || BasicCursor,
    // BSON instance
    bson: options.bson || new BSON([BSON.Binary, BSON.Code, BSON.DBRef, BSON.Decimal128,
      BSON.Double, BSON.Int32, BSON.Long, BSON.Map, BSON.MaxKey, BSON.MinKey,
      BSON.ObjectId, BSON.BSONRegExp, BSON.Symbol, BSON.Timestamp]),
    // Pool
    pool: null,
    // Disconnect handler
    disconnectHandler: options.disconnectHandler,
    // Monitor thread (keeps the connection alive)
    monitoring: typeof options.monitoring == 'boolean' ? options.monitoring : true,
    // Is the server in a topology
    inTopology: typeof options.inTopology == 'boolean' ? options.inTopology : false,
    // Monitoring timeout
    monitoringInterval: typeof options.monitoringInterval == 'number'
      ? options.monitoringInterval
      : 5000,
    // Topology id
    topologyId: -1
  }

  // Curent ismaster
  this.ismaster = null;
  // Current ping time
  this.lastIsMasterMS = -1;
  // The monitoringProcessId
  this.monitoringProcessId = null;
  // Initial connection
  this.initalConnect = true;
  // Wire protocol handler, default to oldest known protocol handler
  // this gets changed when the first ismaster is called.
  this.wireProtocolHandler = new PreTwoSixWireProtocolSupport();
  // Default type
  this._type = 'server';
  // Set the client info
  this.clientInfo = createClientInfo(options);

  // Max Stalleness values
  // last time we updated the ismaster state
  this.lastUpdateTime = 0;
  // Last write time
  this.lastWriteDate = 0;
  // Stalleness
  this.staleness = 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor"></a>[function <span class="apidocSignatureSpan">mongodb.</span>Cursor (bson, ns, cmd, options, topology, topologyOptions)](#apidoc.element.mongodb.Cursor)
- description and source-code
```javascript
Cursor = function (bson, ns, cmd, options, topology, topologyOptions) {
  CoreCursor.apply(this, Array.prototype.slice.call(arguments, 0));
  var self = this;
  var state = Cursor.INIT;
  var streamOptions = {};

  // Tailable cursor options
  var numberOfRetries = options.numberOfRetries || 5;
  var tailableRetryInterval = options.tailableRetryInterval || 500;
  var currentNumberOfRetries = numberOfRetries;

  // Get the promiseLibrary
  var promiseLibrary = options.promiseLibrary;

  // No promise library selected fall back
  if(!promiseLibrary) {
    promiseLibrary = typeof global.Promise == 'function' ?
      global.Promise : require('es6-promise').Promise;
  }

  // Set up
  Readable.call(this, {objectMode: true});

  // Internal cursor state
  this.s = {
    // Tailable cursor options
      numberOfRetries: numberOfRetries
    , tailableRetryInterval: tailableRetryInterval
    , currentNumberOfRetries: currentNumberOfRetries
    // State
    , state: state
    // Stream options
    , streamOptions: streamOptions
    // BSON
    , bson: bson
    // Namespace
    , ns: ns
    // Command
    , cmd: cmd
    // Options
    , options: options
    // Topology
    , topology: topology
    // Topology options
    , topologyOptions: topologyOptions
    // Promise library
    , promiseLibrary: promiseLibrary
    // Current doc
    , currentDoc: null
  }

  // Translate correctly
  if(self.s.options.noCursorTimeout == true) {
    self.addCursorFlag('noCursorTimeout', true);
  }

  // Set the sort value
  this.sortValue = self.s.cmd.sort;

  // Get the batchSize
  var batchSize = cmd.cursor && cmd.cursor.batchSize
    ? cmd.cursor && cmd.cursor.batchSize
    : (options.cursor && options.cursor.batchSize ? options.cursor.batchSize : 1000);

  // Set the batchSize
  this.setCursorBatchSize(batchSize);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.DBRef"></a>[function <span class="apidocSignatureSpan">mongodb.</span>DBRef (namespace, oid, db)](#apidoc.element.mongodb.DBRef)
- description and source-code
```javascript
function DBRef(namespace, oid, db) {
  if(!(this instanceof DBRef)) return new DBRef(namespace, oid, db);

  this._bsontype = 'DBRef';
  this.namespace = namespace;
  this.oid = oid;
  this.db = db;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Db"></a>[function <span class="apidocSignatureSpan">mongodb.</span>Db (databaseName, topology, options)](#apidoc.element.mongodb.Db)
- description and source-code
```javascript
Db = function (databaseName, topology, options) {
  options = options || {};
  if(!(this instanceof Db)) return new Db(databaseName, topology, options);
  EventEmitter.call(this);
  var self = this;

  // Get the promiseLibrary
  var promiseLibrary = options.promiseLibrary;

  // No promise library selected fall back
  if(!promiseLibrary) {
    promiseLibrary = typeof global.Promise == 'function' ?
      global.Promise : require('es6-promise').Promise;
  }

  // Filter the options
  options = filterOptions(options, legalOptionNames);

  // Ensure we put the promiseLib in the options
  options.promiseLibrary = promiseLibrary;

  // var self = this;  // Internal state of the db object
  this.s = {
    // Database name
      databaseName: databaseName
    // DbCache
    , dbCache: {}
    // Children db's
    , children: []
    // Topology
    , topology: topology
    // Options
    , options: options
    // Logger instance
    , logger: Logger('Db', options)
    // Get the bson parser
    , bson: topology ? topology.bson : null
    // Authsource if any
    , authSource: options.authSource
    // Unpack read preference
    , readPreference: options.readPreference
    // Set buffermaxEntries
    , bufferMaxEntries: typeof options.bufferMaxEntries == 'number' ? options.bufferMaxEntries : -1
    // Parent db (if chained)
    , parentDb: options.parentDb || null
    // Set up the primary key factory or fallback to ObjectID
    , pkFactory: options.pkFactory || ObjectID
    // Get native parser
    , nativeParser: options.nativeParser || options.native_parser
    // Promise library
    , promiseLibrary: promiseLibrary
    // No listener
    , noListener: typeof options.noListener == 'boolean' ? options.noListener : false
    // ReadConcern
    , readConcern: options.readConcern
  }

  // Ensure we have a valid db name
  validateDatabaseName(self.s.databaseName);

  // Add a read Only property
  getSingleProperty(this, 'serverConfig', self.s.topology);
  getSingleProperty(this, 'bufferMaxEntries', self.s.bufferMaxEntries);
  getSingleProperty(this, 'databaseName', self.s.databaseName);

  // This is a child db, do not register any listeners
  if(options.parentDb) return;
  if(this.s.noListener) return;

  // Add listeners
  topology.on('error', createListener(self, 'error', self));
  topology.on('timeout', createListener(self, 'timeout', self));
  topology.on('close', createListener(self, 'close', self));
  topology.on('parseError', createListener(self, 'parseError', self));
  topology.once('open', createListener(self, 'open', self));
  topology.once('fullsetup', createListener(self, 'fullsetup', self));
  topology.once('all', createListener(self, 'all', self));
  topology.on('reconnect', createListener(self, 'reconnect', self));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Decimal128"></a>[function <span class="apidocSignatureSpan">mongodb.</span>Decimal128 (bytes)](#apidoc.element.mongodb.Decimal128)
- description and source-code
```javascript
Decimal128 = function (bytes) {
  this._bsontype = 'Decimal128';
  this.bytes = bytes;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Double"></a>[function <span class="apidocSignatureSpan">mongodb.</span>Double (value)](#apidoc.element.mongodb.Double)
- description and source-code
```javascript
function Double(value) {
  if(!(this instanceof Double)) return new Double(value);

  this._bsontype = 'Double';
  this.value = value;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.GridFSBucket"></a>[function <span class="apidocSignatureSpan">mongodb.</span>GridFSBucket (db, options)](#apidoc.element.mongodb.GridFSBucket)
- description and source-code
```javascript
function GridFSBucket(db, options) {
  Emitter.apply(this);
  this.setMaxListeners(0);

  if (options && typeof options === 'object') {
    options = shallowClone(options);
    var keys = Object.keys(DEFAULT_GRIDFS_BUCKET_OPTIONS);
    for (var i = 0; i < keys.length; ++i) {
      if (!options[keys[i]]) {
        options[keys[i]] = DEFAULT_GRIDFS_BUCKET_OPTIONS[keys[i]];
      }
    }
  } else {
    options = DEFAULT_GRIDFS_BUCKET_OPTIONS;
  }

  this.s = {
    db: db,
    options: options,
    _chunksCollection: db.collection(options.bucketName + '.chunks'),
    _filesCollection: db.collection(options.bucketName + '.files'),
    checkedIndexes: false,
    calledOpenUploadStream: false,
    promiseLibrary: db.s.promiseLibrary ||
      (typeof global.Promise == 'function' ? global.Promise : require('es6-promise').Promise)
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.GridStore"></a>[function <span class="apidocSignatureSpan">mongodb.</span>GridStore (db, id, filename, mode, options)](#apidoc.element.mongodb.GridStore)
- description and source-code
```javascript
function GridStore(db, id, filename, mode, options) {
  if(!(this instanceof GridStore)) return new GridStore(db, id, filename, mode, options);
  this.db = db;

  // Handle options
  if(typeof options === 'undefined') options = {};
  // Handle mode
  if(typeof mode === 'undefined') {
    mode = filename;
    filename = undefined;
  } else if(typeof mode == 'object') {
    options = mode;
    mode = filename;
    filename = undefined;
  }

  if(id && id._bsontype == 'ObjectID') {
    this.referenceBy = REFERENCE_BY_ID;
    this.fileId = id;
    this.filename = filename;
  } else if(typeof filename == 'undefined') {
    this.referenceBy = REFERENCE_BY_FILENAME;
    this.filename = id;
    if (mode.indexOf('w') != null) {
      this.fileId = new ObjectID();
    }
  } else {
    this.referenceBy = REFERENCE_BY_ID;
    this.fileId = id;
    this.filename = filename;
  }

  // Set up the rest
  this.mode = mode == null ? "r" : mode;
  this.options = options || {};

  // Opened
  this.isOpen = false;

  // Set the root if overridden
  this.root = this.options['root'] == null ? GridStore.DEFAULT_ROOT_COLLECTION : this.options['root'];
  this.position = 0;
  this.readPreference = this.options.readPreference || db.options.readPreference || ReadPreference.PRIMARY;
  this.writeConcern = _getWriteConcern(db, this.options);
  // Set default chunk size
  this.internalChunkSize = this.options['chunkSize'] == null ? Chunk.DEFAULT_CHUNK_SIZE : this.options['chunkSize'];

  // Get the promiseLibrary
  var promiseLibrary = this.options.promiseLibrary;

  // No promise library selected fall back
  if(!promiseLibrary) {
    promiseLibrary = typeof global.Promise == 'function' ?
      global.Promise : require('es6-promise').Promise;
  }

  // Set the promiseLibrary
  this.promiseLibrary = promiseLibrary;

  Object.defineProperty(this, "chunkSize", { enumerable: true
   , get: function () {
       return this.internalChunkSize;
     }
   , set: function(value) {
       if(!(this.mode[0] == "w" && this.position == 0 && this.uploadDate == null)) {
         this.internalChunkSize = this.internalChunkSize;
       } else {
         this.internalChunkSize = value;
       }
     }
  });

  Object.defineProperty(this, "md5", { enumerable: true
   , get: function () {
       return this.internalMd5;
     }
  });

  Object.defineProperty(this, "chunkNumber", { enumerable: true
   , get: function () {
       return this.currentChunk && this.currentChunk.chunkNumber ? this.currentChunk.chunkNumber : null;
     }
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Int32"></a>[function <span class="apidocSignatureSpan">mongodb.</span>Int32 (value)](#apidoc.element.mongodb.Int32)
- description and source-code
```javascript
Int32 = function (value) {
  if(!(this instanceof Int32)) return new Int32(value);

  this._bsontype = 'Int32';
  this.value = value;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Logger"></a>[function <span class="apidocSignatureSpan">mongodb.</span>Logger (className, options)](#apidoc.element.mongodb.Logger)
- description and source-code
```javascript
Logger = function (className, options) {
  if(!(this instanceof Logger)) return new Logger(className, options);
  options = options || {};

  // Current reference
  this.className = className;

  // Current logger
  if(options.logger) {
    currentLogger = options.logger;
  } else if(currentLogger == null) {
    currentLogger = console.log;
  }

  // Set level of logging, default is error
  if(options.loggerLevel) {
    level = options.loggerLevel || 'error';
  }

  // Add all class names
  if(filteredClasses[this.className] == null) classFilters[this.className] =  true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Long"></a>[function <span class="apidocSignatureSpan">mongodb.</span>Long (low, high)](#apidoc.element.mongodb.Long)
- description and source-code
```javascript
function Long(low, high) {
  if(!(this instanceof Long)) return new Long(low, high);

  this._bsontype = 'Long';
<span class="apidocCodeCommentSpan">  /**
   * @type {number}
   * @ignore
   */
</span>  this.low_ = low | 0;  // force into 32 signed bits.

  /**
   * @type {number}
   * @ignore
   */
  this.high_ = high | 0;  // force into 32 signed bits.
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Map"></a>[function <span class="apidocSignatureSpan">mongodb.</span>Map ()](#apidoc.element.mongodb.Map)
- description and source-code
```javascript
function Map() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.MaxKey"></a>[function <span class="apidocSignatureSpan">mongodb.</span>MaxKey ()](#apidoc.element.mongodb.MaxKey)
- description and source-code
```javascript
function MaxKey() {
  if(!(this instanceof MaxKey)) return new MaxKey();

  this._bsontype = 'MaxKey';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.MinKey"></a>[function <span class="apidocSignatureSpan">mongodb.</span>MinKey ()](#apidoc.element.mongodb.MinKey)
- description and source-code
```javascript
function MinKey() {
  if(!(this instanceof MinKey)) return new MinKey();

  this._bsontype = 'MinKey';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.MongoClient"></a>[function <span class="apidocSignatureSpan">mongodb.</span>MongoClient ()](#apidoc.element.mongodb.MongoClient)
- description and source-code
```javascript
function MongoClient() {
<span class="apidocCodeCommentSpan">  /**
   * The callback format for results
   * @callback MongoClient~connectCallback
   * @param {MongoError} error An error instance representing the error during the execution.
   * @param {Db} db The connected database.
   */
</span>
  /**
   * Connect to MongoDB using a url as documented at
   *
   *  docs.mongodb.org/manual/reference/connection-string/
   *
   * Note that for replicasets the replicaSet query parameter is required in the 2.0 driver
   *
   * @method
   * @param {string} url The connection URI string
   * @param {object} [options] Optional settings.
   * @param {number} [options.poolSize=5] poolSize The maximum size of the individual server pool.
   * @param {boolean} [options.ssl=false] Enable SSL connection.
   * @param {Buffer} [options.sslCA=undefined] SSL Certificate store binary buffer
   * @param {Buffer} [options.sslCRL=undefined] SSL Certificate revocation list binary buffer
   * @param {Buffer} [options.sslCert=undefined] SSL Certificate binary buffer
   * @param {Buffer} [options.sslKey=undefined] SSL Key file binary buffer
   * @param {string} [options.sslPass=undefined] SSL Certificate pass phrase
   * @param {boolean|function} [options.checkServerIdentity=true] Ensure we check server identify during SSL, set to false to disable
 checking. Only works for Node 0.12.x or higher. You can pass in a boolean or your own checkServerIdentity override function.
   * @param {boolean} [options.autoReconnect=true] Enable autoReconnect for single server instances
   * @param {boolean} [options.noDelay=true] TCP Connection no delay
   * @param {boolean} [options.keepAlive=0] The number of milliseconds to wait before initiating keepAlive on the TCP socket.
   * @param {number} [options.connectTimeoutMS=30000] TCP Connection timeout setting
   * @param {number} [options.socketTimeoutMS=30000] TCP Socket timeout setting
   * @param {number} [options.reconnectTries=30] Server attempt to reconnect #times
   * @param {number} [options.reconnectInterval=1000] Server will wait # milliseconds between retries
   * @param {boolean} [options.ha=true] Control if high availability monitoring runs for Replicaset or Mongos proxies.
   * @param {number} [options.haInterval=10000] The High availability period for replicaset inquiry
   * @param {string} [options.replicaSet=undefined] The Replicaset set name
   * @param {number} [options.secondaryAcceptableLatencyMS=15] Cutoff latency point in MS for Replicaset member selection
   * @param {number} [options.acceptableLatencyMS=15] Cutoff latency point in MS for Mongos proxies selection.
   * @param {boolean} [options.connectWithNoPrimary=false] Sets if the driver should connect even if no primary is available
   * @param {string} [options.authSource=undefined] Define the database to authenticate against
   * @param {(number|string)} [options.w=null] The write concern.
   * @param {number} [options.wtimeout=null] The write concern timeout.
   * @param {boolean} [options.j=false] Specify a journal write concern.
   * @param {boolean} [options.forceServerObjectId=false] Force server to assign _id values instead of driver.
   * @param {boolean} [options.serializeFunctions=false] Serialize functions on any object.
   * @param {Boolean} [options.ignoreUndefined=false] Specify if the BSON serializer should ignore undefined fields.
   * @param {boolean} [options.raw=false] Return document results as raw BSON buffers.
   * @param {boolean} [options.promoteLongs=true] Promotes Long values to number if they fit inside the 53 bits resolution.
   * @param {boolean} [options.promoteBuffers=false] Promotes Binary BSON values to native Node Buffers.
   * @param {boolean} [options.promoteValues=true] Promotes BSON values to native types where possible, set to false to only receive
 wrapper types.
   * @param {number} [options.bufferMaxEntries=-1] Sets a cap on how many operations the driver will buffer up before giving up
on getting a working connection, default is -1 which is unlimited.
   * @param {(ReadPreference|string)} [options.readPreference=null] The preferred ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.MongoError"></a>[function <span class="apidocSignatureSpan">mongodb.</span>MongoError (message)](#apidoc.element.mongodb.MongoError)
- description and source-code
```javascript
function MongoError(message) {
  this.name = 'MongoError';
  this.message = message;
  Error.captureStackTrace(this, MongoError);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Mongos"></a>[function <span class="apidocSignatureSpan">mongodb.</span>Mongos (servers, options)](#apidoc.element.mongodb.Mongos)
- description and source-code
```javascript
Mongos = function (servers, options) {
  if(!(this instanceof Mongos)) return new Mongos(servers, options);
  options = options || {};
  var self = this;

  // Filter the options
  options = filterOptions(options, legalOptionNames);

  // Ensure all the instances are Server
  for(var i = 0; i < servers.length; i++) {
    if(!(servers[i] instanceof Server)) {
      throw MongoError.create({message: "all seed list instances must be of the Server type", driver:true});
    }
  }

  // Stored options
  var storeOptions = {
      force: false
    , bufferMaxEntries: typeof options.bufferMaxEntries == 'number' ? options.bufferMaxEntries : MAX_JS_INT
  }

  // Shared global store
  var store = options.store || new Store(self, storeOptions);

  // Set up event emitter
  EventEmitter.call(this);

  // Build seed list
  var seedlist = servers.map(function(x) {
    return {host: x.host, port: x.port}
  });

  // Get the reconnect option
  var reconnect = typeof options.auto_reconnect == 'boolean' ? options.auto_reconnect : true;
  reconnect = typeof options.autoReconnect == 'boolean' ? options.autoReconnect : reconnect;

  // Clone options
  var clonedOptions = mergeOptions({}, {
    disconnectHandler: store,
    cursorFactory: Cursor,
    reconnect: reconnect,
    emitError: typeof options.emitError == 'boolean' ? options.emitError : true,
    size: typeof options.poolSize == 'number' ? options.poolSize : 5
  });

  // Translate any SSL options and other connectivity options
  clonedOptions = translateOptions(clonedOptions, options);

  // Socket options
  var socketOptions = options.socketOptions && Object.keys(options.socketOptions).length > 0
    ? options.socketOptions : options;

  // Translate all the options to the mongodb-core ones
  clonedOptions = translateOptions(clonedOptions, socketOptions);
  if(typeof clonedOptions.keepAlive == 'number') {
    clonedOptions.keepAliveInitialDelay = clonedOptions.keepAlive;
    clonedOptions.keepAlive = clonedOptions.keepAlive > 0;
  }

  // Build default client information
  this.clientInfo = {
    driver: {
      name: "nodejs",
      version: driverVersion
    },
    os: {
      type: type,
      name: name,
      architecture: architecture,
      version: release
    },
    platform: nodejsversion
  }

  // Build default client information
  clonedOptions.clientInfo = this.clientInfo;
  // Do we have an application specific string
  if(options.appname) {
    clonedOptions.clientInfo.application = { name: options.appname };
  }

  // Create the Mongos
  var mongos = new CMongos(seedlist, clonedOptions)
  // Server capabilities
  var sCapabilities = null;

  // Internal state
  this.s = {
    // Create the Mongos
      mongos: mongos
    // Server capabilities
    , sCapabilities: sCapabilities
    // Debug turned on
    , debug: clonedOptions.debug
    // Store option defaults
    , storeOptions: storeOptions
    // Cloned options
    , clonedOptions: clonedOptions
    // Actual store of callbacks
    , store: store
    // Options
    , options: options
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.ObjectID"></a>[function <span class="apidocSignatureSpan">mongodb.</span>ObjectID (id)](#apidoc.element.mongodb.ObjectID)
- description and source-code
```javascript
function ObjectID(id) {
  // Duck-typing to support ObjectId from different npm packages
  if(id instanceof ObjectID) return id;
  if(!(this instanceof ObjectID)) return new ObjectID(id);

  this._bsontype = 'ObjectID';

  // The most common usecase (blank id, new objectId instance)
  if(id == null || typeof id == 'number') {
    // Generate a new id
    this.id = this.generate(id);
    // If we are caching the hex string
    if(ObjectID.cacheHexString) this.__id = this.toString('hex');
    // Return the object
    return;
  }

  // Check if the passed in id is valid
  var valid = ObjectID.isValid(id);

  // Throw an error if it's not a valid setup
  if(!valid && id != null){
    throw new Error("Argument passed in must be a single String of 12 bytes or a string of 24 hex characters");
  } else if(valid && typeof id == 'string' && id.length == 24 && hasBufferType) {
    return new ObjectID(new Buffer(id, 'hex'));
  } else if(valid && typeof id == 'string' && id.length == 24) {
    return ObjectID.createFromHexString(id);
  } else if(id != null && id.length === 12) {
    // assume 12 byte string
    this.id = id;
  } else if(id != null && id.toHexString) {
    // Duck-typing to support ObjectId from different npm packages
    return id;
  } else {
    throw new Error("Argument passed in must be a single String of 12 bytes or a string of 24 hex characters");
  }

  if(ObjectID.cacheHexString) this.__id = this.toString('hex');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.ObjectId"></a>[function <span class="apidocSignatureSpan">mongodb.</span>ObjectId (id)](#apidoc.element.mongodb.ObjectId)
- description and source-code
```javascript
function ObjectID(id) {
  // Duck-typing to support ObjectId from different npm packages
  if(id instanceof ObjectID) return id;
  if(!(this instanceof ObjectID)) return new ObjectID(id);

  this._bsontype = 'ObjectID';

  // The most common usecase (blank id, new objectId instance)
  if(id == null || typeof id == 'number') {
    // Generate a new id
    this.id = this.generate(id);
    // If we are caching the hex string
    if(ObjectID.cacheHexString) this.__id = this.toString('hex');
    // Return the object
    return;
  }

  // Check if the passed in id is valid
  var valid = ObjectID.isValid(id);

  // Throw an error if it's not a valid setup
  if(!valid && id != null){
    throw new Error("Argument passed in must be a single String of 12 bytes or a string of 24 hex characters");
  } else if(valid && typeof id == 'string' && id.length == 24 && hasBufferType) {
    return new ObjectID(new Buffer(id, 'hex'));
  } else if(valid && typeof id == 'string' && id.length == 24) {
    return ObjectID.createFromHexString(id);
  } else if(id != null && id.length === 12) {
    // assume 12 byte string
    this.id = id;
  } else if(id != null && id.toHexString) {
    // Duck-typing to support ObjectId from different npm packages
    return id;
  } else {
    throw new Error("Argument passed in must be a single String of 12 bytes or a string of 24 hex characters");
  }

  if(ObjectID.cacheHexString) this.__id = this.toString('hex');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.ReadPreference"></a>[function <span class="apidocSignatureSpan">mongodb.</span>ReadPreference (mode, tags, options)](#apidoc.element.mongodb.ReadPreference)
- description and source-code
```javascript
ReadPreference = function (mode, tags, options) {
  if(!(this instanceof ReadPreference)) {
    return new ReadPreference(mode, tags, options);
  }

  this._type = 'ReadPreference';
  this.mode = mode;
  this.tags = tags;
  this.options =  options;

  // If no tags were passed in
  if(tags && typeof tags == 'object' && !Array.isArray(tags)) {
    if(tags.maxStalenessSeconds) {
      this.options = tags;
      this.tags = null;
    }
  }

  // Add the maxStalenessSeconds value to the read Preference
  if(this.options && this.options.maxStalenessSeconds) {
    this.maxStalenessSeconds = this.options.maxStalenessSeconds;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.ReplSet"></a>[function <span class="apidocSignatureSpan">mongodb.</span>ReplSet (servers, options)](#apidoc.element.mongodb.ReplSet)
- description and source-code
```javascript
ReplSet = function (servers, options) {
  if(!(this instanceof ReplSet)) return new ReplSet(servers, options);
  options = options || {};
  var self = this;
  // Set up event emitter
  EventEmitter.call(this);

  // Filter the options
  options = filterOptions(options, legalOptionNames);

  // Ensure all the instances are Server
  for(var i = 0; i < servers.length; i++) {
    if(!(servers[i] instanceof Server)) {
      throw MongoError.create({message: "all seed list instances must be of the Server type", driver:true});
    }
  }

  // Stored options
  var storeOptions = {
      force: false
    , bufferMaxEntries: typeof options.bufferMaxEntries == 'number' ? options.bufferMaxEntries : MAX_JS_INT
  }

  // Shared global store
  var store = options.store || new Store(self, storeOptions);

  // Build seed list
  var seedlist = servers.map(function(x) {
    return {host: x.host, port: x.port}
  });

  // Clone options
  var clonedOptions = mergeOptions({}, {
    disconnectHandler: store,
    cursorFactory: Cursor,
    reconnect: false,
    emitError: typeof options.emitError == 'boolean' ? options.emitError : true,
    size: typeof options.poolSize == 'number' ? options.poolSize : 5
  });

  // Translate any SSL options and other connectivity options
  clonedOptions = translateOptions(clonedOptions, options);

  // Socket options
  var socketOptions = options.socketOptions && Object.keys(options.socketOptions).length > 0
    ? options.socketOptions : options;

  // Translate all the options to the mongodb-core ones
  clonedOptions = translateOptions(clonedOptions, socketOptions);
  if(typeof clonedOptions.keepAlive == 'number') {
    clonedOptions.keepAliveInitialDelay = clonedOptions.keepAlive;
    clonedOptions.keepAlive = clonedOptions.keepAlive > 0;
  }

  // Client info
  this.clientInfo = {
    driver: {
      name: "nodejs",
      version: driverVersion
    },
    os: {
      type: type,
      name: name,
      architecture: architecture,
      version: release
    },
    platform: nodejsversion
  }

  // Build default client information
  clonedOptions.clientInfo = this.clientInfo;
  // Do we have an application specific string
  if(options.appname) {
    clonedOptions.clientInfo.application = { name: options.appname };
  }

  // Create the ReplSet
  var replset = new CReplSet(seedlist, clonedOptions);

  // Listen to reconnect event
  replset.on('reconnect', function() {
    self.emit('reconnect');
    store.execute();
  });

  // Internal state
  this.s = {
    // Replicaset
    replset: replset
    // Server capabilities
    , sCapabilities: null
    // Debug tag
    , tag: options.tag
    // Store options
    , storeOptions: storeOptions
    // Cloned options
    , clonedOptions: clonedOptions
    // Store
    , store: store
    // Options
    , options: options
  }

  // Debug
  if(clonedOptions.debug) {
    // Last ismaster
    Object.defineProperty(this, 'replset', {
      enumerable:true, get: function() { return replset; }
    });
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Server"></a>[function <span class="apidocSignatureSpan">mongodb.</span>Server (host, port, options)](#apidoc.element.mongodb.Server)
- description and source-code
```javascript
Server = function (host, port, options) {
  options = options || {};
  if(!(this instanceof Server)) return new Server(host, port, options);
  EventEmitter.call(this);
  var self = this;

  // Filter the options
  options = filterOptions(options, legalOptionNames);

  // Stored options
  var storeOptions = {
      force: false
    , bufferMaxEntries: typeof options.bufferMaxEntries == 'number' ? options.bufferMaxEntries : MAX_JS_INT
  }

  // Shared global store
  var store = options.store || new Store(self, storeOptions);

  // Detect if we have a socket connection
  if(host.indexOf('\/') != -1) {
    if(port != null && typeof port == 'object') {
      options = port;
      port = null;
    }
  } else if(port == null) {
    throw MongoError.create({message: 'port must be specified', driver:true});
  }

  // Get the reconnect option
  var reconnect = typeof options.auto_reconnect == 'boolean' ? options.auto_reconnect : true;
  reconnect = typeof options.autoReconnect == 'boolean' ? options.autoReconnect : reconnect;

  // Clone options
  var clonedOptions = mergeOptions({}, {
    host: host, port: port, disconnectHandler: store,
    cursorFactory: Cursor,
    reconnect: reconnect,
    emitError: typeof options.emitError == 'boolean' ? options.emitError : true,
    size: typeof options.poolSize == 'number' ? options.poolSize : 5
  });

  // Translate any SSL options and other connectivity options
  clonedOptions = translateOptions(clonedOptions, options);

  // Socket options
  var socketOptions = options.socketOptions && Object.keys(options.socketOptions).length > 0
    ? options.socketOptions : options;

  // Translate all the options to the mongodb-core ones
  clonedOptions = translateOptions(clonedOptions, socketOptions);
  if(typeof clonedOptions.keepAlive == 'number') {
    clonedOptions.keepAliveInitialDelay = clonedOptions.keepAlive;
    clonedOptions.keepAlive = clonedOptions.keepAlive > 0;
  }

  // Build default client information
  this.clientInfo = {
    driver: {
      name: "nodejs",
      version: driverVersion
    },
    os: {
      type: type,
      name: name,
      architecture: architecture,
      version: release
    },
    platform: nodejsversion
  }

  // Build default client information
  clonedOptions.clientInfo = this.clientInfo;
  // Do we have an application specific string
  if(options.appname) {
    clonedOptions.clientInfo.application = { name: options.appname };
  }

  // Create an instance of a server instance from mongodb-core
  var server = new CServer(clonedOptions);

  // Define the internal properties
  this.s = {
    // Create an instance of a server instance from mongodb-core
      server: server
    // Server capabilities
    , sCapabilities: null
    // Cloned options
    , clonedOptions: clonedOptions
    // Reconnect
    , reconnect: clonedOptions.reconnect
    // Emit error
    , emitError: clonedOptions.emitError
    // Pool size
    , poolSize: clonedOptions.size
    // Store Options
    , storeOptions: storeOptions
    // Store
    , store: store
    // Host
    , host: host
    // Port
    , port: port
    // Options
    , options: options
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Symbol"></a>[function <span class="apidocSignatureSpan">mongodb.</span>Symbol (value)](#apidoc.element.mongodb.Symbol)
- description and source-code
```javascript
function Symbol(value) {
  if(!(this instanceof Symbol)) return new Symbol(value);
  this._bsontype = 'Symbol';
  this.value = value;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Timestamp"></a>[function <span class="apidocSignatureSpan">mongodb.</span>Timestamp (low, high)](#apidoc.element.mongodb.Timestamp)
- description and source-code
```javascript
function Timestamp(low, high) {
  if(!(this instanceof Timestamp)) return new Timestamp(low, high);
  this._bsontype = 'Timestamp';
<span class="apidocCodeCommentSpan">  /**
   * @type {number}
   * @ignore
   */
</span>  this.low_ = low | 0;  // force into 32 signed bits.

  /**
   * @type {number}
   * @ignore
   */
  this.high_ = high | 0;  // force into 32 signed bits.
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor"></a>[function <span class="apidocSignatureSpan">mongodb.</span>aggregation_cursor (bson, ns, cmd, options, topology, topologyOptions)](#apidoc.element.mongodb.aggregation_cursor)
- description and source-code
```javascript
aggregation_cursor = function (bson, ns, cmd, options, topology, topologyOptions) {
  CoreCursor.apply(this, Array.prototype.slice.call(arguments, 0));
  var state = AggregationCursor.INIT;
  var streamOptions = {};

  // MaxTimeMS
  var maxTimeMS = null;

  // Get the promiseLibrary
  var promiseLibrary = options.promiseLibrary;

  // No promise library selected fall back
  if(!promiseLibrary) {
    promiseLibrary = typeof global.Promise == 'function' ?
      global.Promise : require('es6-promise').Promise;
  }

  // Set up
  Readable.call(this, {objectMode: true});

  // Internal state
  this.s = {
    // MaxTimeMS
      maxTimeMS: maxTimeMS
    // State
    , state: state
    // Stream options
    , streamOptions: streamOptions
    // BSON
    , bson: bson
    // Namespace
    , ns: ns
    // Command
    , cmd: cmd
    // Options
    , options: options
    // Topology
    , topology: topology
    // Topology Options
    , topologyOptions: topologyOptions
    // Promise library
    , promiseLibrary: promiseLibrary
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.apm"></a>[function <span class="apidocSignatureSpan">mongodb.</span>apm (core, options, callback)](#apidoc.element.mongodb.apm)
- description and source-code
```javascript
apm = function (core, options, callback) {
  options = options || {};

  // Optional id generators
  var operationIdGenerator = options.operationIdGenerator || basicOperationIdGenerator;
  // Optional timestamp generator
  var timestampGenerator = options.timestampGenerator || basicTimestampGenerator;
  // Extend with event emitter functionality
  EventEmitter.call(this);

  // Contains all the instrumentation overloads
  this.overloads = [];

  // ---------------------------------------------------------
  //
  // Instrument prototype
  //
  // ---------------------------------------------------------

  var instrumentPrototype = function(callback) {
    var instrumentations = []

    // Classes to support
    var classes = [GridStore, OrderedBulkOperation, UnorderedBulkOperation,
      CommandCursor, AggregationCursor, Cursor, Collection, Db];

    // Add instrumentations to the available list
    for(var i = 0; i < classes.length; i++) {
      if(classes[i].define) {
        instrumentations.push(classes[i].define.generate());
      }
    }

    // Return the list of instrumentation points
    callback(null, instrumentations);
  }

  // Did the user want to instrument the prototype
  if(typeof callback == 'function') {
    instrumentPrototype(callback);
  }

  // ---------------------------------------------------------
  //
  // Server
  //
  // ---------------------------------------------------------

  // Reference
  var self = this;
  // Names of methods we need to wrap
  var methods = ['command', 'insert', 'update', 'remove'];
  // Prototype
  var proto = core.Server.prototype;
  // Core server method we are going to wrap
  methods.forEach(function(x) {
    var func = proto[x];

    // Add to overloaded methods
    self.overloads.push({proto: proto, name:x, func:func});

    // The actual prototype
    proto[x] = function() {
      var requestId = core.Query.nextRequestId();
      // Get the aruments
      var args = Array.prototype.slice.call(arguments, 0);
      var ns = args[0];
      var commandObj = args[1];
      var options = args[2] || {};
      var keys = Object.keys(commandObj);
      var commandName = keys[0];
      var db = ns.split('.')[0];

      // Get the collection
      var col = ns.split('.');
      col.shift();
      col = col.join('.');

      // Do we have a legacy insert/update/remove command
      if(x == 'insert') { //} && !this.lastIsMaster().maxWireVersion) {
        commandName = 'insert';

        // Re-write the command
        commandObj = {
          insert: col, documents: commandObj
        }

        if(options.writeConcern && Object.keys(options.writeConcern).length > 0)  {
          commandObj.writeConcern = options.writeConcern;
        }

        commandObj.ordered = options.ordered != undefined ? options.ordered : true;
      } else if(x == 'update') { // && !this.lastIsMaster().maxWireVersion) {
        commandName = 'update';

        // Re-write the command
        commandObj = {
          update: col, updates: commandObj
        }

        if(options.writeConcern && Object.keys(options.writeConcern).length > 0) {
          commandObj.writeConcern = options.writeConcern;
        }

        commandObj.ordered = options.ordered != undefined ? options.ordered : true;
      } else if(x == 'remove') { //&& !this.lastIsMaster().maxWireVersion) {
        commandName = 'delete';

        // Re-write the command
        commandObj = {
          delete: col, deletes: commandObj
        }

        if(options.writeConcern && Object.keys(options.writeConcern).length > 0) {
          commandObj.writeConcern = options.writeConcern;
        }

        commandObj.ordered = options.ordered != undefined ? options.ordered : true;
      }

      // Get the callback
      var callback = args.pop();
      // Set current callback operation id from the current context or create
      // a new one
      var ourOpId = callback.operationId || operationIdGenerator.next();

      // Get a connection reference for this server instance
      var connection = this.s.pool.get()

      // Emit the start event ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.command_cursor"></a>[function <span class="apidocSignatureSpan">mongodb.</span>command_cursor (bson, ns, cmd, options, topology, topologyOptions)](#apidoc.element.mongodb.command_cursor)
- description and source-code
```javascript
command_cursor = function (bson, ns, cmd, options, topology, topologyOptions) {
  CoreCursor.apply(this, Array.prototype.slice.call(arguments, 0));
  var state = CommandCursor.INIT;
  var streamOptions = {};

  // MaxTimeMS
  var maxTimeMS = null;

  // Get the promiseLibrary
  var promiseLibrary = options.promiseLibrary;

  // No promise library selected fall back
  if(!promiseLibrary) {
    promiseLibrary = typeof global.Promise == 'function' ?
      global.Promise : require('es6-promise').Promise;
  }

  // Set up
  Readable.call(this, {objectMode: true});

  // Internal state
  this.s = {
    // MaxTimeMS
      maxTimeMS: maxTimeMS
    // State
    , state: state
    // Stream options
    , streamOptions: streamOptions
    // BSON
    , bson: bson
    // Namespace
    , ns: ns
    // Command
    , cmd: cmd
    // Options
    , options: options
    // Topology
    , topology: topology
    // Topology Options
    , topologyOptions: topologyOptions
    // Promise library
    , promiseLibrary: promiseLibrary
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.connect"></a>[function <span class="apidocSignatureSpan">mongodb.</span>connect (url, options, callback)](#apidoc.element.mongodb.connect)
- description and source-code
```javascript
connect = function (url, options, callback) {
  var args = Array.prototype.slice.call(arguments, 1);
  callback = typeof args[args.length - 1] == 'function' ? args.pop() : null;
  options = args.length ? args.shift() : null;
  options = options || {};

  // Validate options object
  var err = validOptions(options);

  // Get the promiseLibrary
  var promiseLibrary = options.promiseLibrary;

  // No promise library selected fall back
  if(!promiseLibrary) {
    promiseLibrary = typeof global.Promise == 'function' ?
      global.Promise : require('es6-promise').Promise;
  }

  // Return a promise
  if(typeof callback != 'function') {
    return new promiseLibrary(function(resolve, reject) {
      // Did we have a validation error
      if(err) return reject(err);
      // Attempt to connect
      connect(url, options, function(err, db) {
        if(err) return reject(err);
        resolve(db);
      });
    });
  }

  // Did we have a validation error
  if(err) return callback(err);
  // Fallback to callback based connect
  connect(url, options, callback);
}
```
- example usage
```shell
...
'''js
var MongoClient = require('mongodb').MongoClient
  , assert = require('assert');

// Connection URL
var url = 'mongodb://localhost:27017/myproject';
// Use connect method to connect to the Server
MongoClient.connect(url, function(err, db) {
  assert.equal(null, err);
  console.log("Connected correctly to server");

  db.close();
});
'''
...
```

#### <a name="apidoc.element.mongodb.instrument"></a>[function <span class="apidocSignatureSpan">mongodb.</span>instrument (options, callback)](#apidoc.element.mongodb.instrument)
- description and source-code
```javascript
instrument = function (options, callback) {
  if(typeof options == 'function') callback = options, options = {};
  return new Instrumentation(core, options, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.metadata"></a>[function <span class="apidocSignatureSpan">mongodb.</span>metadata (name, object, stream)](#apidoc.element.mongodb.metadata)
- description and source-code
```javascript
metadata = function (name, object, stream) {
  this.name = name;
  this.object = object;
  this.stream = typeof stream == 'boolean' ? stream : false;
  this.instrumentations = {};
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.Admin"></a>[module mongodb.Admin](#apidoc.module.mongodb.Admin)

#### <a name="apidoc.element.mongodb.Admin.Admin"></a>[function <span class="apidocSignatureSpan">mongodb.</span>Admin (db, topology, promiseLibrary)](#apidoc.element.mongodb.Admin.Admin)
- description and source-code
```javascript
Admin = function (db, topology, promiseLibrary) {
  if(!(this instanceof Admin)) return new Admin(db, topology);

  // Internal state
  this.s = {
      db: db
    , topology: topology
    , promiseLibrary: promiseLibrary
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.Admin.define"></a>[module mongodb.Admin.define](#apidoc.module.mongodb.Admin.define)

#### <a name="apidoc.element.mongodb.Admin.define.object"></a>[function <span class="apidocSignatureSpan">mongodb.Admin.define.</span>object (db, topology, promiseLibrary)](#apidoc.element.mongodb.Admin.define.object)
- description and source-code
```javascript
object = function (db, topology, promiseLibrary) {
  if(!(this instanceof Admin)) return new Admin(db, topology);

  // Internal state
  this.s = {
      db: db
    , topology: topology
    , promiseLibrary: promiseLibrary
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.Admin.prototype"></a>[module mongodb.Admin.prototype](#apidoc.module.mongodb.Admin.prototype)

#### <a name="apidoc.element.mongodb.Admin.prototype.addUser"></a>[function <span class="apidocSignatureSpan">mongodb.Admin.prototype.</span>addUser (username, password, options, callback)](#apidoc.element.mongodb.Admin.prototype.addUser)
- description and source-code
```javascript
addUser = function (username, password, options, callback) {
  var self = this;
  var args = Array.prototype.slice.call(arguments, 2);
  callback = args.pop();
  if(typeof callback != 'function') args.push(callback);
  options = args.length ? args.shift() : {};
  options = options || {};
  // Get the options
  options = writeConcern(options, self.s.db)
  // Set the db name to admin
  options.dbName = 'admin';

  // Execute using callback
  if(typeof callback == 'function')
    return self.s.db.addUser(username, password, options, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    self.s.db.addUser(username, password, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Admin.prototype.authenticate"></a>[function <span class="apidocSignatureSpan">mongodb.Admin.prototype.</span>authenticate (username, password, options, callback)](#apidoc.element.mongodb.Admin.prototype.authenticate)
- description and source-code
```javascript
authenticate = function (username, password, options, callback) {
  var self = this;
  if(typeof options == 'function') callback = options, options = {};
  options = shallowClone(options);
  options.authdb = 'admin';

  // Execute using callback
  if(typeof callback == 'function') return this.s.db.authenticate(username, password, options, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    self.s.db.authenticate(username, password, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Admin.prototype.buildInfo"></a>[function <span class="apidocSignatureSpan">mongodb.Admin.prototype.</span>buildInfo (callback)](#apidoc.element.mongodb.Admin.prototype.buildInfo)
- description and source-code
```javascript
buildInfo = function (callback) {
  var self = this;
  // Execute using callback
  if(typeof callback == 'function') return this.serverInfo(callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    self.serverInfo(function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Admin.prototype.command"></a>[function <span class="apidocSignatureSpan">mongodb.Admin.prototype.</span>command (command, options, callback)](#apidoc.element.mongodb.Admin.prototype.command)
- description and source-code
```javascript
command = function (command, options, callback) {
  var self = this;
  var args = Array.prototype.slice.call(arguments, 1);
  callback = args.pop();
  if(typeof callback != 'function') args.push(callback);
  options = args.length ? args.shift() : {};

  // Execute using callback
  if(typeof callback == 'function') return this.s.db.executeDbAdminCommand(command, options, function(err, doc) {
    return callback != null ? callback(err, doc) : null;
  });

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    self.s.db.executeDbAdminCommand(command, options, function(err, doc) {
      if(err) return reject(err);
      resolve(doc);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Admin.prototype.listDatabases"></a>[function <span class="apidocSignatureSpan">mongodb.Admin.prototype.</span>listDatabases (callback)](#apidoc.element.mongodb.Admin.prototype.listDatabases)
- description and source-code
```javascript
listDatabases = function (callback) {
  var self = this;
  // Execute using callback
  if(typeof callback == 'function') return self.s.db.executeDbAdminCommand({listDatabases:1}, {}, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    self.s.db.executeDbAdminCommand({listDatabases:1}, {}, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Admin.prototype.logout"></a>[function <span class="apidocSignatureSpan">mongodb.Admin.prototype.</span>logout (callback)](#apidoc.element.mongodb.Admin.prototype.logout)
- description and source-code
```javascript
logout = function (callback) {
  var self = this;
  // Execute using callback
  if(typeof callback == 'function') return this.s.db.logout({dbName: 'admin'}, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    self.s.db.logout({dbName: 'admin'}, function(err) {
      if(err) return reject(err);
      resolve(true);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Admin.prototype.ping"></a>[function <span class="apidocSignatureSpan">mongodb.Admin.prototype.</span>ping (options, callback)](#apidoc.element.mongodb.Admin.prototype.ping)
- description and source-code
```javascript
ping = function (options, callback) {
  var self = this;
  var args = Array.prototype.slice.call(arguments, 0);
  callback = args.pop();
  if(typeof callback != 'function') args.push(callback);

  // Execute using callback
  if(typeof callback == 'function') return this.s.db.executeDbAdminCommand({ping: 1}, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    self.s.db.executeDbAdminCommand({ping: 1}, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Admin.prototype.profilingInfo"></a>[function <span class="apidocSignatureSpan">mongodb.Admin.prototype.</span>profilingInfo (callback)](#apidoc.element.mongodb.Admin.prototype.profilingInfo)
- description and source-code
```javascript
profilingInfo = function (callback) {
  var self = this;

  // Execute using callback
  if(typeof callback == 'function') return profilingInfo(self, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    profilingInfo(self, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Admin.prototype.profilingLevel"></a>[function <span class="apidocSignatureSpan">mongodb.Admin.prototype.</span>profilingLevel (callback)](#apidoc.element.mongodb.Admin.prototype.profilingLevel)
- description and source-code
```javascript
profilingLevel = function (callback) {
  var self = this;

  // Execute using callback
  if(typeof callback == 'function') return profilingLevel(self, callback)

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    profilingLevel(self, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Admin.prototype.removeUser"></a>[function <span class="apidocSignatureSpan">mongodb.Admin.prototype.</span>removeUser (username, options, callback)](#apidoc.element.mongodb.Admin.prototype.removeUser)
- description and source-code
```javascript
removeUser = function (username, options, callback) {
  var self = this;
  var args = Array.prototype.slice.call(arguments, 1);
  callback = args.pop();
  if(typeof callback != 'function') args.push(callback);
  options = args.length ? args.shift() : {};
  options = options || {};
  // Get the options
  options = writeConcern(options, self.s.db)
  // Set the db name
  options.dbName = 'admin';

  // Execute using callback
  if(typeof callback == 'function')
    return self.s.db.removeUser(username, options, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    self.s.db.removeUser(username, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Admin.prototype.replSetGetStatus"></a>[function <span class="apidocSignatureSpan">mongodb.Admin.prototype.</span>replSetGetStatus (callback)](#apidoc.element.mongodb.Admin.prototype.replSetGetStatus)
- description and source-code
```javascript
replSetGetStatus = function (callback) {
  var self = this;
  // Execute using callback
  if(typeof callback == 'function') return replSetGetStatus(self, callback);
  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    replSetGetStatus(self, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Admin.prototype.serverInfo"></a>[function <span class="apidocSignatureSpan">mongodb.Admin.prototype.</span>serverInfo (callback)](#apidoc.element.mongodb.Admin.prototype.serverInfo)
- description and source-code
```javascript
serverInfo = function (callback) {
  var self = this;
  // Execute using callback
  if(typeof callback == 'function') return this.s.db.executeDbAdminCommand({buildinfo:1}, function(err, doc) {
    if(err != null) return callback(err, null);
    callback(null, doc);
  });

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    self.s.db.executeDbAdminCommand({buildinfo:1}, function(err, doc) {
      if(err) return reject(err);
      resolve(doc);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Admin.prototype.serverStatus"></a>[function <span class="apidocSignatureSpan">mongodb.Admin.prototype.</span>serverStatus (callback)](#apidoc.element.mongodb.Admin.prototype.serverStatus)
- description and source-code
```javascript
serverStatus = function (callback) {
  var self = this;

  // Execute using callback
  if(typeof callback == 'function') return serverStatus(self, callback)

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    serverStatus(self, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Admin.prototype.setProfilingLevel"></a>[function <span class="apidocSignatureSpan">mongodb.Admin.prototype.</span>setProfilingLevel (level, callback)](#apidoc.element.mongodb.Admin.prototype.setProfilingLevel)
- description and source-code
```javascript
setProfilingLevel = function (level, callback) {
  var self = this;

  // Execute using callback
  if(typeof callback == 'function') return setProfilingLevel(self, level, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    setProfilingLevel(self, level, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Admin.prototype.validateCollection"></a>[function <span class="apidocSignatureSpan">mongodb.Admin.prototype.</span>validateCollection (collectionName, options, callback)](#apidoc.element.mongodb.Admin.prototype.validateCollection)
- description and source-code
```javascript
validateCollection = function (collectionName, options, callback) {
  var self = this;
  var args = Array.prototype.slice.call(arguments, 1);
  callback = args.pop();
  if(typeof callback != 'function') args.push(callback);
  options = args.length ? args.shift() : {};
  options = options || {};

  // Execute using callback
  if(typeof callback == 'function')
    return validateCollection(self, collectionName, options, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    validateCollection(self, collectionName, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.BSONRegExp"></a>[module mongodb.BSONRegExp](#apidoc.module.mongodb.BSONRegExp)

#### <a name="apidoc.element.mongodb.BSONRegExp.BSONRegExp"></a>[function <span class="apidocSignatureSpan">mongodb.</span>BSONRegExp (pattern, options)](#apidoc.element.mongodb.BSONRegExp.BSONRegExp)
- description and source-code
```javascript
function BSONRegExp(pattern, options) {
  if(!(this instanceof BSONRegExp)) return new BSONRegExp();

  // Execute
  this._bsontype = 'BSONRegExp';
  this.pattern = pattern || '';
  this.options = options || '';

  // Validate options
  for(var i = 0; i < this.options.length; i++) {
    if(!(this.options[i] == 'i'
      || this.options[i] == 'm'
      || this.options[i] == 'x'
      || this.options[i] == 'l'
      || this.options[i] == 's'
      || this.options[i] == 'u'
    )) {
      throw new Error('the regular expression options [' + this.options[i] + "] is not supported");
    }
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.Binary"></a>[module mongodb.Binary](#apidoc.module.mongodb.Binary)

#### <a name="apidoc.element.mongodb.Binary.Binary"></a>[function <span class="apidocSignatureSpan">mongodb.</span>Binary (buffer, subType)](#apidoc.element.mongodb.Binary.Binary)
- description and source-code
```javascript
function Binary(buffer, subType) {
  if(!(this instanceof Binary)) return new Binary(buffer, subType);

  this._bsontype = 'Binary';

  if(buffer instanceof Number) {
    this.sub_type = buffer;
    this.position = 0;
  } else {
    this.sub_type = subType == null ? BSON_BINARY_SUBTYPE_DEFAULT : subType;
    this.position = 0;
  }

  if(buffer != null && !(buffer instanceof Number)) {
    // Only accept Buffer, Uint8Array or Arrays
    if(typeof buffer == 'string') {
      // Different ways of writing the length of the string for the different types
      if(typeof Buffer != 'undefined') {
        this.buffer = new Buffer(buffer);
      } else if(typeof Uint8Array != 'undefined' || (Object.prototype.toString.call(buffer) == '[object Array]')) {
        this.buffer = writeStringToArray(buffer);
      } else {
        throw new Error("only String, Buffer, Uint8Array or Array accepted");
      }
    } else {
      this.buffer = buffer;
    }
    this.position = buffer.length;
  } else {
    if(typeof Buffer != 'undefined') {
      this.buffer =  new Buffer(Binary.BUFFER_SIZE);
    } else if(typeof Uint8Array != 'undefined'){
      this.buffer = new Uint8Array(new ArrayBuffer(Binary.BUFFER_SIZE));
    } else {
      this.buffer = new Array(Binary.BUFFER_SIZE);
    }
    // Set position to start of buffer
    this.position = 0;
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.Binary.prototype"></a>[module mongodb.Binary.prototype](#apidoc.module.mongodb.Binary.prototype)

#### <a name="apidoc.element.mongodb.Binary.prototype.length"></a>[function <span class="apidocSignatureSpan">mongodb.Binary.prototype.</span>length ()](#apidoc.element.mongodb.Binary.prototype.length)
- description and source-code
```javascript
function length() {
  return this.position;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Binary.prototype.put"></a>[function <span class="apidocSignatureSpan">mongodb.Binary.prototype.</span>put (byte_value)](#apidoc.element.mongodb.Binary.prototype.put)
- description and source-code
```javascript
function put(byte_value) {
  // If it's a string and a has more than one character throw an error
  if(byte_value['length'] != null && typeof byte_value != 'number' && byte_value.length != 1) throw new Error("only accepts single
 character String, Uint8Array or Array");
  if(typeof byte_value != 'number' && byte_value < 0 || byte_value > 255) throw new Error("only accepts number in a valid unsigned
 byte range 0-255");

  // Decode the byte value once
  var decoded_byte = null;
  if(typeof byte_value == 'string') {
    decoded_byte = byte_value.charCodeAt(0);
  } else if(byte_value['length'] != null) {
    decoded_byte = byte_value[0];
  } else {
    decoded_byte = byte_value;
  }

  if(this.buffer.length > this.position) {
    this.buffer[this.position++] = decoded_byte;
  } else {
    if(typeof Buffer != 'undefined' && Buffer.isBuffer(this.buffer)) {
      // Create additional overflow buffer
      var buffer = new Buffer(Binary.BUFFER_SIZE + this.buffer.length);
      // Combine the two buffers together
      this.buffer.copy(buffer, 0, 0, this.buffer.length);
      this.buffer = buffer;
      this.buffer[this.position++] = decoded_byte;
    } else {
      var buffer = null;
      // Create a new buffer (typed or normal array)
      if(Object.prototype.toString.call(this.buffer) == '[object Uint8Array]') {
        buffer = new Uint8Array(new ArrayBuffer(Binary.BUFFER_SIZE + this.buffer.length));
      } else {
        buffer = new Array(Binary.BUFFER_SIZE + this.buffer.length);
      }

      // We need to copy all the content to the new array
      for(var i = 0; i < this.buffer.length; i++) {
        buffer[i] = this.buffer[i];
      }

      // Reassign the buffer
      this.buffer = buffer;
      // Write the byte
      this.buffer[this.position++] = decoded_byte;
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Binary.prototype.read"></a>[function <span class="apidocSignatureSpan">mongodb.Binary.prototype.</span>read (position, length)](#apidoc.element.mongodb.Binary.prototype.read)
- description and source-code
```javascript
function read(position, length) {
  length = length && length > 0
    ? length
    : this.position;

  // Let's return the data based on the type we have
  if(this.buffer['slice']) {
    return this.buffer.slice(position, position + length);
  } else {
    // Create a buffer to keep the result
    var buffer = typeof Uint8Array != 'undefined' ? new Uint8Array(new ArrayBuffer(length)) : new Array(length);
    for(var i = 0; i < length; i++) {
      buffer[i] = this.buffer[position++];
    }
  }
  // Return the buffer
  return buffer;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Binary.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">mongodb.Binary.prototype.</span>toJSON ()](#apidoc.element.mongodb.Binary.prototype.toJSON)
- description and source-code
```javascript
toJSON = function () {
  return this.buffer != null ? this.buffer.toString('base64') : '';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Binary.prototype.toString"></a>[function <span class="apidocSignatureSpan">mongodb.Binary.prototype.</span>toString (format)](#apidoc.element.mongodb.Binary.prototype.toString)
- description and source-code
```javascript
toString = function (format) {
  return this.buffer != null ? this.buffer.slice(0, this.position).toString(format) : '';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Binary.prototype.value"></a>[function <span class="apidocSignatureSpan">mongodb.Binary.prototype.</span>value (asRaw)](#apidoc.element.mongodb.Binary.prototype.value)
- description and source-code
```javascript
function value(asRaw) {
  asRaw = asRaw == null ? false : asRaw;

  // Optimize to serialize for the situation where the data == size of buffer
  if(asRaw && typeof Buffer != 'undefined' && Buffer.isBuffer(this.buffer) && this.buffer.length == this.position)
    return this.buffer;

  // If it's a node.js buffer object
  if(typeof Buffer != 'undefined' && Buffer.isBuffer(this.buffer)) {
    return asRaw ? this.buffer.slice(0, this.position) : this.buffer.toString('binary', 0, this.position);
  } else {
    if(asRaw) {
      // we support the slice command use it
      if(this.buffer['slice'] != null) {
        return this.buffer.slice(0, this.position);
      } else {
        // Create a new buffer to copy content to
        var newBuffer = Object.prototype.toString.call(this.buffer) == '[object Uint8Array]' ? new Uint8Array(new ArrayBuffer(this
.position)) : new Array(this.position);
        // Copy content
        for(var i = 0; i < this.position; i++) {
          newBuffer[i] = this.buffer[i];
        }
        // Return the buffer
        return newBuffer;
      }
    } else {
      return convertArraytoUtf8BinaryString(this.buffer, 0, this.position);
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Binary.prototype.write"></a>[function <span class="apidocSignatureSpan">mongodb.Binary.prototype.</span>write (string, offset)](#apidoc.element.mongodb.Binary.prototype.write)
- description and source-code
```javascript
function write(string, offset) {
  offset = typeof offset == 'number' ? offset : this.position;

  // If the buffer is to small let's extend the buffer
  if(this.buffer.length < offset + string.length) {
    var buffer = null;
    // If we are in node.js
    if(typeof Buffer != 'undefined' && Buffer.isBuffer(this.buffer)) {
      buffer = new Buffer(this.buffer.length + string.length);
      this.buffer.copy(buffer, 0, 0, this.buffer.length);
    } else if(Object.prototype.toString.call(this.buffer) == '[object Uint8Array]') {
      // Create a new buffer
      buffer = new Uint8Array(new ArrayBuffer(this.buffer.length + string.length))
      // Copy the content
      for(var i = 0; i < this.position; i++) {
        buffer[i] = this.buffer[i];
      }
    }

    // Assign the new buffer
    this.buffer = buffer;
  }

  if(typeof Buffer != 'undefined' && Buffer.isBuffer(string) && Buffer.isBuffer(this.buffer)) {
    string.copy(this.buffer, offset, 0, string.length);
    this.position = (offset + string.length) > this.position ? (offset + string.length) : this.position;
    // offset = string.length
  } else if(typeof Buffer != 'undefined' && typeof string == 'string' && Buffer.isBuffer(this.buffer)) {
    this.buffer.write(string, offset, 'binary');
    this.position = (offset + string.length) > this.position ? (offset + string.length) : this.position;
    // offset = string.length;
  } else if(Object.prototype.toString.call(string) == '[object Uint8Array]'
    || Object.prototype.toString.call(string) == '[object Array]' && typeof string != 'string') {
    for(var i = 0; i < string.length; i++) {
      this.buffer[offset++] = string[i];
    }

    this.position = offset > this.position ? offset : this.position;
  } else if(typeof string == 'string') {
    for(var i = 0; i < string.length; i++) {
      this.buffer[offset++] = string.charCodeAt(i);
    }

    this.position = offset > this.position ? offset : this.position;
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.Chunk"></a>[module mongodb.Chunk](#apidoc.module.mongodb.Chunk)

#### <a name="apidoc.element.mongodb.Chunk.Chunk"></a>[function <span class="apidocSignatureSpan">mongodb.</span>Chunk (file, mongoObject, writeConcern)](#apidoc.element.mongodb.Chunk.Chunk)
- description and source-code
```javascript
Chunk = function (file, mongoObject, writeConcern) {
  if(!(this instanceof Chunk)) return new Chunk(file, mongoObject);

  this.file = file;
  var mongoObjectFinal = mongoObject == null ? {} : mongoObject;
  this.writeConcern = writeConcern || {w:1};
  this.objectId = mongoObjectFinal._id == null ? new ObjectID() : mongoObjectFinal._id;
  this.chunkNumber = mongoObjectFinal.n == null ? 0 : mongoObjectFinal.n;
  this.data = new Binary();

  if(typeof mongoObjectFinal.data == "string") {
    var buffer = new Buffer(mongoObjectFinal.data.length);
    buffer.write(mongoObjectFinal.data, 0, mongoObjectFinal.data.length, 'binary');
    this.data = new Binary(buffer);
  } else if(Array.isArray(mongoObjectFinal.data)) {
    buffer = new Buffer(mongoObjectFinal.data.length);
    var data = mongoObjectFinal.data.join('');
    buffer.write(data, 0, data.length, 'binary');
    this.data = new Binary(buffer);
  } else if(mongoObjectFinal.data && mongoObjectFinal.data._bsontype === 'Binary') {
    this.data = mongoObjectFinal.data;
  } else if(!Buffer.isBuffer(mongoObjectFinal.data) && !(mongoObjectFinal.data == null)){
    throw Error("Illegal chunk format");
  }

  // Update position
  this.internalPosition = 0;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.Chunk.prototype"></a>[module mongodb.Chunk.prototype](#apidoc.module.mongodb.Chunk.prototype)

#### <a name="apidoc.element.mongodb.Chunk.prototype.buildMongoObject"></a>[function <span class="apidocSignatureSpan">mongodb.Chunk.prototype.</span>buildMongoObject (callback)](#apidoc.element.mongodb.Chunk.prototype.buildMongoObject)
- description and source-code
```javascript
buildMongoObject = function (callback) {
  var mongoObject = {
    'files_id': this.file.fileId,
    'n': this.chunkNumber,
    'data': this.data};
  // If we are saving using a specific ObjectId
  if(this.objectId != null) mongoObject._id = this.objectId;

  callback(mongoObject);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Chunk.prototype.eof"></a>[function <span class="apidocSignatureSpan">mongodb.Chunk.prototype.</span>eof ()](#apidoc.element.mongodb.Chunk.prototype.eof)
- description and source-code
```javascript
eof = function () {
  return this.internalPosition == this.length() ? true : false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Chunk.prototype.getc"></a>[function <span class="apidocSignatureSpan">mongodb.Chunk.prototype.</span>getc ()](#apidoc.element.mongodb.Chunk.prototype.getc)
- description and source-code
```javascript
getc = function () {
  return this.read(1);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Chunk.prototype.length"></a>[function <span class="apidocSignatureSpan">mongodb.Chunk.prototype.</span>length ()](#apidoc.element.mongodb.Chunk.prototype.length)
- description and source-code
```javascript
length = function () {
  return this.data.length();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Chunk.prototype.read"></a>[function <span class="apidocSignatureSpan">mongodb.Chunk.prototype.</span>read (length)](#apidoc.element.mongodb.Chunk.prototype.read)
- description and source-code
```javascript
read = function (length) {
  // Default to full read if no index defined
  length = length == null || length == 0 ? this.length() : length;

  if(this.length() - this.internalPosition + 1 >= length) {
    var data = this.data.read(this.internalPosition, length);
    this.internalPosition = this.internalPosition + length;
    return data;
  } else {
    return '';
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Chunk.prototype.readSlice"></a>[function <span class="apidocSignatureSpan">mongodb.Chunk.prototype.</span>readSlice (length)](#apidoc.element.mongodb.Chunk.prototype.readSlice)
- description and source-code
```javascript
readSlice = function (length) {
  if ((this.length() - this.internalPosition) >= length) {
    var data = null;
    if (this.data.buffer != null) { //Pure BSON
      data = this.data.buffer.slice(this.internalPosition, this.internalPosition + length);
    } else { //Native BSON
      data = new Buffer(length);
      length = this.data.readInto(data, this.internalPosition);
    }
    this.internalPosition = this.internalPosition + length;
    return data;
  } else {
    return null;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Chunk.prototype.rewind"></a>[function <span class="apidocSignatureSpan">mongodb.Chunk.prototype.</span>rewind ()](#apidoc.element.mongodb.Chunk.prototype.rewind)
- description and source-code
```javascript
rewind = function () {
  this.internalPosition = 0;
  this.data = new Binary();
}
```
- example usage
```shell
...
 * @param {object[]} documents All the documents the satisfy the cursor.
 */

/**
 * Returns an array of documents. The caller is responsible for making sure that there
 * is enough memory to store the results. Note that the array only contain partial
 * results when this cursor had been previouly accessed. In that case,
 * cursor.rewind() can be used to reset the cursor.
 * @method AggregationCursor.prototype.toArray
 * @param {AggregationCursor~toArrayResultCallback} [callback] The result callback.
 * @throws {MongoError}
 * @return {Promise} returns Promise if no callback passed
 */

/**
...
```

#### <a name="apidoc.element.mongodb.Chunk.prototype.save"></a>[function <span class="apidocSignatureSpan">mongodb.Chunk.prototype.</span>save (options, callback)](#apidoc.element.mongodb.Chunk.prototype.save)
- description and source-code
```javascript
save = function (options, callback) {
  var self = this;
  if(typeof options == 'function') {
    callback = options;
    options = {};
  }

  self.file.chunkCollection(function(err, collection) {
    if(err) return callback(err);

    // Merge the options
    var writeOptions = { upsert: true };
    for(var name in options) writeOptions[name] = options[name];
    for(name in self.writeConcern) writeOptions[name] = self.writeConcern[name];

    if(self.data.length() > 0) {
      self.buildMongoObject(function(mongoObject) {
        var options = {forceServerObjectId:true};
        for(var name in self.writeConcern) {
          options[name] = self.writeConcern[name];
        }

        collection.replaceOne({'_id':self.objectId}, mongoObject, writeOptions, function(err) {
          callback(err, self);
        });
      });
    } else {
      callback(null, self);
    }
    // });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Chunk.prototype.write"></a>[function <span class="apidocSignatureSpan">mongodb.Chunk.prototype.</span>write (data, callback)](#apidoc.element.mongodb.Chunk.prototype.write)
- description and source-code
```javascript
write = function (data, callback) {
  this.data.write(data, this.internalPosition, data.length, 'binary');
  this.internalPosition = this.data.length();
  if(callback != null) return callback(null, this);
  return this;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.Code"></a>[module mongodb.Code](#apidoc.module.mongodb.Code)

#### <a name="apidoc.element.mongodb.Code.Code"></a>[function <span class="apidocSignatureSpan">mongodb.</span>Code (code, scope)](#apidoc.element.mongodb.Code.Code)
- description and source-code
```javascript
function Code(code, scope) {
  if(!(this instanceof Code)) return new Code(code, scope);
  this._bsontype = 'Code';
  this.code = code;
  this.scope = scope;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.Code.prototype"></a>[module mongodb.Code.prototype](#apidoc.module.mongodb.Code.prototype)

#### <a name="apidoc.element.mongodb.Code.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">mongodb.Code.prototype.</span>toJSON ()](#apidoc.element.mongodb.Code.prototype.toJSON)
- description and source-code
```javascript
toJSON = function () {
  return {scope:this.scope, code:this.code};
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.Collection"></a>[module mongodb.Collection](#apidoc.module.mongodb.Collection)

#### <a name="apidoc.element.mongodb.Collection.Collection"></a>[function <span class="apidocSignatureSpan">mongodb.</span>Collection (db, topology, dbName, name, pkFactory, options)](#apidoc.element.mongodb.Collection.Collection)
- description and source-code
```javascript
Collection = function (db, topology, dbName, name, pkFactory, options) {
  checkCollectionName(name);

  // Unpack variables
  var internalHint = null;
  var slaveOk = options == null || options.slaveOk == null ? db.slaveOk : options.slaveOk;
  var serializeFunctions = options == null || options.serializeFunctions == null ? db.s.options.serializeFunctions : options.serializeFunctions
;
  var raw = options == null || options.raw == null ? db.s.options.raw : options.raw;
  var promoteLongs = options == null || options.promoteLongs == null ? db.s.options.promoteLongs : options.promoteLongs;
  var promoteValues = options == null || options.promoteValues == null ? db.s.options.promoteValues : options.promoteValues;
  var promoteBuffers = options == null || options.promoteBuffers == null ? db.s.options.promoteBuffers : options.promoteBuffers;
  var readPreference = null;
  var collectionHint = null;
  var namespace = f("%s.%s", dbName, name);

  // Get the promiseLibrary
  var promiseLibrary = options.promiseLibrary;

  // No promise library selected fall back
  if(!promiseLibrary) {
    promiseLibrary = typeof global.Promise == 'function' ?
      global.Promise : require('es6-promise').Promise;
  }

  // Assign the right collection level readPreference
  if(options && options.readPreference) {
    readPreference = options.readPreference;
  } else if(db.options.readPreference) {
    readPreference = db.options.readPreference;
  }

  // Set custom primary key factory if provided
  pkFactory = pkFactory == null
    ? ObjectID
    : pkFactory;

  // Internal state
  this.s = {
    // Set custom primary key factory if provided
      pkFactory: pkFactory
    // Db
    , db: db
    // Topology
    , topology: topology
    // dbName
    , dbName: dbName
    // Options
    , options: options
    // Namespace
    , namespace: namespace
    // Read preference
    , readPreference: readPreference
    // SlaveOK
    , slaveOk: slaveOk
    // Serialize functions
    , serializeFunctions: serializeFunctions
    // Raw
    , raw: raw
    // promoteLongs
    , promoteLongs: promoteLongs
    // promoteValues
    , promoteValues: promoteValues
    // promoteBuffers
    , promoteBuffers: promoteBuffers
    // internalHint
    , internalHint: internalHint
    // collectionHint
    , collectionHint: collectionHint
    // Name
    , name: name
    // Promise library
    , promiseLibrary: promiseLibrary
    // Read Concern
    , readConcern: options.readConcern
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.Collection.define"></a>[module mongodb.Collection.define](#apidoc.module.mongodb.Collection.define)

#### <a name="apidoc.element.mongodb.Collection.define.object"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.define.</span>object (db, topology, dbName, name, pkFactory, options)](#apidoc.element.mongodb.Collection.define.object)
- description and source-code
```javascript
object = function (db, topology, dbName, name, pkFactory, options) {
  checkCollectionName(name);

  // Unpack variables
  var internalHint = null;
  var slaveOk = options == null || options.slaveOk == null ? db.slaveOk : options.slaveOk;
  var serializeFunctions = options == null || options.serializeFunctions == null ? db.s.options.serializeFunctions : options.serializeFunctions
;
  var raw = options == null || options.raw == null ? db.s.options.raw : options.raw;
  var promoteLongs = options == null || options.promoteLongs == null ? db.s.options.promoteLongs : options.promoteLongs;
  var promoteValues = options == null || options.promoteValues == null ? db.s.options.promoteValues : options.promoteValues;
  var promoteBuffers = options == null || options.promoteBuffers == null ? db.s.options.promoteBuffers : options.promoteBuffers;
  var readPreference = null;
  var collectionHint = null;
  var namespace = f("%s.%s", dbName, name);

  // Get the promiseLibrary
  var promiseLibrary = options.promiseLibrary;

  // No promise library selected fall back
  if(!promiseLibrary) {
    promiseLibrary = typeof global.Promise == 'function' ?
      global.Promise : require('es6-promise').Promise;
  }

  // Assign the right collection level readPreference
  if(options && options.readPreference) {
    readPreference = options.readPreference;
  } else if(db.options.readPreference) {
    readPreference = db.options.readPreference;
  }

  // Set custom primary key factory if provided
  pkFactory = pkFactory == null
    ? ObjectID
    : pkFactory;

  // Internal state
  this.s = {
    // Set custom primary key factory if provided
      pkFactory: pkFactory
    // Db
    , db: db
    // Topology
    , topology: topology
    // dbName
    , dbName: dbName
    // Options
    , options: options
    // Namespace
    , namespace: namespace
    // Read preference
    , readPreference: readPreference
    // SlaveOK
    , slaveOk: slaveOk
    // Serialize functions
    , serializeFunctions: serializeFunctions
    // Raw
    , raw: raw
    // promoteLongs
    , promoteLongs: promoteLongs
    // promoteValues
    , promoteValues: promoteValues
    // promoteBuffers
    , promoteBuffers: promoteBuffers
    // internalHint
    , internalHint: internalHint
    // collectionHint
    , collectionHint: collectionHint
    // Name
    , name: name
    // Promise library
    , promiseLibrary: promiseLibrary
    // Read Concern
    , readConcern: options.readConcern
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.Collection.prototype"></a>[module mongodb.Collection.prototype](#apidoc.module.mongodb.Collection.prototype)

#### <a name="apidoc.element.mongodb.Collection.prototype.aggregate"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>aggregate (pipeline, options, callback)](#apidoc.element.mongodb.Collection.prototype.aggregate)
- description and source-code
```javascript
aggregate = function (pipeline, options, callback) {
  var self = this;

  if(Array.isArray(pipeline)) {
    // Set up callback if one is provided
    if(typeof options == 'function') {
      callback = options;
      options = {};
    }

    // If we have no options or callback we are doing
    // a cursor based aggregation
    if(options == null && callback == null) {
      options = {};
    }
  } else {
    // Aggregation pipeline passed as arguments on the method
    var args = Array.prototype.slice.call(arguments, 0);
    // Get the callback
    callback = args.pop();
    // Get the possible options object
    var opts = args[args.length - 1];
    // If it contains any of the admissible options pop it of the args
    options = opts && (opts.readPreference
      || opts.explain || opts.cursor || opts.out
      || opts.maxTimeMS || opts.allowDiskUse) ? args.pop() : {};
      // Left over arguments is the pipeline
    pipeline = args;
  }

  // Ignore readConcern option
  var ignoreReadConcern = false;

  // Build the command
  var command = { aggregate : this.s.name, pipeline : pipeline};

  // If out was specified
  if(typeof options.out == 'string') {
    pipeline.push({$out: options.out});
    // Ignore read concern
    ignoreReadConcern = true;
  } else if(pipeline.length > 0 && pipeline[pipeline.length - 1]['$out']) {
    ignoreReadConcern = true;
  }

  // Decorate command with writeConcern if out has been specified
  if(pipeline.length > 0 && pipeline[pipeline.length - 1]['$out']) {
    decorateWithWriteConcern(command, self, options);
  }

  // Have we specified collation
  decorateWithCollation(command, self, options);

  // If we have bypassDocumentValidation set
  if(typeof options.bypassDocumentValidation == 'boolean') {
    command.bypassDocumentValidation = options.bypassDocumentValidation;
  }

  // Do we have a readConcern specified
  if(!ignoreReadConcern && this.s.readConcern) {
    command.readConcern = this.s.readConcern;
  }

  // If we have allowDiskUse defined
  if(options.allowDiskUse) command.allowDiskUse = options.allowDiskUse;
  if(typeof options.maxTimeMS == 'number') command.maxTimeMS = options.maxTimeMS;

  options = shallowClone(options);
  // Ensure we have the right read preference inheritance
  options = getReadPreference(this, options, this.s.db, this);

  // If explain has been specified add it
  if(options.explain) command.explain = options.explain;

  // Validate that cursor options is valid
  if(options.cursor != null && typeof options.cursor != 'object') {
    throw toError('cursor options must be an object');
  }

  // promiseLibrary
  options.promiseLibrary = this.s.promiseLibrary;

  // Set the AggregationCursor constructor
  options.cursorFactory = AggregationCursor;
  if(typeof callback != 'function') {
    if(!this.s.topology.capabilities()) {
      throw new MongoError('cannot connect to server');
    }

    if(this.s.topology.capabilities().hasAggregationCursor) {
      options.cursor = options.cursor || { batchSize : 1000 };
      command.cursor = options.cursor;
    }

    // Allow disk usage command
    if(typeof options.allowDiskUse == 'boolean') command.allowDiskUse = options.allowDiskUse;
    if(typeof options.maxTimeMS == 'number') command.maxTimeMS = options.maxTimeMS;

    // Execute the cursor
    return this.s.topology.cursor(this.s.namespace, command, options);
  }

  // We do not allow cursor
  if(options.cursor) {
    return this.s.topology.cursor(this.s.namespace, command, options);
  }

  // Execute the command
  this.s.db.command(command, options, function(err, result) {
    if(err) {
      handleCallback(callback, err);
    } else if(result['err'] || result['errmsg']) {
      handleCallback(callback, toError(result));
    } else if(typeof result == 'object' && result['serverPipeline']) {
      handleCallback(callback, null, result['serverPipeline']);
    } else if(typeof result == 'object' && result['stages']) {
      handleCallback(callback, null, result['stages']);
    } else {
      handleCallback(callback, null, result.result);
    }
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Collection.prototype.bulkWrite"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>bulkWrite (operations, options, callback)](#apidoc.element.mongodb.Collection.prototype.bulkWrite)
- description and source-code
```javascript
bulkWrite = function (operations, options, callback) {
  var self = this;
  if(typeof options == 'function') callback = options, options = {};
  options = options || {ordered:true};

  if(!Array.isArray(operations)) {
    throw MongoError.create({message: "operations must be an array of documents", driver:true });
  }

  // Execute using callback
  if(typeof callback == 'function') return bulkWrite(self, operations, options, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    bulkWrite(self, operations, options, function(err, r) {
      if(err && r == null) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Collection.prototype.count"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>count (query, options, callback)](#apidoc.element.mongodb.Collection.prototype.count)
- description and source-code
```javascript
count = function (query, options, callback) {
  var self = this;
  var args = Array.prototype.slice.call(arguments, 0);
  callback = args.pop();
  if(typeof callback != 'function') args.push(callback);
  var queryOption = args.length ? args.shift() || {} : {};
  var optionsOption = args.length ? args.shift() || {} : {};

  // Execute using callback
  if(typeof callback == 'function') return count(self, queryOption, optionsOption, callback);

  // Check if query is empty
  query = query || {};
  options = options || {};

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    count(self, query, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Collection.prototype.createIndex"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>createIndex (fieldOrSpec, options, callback)](#apidoc.element.mongodb.Collection.prototype.createIndex)
- description and source-code
```javascript
createIndex = function (fieldOrSpec, options, callback) {
  var self = this;
  var args = Array.prototype.slice.call(arguments, 1);
  callback = args.pop();
  if(typeof callback != 'function') args.push(callback);
  options = args.length ? args.shift() || {} : {};
  options = typeof callback === 'function' ? options : callback;
  options = options == null ? {} : options;

  // Execute using callback
  if(typeof callback == 'function') return createIndex(self, fieldOrSpec, options, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    createIndex(self, fieldOrSpec, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Collection.prototype.createIndexes"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>createIndexes (indexSpecs, callback)](#apidoc.element.mongodb.Collection.prototype.createIndexes)
- description and source-code
```javascript
createIndexes = function (indexSpecs, callback) {
  var self = this;

  // Execute using callback
  if(typeof callback == 'function') return createIndexes(self, indexSpecs, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    createIndexes(self, indexSpecs, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Collection.prototype.deleteMany"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>deleteMany (filter, options, callback)](#apidoc.element.mongodb.Collection.prototype.deleteMany)
- description and source-code
```javascript
deleteMany = function (filter, options, callback) {
  var self = this;
  if(typeof options == 'function') callback = options, options = {};
  options = shallowClone(options);

  // Add ignoreUndfined
  if(this.s.options.ignoreUndefined) {
    options = shallowClone(options);
    options.ignoreUndefined = this.s.options.ignoreUndefined;
  }

  // Execute using callback
  if(typeof callback == 'function') return deleteMany(self, filter, options, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    deleteMany(self, filter, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Collection.prototype.deleteOne"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>deleteOne (filter, options, callback)](#apidoc.element.mongodb.Collection.prototype.deleteOne)
- description and source-code
```javascript
deleteOne = function (filter, options, callback) {
  var self = this;
  if(typeof options == 'function') callback = options, options = {};
  options = shallowClone(options);

  // Add ignoreUndfined
  if(this.s.options.ignoreUndefined) {
    options = shallowClone(options);
    options.ignoreUndefined = this.s.options.ignoreUndefined;
  }

  // Execute using callback
  if(typeof callback == 'function') return deleteOne(self, filter, options, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    deleteOne(self, filter, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
...
Next lets delete the document where the field **a** equals to **3**.

'''js
var deleteDocument = function(db, callback) {
  // Get the documents collection
  var collection = db.collection('documents');
  // Insert some documents
  collection.deleteOne({ a : 3 }, function(err, result) {
    assert.equal(err, null);
    assert.equal(1, result.result.n);
    console.log("Removed the document with the field a equal to 3");
    callback(result);
  });
}
'''
...
```

#### <a name="apidoc.element.mongodb.Collection.prototype.distinct"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>distinct (key, query, options, callback)](#apidoc.element.mongodb.Collection.prototype.distinct)
- description and source-code
```javascript
distinct = function (key, query, options, callback) {
  var self = this;
  var args = Array.prototype.slice.call(arguments, 1);
  callback = args.pop();
  if(typeof callback != 'function') args.push(callback);
  var queryOption = args.length ? args.shift() || {} : {};
  var optionsOption = args.length ? args.shift() || {} : {};

  // Execute using callback
  if(typeof callback == 'function') return distinct(self, key, queryOption, optionsOption, callback);

  // Ensure the query and options are set
  query = query || {};
  options = options || {};

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    distinct(self, key, query, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Collection.prototype.drop"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>drop (options, callback)](#apidoc.element.mongodb.Collection.prototype.drop)
- description and source-code
```javascript
drop = function (options, callback) {
  var self = this;
  if(typeof options == 'function') callback = options, options = {};
  options = options || {};

  // Execute using callback
  if(typeof callback == 'function') return self.s.db.dropCollection(self.s.name, options, callback);
  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    self.s.db.dropCollection(self.s.name, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Collection.prototype.dropAllIndexes"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>dropAllIndexes (options, callback)](#apidoc.element.mongodb.Collection.prototype.dropAllIndexes)
- description and source-code
```javascript
dropAllIndexes = function (options, callback) {
  var self = this;

  // Do we have options
  if(typeof options == 'function') callback = options, options = {};
  options = options || {};

  // Execute using callback
  if(typeof callback == 'function') return dropIndexes(self, options, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    dropIndexes(self, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Collection.prototype.dropIndex"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>dropIndex (indexName, options, callback)](#apidoc.element.mongodb.Collection.prototype.dropIndex)
- description and source-code
```javascript
dropIndex = function (indexName, options, callback) {
  var self = this;
  var args = Array.prototype.slice.call(arguments, 1);
  callback = args.pop();
  if(typeof callback != 'function') args.push(callback);
  options = args.length ? args.shift() || {} : {};
  // Run only against primary
  options.readPreference = ReadPreference.PRIMARY;

  // Execute using callback
  if(typeof callback == 'function') return dropIndex(self, indexName, options, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    dropIndex(self, indexName, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Collection.prototype.dropIndexes"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>dropIndexes (options, callback)](#apidoc.element.mongodb.Collection.prototype.dropIndexes)
- description and source-code
```javascript
dropIndexes = function (options, callback) {
  var self = this;

  // Do we have options
  if(typeof options == 'function') callback = options, options = {};
  options = options || {};

  // Execute using callback
  if(typeof callback == 'function') return dropIndexes(self, options, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    dropIndexes(self, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Collection.prototype.ensureIndex"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>ensureIndex (fieldOrSpec, options, callback)](#apidoc.element.mongodb.Collection.prototype.ensureIndex)
- description and source-code
```javascript
ensureIndex = function (fieldOrSpec, options, callback) {
  var self = this;
  if(typeof options == 'function') callback = options, options = {};
  options = options || {};

  // Execute using callback
  if(typeof callback == 'function') return ensureIndex(self, fieldOrSpec, options, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    ensureIndex(self, fieldOrSpec, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Collection.prototype.find"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>find ()](#apidoc.element.mongodb.Collection.prototype.find)
- description and source-code
```javascript
find = function () {
  var options
    , args = Array.prototype.slice.call(arguments, 0)
    , has_callback = typeof args[args.length - 1] === 'function'
    , has_weird_callback = typeof args[0] === 'function'
    , callback = has_callback ? args.pop() : (has_weird_callback ? args.shift() : null)
    , len = args.length
    , selector = len >= 1 ? args[0] : {}
    , fields = len >= 2 ? args[1] : undefined;

  if(len === 1 && has_weird_callback) {
    // backwards compat for callback?, options case
    selector = {};
    options = args[0];
  }

  if(len === 2 && fields !== undefined && !Array.isArray(fields)) {
    var fieldKeys = Object.keys(fields);
    var is_option = false;

    for(var i = 0; i < fieldKeys.length; i++) {
      if(testForFields[fieldKeys[i]] != null) {
        is_option = true;
        break;
      }
    }

    if(is_option) {
      options = fields;
      fields = undefined;
    } else {
      options = {};
    }
  } else if(len === 2 && Array.isArray(fields) && !Array.isArray(fields[0])) {
    var newFields = {};
    // Rewrite the array
    for(i = 0; i < fields.length; i++) {
      newFields[fields[i]] = 1;
    }
    // Set the fields
    fields = newFields;
  }

  if(3 === len) {
    options = args[2];
  }

  // Ensure selector is not null
  selector = selector == null ? {} : selector;
  // Validate correctness off the selector
  var object = selector;
  if(Buffer.isBuffer(object)) {
    var object_size = object[0] | object[1] << 8 | object[2] << 16 | object[3] << 24;
    if(object_size != object.length)  {
      var error = new Error("query selector raw message size does not match message header size [" + object.length + "] != [" +
object_size + "]");
      error.name = 'MongoError';
      throw error;
    }
  }

  // Validate correctness of the field selector
  object = fields;
  if(Buffer.isBuffer(object)) {
    object_size = object[0] | object[1] << 8 | object[2] << 16 | object[3] << 24;
    if(object_size != object.length)  {
      error = new Error("query fields raw message size does not match message header size [" + object.length + "] != [" + object_size
 + "]");
      error.name = 'MongoError';
      throw error;
    }
  }

  // Check special case where we are using an objectId
  if(selector != null && selector._bsontype == 'ObjectID') {
    selector = {_id:selector};
  }

  // If it's a serialized fields field we need to just let it through
  // user be warned it better be good
  if(options && options.fields && !(Buffer.isBuffer(options.fields))) {
    fields = {};

    if(Array.isArray(options.fields)) {
      if(!options.fields.length) {
        fields['_id'] = 1;
      } else {
        var l = options.fields.length;

        for (i = 0; i < l; i++) {
          fields[options.fields[i]] = 1;
        }
      }
    } else {
      fields = options.fields;
    }
  }

  if (!options) options = {};

  var newOptions = {};
  // Make a shallow copy of options
  for (var key in options) {
    newOptions[key] = options[key];
  }

  // Unpack options
  newOptions.skip = len > 3 ? args[2] : options.skip ? options.skip : 0;
  newOptions.limit = len > 3 ? args[3] : options.limit ? options.limit : 0;
  newOptions.raw = options.raw != null && typeof options.raw === 'boolean' ? options.raw : this.s.raw;
  newOptions.hint = options.hint != null ? normalizeHintField(options.hint) : this.s.collectionHint;
  newOptions.timeout = len == 5 ? args[4] : typeof options.timeout === 'undefined' ? undefined : options.timeout;
  // // If we have overridden slaveOk otherwise use the default db setting
  newOptions.slaveOk = options.slaveOk != null ? options.slaveOk : this.s.db.slaveOk;

  // Add read preference if needed
  newOptions = getReadPreference(this, newOptions, this.s.db, this);

  // Set slave ok to true if read preference different from primary
  if(newOptions.readPreference != null
    && (newOptions.readPreference != 'primary' || newOptions.readPreference.mode != 'primary')) {
    newOptions.slaveOk = true;
  }

  // Ensure the query is an object
  if(selector != null && typeof selector != 'object') { ...
```
- example usage
```shell
...
We will finish up the Quickstart CRUD methods by performing a simple query that returns all the documents matching the query.

'''js
var findDocuments = function(db, callback) {
  // Get the documents collection
  var collection = db.collection('documents');
  // Find some documents
  collection.find({}).toArray(function(err, docs) {
    assert.equal(err, null);
    assert.equal(2, docs.length);
    console.log("Found the following records");
    console.dir(docs);
    callback(docs);
  });
}
...
```

#### <a name="apidoc.element.mongodb.Collection.prototype.findAndModify"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>findAndModify (query, sort, doc, options, callback)](#apidoc.element.mongodb.Collection.prototype.findAndModify)
- description and source-code
```javascript
findAndModify = function (query, sort, doc, options, callback) {
  var self = this;
  var args = Array.prototype.slice.call(arguments, 1);
  callback = args.pop();
  if(typeof callback != 'function') args.push(callback);
  sort = args.length ? args.shift() || [] : [];
  doc = args.length ? args.shift() : null;
  options = args.length ? args.shift() || {} : {};

  // Clone options
  options = shallowClone(options);
  // Force read preference primary
  options.readPreference = ReadPreference.PRIMARY;

  // Execute using callback
  if(typeof callback == 'function') return findAndModify(self, query, sort, doc, options, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    options = options || {};

    findAndModify(self, query, sort, doc, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Collection.prototype.findAndRemove"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>findAndRemove (query, sort, options, callback)](#apidoc.element.mongodb.Collection.prototype.findAndRemove)
- description and source-code
```javascript
findAndRemove = function (query, sort, options, callback) {
  var self = this;
  var args = Array.prototype.slice.call(arguments, 1);
  callback = args.pop();
  if(typeof callback != 'function') args.push(callback);
  sort = args.length ? args.shift() || [] : [];
  options = args.length ? args.shift() || {} : {};

  // Execute using callback
  if(typeof callback == 'function') return findAndRemove(self, query, sort, options, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    findAndRemove(self, query, sort, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Collection.prototype.findOne"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>findOne ()](#apidoc.element.mongodb.Collection.prototype.findOne)
- description and source-code
```javascript
findOne = function () {
  var self = this;
  var args = Array.prototype.slice.call(arguments, 0);
  var callback = args.pop();
  if(typeof callback != 'function') args.push(callback);

  // Execute using callback
  if(typeof callback == 'function') return findOne(self, args, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    findOne(self, args, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Collection.prototype.findOneAndDelete"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>findOneAndDelete (filter, options, callback)](#apidoc.element.mongodb.Collection.prototype.findOneAndDelete)
- description and source-code
```javascript
findOneAndDelete = function (filter, options, callback) {
  var self = this;
  if(typeof options == 'function') callback = options, options = {};
  options = options || {};

  // Basic validation
  if(filter == null || typeof filter != 'object') throw toError('filter parameter must be an object');

  // Execute using callback
  if(typeof callback == 'function') return findOneAndDelete(self, filter, options, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    options = options || {};

    findOneAndDelete(self, filter, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Collection.prototype.findOneAndReplace"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>findOneAndReplace (filter, replacement, options, callback)](#apidoc.element.mongodb.Collection.prototype.findOneAndReplace)
- description and source-code
```javascript
findOneAndReplace = function (filter, replacement, options, callback) {
  var self = this;
  if(typeof options == 'function') callback = options, options = {};
  options = options || {};

  // Basic validation
  if(filter == null || typeof filter != 'object') throw toError('filter parameter must be an object');
  if(replacement == null || typeof replacement != 'object') throw toError('replacement parameter must be an object');

  // Execute using callback
  if(typeof callback == 'function') return findOneAndReplace(self, filter, replacement, options, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    options = options || {};

    findOneAndReplace(self, filter, replacement, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Collection.prototype.findOneAndUpdate"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>findOneAndUpdate (filter, update, options, callback)](#apidoc.element.mongodb.Collection.prototype.findOneAndUpdate)
- description and source-code
```javascript
findOneAndUpdate = function (filter, update, options, callback) {
  var self = this;
  if(typeof options == 'function') callback = options, options = {};
  options = options || {};

  // Basic validation
  if(filter == null || typeof filter != 'object') throw toError('filter parameter must be an object');
  if(update == null || typeof update != 'object') throw toError('update parameter must be an object');

  // Execute using callback
  if(typeof callback == 'function') return findOneAndUpdate(self, filter, update, options, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    options = options || {};

    findOneAndUpdate(self, filter, update, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Collection.prototype.geoHaystackSearch"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>geoHaystackSearch (x, y, options, callback)](#apidoc.element.mongodb.Collection.prototype.geoHaystackSearch)
- description and source-code
```javascript
geoHaystackSearch = function (x, y, options, callback) {
  var self = this;
  var args = Array.prototype.slice.call(arguments, 2);
  callback = args.pop();
  if(typeof callback != 'function') args.push(callback);
  // Fetch all commands
  options = args.length ? args.shift() || {} : {};

  // Execute using callback
  if(typeof callback == 'function') return geoHaystackSearch(self, x, y, options, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    geoHaystackSearch(self, x, y, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Collection.prototype.geoNear"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>geoNear (x, y, options, callback)](#apidoc.element.mongodb.Collection.prototype.geoNear)
- description and source-code
```javascript
geoNear = function (x, y, options, callback) {
  var self = this;
  var point = typeof(x) == 'object' && x
    , args = Array.prototype.slice.call(arguments, point?1:2);

  callback = args.pop();
  if(typeof callback != 'function') args.push(callback);
  // Fetch all commands
  options = args.length ? args.shift() || {} : {};

  // Execute using callback
  if(typeof callback == 'function') return geoNear(self, x, y, point, options, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    geoNear(self, x, y, point, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Collection.prototype.group"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>group (keys, condition, initial, reduce, finalize, command, options, callback)](#apidoc.element.mongodb.Collection.prototype.group)
- description and source-code
```javascript
group = function (keys, condition, initial, reduce, finalize, command, options, callback) {
  var self = this;
  var args = Array.prototype.slice.call(arguments, 3);
  callback = args.pop();
  if(typeof callback != 'function') args.push(callback);
  // Fetch all commands
  reduce = args.length ? args.shift() : null;
  finalize = args.length ? args.shift() : null;
  command = args.length ? args.shift() : null;
  options = args.length ? args.shift() || {} : {};

  // Make sure we are backward compatible
  if(!(typeof finalize == 'function')) {
    command = finalize;
    finalize = null;
  }

  if (!Array.isArray(keys) && keys instanceof Object && typeof(keys) !== 'function' && !(keys._bsontype == 'Code')) {
    keys = Object.keys(keys);
  }

  if(typeof reduce === 'function') {
    reduce = reduce.toString();
  }

  if(typeof finalize === 'function') {
    finalize = finalize.toString();
  }

  // Set up the command as default
  command = command == null ? true : command;

  // Execute using callback
  if(typeof callback == 'function') return group(self, keys, condition, initial, reduce, finalize, command, options, callback);
  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    group(self, keys, condition, initial, reduce, finalize, command, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Collection.prototype.indexExists"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>indexExists (indexes, callback)](#apidoc.element.mongodb.Collection.prototype.indexExists)
- description and source-code
```javascript
indexExists = function (indexes, callback) {
  var self = this;

  // Execute using callback
  if(typeof callback == 'function') return indexExists(self, indexes, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    indexExists(self, indexes, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Collection.prototype.indexInformation"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>indexInformation (options, callback)](#apidoc.element.mongodb.Collection.prototype.indexInformation)
- description and source-code
```javascript
indexInformation = function (options, callback) {
  var self = this;
  // Unpack calls
  var args = Array.prototype.slice.call(arguments, 0);
  callback = args.pop();
  if(typeof callback != 'function') args.push(callback);
  options = args.length ? args.shift() || {} : {};

  // Execute using callback
  if(typeof callback == 'function') return indexInformation(self, options, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    indexInformation(self, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Collection.prototype.indexes"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>indexes (callback)](#apidoc.element.mongodb.Collection.prototype.indexes)
- description and source-code
```javascript
indexes = function (callback) {
  var self = this;
  // Execute using callback
  if(typeof callback == 'function') return indexes(self, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    indexes(self, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Collection.prototype.initializeOrderedBulkOp"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>initializeOrderedBulkOp (options)](#apidoc.element.mongodb.Collection.prototype.initializeOrderedBulkOp)
- description and source-code
```javascript
initializeOrderedBulkOp = function (options) {
  options = options || {};
  options.promiseLibrary = this.s.promiseLibrary;
  return ordered(this.s.topology, this, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Collection.prototype.initializeUnorderedBulkOp"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>initializeUnorderedBulkOp (options)](#apidoc.element.mongodb.Collection.prototype.initializeUnorderedBulkOp)
- description and source-code
```javascript
initializeUnorderedBulkOp = function (options) {
  options = options || {};
  options.promiseLibrary = this.s.promiseLibrary;
  return unordered(this.s.topology, this, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Collection.prototype.insert"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>insert (docs, options, callback)](#apidoc.element.mongodb.Collection.prototype.insert)
- description and source-code
```javascript
insert = function (docs, options, callback) {
  if(typeof options == 'function') callback = options, options = {};
  options = options || {ordered:false};
  docs = !Array.isArray(docs) ? [docs] : docs;

  if(options.keepGoing == true) {
    options.ordered = false;
  }

  return this.insertMany(docs, options, callback);
}
```
- example usage
```shell
...
* // Connection url
* var url = 'mongodb://localhost:27017/test';
* // Connect using MongoClient
* MongoClient.connect(url, function(err, db) {
*   // Create a collection we want to drop later
*   var col = db.collection('createIndexExample1');
*   // Insert a bunch of documents
*   col.insert([{a:1, b:1}
*     , {a:2, b:2}, {a:3, b:3}
*     , {a:4, b:4}], {w:1}, function(err, result) {
*     test.equal(null, err);
*     // Show that duplicate records got dropped
*     col.aggregation({}, {cursor: {}}).toArray(function(err, items) {
*       test.equal(null, err);
*       test.equal(4, items.length);
...
```

#### <a name="apidoc.element.mongodb.Collection.prototype.insertMany"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>insertMany (docs, options, callback)](#apidoc.element.mongodb.Collection.prototype.insertMany)
- description and source-code
```javascript
insertMany = function (docs, options, callback) {
  var self = this;
  if(typeof options == 'function') callback = options, options = {};
  options = options || {ordered:true};
  if(!Array.isArray(docs) && typeof callback == 'function') {
    return callback(MongoError.create({message: 'docs parameter must be an array of documents', driver:true }));
  } else if(!Array.isArray(docs)) {
    return new this.s.promiseLibrary(function(resolve, reject) {
      reject(MongoError.create({message: 'docs parameter must be an array of documents', driver:true }));
    });
  }

  // Get the write concern options
  if(typeof options.checkKeys != 'boolean') {
    options.checkKeys = true;
  }

  // If keep going set unordered
  options['serializeFunctions'] = options['serializeFunctions'] || self.s.serializeFunctions;

  // Set up the force server object id
  var forceServerObjectId = typeof options.forceServerObjectId == 'boolean'
    ? options.forceServerObjectId : self.s.db.options.forceServerObjectId;

  // Do we want to force the server to assign the _id key
  if(forceServerObjectId !== true) {
    // Add _id if not specified
    for(var i = 0; i < docs.length; i++) {
      if(docs[i]._id == null) docs[i]._id = self.s.pkFactory.createPk();
    }
  }

  // Generate the bulk write operations
  var operations = [{
    insertMany: docs
  }];

  // Execute using callback
  if(typeof callback == 'function') return bulkWrite(self, operations, options, function(err, r) {
    if(err) return callback(err, r);
    callback(null, mapInserManyResults(docs, r));
  });

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    bulkWrite(self, operations, options, function(err, r) {
      if(err) return reject(err);
      resolve(mapInserManyResults(docs, r));
    });
  });
}
```
- example usage
```shell
...
Let's create a function that will insert some documents for us.

'''js
var insertDocuments = function(db, callback) {
// Get the documents collection
var collection = db.collection('documents');
// Insert some documents
collection.insertMany([
  {a : 1}, {a : 2}, {a : 3}
], function(err, result) {
  assert.equal(err, null);
  assert.equal(3, result.result.n);
  assert.equal(3, result.ops.length);
  console.log("Inserted 3 documents into the document collection");
  callback(result);
...
```

#### <a name="apidoc.element.mongodb.Collection.prototype.insertOne"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>insertOne (doc, options, callback)](#apidoc.element.mongodb.Collection.prototype.insertOne)
- description and source-code
```javascript
insertOne = function (doc, options, callback) {
  var self = this;
  if(typeof options == 'function') callback = options, options = {};
  options = options || {};
  if(Array.isArray(doc) && typeof callback == 'function') {
    return callback(MongoError.create({message: 'doc parameter must be an object', driver:true }));
  } else if(Array.isArray(doc)) {
    return new this.s.promiseLibrary(function(resolve, reject) {
      reject(MongoError.create({message: 'doc parameter must be an object', driver:true }));
    });
  }

  // Add ignoreUndfined
  if(this.s.options.ignoreUndefined) {
    options = shallowClone(options);
    options.ignoreUndefined = this.s.options.ignoreUndefined;
  }

  // Execute using callback
  if(typeof callback == 'function') return insertOne(self, doc, options, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    insertOne(self, doc, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Collection.prototype.isCapped"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>isCapped (callback)](#apidoc.element.mongodb.Collection.prototype.isCapped)
- description and source-code
```javascript
isCapped = function (callback) {
  var self = this;

  // Execute using callback
  if(typeof callback == 'function') return isCapped(self, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    isCapped(self, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Collection.prototype.listIndexes"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>listIndexes (options)](#apidoc.element.mongodb.Collection.prototype.listIndexes)
- description and source-code
```javascript
listIndexes = function (options) {
  options = options || {};
  // Clone the options
  options = shallowClone(options);
  // Determine the read preference in the options.
  options = getReadPreference(this, options, this.s.db, this);
  // Set the CommandCursor constructor
  options.cursorFactory = CommandCursor;
  // Set the promiseLibrary
  options.promiseLibrary = this.s.promiseLibrary;

  if(!this.s.topology.capabilities()) {
    throw new MongoError('cannot connect to server');
  }

  // We have a list collections command
  if(this.s.topology.capabilities().hasListIndexesCommand) {
    // Cursor options
    var cursor = options.batchSize ? {batchSize: options.batchSize} : {}
    // Build the command
    var command = { listIndexes: this.s.name, cursor: cursor };
    // Execute the cursor
    cursor = this.s.topology.cursor(f('%s.$cmd', this.s.dbName), command, options);
    // Do we have a readPreference, apply it
    if(options.readPreference) cursor.setReadPreference(options.readPreference);
    // Return the cursor
    return cursor;
  }

  // Get the namespace
  var ns = f('%s.system.indexes', this.s.dbName);
  // Get the query
  cursor = this.s.topology.cursor(ns, {find: ns, query: {ns: this.s.namespace}}, options);
  // Do we have a readPreference, apply it
  if(options.readPreference) cursor.setReadPreference(options.readPreference);
  // Set the passed in batch size if one was provided
  if(options.batchSize) cursor = cursor.batchSize(options.batchSize);
  // Return the cursor
  return cursor;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Collection.prototype.mapReduce"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>mapReduce (map, reduce, options, callback)](#apidoc.element.mongodb.Collection.prototype.mapReduce)
- description and source-code
```javascript
mapReduce = function (map, reduce, options, callback) {
  var self = this;
  if('function' === typeof options) callback = options, options = {};
  // Out must allways be defined (make sure we don't break weirdly on pre 1.8+ servers)
  if(null == options.out) {
    throw new Error("the out option parameter must be defined, see mongodb docs for possible values");
  }

  if('function' === typeof map) {
    map = map.toString();
  }

  if('function' === typeof reduce) {
    reduce = reduce.toString();
  }

  if('function' === typeof options.finalize) {
    options.finalize = options.finalize.toString();
  }

  // Execute using callback
  if(typeof callback == 'function') return mapReduce(self, map, reduce, options, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    mapReduce(self, map, reduce, options, function(err, r, r1) {
      if(err) return reject(err);
      if(!r1) return resolve(r);
      resolve({results: r, stats: r1});
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Collection.prototype.options"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>options (callback)](#apidoc.element.mongodb.Collection.prototype.options)
- description and source-code
```javascript
options = function (callback) {
  var self = this;

  // Execute using callback
  if(typeof callback == 'function') return options(self, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    options(self, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Collection.prototype.parallelCollectionScan"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>parallelCollectionScan (options, callback)](#apidoc.element.mongodb.Collection.prototype.parallelCollectionScan)
- description and source-code
```javascript
parallelCollectionScan = function (options, callback) {
  var self = this;
  if(typeof options == 'function') callback = options, options = {numCursors: 1};
  // Set number of cursors to 1
  options.numCursors = options.numCursors || 1;
  options.batchSize = options.batchSize || 1000;

  options = shallowClone(options);
  // Ensure we have the right read preference inheritance
  options = getReadPreference(this, options, this.s.db, this);

  // Add a promiseLibrary
  options.promiseLibrary = this.s.promiseLibrary;

  // Execute using callback
  if(typeof callback == 'function') return parallelCollectionScan(self, options, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    parallelCollectionScan(self, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Collection.prototype.reIndex"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>reIndex (options, callback)](#apidoc.element.mongodb.Collection.prototype.reIndex)
- description and source-code
```javascript
reIndex = function (options, callback) {
  var self = this;
  if(typeof options == 'function') callback = options, options = {};
  options = options || {};

  // Execute using callback
  if(typeof callback == 'function') return reIndex(self, options, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    reIndex(self, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Collection.prototype.remove"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>remove (selector, options, callback)](#apidoc.element.mongodb.Collection.prototype.remove)
- description and source-code
```javascript
remove = function (selector, options, callback) {
  var self = this;

  // Add ignoreUndfined
  if(this.s.options.ignoreUndefined) {
    options = shallowClone(options);
    options.ignoreUndefined = this.s.options.ignoreUndefined;
  }

  // Execute using callback
  if(typeof callback == 'function') return removeDocuments(self, selector, options, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    removeDocuments(self, selector, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Collection.prototype.removeMany"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>removeMany (filter, options, callback)](#apidoc.element.mongodb.Collection.prototype.removeMany)
- description and source-code
```javascript
removeMany = function (filter, options, callback) {
  var self = this;
  if(typeof options == 'function') callback = options, options = {};
  options = shallowClone(options);

  // Add ignoreUndfined
  if(this.s.options.ignoreUndefined) {
    options = shallowClone(options);
    options.ignoreUndefined = this.s.options.ignoreUndefined;
  }

  // Execute using callback
  if(typeof callback == 'function') return deleteMany(self, filter, options, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    deleteMany(self, filter, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Collection.prototype.removeOne"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>removeOne (filter, options, callback)](#apidoc.element.mongodb.Collection.prototype.removeOne)
- description and source-code
```javascript
removeOne = function (filter, options, callback) {
  var self = this;
  if(typeof options == 'function') callback = options, options = {};
  options = shallowClone(options);

  // Add ignoreUndfined
  if(this.s.options.ignoreUndefined) {
    options = shallowClone(options);
    options.ignoreUndefined = this.s.options.ignoreUndefined;
  }

  // Execute using callback
  if(typeof callback == 'function') return deleteOne(self, filter, options, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    deleteOne(self, filter, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Collection.prototype.rename"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>rename (newName, opt, callback)](#apidoc.element.mongodb.Collection.prototype.rename)
- description and source-code
```javascript
rename = function (newName, opt, callback) {
  var self = this;
  if(typeof opt == 'function') callback = opt, opt = {};
  opt = assign({}, opt, {readPreference: ReadPreference.PRIMARY});

  // Execute using callback
  if(typeof callback == 'function') return rename(self, newName, opt, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    rename(self, newName, opt, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Collection.prototype.replaceOne"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>replaceOne (filter, doc, options, callback)](#apidoc.element.mongodb.Collection.prototype.replaceOne)
- description and source-code
```javascript
replaceOne = function (filter, doc, options, callback) {
  var self = this;
  if(typeof options == 'function') callback = options, options = {};
  options = shallowClone(options)

  // Add ignoreUndfined
  if(this.s.options.ignoreUndefined) {
    options = shallowClone(options);
    options.ignoreUndefined = this.s.options.ignoreUndefined;
  }

  // Execute using callback
  if(typeof callback == 'function') return replaceOne(self, filter, doc, options, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    replaceOne(self, filter, doc, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Collection.prototype.save"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>save (doc, options, callback)](#apidoc.element.mongodb.Collection.prototype.save)
- description and source-code
```javascript
save = function (doc, options, callback) {
  var self = this;
  if(typeof options == 'function') callback = options, options = {};
  options = options || {};

  // Add ignoreUndfined
  if(this.s.options.ignoreUndefined) {
    options = shallowClone(options);
    options.ignoreUndefined = this.s.options.ignoreUndefined;
  }

  // Execute using callback
  if(typeof callback == 'function') return save(self, doc, options, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    save(self, doc, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Collection.prototype.stats"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>stats (options, callback)](#apidoc.element.mongodb.Collection.prototype.stats)
- description and source-code
```javascript
stats = function (options, callback) {
  var self = this;
  var args = Array.prototype.slice.call(arguments, 0);
  callback = args.pop();
  if(typeof callback != 'function') args.push(callback);
  // Fetch all commands
  options = args.length ? args.shift() || {} : {};

  // Execute using callback
  if(typeof callback == 'function') return stats(self, options, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    stats(self, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Collection.prototype.update"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>update (selector, document, options, callback)](#apidoc.element.mongodb.Collection.prototype.update)
- description and source-code
```javascript
update = function (selector, document, options, callback) {
  var self = this;

  // Add ignoreUndfined
  if(this.s.options.ignoreUndefined) {
    options = shallowClone(options);
    options.ignoreUndefined = this.s.options.ignoreUndefined;
  }

  // Execute using callback
  if(typeof callback == 'function') return updateDocuments(self, selector, document, options, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    updateDocuments(self, selector, document, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Collection.prototype.updateMany"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>updateMany (filter, update, options, callback)](#apidoc.element.mongodb.Collection.prototype.updateMany)
- description and source-code
```javascript
updateMany = function (filter, update, options, callback) {
  var self = this;
  if(typeof options == 'function') callback = options, options = {};
  options = shallowClone(options)

  // Add ignoreUndfined
  if(this.s.options.ignoreUndefined) {
    options = shallowClone(options);
    options.ignoreUndefined = this.s.options.ignoreUndefined;
  }

  // Execute using callback
  if(typeof callback == 'function') return updateMany(self, filter, update, options, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    updateMany(self, filter, update, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Collection.prototype.updateOne"></a>[function <span class="apidocSignatureSpan">mongodb.Collection.prototype.</span>updateOne (filter, update, options, callback)](#apidoc.element.mongodb.Collection.prototype.updateOne)
- description and source-code
```javascript
updateOne = function (filter, update, options, callback) {
  var self = this;
  if(typeof options == 'function') callback = options, options = {};
  options = shallowClone(options)

  // Add ignoreUndfined
  if(this.s.options.ignoreUndefined) {
    options = shallowClone(options);
    options.ignoreUndefined = this.s.options.ignoreUndefined;
  }

  // Execute using callback
  if(typeof callback == 'function') return updateOne(self, filter, update, options, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    updateOne(self, filter, update, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
...
Let's look at how to do a simple document update by adding a new field **b** to the document that has the field **a** set to **2
**.

'''js
var updateDocument = function(db, callback) {
  // Get the documents collection
  var collection = db.collection('documents');
  // Update document where a is 2, set b equal to 1
  collection.updateOne({ a : 2 }
    , { $set: { b : 1 } }, function(err, result) {
    assert.equal(err, null);
    assert.equal(1, result.result.n);
    console.log("Updated the document with the field a equal to 2");
    callback(result);
  });
}
...
```



# <a name="apidoc.module.mongodb.CoreConnection"></a>[module mongodb.CoreConnection](#apidoc.module.mongodb.CoreConnection)

#### <a name="apidoc.element.mongodb.CoreConnection.CoreConnection"></a>[function <span class="apidocSignatureSpan">mongodb.</span>CoreConnection (messageHandler, options)](#apidoc.element.mongodb.CoreConnection.CoreConnection)
- description and source-code
```javascript
CoreConnection = function (messageHandler, options) {
  // Add event listener
  EventEmitter.call(this);
  // Set empty if no options passed
  this.options = options || {};
  // Identification information
  this.id = _id++;
  // Logger instance
  this.logger = Logger('Connection', options);
  // No bson parser passed in
  if(!options.bson) throw new Error("must pass in valid bson parser");
  // Get bson parser
  this.bson = options.bson;
  // Grouping tag used for debugging purposes
  this.tag = options.tag;
  // Message handler
  this.messageHandler = messageHandler;

  // Max BSON message size
  this.maxBsonMessageSize = options.maxBsonMessageSize || (1024 * 1024 * 16 * 4);
  // Debug information
  if(this.logger.isDebug()) this.logger.debug(f('creating connection %s with options [%s]', this.id, JSON.stringify(debugOptions
(debugFields, options))));

  // Default options
  this.port = options.port || 27017;
  this.host = options.host || 'localhost';
  this.keepAlive = typeof options.keepAlive == 'boolean' ? options.keepAlive : true;
  this.keepAliveInitialDelay = options.keepAliveInitialDelay || 0;
  this.noDelay = typeof options.noDelay == 'boolean' ? options.noDelay : true;
  this.connectionTimeout = options.connectionTimeout || 0;
  this.socketTimeout = options.socketTimeout || 0;

  // If connection was destroyed
  this.destroyed = false;

  // Check if we have a domain socket
  this.domainSocket = this.host.indexOf('\/') != -1;

  // Serialize commands using function
  this.singleBufferSerializtion = typeof options.singleBufferSerializtion == 'boolean' ? options.singleBufferSerializtion : true
;
  this.serializationFunction = this.singleBufferSerializtion ? 'toBinUnified' : 'toBin';

  // SSL options
  this.ca = options.ca || null;
  this.crl = options.crl || null;
  this.cert = options.cert || null;
  this.key = options.key || null;
  this.passphrase = options.passphrase || null;
  this.ssl = typeof options.ssl == 'boolean' ? options.ssl : false;
  this.rejectUnauthorized = typeof options.rejectUnauthorized == 'boolean' ? options.rejectUnauthorized : true;
  this.checkServerIdentity = typeof options.checkServerIdentity == 'boolean'
    || typeof options.checkServerIdentity == 'function' ? options.checkServerIdentity : true;

  // If ssl not enabled
  if(!this.ssl) this.rejectUnauthorized = false;

  // Response options
  this.responseOptions = {
    promoteLongs: typeof options.promoteLongs == 'boolean' ?  options.promoteLongs : true,
    promoteValues: typeof options.promoteValues == 'boolean' ? options.promoteValues : true,
    promoteBuffers: typeof options.promoteBuffers == 'boolean' ? options.promoteBuffers: false
  }

  // Flushing
  this.flushing = false;
  this.queue = [];

  // Internal state
  this.connection = null;
  this.writeStream = null;

  // Create hash method
  var hash = crypto.createHash('sha1');
  hash.update(f('%s:%s', this.host, this.port));

  // Create a hash name
  this.hashedName = hash.digest('hex');

  // All operations in flight on the connection
  this.workItems = [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.CoreConnection.connections"></a>[function <span class="apidocSignatureSpan">mongodb.CoreConnection.</span>connections ()](#apidoc.element.mongodb.CoreConnection.connections)
- description and source-code
```javascript
connections = function () {
  return connections;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.CoreConnection.disableConnectionAccounting"></a>[function <span class="apidocSignatureSpan">mongodb.CoreConnection.</span>disableConnectionAccounting ()](#apidoc.element.mongodb.CoreConnection.disableConnectionAccounting)
- description and source-code
```javascript
disableConnectionAccounting = function () {
  connectionAccounting = false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.CoreConnection.enableConnectionAccounting"></a>[function <span class="apidocSignatureSpan">mongodb.CoreConnection.</span>enableConnectionAccounting ()](#apidoc.element.mongodb.CoreConnection.enableConnectionAccounting)
- description and source-code
```javascript
enableConnectionAccounting = function () {
  connectionAccounting = true;
  connections = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.CoreConnection.super_"></a>[function <span class="apidocSignatureSpan">mongodb.CoreConnection.</span>super_ ()](#apidoc.element.mongodb.CoreConnection.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.CoreConnection.prototype"></a>[module mongodb.CoreConnection.prototype](#apidoc.module.mongodb.CoreConnection.prototype)

#### <a name="apidoc.element.mongodb.CoreConnection.prototype.connect"></a>[function <span class="apidocSignatureSpan">mongodb.CoreConnection.prototype.</span>connect (_options)](#apidoc.element.mongodb.CoreConnection.prototype.connect)
- description and source-code
```javascript
connect = function (_options) {
  var self = this;
  _options = _options || {};
  // Set the connections
  if(connectionAccounting) addConnection(this.id, this);
  // Check if we are overriding the promoteLongs
  if(typeof _options.promoteLongs == 'boolean') {
    self.responseOptions.promoteLongs = _options.promoteLongs;
    self.responseOptions.promoteValues = _options.promoteValues;
    self.responseOptions.promoteBuffers = _options.promoteBuffers;
  }

  // Create new connection instance
  self.connection = self.domainSocket
    ? net.createConnection(self.host)
    : net.createConnection(self.port, self.host);

  // Set the options for the connection
  self.connection.setKeepAlive(self.keepAlive, self.keepAliveInitialDelay);
  self.connection.setTimeout(self.connectionTimeout);
  self.connection.setNoDelay(self.noDelay);

  // If we have ssl enabled
  if(self.ssl) {
    var sslOptions = {
        socket: self.connection
      , rejectUnauthorized: self.rejectUnauthorized
    }

    // Merge in options
    merge(sslOptions, this.options);
    merge(sslOptions, _options);

    // Set options for ssl
    if(self.ca) sslOptions.ca = self.ca;
    if(self.crl) sslOptions.crl = self.crl;
    if(self.cert) sslOptions.cert = self.cert;
    if(self.key) sslOptions.key = self.key;
    if(self.passphrase) sslOptions.passphrase = self.passphrase;

    // Override checkServerIdentity behavior
    if(self.checkServerIdentity == false) {
      // Skip the identiy check by retuning undefined as per node documents
      // https://nodejs.org/api/tls.html#tls_tls_connect_options_callback
      sslOptions.checkServerIdentity = function() {
        return undefined;
      }
    } else if(typeof self.checkServerIdentity == 'function') {
      sslOptions.checkServerIdentity = self.checkServerIdentity;
    }

    // Set default sni servername to be the same as host
    if(sslOptions.servername == null) {
      sslOptions.servername = self.host;
    }

    // Attempt SSL connection
    self.connection = tls.connect(self.port, self.host, sslOptions, function() {
      // Error on auth or skip
      if(self.connection.authorizationError && self.rejectUnauthorized) {
        return self.emit("error", self.connection.authorizationError, self, {ssl:true});
      }

      // Set socket timeout instead of connection timeout
      self.connection.setTimeout(self.socketTimeout);
      // We are done emit connect
      self.emit('connect', self);
    });
    self.connection.setTimeout(self.connectionTimeout);
  } else {
    self.connection.on('connect', function() {
      // Set socket timeout instead of connection timeout
      self.connection.setTimeout(self.socketTimeout);
      // Emit connect event
      self.emit('connect', self);
    });
  }

  // Add handlers for events
  self.connection.once('error', errorHandler(self));
  self.connection.once('timeout', timeoutHandler(self));
  self.connection.once('close', closeHandler(self));
  self.connection.on('data', dataHandler(self));
}
```
- example usage
```shell
...
'''js
var MongoClient = require('mongodb').MongoClient
  , assert = require('assert');

// Connection URL
var url = 'mongodb://localhost:27017/myproject';
// Use connect method to connect to the Server
MongoClient.connect(url, function(err, db) {
  assert.equal(null, err);
  console.log("Connected correctly to server");

  db.close();
});
'''
...
```

#### <a name="apidoc.element.mongodb.CoreConnection.prototype.destroy"></a>[function <span class="apidocSignatureSpan">mongodb.CoreConnection.prototype.</span>destroy ()](#apidoc.element.mongodb.CoreConnection.prototype.destroy)
- description and source-code
```javascript
destroy = function () {
  // Set the connections
  if(connectionAccounting) deleteConnection(this.id);
  if(this.connection) {
    this.connection.end();
    this.connection.destroy();
  }

  this.destroyed = true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.CoreConnection.prototype.isConnected"></a>[function <span class="apidocSignatureSpan">mongodb.CoreConnection.prototype.</span>isConnected ()](#apidoc.element.mongodb.CoreConnection.prototype.isConnected)
- description and source-code
```javascript
isConnected = function () {
  if(this.destroyed) return false;
  return !this.connection.destroyed && this.connection.writable;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.CoreConnection.prototype.resetSocketTimeout"></a>[function <span class="apidocSignatureSpan">mongodb.CoreConnection.prototype.</span>resetSocketTimeout ()](#apidoc.element.mongodb.CoreConnection.prototype.resetSocketTimeout)
- description and source-code
```javascript
resetSocketTimeout = function () {
  if(this.connection) {
    this.connection.setTimeout(this.socketTimeout);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.CoreConnection.prototype.setSocketTimeout"></a>[function <span class="apidocSignatureSpan">mongodb.CoreConnection.prototype.</span>setSocketTimeout (value)](#apidoc.element.mongodb.CoreConnection.prototype.setSocketTimeout)
- description and source-code
```javascript
setSocketTimeout = function (value) {
  if(this.connection) {
    this.connection.setTimeout(value);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.CoreConnection.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">mongodb.CoreConnection.prototype.</span>toJSON ()](#apidoc.element.mongodb.CoreConnection.prototype.toJSON)
- description and source-code
```javascript
toJSON = function () {
  return {id: this.id, host: this.host, port: this.port};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.CoreConnection.prototype.toString"></a>[function <span class="apidocSignatureSpan">mongodb.CoreConnection.prototype.</span>toString ()](#apidoc.element.mongodb.CoreConnection.prototype.toString)
- description and source-code
```javascript
toString = function () {
  return "" + this.id;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.CoreConnection.prototype.unref"></a>[function <span class="apidocSignatureSpan">mongodb.CoreConnection.prototype.</span>unref ()](#apidoc.element.mongodb.CoreConnection.prototype.unref)
- description and source-code
```javascript
unref = function () {
  if (this.connection) this.connection.unref();
  else {
    var self = this;
    this.once('connect', function() {
      self.connection.unref();
    });
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.CoreConnection.prototype.write"></a>[function <span class="apidocSignatureSpan">mongodb.CoreConnection.prototype.</span>write (buffer)](#apidoc.element.mongodb.CoreConnection.prototype.write)
- description and source-code
```javascript
write = function (buffer) {
  var i;
  // Debug Log
  if(this.logger.isDebug()) {
    if(!Array.isArray(buffer)) {
      this.logger.debug(f('writing buffer [%s] to %s:%s', buffer.toString('hex'), this.host, this.port));
    } else {
      for(i = 0; i < buffer.length; i++)
        this.logger.debug(f('writing buffer [%s] to %s:%s', buffer[i].toString('hex'), this.host, this.port));
    }
  }

  // Write out the command
  if(!Array.isArray(buffer)) return this.connection.write(buffer, 'binary');
  // Iterate over all buffers and write them in order to the socket
  for(i = 0; i < buffer.length; i++) this.connection.write(buffer[i], 'binary');
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.CoreServer"></a>[module mongodb.CoreServer](#apidoc.module.mongodb.CoreServer)

#### <a name="apidoc.element.mongodb.CoreServer.CoreServer"></a>[function <span class="apidocSignatureSpan">mongodb.</span>CoreServer (options)](#apidoc.element.mongodb.CoreServer.CoreServer)
- description and source-code
```javascript
CoreServer = function (options) {
  options = options || {};

  // Add event listener
  EventEmitter.call(this);

  // Server instance id
  this.id = id++;

  // Internal state
  this.s = {
    // Options
    options: options,
    // Logger
    logger: Logger('Server', options),
    // Factory overrides
    Cursor: options.cursorFactory || BasicCursor,
    // BSON instance
    bson: options.bson || new BSON([BSON.Binary, BSON.Code, BSON.DBRef, BSON.Decimal128,
      BSON.Double, BSON.Int32, BSON.Long, BSON.Map, BSON.MaxKey, BSON.MinKey,
      BSON.ObjectId, BSON.BSONRegExp, BSON.Symbol, BSON.Timestamp]),
    // Pool
    pool: null,
    // Disconnect handler
    disconnectHandler: options.disconnectHandler,
    // Monitor thread (keeps the connection alive)
    monitoring: typeof options.monitoring == 'boolean' ? options.monitoring : true,
    // Is the server in a topology
    inTopology: typeof options.inTopology == 'boolean' ? options.inTopology : false,
    // Monitoring timeout
    monitoringInterval: typeof options.monitoringInterval == 'number'
      ? options.monitoringInterval
      : 5000,
    // Topology id
    topologyId: -1
  }

  // Curent ismaster
  this.ismaster = null;
  // Current ping time
  this.lastIsMasterMS = -1;
  // The monitoringProcessId
  this.monitoringProcessId = null;
  // Initial connection
  this.initalConnect = true;
  // Wire protocol handler, default to oldest known protocol handler
  // this gets changed when the first ismaster is called.
  this.wireProtocolHandler = new PreTwoSixWireProtocolSupport();
  // Default type
  this._type = 'server';
  // Set the client info
  this.clientInfo = createClientInfo(options);

  // Max Stalleness values
  // last time we updated the ismaster state
  this.lastUpdateTime = 0;
  // Last write time
  this.lastWriteDate = 0;
  // Stalleness
  this.staleness = 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.CoreServer.disableServerAccounting"></a>[function <span class="apidocSignatureSpan">mongodb.CoreServer.</span>disableServerAccounting ()](#apidoc.element.mongodb.CoreServer.disableServerAccounting)
- description and source-code
```javascript
disableServerAccounting = function () {
  serverAccounting = false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.CoreServer.enableServerAccounting"></a>[function <span class="apidocSignatureSpan">mongodb.CoreServer.</span>enableServerAccounting ()](#apidoc.element.mongodb.CoreServer.enableServerAccounting)
- description and source-code
```javascript
enableServerAccounting = function () {
  serverAccounting = true;
  servers = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.CoreServer.servers"></a>[function <span class="apidocSignatureSpan">mongodb.CoreServer.</span>servers ()](#apidoc.element.mongodb.CoreServer.servers)
- description and source-code
```javascript
servers = function () {
  return servers;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.CoreServer.super_"></a>[function <span class="apidocSignatureSpan">mongodb.CoreServer.</span>super_ ()](#apidoc.element.mongodb.CoreServer.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.CoreServer.prototype"></a>[module mongodb.CoreServer.prototype](#apidoc.module.mongodb.CoreServer.prototype)

#### <a name="apidoc.element.mongodb.CoreServer.prototype.auth"></a>[function <span class="apidocSignatureSpan">mongodb.CoreServer.prototype.</span>auth (mechanism, db)](#apidoc.element.mongodb.CoreServer.prototype.auth)
- description and source-code
```javascript
auth = function (mechanism, db) {
  var self = this;

  // If we have the default mechanism we pick mechanism based on the wire
  // protocol max version. If it's >= 3 then scram-sha1 otherwise mongodb-cr
  if(mechanism == 'default' && self.ismaster && self.ismaster.maxWireVersion >= 3) {
    mechanism = 'scram-sha-1';
  } else if(mechanism == 'default') {
    mechanism = 'mongocr';
  }

  // Slice all the arguments off
  var args = Array.prototype.slice.call(arguments, 0);
  // Set the mechanism
  args[0] = mechanism;
  // Get the callback
  var callback = args[args.length - 1];

  // If we are not connected or have a disconnectHandler specified
  if(disconnectHandler(self, 'auth', db, args, {}, callback)) {
    return;
  }

  // Do not authenticate if we are an arbiter
  if(this.lastIsMaster() && this.lastIsMaster().arbiterOnly) {
    return callback(null, true);
  }

  // Apply the arguments to the pool
  self.s.pool.auth.apply(self.s.pool, args);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.CoreServer.prototype.command"></a>[function <span class="apidocSignatureSpan">mongodb.CoreServer.prototype.</span>command (ns, cmd, options, callback)](#apidoc.element.mongodb.CoreServer.prototype.command)
- description and source-code
```javascript
command = function (ns, cmd, options, callback) {
  var self = this;
  if(typeof options == 'function') callback = options, options = {}, options = options || {};
  var result = basicReadValidations(self, options);
  if(result) return callback(result);

  // Debug log
  if(self.s.logger.isDebug()) self.s.logger.debug(f('executing command [%s] against %s', JSON.stringify({
    ns: ns, cmd: cmd, options: debugOptions(debugFields, options)
  }), self.name));

  // If we are not connected or have a disconnectHandler specified
  if(disconnectHandler(self, 'command', ns, cmd, options, callback)) return;

  // Check if we have collation support
  if(this.ismaster && this.ismaster.maxWireVersion < 5 && cmd.collation) {
    return callback(new MongoError(f('server %s does not support collation', this.name)));
  }

  // Query options
  var queryOptions = {
    numberToSkip: 0,
    numberToReturn: -1,
    checkKeys: typeof options.checkKeys == 'boolean' ? options.checkKeys: false,
    serializeFunctions: typeof options.serializeFunctions == 'boolean' ? options.serializeFunctions : false,
    ignoreUndefined: typeof options.ignoreUndefined == 'boolean' ? options.ignoreUndefined : false
  };

  // Are we executing against a specific topology
  var topology = options.topology || {};
  // Create the query object
  var query = self.wireProtocolHandler.command(self.s.bson, ns, cmd, {}, topology, options);
  // Set slave OK of the query
  query.slaveOk = options.readPreference ? options.readPreference.slaveOk() : false;

  // Write options
  var writeOptions = {
    raw: typeof options.raw == 'boolean' ? options.raw : false,
    promoteLongs: typeof options.promoteLongs == 'boolean' ? options.promoteLongs : true,
    promoteValues: typeof options.promoteValues == 'boolean' ? options.promoteValues : true,
    promoteBuffers: typeof options.promoteBuffers == 'boolean' ? options.promoteBuffers : false,
    command: true,
    monitoring: typeof options.monitoring == 'boolean' ? options.monitoring : false,
    fullResult: typeof options.fullResult == 'boolean' ? options.fullResult : false,
    requestId: query.requestId,
    socketTimeout: typeof options.socketTimeout == 'number' ? options.socketTimeout : null,
  };

  // Write the operation to the pool
  self.s.pool.write(query, writeOptions, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.CoreServer.prototype.connect"></a>[function <span class="apidocSignatureSpan">mongodb.CoreServer.prototype.</span>connect (options)](#apidoc.element.mongodb.CoreServer.prototype.connect)
- description and source-code
```javascript
connect = function (options) {
  var self = this;
  options = options || {};

  // Set the connections
  if(serverAccounting) servers[this.id] = this;

  // Do not allow connect to be called on anything that's not disconnected
  if(self.s.pool && !self.s.pool.isDisconnected() && !self.s.pool.isDestroyed()) {
    throw MongoError.create(f('server instance in invalid state %s', self.s.state));
  }

  // Create a pool
  self.s.pool = new Pool(assign(self.s.options, options, {bson: this.s.bson}));

  // Set up listeners
  self.s.pool.on('close', eventHandler(self, 'close'));
  self.s.pool.on('error', eventHandler(self, 'error'));
  self.s.pool.on('timeout', eventHandler(self, 'timeout'));
  self.s.pool.on('parseError', eventHandler(self, 'parseError'));
  self.s.pool.on('connect', eventHandler(self, 'connect'));
  self.s.pool.on('reconnect', eventHandler(self, 'reconnect'));
  self.s.pool.on('reconnectFailed', eventHandler(self, 'reconnectFailed'));

  // Emit toplogy opening event if not in topology
  if(!self.s.inTopology) {
    this.emit('topologyOpening', { topologyId: self.id });
  }

  // Emit opening server event
  self.emit('serverOpening', {
    topologyId: self.s.topologyId != -1 ? self.s.topologyId : self.id,
    address: self.name
  });

  // Connect with optional auth settings
  if(options.auth) {
    self.s.pool.connect.apply(self.s.pool, options.auth);
  } else {
    self.s.pool.connect();
  }
}
```
- example usage
```shell
...
'''js
var MongoClient = require('mongodb').MongoClient
  , assert = require('assert');

// Connection URL
var url = 'mongodb://localhost:27017/myproject';
// Use connect method to connect to the Server
MongoClient.connect(url, function(err, db) {
  assert.equal(null, err);
  console.log("Connected correctly to server");

  db.close();
});
'''
...
```

#### <a name="apidoc.element.mongodb.CoreServer.prototype.connections"></a>[function <span class="apidocSignatureSpan">mongodb.CoreServer.prototype.</span>connections ()](#apidoc.element.mongodb.CoreServer.prototype.connections)
- description and source-code
```javascript
connections = function () {
  return this.s.pool.allConnections();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.CoreServer.prototype.cursor"></a>[function <span class="apidocSignatureSpan">mongodb.CoreServer.prototype.</span>cursor (ns, cmd, cursorOptions)](#apidoc.element.mongodb.CoreServer.prototype.cursor)
- description and source-code
```javascript
cursor = function (ns, cmd, cursorOptions) {
  var s = this.s;
  cursorOptions = cursorOptions || {};
  // Set up final cursor type
  var FinalCursor = cursorOptions.cursorFactory || s.Cursor;
  // Return the cursor
  return new FinalCursor(s.bson, ns, cmd, cursorOptions, this, s.options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.CoreServer.prototype.destroy"></a>[function <span class="apidocSignatureSpan">mongodb.CoreServer.prototype.</span>destroy (options)](#apidoc.element.mongodb.CoreServer.prototype.destroy)
- description and source-code
```javascript
destroy = function (options) {
  options = options || {};
  var self = this;

  // Set the connections
  if(serverAccounting) delete servers[this.id];

  // Destroy the monitoring process if any
  if(this.monitoringProcessId) {
    clearTimeout(this.monitoringProcessId);
  }

  // No pool, return
  if(!self.s.pool) return;

  // Emit close event
  if(options.emitClose) {
    self.emit('close', self);
  }

  // Emit destroy event
  if(options.emitDestroy) {
    self.emit('destroy', self);
  }

  // Remove all listeners
  listeners.forEach(function(event) {
    self.s.pool.removeAllListeners(event);
  });

  // Emit opening server event
  if(self.listeners('serverClosed').length > 0) self.emit('serverClosed', {
    topologyId: self.s.topologyId != -1 ? self.s.topologyId : self.id, address: self.name
  });

  // Emit toplogy opening event if not in topology
  if(self.listeners('topologyClosed').length > 0 && !self.s.inTopology) {
    self.emit('topologyClosed', { topologyId: self.id });
  }

  if(self.s.logger.isDebug()) {
    self.s.logger.debug(f('destroy called on server %s', self.name));
  }

  // Destroy the pool
  this.s.pool.destroy(options.force);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.CoreServer.prototype.equals"></a>[function <span class="apidocSignatureSpan">mongodb.CoreServer.prototype.</span>equals (server)](#apidoc.element.mongodb.CoreServer.prototype.equals)
- description and source-code
```javascript
equals = function (server) {
  if(typeof server == 'string') return this.name.toLowerCase() == server.toLowerCase();
  if(server.name) return this.name.toLowerCase() == server.name.toLowerCase();
  return false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.CoreServer.prototype.getConnection"></a>[function <span class="apidocSignatureSpan">mongodb.CoreServer.prototype.</span>getConnection ()](#apidoc.element.mongodb.CoreServer.prototype.getConnection)
- description and source-code
```javascript
getConnection = function () {
  return this.s.pool.get();
}
```
- example usage
```shell
...
}

// Set up the connection
var connectionId = null;

// Set local connection
if(this.connection) connectionId = this.connection;
if(!connectionId && this.server && this.server.getConnection) connectionId = this.server.getConnection();

// Get the command Name
var commandName = x == '_find' ? Object.keys(command)[0] : commandTranslation[x];

// Emit the start event for the command
command = {
  // Returns the command.
...
```

#### <a name="apidoc.element.mongodb.CoreServer.prototype.getDescription"></a>[function <span class="apidocSignatureSpan">mongodb.CoreServer.prototype.</span>getDescription ()](#apidoc.element.mongodb.CoreServer.prototype.getDescription)
- description and source-code
```javascript
getDescription = function () {
  var ismaster = this.ismaster || {};
  var description = {
    type: sdam.getTopologyType(this),
    address: this.name,
  };

  // Add fields if available
  if(ismaster.hosts) description.hosts = ismaster.hosts;
  if(ismaster.arbiters) description.arbiters = ismaster.arbiters;
  if(ismaster.passives) description.passives = ismaster.passives;
  if(ismaster.setName) description.setName = ismaster.setName;
  return description;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.CoreServer.prototype.getServer"></a>[function <span class="apidocSignatureSpan">mongodb.CoreServer.prototype.</span>getServer ()](#apidoc.element.mongodb.CoreServer.prototype.getServer)
- description and source-code
```javascript
getServer = function () {
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.CoreServer.prototype.insert"></a>[function <span class="apidocSignatureSpan">mongodb.CoreServer.prototype.</span>insert (ns, ops, options, callback)](#apidoc.element.mongodb.CoreServer.prototype.insert)
- description and source-code
```javascript
insert = function (ns, ops, options, callback) {
  var self = this;
  if(typeof options == 'function') callback = options, options = {}, options = options || {};
  var result = basicWriteValidations(self, options);
  if(result) return callback(result);

  // If we are not connected or have a disconnectHandler specified
  if(disconnectHandler(self, 'insert', ns, ops, options, callback)) return;

  // Setup the docs as an array
  ops = Array.isArray(ops) ? ops : [ops];

  // Execute write
  return self.wireProtocolHandler.insert(self.s.pool, self.ismaster, ns, self.s.bson, ops, options, callback);
}
```
- example usage
```shell
...
* // Connection url
* var url = 'mongodb://localhost:27017/test';
* // Connect using MongoClient
* MongoClient.connect(url, function(err, db) {
*   // Create a collection we want to drop later
*   var col = db.collection('createIndexExample1');
*   // Insert a bunch of documents
*   col.insert([{a:1, b:1}
*     , {a:2, b:2}, {a:3, b:3}
*     , {a:4, b:4}], {w:1}, function(err, result) {
*     test.equal(null, err);
*     // Show that duplicate records got dropped
*     col.aggregation({}, {cursor: {}}).toArray(function(err, items) {
*       test.equal(null, err);
*       test.equal(4, items.length);
...
```

#### <a name="apidoc.element.mongodb.CoreServer.prototype.isConnected"></a>[function <span class="apidocSignatureSpan">mongodb.CoreServer.prototype.</span>isConnected ()](#apidoc.element.mongodb.CoreServer.prototype.isConnected)
- description and source-code
```javascript
isConnected = function () {
  if(!this.s.pool) return false;
  return this.s.pool.isConnected();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.CoreServer.prototype.isDestroyed"></a>[function <span class="apidocSignatureSpan">mongodb.CoreServer.prototype.</span>isDestroyed ()](#apidoc.element.mongodb.CoreServer.prototype.isDestroyed)
- description and source-code
```javascript
isDestroyed = function () {
  if(!this.s.pool) return false;
  return this.s.pool.isDestroyed();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.CoreServer.prototype.lastIsMaster"></a>[function <span class="apidocSignatureSpan">mongodb.CoreServer.prototype.</span>lastIsMaster ()](#apidoc.element.mongodb.CoreServer.prototype.lastIsMaster)
- description and source-code
```javascript
lastIsMaster = function () {
  return this.ismaster;
}
```
- example usage
```shell
...
/**
 * Add a maxTimeMS stage to the aggregation pipeline
 * @method
 * @param {number} value The state maxTimeMS value.
 * @return {AggregationCursor}
 */
AggregationCursor.prototype.maxTimeMS = function(value) {
  if(this.s.topology.lastIsMaster().minWireVersion > 2) {
    this.s.cmd.maxTimeMS = value;
  }
  return this;
}

define.classMethod('maxTimeMS', {callback: false, promise:false, returns: [AggregationCursor]});
...
```

#### <a name="apidoc.element.mongodb.CoreServer.prototype.logout"></a>[function <span class="apidocSignatureSpan">mongodb.CoreServer.prototype.</span>logout (dbName, callback)](#apidoc.element.mongodb.CoreServer.prototype.logout)
- description and source-code
```javascript
logout = function (dbName, callback) {
  this.s.pool.logout(dbName, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.CoreServer.prototype.remove"></a>[function <span class="apidocSignatureSpan">mongodb.CoreServer.prototype.</span>remove (ns, ops, options, callback)](#apidoc.element.mongodb.CoreServer.prototype.remove)
- description and source-code
```javascript
remove = function (ns, ops, options, callback) {
  var self = this;
  if(typeof options == 'function') callback = options, options = {}, options = options || {};
  var result = basicWriteValidations(self, options);
  if(result) return callback(result);

  // If we are not connected or have a disconnectHandler specified
  if(disconnectHandler(self, 'remove', ns, ops, options, callback)) return;

  // Check if we have collation support
  if(this.ismaster && this.ismaster.maxWireVersion < 5 && options.collation) {
    return callback(new MongoError(f('server %s does not support collation', this.name)));
  }

  // Setup the docs as an array
  ops = Array.isArray(ops) ? ops : [ops];
  // Execute write
  return self.wireProtocolHandler.remove(self.s.pool, self.ismaster, ns, self.s.bson, ops, options, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.CoreServer.prototype.unref"></a>[function <span class="apidocSignatureSpan">mongodb.CoreServer.prototype.</span>unref ()](#apidoc.element.mongodb.CoreServer.prototype.unref)
- description and source-code
```javascript
unref = function () {
  this.s.pool.unref();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.CoreServer.prototype.update"></a>[function <span class="apidocSignatureSpan">mongodb.CoreServer.prototype.</span>update (ns, ops, options, callback)](#apidoc.element.mongodb.CoreServer.prototype.update)
- description and source-code
```javascript
update = function (ns, ops, options, callback) {
  var self = this;
  if(typeof options == 'function') callback = options, options = {}, options = options || {};
  var result = basicWriteValidations(self, options);
  if(result) return callback(result);

  // If we are not connected or have a disconnectHandler specified
  if(disconnectHandler(self, 'update', ns, ops, options, callback)) return;

  // Check if we have collation support
  if(this.ismaster && this.ismaster.maxWireVersion < 5 && options.collation) {
    return callback(new MongoError(f('server %s does not support collation', this.name)));
  }

  // Setup the docs as an array
  ops = Array.isArray(ops) ? ops : [ops];
  // Execute write
  return self.wireProtocolHandler.update(self.s.pool, self.ismaster, ns, self.s.bson, ops, options, callback);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.Cursor"></a>[module mongodb.Cursor](#apidoc.module.mongodb.Cursor)

#### <a name="apidoc.element.mongodb.Cursor.Cursor"></a>[function <span class="apidocSignatureSpan">mongodb.</span>Cursor (bson, ns, cmd, options, topology, topologyOptions)](#apidoc.element.mongodb.Cursor.Cursor)
- description and source-code
```javascript
Cursor = function (bson, ns, cmd, options, topology, topologyOptions) {
  CoreCursor.apply(this, Array.prototype.slice.call(arguments, 0));
  var self = this;
  var state = Cursor.INIT;
  var streamOptions = {};

  // Tailable cursor options
  var numberOfRetries = options.numberOfRetries || 5;
  var tailableRetryInterval = options.tailableRetryInterval || 500;
  var currentNumberOfRetries = numberOfRetries;

  // Get the promiseLibrary
  var promiseLibrary = options.promiseLibrary;

  // No promise library selected fall back
  if(!promiseLibrary) {
    promiseLibrary = typeof global.Promise == 'function' ?
      global.Promise : require('es6-promise').Promise;
  }

  // Set up
  Readable.call(this, {objectMode: true});

  // Internal cursor state
  this.s = {
    // Tailable cursor options
      numberOfRetries: numberOfRetries
    , tailableRetryInterval: tailableRetryInterval
    , currentNumberOfRetries: currentNumberOfRetries
    // State
    , state: state
    // Stream options
    , streamOptions: streamOptions
    // BSON
    , bson: bson
    // Namespace
    , ns: ns
    // Command
    , cmd: cmd
    // Options
    , options: options
    // Topology
    , topology: topology
    // Topology options
    , topologyOptions: topologyOptions
    // Promise library
    , promiseLibrary: promiseLibrary
    // Current doc
    , currentDoc: null
  }

  // Translate correctly
  if(self.s.options.noCursorTimeout == true) {
    self.addCursorFlag('noCursorTimeout', true);
  }

  // Set the sort value
  this.sortValue = self.s.cmd.sort;

  // Get the batchSize
  var batchSize = cmd.cursor && cmd.cursor.batchSize
    ? cmd.cursor && cmd.cursor.batchSize
    : (options.cursor && options.cursor.batchSize ? options.cursor.batchSize : 1000);

  // Set the batchSize
  this.setCursorBatchSize(batchSize);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.super_"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.</span>super_ (options)](#apidoc.element.mongodb.Cursor.super_)
- description and source-code
```javascript
function Readable(options) {
  if (!(this instanceof Readable))
    return new Readable(options);

  this._readableState = new ReadableState(options, this);

  // legacy
  this.readable = true;

  if (options && typeof options.read === 'function')
    this._read = options.read;

  Stream.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.Cursor.define"></a>[module mongodb.Cursor.define](#apidoc.module.mongodb.Cursor.define)

#### <a name="apidoc.element.mongodb.Cursor.define.object"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.define.</span>object (bson, ns, cmd, options, topology, topologyOptions)](#apidoc.element.mongodb.Cursor.define.object)
- description and source-code
```javascript
object = function (bson, ns, cmd, options, topology, topologyOptions) {
  CoreCursor.apply(this, Array.prototype.slice.call(arguments, 0));
  var self = this;
  var state = Cursor.INIT;
  var streamOptions = {};

  // Tailable cursor options
  var numberOfRetries = options.numberOfRetries || 5;
  var tailableRetryInterval = options.tailableRetryInterval || 500;
  var currentNumberOfRetries = numberOfRetries;

  // Get the promiseLibrary
  var promiseLibrary = options.promiseLibrary;

  // No promise library selected fall back
  if(!promiseLibrary) {
    promiseLibrary = typeof global.Promise == 'function' ?
      global.Promise : require('es6-promise').Promise;
  }

  // Set up
  Readable.call(this, {objectMode: true});

  // Internal cursor state
  this.s = {
    // Tailable cursor options
      numberOfRetries: numberOfRetries
    , tailableRetryInterval: tailableRetryInterval
    , currentNumberOfRetries: currentNumberOfRetries
    // State
    , state: state
    // Stream options
    , streamOptions: streamOptions
    // BSON
    , bson: bson
    // Namespace
    , ns: ns
    // Command
    , cmd: cmd
    // Options
    , options: options
    // Topology
    , topology: topology
    // Topology options
    , topologyOptions: topologyOptions
    // Promise library
    , promiseLibrary: promiseLibrary
    // Current doc
    , currentDoc: null
  }

  // Translate correctly
  if(self.s.options.noCursorTimeout == true) {
    self.addCursorFlag('noCursorTimeout', true);
  }

  // Set the sort value
  this.sortValue = self.s.cmd.sort;

  // Get the batchSize
  var batchSize = cmd.cursor && cmd.cursor.batchSize
    ? cmd.cursor && cmd.cursor.batchSize
    : (options.cursor && options.cursor.batchSize ? options.cursor.batchSize : 1000);

  // Set the batchSize
  this.setCursorBatchSize(batchSize);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.Cursor.prototype"></a>[module mongodb.Cursor.prototype](#apidoc.module.mongodb.Cursor.prototype)

#### <a name="apidoc.element.mongodb.Cursor.prototype._find"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>_find (callback)](#apidoc.element.mongodb.Cursor.prototype._find)
- description and source-code
```javascript
_find = function (callback) {
  var self = this;

  if(self.logger.isDebug()) {
    self.logger.debug(f('issue initial query [%s] with flags [%s]'
      , JSON.stringify(self.cmd)
      , JSON.stringify(self.query)));
  }

  var queryCallback = function(err, r) {
    if(err) return callback(err);

    // Get the raw message
    var result = r.message;

    // Query failure bit set
    if(result.queryFailure) {
      return callback(MongoError.create(result.documents[0]), null);
    }

    // Check if we have a command cursor
    if(Array.isArray(result.documents) && result.documents.length == 1
      && (!self.cmd.find || (self.cmd.find && self.cmd.virtual == false))
      && (result.documents[0].cursor != 'string'
        || result.documents[0]['$err']
        || result.documents[0]['errmsg']
        || Array.isArray(result.documents[0].result))
      ) {

      // We have a an error document return the error
      if(result.documents[0]['$err']
        || result.documents[0]['errmsg']) {
        return callback(MongoError.create(result.documents[0]), null);
      }

      // We have a cursor document
      if(result.documents[0].cursor != null
        && typeof result.documents[0].cursor != 'string') {
          var id = result.documents[0].cursor.id;
          // If we have a namespace change set the new namespace for getmores
          if(result.documents[0].cursor.ns) {
            self.ns = result.documents[0].cursor.ns;
          }
          // Promote id to long if needed
          self.cursorState.cursorId = typeof id == 'number' ? Long.fromNumber(id) : id;
          self.cursorState.lastCursorId = self.cursorState.cursorId;
          // If we have a firstBatch set it
          if(Array.isArray(result.documents[0].cursor.firstBatch)) {
            self.cursorState.documents = result.documents[0].cursor.firstBatch;//.reverse();
          }

          // Return after processing command cursor
          return callback(null, null);
      }

      if(Array.isArray(result.documents[0].result)) {
        self.cursorState.documents = result.documents[0].result;
        self.cursorState.cursorId = Long.ZERO;
        return callback(null, null);
      }
    }

    // Otherwise fall back to regular find path
    self.cursorState.cursorId = result.cursorId;
    self.cursorState.documents = result.documents;
    self.cursorState.lastCursorId = result.cursorId;

    // Transform the results with passed in transformation method if provided
    if(self.cursorState.transforms && typeof self.cursorState.transforms.query == 'function') {
      self.cursorState.documents = self.cursorState.transforms.query(result);
    }

    // Return callback
    callback(null, null);
  }

  // Options passed to the pool
  var queryOptions = {};

  // If we have a raw query decorate the function
  if(self.options.raw || self.cmd.raw) {
    // queryCallback.raw = self.options.raw || self.cmd.raw;
    queryOptions.raw = self.options.raw || self.cmd.raw;
  }

  // Do we have documentsReturnedIn set on the query
  if(typeof self.query.documentsReturnedIn == 'string') {
    // queryCallback.documentsReturnedIn = self.query.documentsReturnedIn;
    queryOptions.documentsReturnedIn = self.query.documentsReturnedIn;
  }

  // Add promote Long value if defined
  if(typeof self.cursorState.promoteLongs == 'boolean') {
    queryOptions.promoteLongs = self.cursorState.promoteLongs;
  }

  // Add promote values if defined
  if(typeof self.cursorState.promoteValues == 'boolean') {
    queryOptions.promoteValues = self.cursorState.promoteValues;
  }

  // Add promote values if defined
  if(typeof self.cursorState.promoteBuffers == 'boolean') {
    queryOptions.promoteBuffers = self.cursorState.promoteBuffers;
  }
  // Write the initial command out
  self.server.s.pool.write(self.query, queryOptions, queryCallback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype._getmore"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>_getmore (callback)](#apidoc.element.mongodb.Cursor.prototype._getmore)
- description and source-code
```javascript
_getmore = function (callback) {
  if(this.logger.isDebug()) this.logger.debug(f('schedule getMore call for query [%s]', JSON.stringify(this.query)))
  // Determine if it's a raw query
  var raw = this.options.raw || this.cmd.raw;

  // Set the current batchSize
  var batchSize = this.cursorState.batchSize;
  if(this.cursorState.limit > 0
    && ((this.cursorState.currentLimit + batchSize) > this.cursorState.limit)) {
    batchSize = this.cursorState.limit - this.cursorState.currentLimit;
  }

  // Default pool
  var pool = this.server.s.pool;

  // We have a wire protocol handler
  this.server.wireProtocolHandler.getMore(this.bson, this.ns, this.cursorState, batchSize, raw, pool, this.options, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype._killcursor"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>_killcursor (callback)](#apidoc.element.mongodb.Cursor.prototype._killcursor)
- description and source-code
```javascript
_killcursor = function (callback) {
  // Set cursor to dead
  this.cursorState.dead = true;
  this.cursorState.killed = true;
  // Remove documents
  this.cursorState.documents = [];

  // If no cursor id just return
  if(this.cursorState.cursorId == null || this.cursorState.cursorId.isZero() || this.cursorState.init == false) {
    if(callback) callback(null, null);
    return;
  }

  // Default pool
  var pool = this.server.s.pool;
  // Execute command
  this.server.wireProtocolHandler.killCursor(this.bson, this.ns, this.cursorState.cursorId, pool, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype._next"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>_next (callback)](#apidoc.element.mongodb.Cursor.prototype._next)
- description and source-code
```javascript
_next = function (callback) {
  nextFunction(this, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype._read"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>_read ()](#apidoc.element.mongodb.Cursor.prototype._read)
- description and source-code
```javascript
_read = function () {
  var self = this;
  if(self.s.state == Cursor.CLOSED || self.isDead()) {
    return self.push(null);
  }

  // Get the next item
  self.nextObject(function(err, result) {
    if(err) {
      if(self.listeners('error') && self.listeners('error').length > 0) {
        self.emit('error', err);
      }
      if(!self.isDead()) self.close();

      // Emit end event
      self.emit('end');
      return self.emit('finish');
    }

    // If we provided a transformation method
    if(typeof self.s.streamOptions.transform == 'function' && result != null) {
      return self.push(self.s.streamOptions.transform(result));
    }

    // If we provided a map function
    if(self.cursorState.transforms && typeof self.cursorState.transforms.doc == 'function' && result != null) {
      return self.push(self.cursorState.transforms.doc(result));
    }

    // Return the result
    self.push(result);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.addCursorFlag"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>addCursorFlag (flag, value)](#apidoc.element.mongodb.Cursor.prototype.addCursorFlag)
- description and source-code
```javascript
addCursorFlag = function (flag, value) {
  if(this.s.state == Cursor.CLOSED || this.s.state == Cursor.OPEN || this.isDead()) throw MongoError.create({message: "Cursor is
 closed", driver:true});
  if(flags.indexOf(flag) == -1) throw MongoError.create({message: f("flag %s not a supported flag %s", flag, flags), driver:true
 });
  if(typeof value != 'boolean') throw MongoError.create({message: f("flag %s must be a boolean value", flag), driver:true});
  this.s.cmd[flag] = value;
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.addQueryModifier"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>addQueryModifier (name, value)](#apidoc.element.mongodb.Cursor.prototype.addQueryModifier)
- description and source-code
```javascript
addQueryModifier = function (name, value) {
  if(this.s.state == Cursor.CLOSED || this.s.state == Cursor.OPEN || this.isDead()) throw MongoError.create({message: "Cursor is
 closed", driver:true});
  if(name[0] != '$') throw MongoError.create({message: f("%s is not a valid query modifier"), driver:true});
  // Strip of the $
  var field = name.substr(1);
  // Set on the command
  this.s.cmd[field] = value;
  // Deal with the special case for sort
  if(field == 'orderby') this.s.cmd.sort = this.s.cmd[field];
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.batchSize"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>batchSize (value)](#apidoc.element.mongodb.Cursor.prototype.batchSize)
- description and source-code
```javascript
batchSize = function (value) {
  if(this.s.options.tailable) throw MongoError.create({message: "Tailable cursor doesn't support batchSize", driver:true});
  if(this.s.state == Cursor.CLOSED || this.isDead()) throw MongoError.create({message: "Cursor is closed", driver:true});
  if(typeof value != 'number') throw MongoError.create({message: "batchSize requires an integer", driver:true});
  this.s.cmd.batchSize = value;
  this.setCursorBatchSize(value);
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.bufferedCount"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>bufferedCount ()](#apidoc.element.mongodb.Cursor.prototype.bufferedCount)
- description and source-code
```javascript
bufferedCount = function () {
  return this.cursorState.documents.length - this.cursorState.cursorIndex;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.clone"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>clone ()](#apidoc.element.mongodb.Cursor.prototype.clone)
- description and source-code
```javascript
clone = function () {
  return this.topology.cursor(this.ns, this.cmd, this.options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.close"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>close (callback)](#apidoc.element.mongodb.Cursor.prototype.close)
- description and source-code
```javascript
close = function (callback) {
  this.s.state = Cursor.CLOSED;
  // Kill the cursor
  this.kill();
  // Emit the close event for the cursor
  this.emit('close');
  // Callback if provided
  if(typeof callback == 'function') return handleCallback(callback, null, this);
  // Return a Promise
  return new this.s.promiseLibrary(function(resolve) {
    resolve();
  });
}
```
- example usage
```shell
...
// Connection URL
var url = 'mongodb://localhost:27017/myproject';
// Use connect method to connect to the Server
MongoClient.connect(url, function(err, db) {
  assert.equal(null, err);
  console.log("Connected correctly to server");

  db.close();
});
'''

Given that you booted up the **mongod** process earlier the application should connect successfully and print **Connected correctly
 to server** to the console.

Let's Add some code to show the different CRUD operations available.
...
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.collation"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>collation (value)](#apidoc.element.mongodb.Cursor.prototype.collation)
- description and source-code
```javascript
collation = function (value) {
  this.s.cmd.collation = value;
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.comment"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>comment (value)](#apidoc.element.mongodb.Cursor.prototype.comment)
- description and source-code
```javascript
comment = function (value) {
  if(this.s.state == Cursor.CLOSED || this.s.state == Cursor.OPEN || this.isDead()) throw MongoError.create({message: "Cursor is
 closed", driver:true});
  this.s.cmd.comment = value;
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.count"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>count (applySkipLimit, opts, callback)](#apidoc.element.mongodb.Cursor.prototype.count)
- description and source-code
```javascript
count = function (applySkipLimit, opts, callback) {
  var self = this;
  if(self.s.cmd.query == null) throw MongoError.create({message: "count can only be used with find command", driver:true});
  if(typeof opts == 'function') callback = opts, opts = {};
  opts = opts || {};

  // Execute using callback
  if(typeof callback == 'function') return count(self, applySkipLimit, opts, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    count(self, applySkipLimit, opts, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.cursorBatchSize"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>cursorBatchSize ()](#apidoc.element.mongodb.Cursor.prototype.cursorBatchSize)
- description and source-code
```javascript
cursorBatchSize = function () {
  return this.cursorState.batchSize;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.cursorLimit"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>cursorLimit ()](#apidoc.element.mongodb.Cursor.prototype.cursorLimit)
- description and source-code
```javascript
cursorLimit = function () {
  return this.cursorState.limit;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.cursorSkip"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>cursorSkip ()](#apidoc.element.mongodb.Cursor.prototype.cursorSkip)
- description and source-code
```javascript
cursorSkip = function () {
  return this.cursorState.skip;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.destroy"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>destroy (err)](#apidoc.element.mongodb.Cursor.prototype.destroy)
- description and source-code
```javascript
destroy = function (err) {
  if(err) this.emit('error', err);
  this.pause();
  this.close();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.each"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>each (callback)](#apidoc.element.mongodb.Cursor.prototype.each)
- description and source-code
```javascript
each = function (callback) {
  // Rewind cursor state
  this.rewind();
  // Set current cursor to INIT
  this.s.state = Cursor.INIT;
  // Run the query
  _each(this, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.explain"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>explain (callback)](#apidoc.element.mongodb.Cursor.prototype.explain)
- description and source-code
```javascript
explain = function (callback) {
  var self = this;
  this.s.cmd.explain = true;

  // Do we have a readConcern
  if(this.s.cmd.readConcern) {
    delete this.s.cmd['readConcern'];
  }

  // Execute using callback
  if(typeof callback == 'function') return this._next(callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    self._next(function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.filter"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>filter (filter)](#apidoc.element.mongodb.Cursor.prototype.filter)
- description and source-code
```javascript
filter = function (filter) {
  if(this.s.state == Cursor.CLOSED || this.s.state == Cursor.OPEN || this.isDead()) throw MongoError.create({message: "Cursor is
 closed", driver:true});
  this.s.cmd.query = filter;
  return this;
}
```
- example usage
```shell
...

    // No entry returned for duplicate servr
    if(deduplicatedServers[_host + "_" + _port]) return null;
    deduplicatedServers[_host + "_" + _port] = 1;

    // Return the mapped object
    return {host: _host, port: _port};
  }).filter(function(x) {
    return x != null;
  });
}

// Get the db name
object.dbName = dbName || 'admin';
// Split up all the options
...
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.forEach"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>forEach (iterator, callback)](#apidoc.element.mongodb.Cursor.prototype.forEach)
- description and source-code
```javascript
forEach = function (iterator, callback) {
  this.each(function(err, doc){
    if(err) { callback(err); return false; }
    if(doc != null) { iterator(doc); return true; }
    if(doc == null && callback) {
      var internalCallback = callback;
      callback = null;
      internalCallback(null);
      return false;
    }
  });
}
```
- example usage
```shell
...
  // Reference
  var self = this;
  // Names of methods we need to wrap
  var methods = ['command', 'insert', 'update', 'remove'];
  // Prototype
  var proto = core.Server.prototype;
  // Core server method we are going to wrap
  methods.forEach(function(x) {
var func = proto[x];

// Add to overloaded methods
self.overloads.push({proto: proto, name:x, func:func});

// The actual prototype
proto[x] = function() {
...
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.hasNext"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>hasNext (callback)](#apidoc.element.mongodb.Cursor.prototype.hasNext)
- description and source-code
```javascript
hasNext = function (callback) {
  var self = this;

  // Execute using callback
  if(typeof callback == 'function') {
    if(self.s.currentDoc){
      return callback(null, true);
    } else {
      return nextObject(self, function(err, doc) {
        if(!doc) return callback(null, false);
        self.s.currentDoc = doc;
        callback(null, true);
      });
    }
  }

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    if(self.s.currentDoc){
      resolve(true);
    } else {
      nextObject(self, function(err, doc) {
        if(self.s.state == Cursor.CLOSED || self.isDead()) return resolve(false);
        if(err) return reject(err);
        if(!doc) return resolve(false);
        self.s.currentDoc = doc;
        resolve(true);
      });
    }
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.hint"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>hint (hint)](#apidoc.element.mongodb.Cursor.prototype.hint)
- description and source-code
```javascript
hint = function (hint) {
  if(this.s.state == Cursor.CLOSED || this.s.state == Cursor.OPEN || this.isDead()) throw MongoError.create({message: "Cursor is
 closed", driver:true});
  this.s.cmd.hint = hint;
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.isClosed"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>isClosed ()](#apidoc.element.mongodb.Cursor.prototype.isClosed)
- description and source-code
```javascript
isClosed = function () {
  return this.isDead();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.isDead"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>isDead ()](#apidoc.element.mongodb.Cursor.prototype.isDead)
- description and source-code
```javascript
isDead = function () {
  return this.cursorState.dead == true;
}
```
- example usage
```shell
...
 * Set the batch size for the cursor.
 * @method
 * @param {number} value The batchSize for the cursor.
 * @throws {MongoError}
 * @return {AggregationCursor}
 */
AggregationCursor.prototype.batchSize = function(value) {
  if(this.s.state == AggregationCursor.CLOSED || this.isDead()) throw MongoError.create({message: "Cursor is closed", driver:true
 });
  if(typeof value != 'number') throw MongoError.create({message: "batchSize requires an integer", drvier:true });
  if(this.s.cmd.cursor) this.s.cmd.cursor.batchSize = value;
  this.setCursorBatchSize(value);
  return this;
}

define.classMethod('batchSize', {callback: false, promise:false, returns: [AggregationCursor]});
...
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.isKilled"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>isKilled ()](#apidoc.element.mongodb.Cursor.prototype.isKilled)
- description and source-code
```javascript
isKilled = function () {
  return this.cursorState.killed == true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.isNotified"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>isNotified ()](#apidoc.element.mongodb.Cursor.prototype.isNotified)
- description and source-code
```javascript
isNotified = function () {
  return this.cursorState.notified == true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.kill"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>kill (callback)](#apidoc.element.mongodb.Cursor.prototype.kill)
- description and source-code
```javascript
kill = function (callback) {
  this._killcursor(callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.limit"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>limit (value)](#apidoc.element.mongodb.Cursor.prototype.limit)
- description and source-code
```javascript
limit = function (value) {
  if(this.s.options.tailable) throw MongoError.create({message: "Tailable cursor doesn't support limit", driver:true});
  if(this.s.state == Cursor.OPEN || this.s.state == Cursor.CLOSED || this.isDead()) throw MongoError.create({message: "Cursor is
 closed", driver:true});
  if(typeof value != 'number') throw MongoError.create({message: "limit requires an integer", driver:true});
  this.s.cmd.limit = value;
  // this.cursorLimit = value;
  this.setCursorLimit(value);
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.map"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>map (transform)](#apidoc.element.mongodb.Cursor.prototype.map)
- description and source-code
```javascript
map = function (transform) {
  this.cursorState.transforms = { doc: transform };
  return this;
}
```
- example usage
```shell
...
  } else {
// Split up the db
hostPart = connection_part;
// Deduplicate servers
var deduplicatedServers = {};

// Parse all server results
servers = hostPart.split(',').map(function(h) {
  var _host, _port, ipv6match;
  //check if it matches [IPv6]:port, where the port number is optional
  if ((ipv6match = /\[([^\]]+)\](?:\:(.+))?/.exec(h))) {
    _host = ipv6match[1];
    _port = parseInt(ipv6match[2], 10) || 27017;
  } else {
    //otherwise assume it's IPv4, or plain hostname
...
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.max"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>max (max)](#apidoc.element.mongodb.Cursor.prototype.max)
- description and source-code
```javascript
max = function (max) {
  if(this.s.state == Cursor.CLOSED || this.s.state == Cursor.OPEN || this.isDead()) throw MongoError.create({message: "Cursor is
 closed", driver:true});
  this.s.cmd.max = max;
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.maxAwaitTimeMS"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>maxAwaitTimeMS (value)](#apidoc.element.mongodb.Cursor.prototype.maxAwaitTimeMS)
- description and source-code
```javascript
maxAwaitTimeMS = function (value) {
  if(typeof value != 'number') throw MongoError.create({message: "maxAwaitTimeMS must be a number", driver:true});
  if(this.s.state == Cursor.CLOSED || this.s.state == Cursor.OPEN || this.isDead()) throw MongoError.create({message: "Cursor is
 closed", driver:true});
  this.s.cmd.maxAwaitTimeMS = value;
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.maxScan"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>maxScan (maxScan)](#apidoc.element.mongodb.Cursor.prototype.maxScan)
- description and source-code
```javascript
maxScan = function (maxScan) {
  if(this.s.state == Cursor.CLOSED || this.s.state == Cursor.OPEN || this.isDead()) throw MongoError.create({message: "Cursor is
 closed", driver:true});
  this.s.cmd.maxScan = maxScan;
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.maxTimeMS"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>maxTimeMS (value)](#apidoc.element.mongodb.Cursor.prototype.maxTimeMS)
- description and source-code
```javascript
maxTimeMS = function (value) {
  if(typeof value != 'number') throw MongoError.create({message: "maxTimeMS must be a number", driver:true});
  if(this.s.state == Cursor.CLOSED || this.s.state == Cursor.OPEN || this.isDead()) throw MongoError.create({message: "Cursor is
 closed", driver:true});
  this.s.cmd.maxTimeMS = value;
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.maxTimeMs"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>maxTimeMs (value)](#apidoc.element.mongodb.Cursor.prototype.maxTimeMs)
- description and source-code
```javascript
maxTimeMs = function (value) {
  if(typeof value != 'number') throw MongoError.create({message: "maxTimeMS must be a number", driver:true});
  if(this.s.state == Cursor.CLOSED || this.s.state == Cursor.OPEN || this.isDead()) throw MongoError.create({message: "Cursor is
 closed", driver:true});
  this.s.cmd.maxTimeMS = value;
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.min"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>min (min)](#apidoc.element.mongodb.Cursor.prototype.min)
- description and source-code
```javascript
min = function (min) {
  if(this.s.state == Cursor.CLOSED || this.s.state == Cursor.OPEN || this.isDead()) throw MongoError.create({message: "Cursor is
 closed", driver:true});
  this.s.cmd.min = min;
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.next"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>next (callback)](#apidoc.element.mongodb.Cursor.prototype.next)
- description and source-code
```javascript
next = function (callback) {
  var self = this;

  // Execute using callback
  if(typeof callback == 'function') {
    // Return the currentDoc if someone called hasNext first
    if(self.s.currentDoc) {
      var doc = self.s.currentDoc;
      self.s.currentDoc = null;
      return callback(null, doc);
    }

    // Return the next object
    return nextObject(self, callback)
  }

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    // Return the currentDoc if someone called hasNext first
    if(self.s.currentDoc) {
      var doc = self.s.currentDoc;
      self.s.currentDoc = null;
      return resolve(doc);
    }

    nextObject(self, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
...
  commandObj.ordered = options.ordered != undefined ? options.ordered : true;
}

// Get the callback
var callback = args.pop();
// Set current callback operation id from the current context or create
// a new one
var ourOpId = callback.operationId || operationIdGenerator.next();

// Get a connection reference for this server instance
var connection = this.s.pool.get()

// Emit the start event for the command
var command = {
  // Returns the command.
...
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.nextObject"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>nextObject (callback)](#apidoc.element.mongodb.Cursor.prototype.nextObject)
- description and source-code
```javascript
nextObject = function (callback) {
  var self = this;

  // Execute using callback
  if(typeof callback == 'function') {
    // Return the currentDoc if someone called hasNext first
    if(self.s.currentDoc) {
      var doc = self.s.currentDoc;
      self.s.currentDoc = null;
      return callback(null, doc);
    }

    // Return the next object
    return nextObject(self, callback)
  }

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    // Return the currentDoc if someone called hasNext first
    if(self.s.currentDoc) {
      var doc = self.s.currentDoc;
      self.s.currentDoc = null;
      return resolve(doc);
    }

    nextObject(self, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.project"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>project (value)](#apidoc.element.mongodb.Cursor.prototype.project)
- description and source-code
```javascript
project = function (value) {
  if(this.s.state == Cursor.CLOSED || this.s.state == Cursor.OPEN || this.isDead()) throw MongoError.create({message: "Cursor is
 closed", driver:true});
  this.s.cmd.fields = value;
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.readBufferedDocuments"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>readBufferedDocuments (number)](#apidoc.element.mongodb.Cursor.prototype.readBufferedDocuments)
- description and source-code
```javascript
readBufferedDocuments = function (number) {
  var unreadDocumentsLength = this.cursorState.documents.length - this.cursorState.cursorIndex;
  var length = number < unreadDocumentsLength ? number : unreadDocumentsLength;
  var elements = this.cursorState.documents.slice(this.cursorState.cursorIndex, this.cursorState.cursorIndex + length);

  // Transform the doc with passed in transformation method if provided
  if(this.cursorState.transforms && typeof this.cursorState.transforms.doc == 'function') {
    // Transform all the elements
    for(var i = 0; i < elements.length; i++) {
      elements[i] = this.cursorState.transforms.doc(elements[i]);
    }
  }

  // Ensure we do not return any more documents than the limit imposed
  // Just return the number of elements up to the limit
  if(this.cursorState.limit > 0 && (this.cursorState.currentLimit + elements.length) > this.cursorState.limit) {
    elements = elements.slice(0, (this.cursorState.limit - this.cursorState.currentLimit));
    this.kill();
  }

  // Adjust current limit
  this.cursorState.currentLimit = this.cursorState.currentLimit + elements.length;
  this.cursorState.cursorIndex = this.cursorState.cursorIndex + elements.length;

  // Return elements
  return elements;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.returnKey"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>returnKey (value)](#apidoc.element.mongodb.Cursor.prototype.returnKey)
- description and source-code
```javascript
returnKey = function (value) {
  if(this.s.state == Cursor.CLOSED || this.s.state == Cursor.OPEN || this.isDead()) throw MongoError.create({message: "Cursor is
 closed", driver:true});
  this.s.cmd.returnKey = value;
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.rewind"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>rewind ()](#apidoc.element.mongodb.Cursor.prototype.rewind)
- description and source-code
```javascript
rewind = function () {
  if(this.cursorState.init) {
    if(!this.cursorState.dead) {
      this.kill();
    }

    this.cursorState.currentLimit = 0;
    this.cursorState.init = false;
    this.cursorState.dead = false;
    this.cursorState.killed = false;
    this.cursorState.notified = false;
    this.cursorState.documents = [];
    this.cursorState.cursorId = null;
    this.cursorState.cursorIndex = 0;
  }
}
```
- example usage
```shell
...
 * @param {object[]} documents All the documents the satisfy the cursor.
 */

/**
 * Returns an array of documents. The caller is responsible for making sure that there
 * is enough memory to store the results. Note that the array only contain partial
 * results when this cursor had been previouly accessed. In that case,
 * cursor.rewind() can be used to reset the cursor.
 * @method AggregationCursor.prototype.toArray
 * @param {AggregationCursor~toArrayResultCallback} [callback] The result callback.
 * @throws {MongoError}
 * @return {Promise} returns Promise if no callback passed
 */

/**
...
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.setCursorBatchSize"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>setCursorBatchSize (value)](#apidoc.element.mongodb.Cursor.prototype.setCursorBatchSize)
- description and source-code
```javascript
setCursorBatchSize = function (value) {
  this.cursorState.batchSize = value;
}
```
- example usage
```shell
...
* @throws {MongoError}
* @return {AggregationCursor}
*/
AggregationCursor.prototype.batchSize = function(value) {
 if(this.s.state == AggregationCursor.CLOSED || this.isDead()) throw MongoError.create({message: "Cursor is closed", driver:true
 });
 if(typeof value != 'number') throw MongoError.create({message: "batchSize requires an integer", drvier:true });
 if(this.s.cmd.cursor) this.s.cmd.cursor.batchSize = value;
 this.setCursorBatchSize(value);
 return this;
}

define.classMethod('batchSize', {callback: false, promise:false, returns: [AggregationCursor]});

/**
* Add a geoNear stage to the aggregation pipeline
...
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.setCursorLimit"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>setCursorLimit (value)](#apidoc.element.mongodb.Cursor.prototype.setCursorLimit)
- description and source-code
```javascript
setCursorLimit = function (value) {
  this.cursorState.limit = value;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.setCursorOption"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>setCursorOption (field, value)](#apidoc.element.mongodb.Cursor.prototype.setCursorOption)
- description and source-code
```javascript
setCursorOption = function (field, value) {
  if(this.s.state == Cursor.CLOSED || this.s.state == Cursor.OPEN || this.isDead()) throw MongoError.create({message: "Cursor is
 closed", driver:true});
  if(fields.indexOf(field) == -1) throw MongoError.create({message: f("option %s not a supported option %s", field, fields), driver
:true });
  this.s[field] = value;
  if(field == 'numberOfRetries')
    this.s.currentNumberOfRetries = value;
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.setCursorSkip"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>setCursorSkip (value)](#apidoc.element.mongodb.Cursor.prototype.setCursorSkip)
- description and source-code
```javascript
setCursorSkip = function (value) {
  this.cursorState.skip = value;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.setReadPreference"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>setReadPreference (r)](#apidoc.element.mongodb.Cursor.prototype.setReadPreference)
- description and source-code
```javascript
setReadPreference = function (r) {
  if(this.s.state != Cursor.INIT) throw MongoError.create({message: 'cannot change cursor readPreference after cursor has been accessed
', driver:true});
  if(r instanceof ReadPreference) {
    this.s.options.readPreference = new CoreReadPreference(r.mode, r.tags, {maxStalenessSeconds: r.maxStalenessSeconds});
  } else if(typeof r == 'string'){
    this.s.options.readPreference = new CoreReadPreference(r);
  } else if(r instanceof CoreReadPreference) {
    this.s.options.readPreference = r;
  }

  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.showRecordId"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>showRecordId (value)](#apidoc.element.mongodb.Cursor.prototype.showRecordId)
- description and source-code
```javascript
showRecordId = function (value) {
  if(this.s.state == Cursor.CLOSED || this.s.state == Cursor.OPEN || this.isDead()) throw MongoError.create({message: "Cursor is
 closed", driver:true});
  this.s.cmd.showDiskLoc = value;
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.skip"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>skip (value)](#apidoc.element.mongodb.Cursor.prototype.skip)
- description and source-code
```javascript
skip = function (value) {
  if(this.s.options.tailable) throw MongoError.create({message: "Tailable cursor doesn't support skip", driver:true});
  if(this.s.state == Cursor.OPEN || this.s.state == Cursor.CLOSED || this.isDead()) throw MongoError.create({message: "Cursor is
 closed", driver:true});
  if(typeof value != 'number') throw MongoError.create({message: "skip requires an integer", driver:true});
  this.s.cmd.skip = value;
  this.setCursorSkip(value);
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.snapshot"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>snapshot (value)](#apidoc.element.mongodb.Cursor.prototype.snapshot)
- description and source-code
```javascript
snapshot = function (value) {
  if(this.s.state == Cursor.CLOSED || this.s.state == Cursor.OPEN || this.isDead()) throw MongoError.create({message: "Cursor is
 closed", driver:true});
  this.s.cmd.snapshot = value;
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.sort"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>sort (keyOrList, direction)](#apidoc.element.mongodb.Cursor.prototype.sort)
- description and source-code
```javascript
sort = function (keyOrList, direction) {
  if(this.s.options.tailable) throw MongoError.create({message: "Tailable cursor doesn't support sorting", driver:true});
  if(this.s.state == Cursor.CLOSED || this.s.state == Cursor.OPEN || this.isDead()) throw MongoError.create({message: "Cursor is
 closed", driver:true});
  var order = keyOrList;

  // We have an array of arrays, we need to preserve the order of the sort
  // so we will us a Map
  if(Array.isArray(order) && Array.isArray(order[0])) {
    order = new Map(order.map(function(x) {
      var value = [x[0], null];
      if(x[1] == 'asc') {
        value[1] = 1;
      } else if(x[1] == 'desc') {
        value[1] = -1;
      } else if(x[1] == 1 || x[1] == -1) {
        value[1] = x[1];
      } else {
        throw new MongoError("Illegal sort clause, must be of the form [['field1', '(ascending|descending)'], ['field2', '(ascending
|descending)']]");
      }

      return value;
    }));
  }

  if(direction != null) {
    order = [[keyOrList, direction]];
  }

  this.s.cmd.sort = order;
  this.sortValue = order;
  return this;
}
```
- example usage
```shell
...
this.name = name;
this.object = object;
this.stream = typeof stream == 'boolean' ? stream : false;
this.instrumentations = {};
}

Define.prototype.classMethod = function(name, options) {
var keys = Object.keys(options).sort();
var key = generateKey(keys, options);

// Add a list of instrumentations
if(this.instrumentations[key] == null) {
  this.instrumentations[key] = {
    methods: [], options: options
  }
...
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.stream"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>stream (options)](#apidoc.element.mongodb.Cursor.prototype.stream)
- description and source-code
```javascript
stream = function (options) {
  this.s.streamOptions = options || {};
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Cursor.prototype.toArray"></a>[function <span class="apidocSignatureSpan">mongodb.Cursor.prototype.</span>toArray (callback)](#apidoc.element.mongodb.Cursor.prototype.toArray)
- description and source-code
```javascript
toArray = function (callback) {
  var self = this;
  if(self.s.options.tailable) throw MongoError.create({message: 'Tailable cursor cannot be converted to array', driver:true});

  // Execute using callback
  if(typeof callback == 'function') return toArray(self, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    toArray(self, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
...
We will finish up the Quickstart CRUD methods by performing a simple query that returns all the documents matching the query.

'''js
var findDocuments = function(db, callback) {
  // Get the documents collection
  var collection = db.collection('documents');
  // Find some documents
  collection.find({}).toArray(function(err, docs) {
    assert.equal(err, null);
    assert.equal(2, docs.length);
    console.log("Found the following records");
    console.dir(docs);
    callback(docs);
  });
}
...
```



# <a name="apidoc.module.mongodb.DBRef"></a>[module mongodb.DBRef](#apidoc.module.mongodb.DBRef)

#### <a name="apidoc.element.mongodb.DBRef.DBRef"></a>[function <span class="apidocSignatureSpan">mongodb.</span>DBRef (namespace, oid, db)](#apidoc.element.mongodb.DBRef.DBRef)
- description and source-code
```javascript
function DBRef(namespace, oid, db) {
  if(!(this instanceof DBRef)) return new DBRef(namespace, oid, db);

  this._bsontype = 'DBRef';
  this.namespace = namespace;
  this.oid = oid;
  this.db = db;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.DBRef.prototype"></a>[module mongodb.DBRef.prototype](#apidoc.module.mongodb.DBRef.prototype)

#### <a name="apidoc.element.mongodb.DBRef.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">mongodb.DBRef.prototype.</span>toJSON ()](#apidoc.element.mongodb.DBRef.prototype.toJSON)
- description and source-code
```javascript
toJSON = function () {
  return {
    '$ref':this.namespace,
    '$id':this.oid,
    '$db':this.db == null ? '' : this.db
  };
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.Db"></a>[module mongodb.Db](#apidoc.module.mongodb.Db)

#### <a name="apidoc.element.mongodb.Db.Db"></a>[function <span class="apidocSignatureSpan">mongodb.</span>Db (databaseName, topology, options)](#apidoc.element.mongodb.Db.Db)
- description and source-code
```javascript
Db = function (databaseName, topology, options) {
  options = options || {};
  if(!(this instanceof Db)) return new Db(databaseName, topology, options);
  EventEmitter.call(this);
  var self = this;

  // Get the promiseLibrary
  var promiseLibrary = options.promiseLibrary;

  // No promise library selected fall back
  if(!promiseLibrary) {
    promiseLibrary = typeof global.Promise == 'function' ?
      global.Promise : require('es6-promise').Promise;
  }

  // Filter the options
  options = filterOptions(options, legalOptionNames);

  // Ensure we put the promiseLib in the options
  options.promiseLibrary = promiseLibrary;

  // var self = this;  // Internal state of the db object
  this.s = {
    // Database name
      databaseName: databaseName
    // DbCache
    , dbCache: {}
    // Children db's
    , children: []
    // Topology
    , topology: topology
    // Options
    , options: options
    // Logger instance
    , logger: Logger('Db', options)
    // Get the bson parser
    , bson: topology ? topology.bson : null
    // Authsource if any
    , authSource: options.authSource
    // Unpack read preference
    , readPreference: options.readPreference
    // Set buffermaxEntries
    , bufferMaxEntries: typeof options.bufferMaxEntries == 'number' ? options.bufferMaxEntries : -1
    // Parent db (if chained)
    , parentDb: options.parentDb || null
    // Set up the primary key factory or fallback to ObjectID
    , pkFactory: options.pkFactory || ObjectID
    // Get native parser
    , nativeParser: options.nativeParser || options.native_parser
    // Promise library
    , promiseLibrary: promiseLibrary
    // No listener
    , noListener: typeof options.noListener == 'boolean' ? options.noListener : false
    // ReadConcern
    , readConcern: options.readConcern
  }

  // Ensure we have a valid db name
  validateDatabaseName(self.s.databaseName);

  // Add a read Only property
  getSingleProperty(this, 'serverConfig', self.s.topology);
  getSingleProperty(this, 'bufferMaxEntries', self.s.bufferMaxEntries);
  getSingleProperty(this, 'databaseName', self.s.databaseName);

  // This is a child db, do not register any listeners
  if(options.parentDb) return;
  if(this.s.noListener) return;

  // Add listeners
  topology.on('error', createListener(self, 'error', self));
  topology.on('timeout', createListener(self, 'timeout', self));
  topology.on('close', createListener(self, 'close', self));
  topology.on('parseError', createListener(self, 'parseError', self));
  topology.once('open', createListener(self, 'open', self));
  topology.once('fullsetup', createListener(self, 'fullsetup', self));
  topology.once('all', createListener(self, 'all', self));
  topology.on('reconnect', createListener(self, 'reconnect', self));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Db.super_"></a>[function <span class="apidocSignatureSpan">mongodb.Db.</span>super_ ()](#apidoc.element.mongodb.Db.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.Db.define"></a>[module mongodb.Db.define](#apidoc.module.mongodb.Db.define)

#### <a name="apidoc.element.mongodb.Db.define.object"></a>[function <span class="apidocSignatureSpan">mongodb.Db.define.</span>object (databaseName, topology, options)](#apidoc.element.mongodb.Db.define.object)
- description and source-code
```javascript
object = function (databaseName, topology, options) {
  options = options || {};
  if(!(this instanceof Db)) return new Db(databaseName, topology, options);
  EventEmitter.call(this);
  var self = this;

  // Get the promiseLibrary
  var promiseLibrary = options.promiseLibrary;

  // No promise library selected fall back
  if(!promiseLibrary) {
    promiseLibrary = typeof global.Promise == 'function' ?
      global.Promise : require('es6-promise').Promise;
  }

  // Filter the options
  options = filterOptions(options, legalOptionNames);

  // Ensure we put the promiseLib in the options
  options.promiseLibrary = promiseLibrary;

  // var self = this;  // Internal state of the db object
  this.s = {
    // Database name
      databaseName: databaseName
    // DbCache
    , dbCache: {}
    // Children db's
    , children: []
    // Topology
    , topology: topology
    // Options
    , options: options
    // Logger instance
    , logger: Logger('Db', options)
    // Get the bson parser
    , bson: topology ? topology.bson : null
    // Authsource if any
    , authSource: options.authSource
    // Unpack read preference
    , readPreference: options.readPreference
    // Set buffermaxEntries
    , bufferMaxEntries: typeof options.bufferMaxEntries == 'number' ? options.bufferMaxEntries : -1
    // Parent db (if chained)
    , parentDb: options.parentDb || null
    // Set up the primary key factory or fallback to ObjectID
    , pkFactory: options.pkFactory || ObjectID
    // Get native parser
    , nativeParser: options.nativeParser || options.native_parser
    // Promise library
    , promiseLibrary: promiseLibrary
    // No listener
    , noListener: typeof options.noListener == 'boolean' ? options.noListener : false
    // ReadConcern
    , readConcern: options.readConcern
  }

  // Ensure we have a valid db name
  validateDatabaseName(self.s.databaseName);

  // Add a read Only property
  getSingleProperty(this, 'serverConfig', self.s.topology);
  getSingleProperty(this, 'bufferMaxEntries', self.s.bufferMaxEntries);
  getSingleProperty(this, 'databaseName', self.s.databaseName);

  // This is a child db, do not register any listeners
  if(options.parentDb) return;
  if(this.s.noListener) return;

  // Add listeners
  topology.on('error', createListener(self, 'error', self));
  topology.on('timeout', createListener(self, 'timeout', self));
  topology.on('close', createListener(self, 'close', self));
  topology.on('parseError', createListener(self, 'parseError', self));
  topology.once('open', createListener(self, 'open', self));
  topology.once('fullsetup', createListener(self, 'fullsetup', self));
  topology.once('all', createListener(self, 'all', self));
  topology.on('reconnect', createListener(self, 'reconnect', self));
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.Db.prototype"></a>[module mongodb.Db.prototype](#apidoc.module.mongodb.Db.prototype)

#### <a name="apidoc.element.mongodb.Db.prototype.addChild"></a>[function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>addChild (db)](#apidoc.element.mongodb.Db.prototype.addChild)
- description and source-code
```javascript
addChild = function (db) {
  if(this.s.parentDb) return this.s.parentDb.addChild(db);
  this.s.children.push(db);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Db.prototype.addUser"></a>[function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>addUser (username, password, options, callback)](#apidoc.element.mongodb.Db.prototype.addUser)
- description and source-code
```javascript
addUser = function (username, password, options, callback) {
  // Unpack the parameters
  var self = this;
  var args = Array.prototype.slice.call(arguments, 2);
  callback = args.pop();
  if(typeof callback != 'function') args.push(callback);
  options = args.length ? args.shift() || {} : {};

  // If we have a callback fallback
  if(typeof callback == 'function') return addUser(self, username, password, options, callback);

  // Return a promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    addUser(self, username, password, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Db.prototype.admin"></a>[function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>admin ()](#apidoc.element.mongodb.Db.prototype.admin)
- description and source-code
```javascript
admin = function () {
  return new Admin(this, this.s.topology, this.s.promiseLibrary);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Db.prototype.authenticate"></a>[function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>authenticate (username, password, options, callback)](#apidoc.element.mongodb.Db.prototype.authenticate)
- description and source-code
```javascript
authenticate = function (username, password, options, callback) {
  if(typeof options == 'function') callback = options, options = {};
  var self = this;
  // Shallow copy the options
  options = shallowClone(options);

  // Set default mechanism
  if(!options.authMechanism) {
    options.authMechanism = 'DEFAULT';
  } else if(options.authMechanism != 'GSSAPI'
    && options.authMechanism != 'DEFAULT'
    && options.authMechanism != 'MONGODB-CR'
    && options.authMechanism != 'MONGODB-X509'
    && options.authMechanism != 'SCRAM-SHA-1'
    && options.authMechanism != 'PLAIN') {
      return handleCallback(callback, MongoError.create({message: "only DEFAULT, GSSAPI, PLAIN, MONGODB-X509, SCRAM-SHA-1 or MONGODB
-CR is supported by authMechanism", driver:true}));
  }

  // If we have a callback fallback
  if(typeof callback == 'function') return authenticate(self, username, password, options, function(err, r) {
    // Support failed auth method
    if(err && err.message && err.message.indexOf('saslStart') != -1) err.code = 59;
    // Reject error
    if(err) return callback(err, r);
    callback(null, r);
  });

  // Return a promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    authenticate(self, username, password, options, function(err, r) {
      // Support failed auth method
      if(err && err.message && err.message.indexOf('saslStart') != -1) err.code = 59;
      // Reject error
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Db.prototype.close"></a>[function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>close (force, callback)](#apidoc.element.mongodb.Db.prototype.close)
- description and source-code
```javascript
close = function (force, callback) {
  if(typeof force == 'function') callback = force, force = false;
  this.s.topology.close(force);
  var self = this;

  // Fire close event if any listeners
  if(this.listeners('close').length > 0) {
    this.emit('close');

    // If it's the top level db emit close on all children
    if(this.parentDb == null) {
      // Fire close on all children
      for(var i = 0; i < this.s.children.length; i++) {
        this.s.children[i].emit('close');
      }
    }

    // Remove listeners after emit
    self.removeAllListeners('close');
  }

  // Close parent db if set
  if(this.s.parentDb) this.s.parentDb.close();
  // Callback after next event loop tick
  if(typeof callback == 'function') return process.nextTick(function() {
    handleCallback(callback, null);
  })

  // Return dummy promise
  return new this.s.promiseLibrary(function(resolve) {
    resolve();
  });
}
```
- example usage
```shell
...
// Connection URL
var url = 'mongodb://localhost:27017/myproject';
// Use connect method to connect to the Server
MongoClient.connect(url, function(err, db) {
  assert.equal(null, err);
  console.log("Connected correctly to server");

  db.close();
});
'''

Given that you booted up the **mongod** process earlier the application should connect successfully and print **Connected correctly
 to server** to the console.

Let's Add some code to show the different CRUD operations available.
...
```

#### <a name="apidoc.element.mongodb.Db.prototype.collection"></a>[function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>collection (name, options, callback)](#apidoc.element.mongodb.Db.prototype.collection)
- description and source-code
```javascript
collection = function (name, options, callback) {
  var self = this;
  if(typeof options == 'function') callback = options, options = {};
  options = options || {};
  options = shallowClone(options);
  // Set the promise library
  options.promiseLibrary = this.s.promiseLibrary;

  // If we have not set a collection level readConcern set the db level one
  options.readConcern = options.readConcern || this.s.readConcern;

  // Do we have ignoreUndefined set
  if(this.s.options.ignoreUndefined) {
    options.ignoreUndefined = this.s.options.ignoreUndefined;
  }

  // Execute
  if(options == null || !options.strict) {
    try {
      var collection = new Collection(this, this.s.topology, this.s.databaseName, name, this.s.pkFactory, options);
      if(callback) callback(null, collection);
      return collection;
    } catch(err) {
      if(callback) return callback(err);
      throw err;
    }
  }

  // Strict mode
  if(typeof callback != 'function') {
    throw toError(f("A callback is required in strict mode. While getting collection %s.", name));
  }

  // Did the user destroy the topology
  if(self.serverConfig && self.serverConfig.isDestroyed()) {
    return callback(new MongoError('topology was destroyed'));
  }

  // Strict mode
  this.listCollections({name:name}).toArray(function(err, collections) {
    if(err != null) return handleCallback(callback, err, null);
    if(collections.length == 0) return handleCallback(callback, toError(f("Collection %s does not exist. Currently in strict mode
.", name)), null);

    try {
      return handleCallback(callback, null, new Collection(self, self.s.topology, self.s.databaseName, name, self.s.pkFactory, options
));
    } catch(err) {
      return handleCallback(callback, err, null);
    }
  });
}
```
- example usage
```shell
...
Inserting a Document
--------------------
Let's create a function that will insert some documents for us.

'''js
var insertDocuments = function(db, callback) {
// Get the documents collection
var collection = db.collection('documents');
// Insert some documents
collection.insertMany([
  {a : 1}, {a : 2}, {a : 3}
], function(err, result) {
  assert.equal(err, null);
  assert.equal(3, result.result.n);
  assert.equal(3, result.ops.length);
...
```

#### <a name="apidoc.element.mongodb.Db.prototype.collections"></a>[function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>collections (callback)](#apidoc.element.mongodb.Db.prototype.collections)
- description and source-code
```javascript
collections = function (callback) {
  var self = this;

  // Return the callback
  if(typeof callback == 'function') return collections(self, callback);
  // Return the promise
  return new self.s.promiseLibrary(function(resolve, reject) {
    collections(self, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Db.prototype.command"></a>[function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>command (command, options, callback)](#apidoc.element.mongodb.Db.prototype.command)
- description and source-code
```javascript
command = function (command, options, callback) {
  var self = this;
  // Change the callback
  if(typeof options == 'function') callback = options, options = {};
  // Clone the options
  options = shallowClone(options);

  // Do we have a callback
  if(typeof callback == 'function') return executeCommand(self, command, options, callback);
  // Return a promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    executeCommand(self, command, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Db.prototype.createCollection"></a>[function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>createCollection (name, options, callback)](#apidoc.element.mongodb.Db.prototype.createCollection)
- description and source-code
```javascript
createCollection = function (name, options, callback) {
  var self = this;
  var args = Array.prototype.slice.call(arguments, 0);
  callback = args.pop();
  if(typeof callback != 'function') args.push(callback);
  name = args.length ? args.shift() : null;
  options = args.length ? args.shift() || {} : {};

  // Do we have a promisesLibrary
  options.promiseLibrary = options.promiseLibrary || this.s.promiseLibrary;

  // Check if the callback is in fact a string
  if(typeof callback == 'string') name = callback;

  // Execute the fallback callback
  if(typeof callback == 'function') return createCollection(self, name, options, callback);
  return new this.s.promiseLibrary(function(resolve, reject) {
    createCollection(self, name, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Db.prototype.createIndex"></a>[function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>createIndex (name, fieldOrSpec, options, callback)](#apidoc.element.mongodb.Db.prototype.createIndex)
- description and source-code
```javascript
createIndex = function (name, fieldOrSpec, options, callback) {
  var self = this;
  var args = Array.prototype.slice.call(arguments, 2);
  callback = args.pop();
  if(typeof callback != 'function') args.push(callback);
  options = args.length ? args.shift() || {} : {};
  options = typeof callback === 'function' ? options : callback;
  options = options == null ? {} : options;
  // Shallow clone the options
  options = shallowClone(options);

  // If we have a callback fallback
  if(typeof callback == 'function') return createIndex(self, name, fieldOrSpec, options, callback);
  // Return a promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    createIndex(self, name, fieldOrSpec, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Db.prototype.db"></a>[function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>db (dbName, options)](#apidoc.element.mongodb.Db.prototype.db)
- description and source-code
```javascript
db = function (dbName, options) {
  options = options || {};

  // Copy the options and add out internal override of the not shared flag
  var finalOptions = assign({}, this.options, options);

  // Do we have the db in the cache already
  if(this.s.dbCache[dbName] && finalOptions.returnNonCachedInstance !== true) {
    return this.s.dbCache[dbName];
  }

  // Add current db as parentDb
  if(finalOptions.noListener == null || finalOptions.noListener == false) {
    finalOptions.parentDb = this;
  }

  // Add promiseLibrary
  finalOptions.promiseLibrary = this.s.promiseLibrary;

  // Return the db object
  var db = new Db(dbName, this.s.topology, finalOptions)

  // Add as child
  if(finalOptions.noListener == null || finalOptions.noListener == false) {
    this.addChild(db);
  }

  // Add the db to the cache
  this.s.dbCache[dbName] = db;
  // Return the database
  return db;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Db.prototype.dropCollection"></a>[function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>dropCollection (name, options, callback)](#apidoc.element.mongodb.Db.prototype.dropCollection)
- description and source-code
```javascript
dropCollection = function (name, options, callback) {
  var self = this;
  if(typeof options == 'function') callback = options, options = {};
  options = options || {};

  // Command to execute
  var cmd = {'drop':name}

  // Decorate with write concern
  decorateWithWriteConcern(cmd, self, options);

  // options
  options = assign({}, this.s.options, {readPreference: ReadPreference.PRIMARY});

  // Check if the callback is in fact a string
  if(typeof callback == 'function') return this.command(cmd, options, function(err, result) {
    // Did the user destroy the topology
    if(self.serverConfig && self.serverConfig.isDestroyed()) return callback(new MongoError('topology was destroyed'));
    if(err) return handleCallback(callback, err);
    if(result.ok) return handleCallback(callback, null, true);
    handleCallback(callback, null, false);
  });

  // Clone the options
  options = shallowClone(self.s.options);
  // Set readPreference PRIMARY
  options.readPreference = ReadPreference.PRIMARY;

  // Execute the command
  return new this.s.promiseLibrary(function(resolve, reject) {
    // Execute command
    self.command(cmd, options, function(err, result) {
      // Did the user destroy the topology
      if(self.serverConfig && self.serverConfig.isDestroyed()) return reject(new MongoError('topology was destroyed'));
      if(err) return reject(err);
      if(result.ok) return resolve(true);
      resolve(false);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Db.prototype.dropDatabase"></a>[function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>dropDatabase (options, callback)](#apidoc.element.mongodb.Db.prototype.dropDatabase)
- description and source-code
```javascript
dropDatabase = function (options, callback) {
  var self = this;
  if(typeof options == 'function') callback = options, options = {};
  options = options || {};
  // Drop database command
  var cmd = {'dropDatabase':1};

  // Decorate with write concern
  decorateWithWriteConcern(cmd, self, options);

  // Ensure primary only
  options = assign({}, this.s.options, {readPreference: ReadPreference.PRIMARY});

  // Check if the callback is in fact a string
  if(typeof callback == 'function') return this.command(cmd, options, function(err, result) {
    // Did the user destroy the topology
    if(self.serverConfig && self.serverConfig.isDestroyed()) return callback(new MongoError('topology was destroyed'));
    if(callback == null) return;
    if(err) return handleCallback(callback, err, null);
    handleCallback(callback, null, result.ok ? true : false);
  });

  // Execute the command
  return new this.s.promiseLibrary(function(resolve, reject) {
    // Execute command
    self.command(cmd, options, function(err, result) {
      // Did the user destroy the topology
      if(self.serverConfig && self.serverConfig.isDestroyed()) return reject(new MongoError('topology was destroyed'));
      if(err) return reject(err);
      if(result.ok) return resolve(true);
      resolve(false);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Db.prototype.ensureIndex"></a>[function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>ensureIndex (name, fieldOrSpec, options, callback)](#apidoc.element.mongodb.Db.prototype.ensureIndex)
- description and source-code
```javascript
ensureIndex = function (name, fieldOrSpec, options, callback) {
  var self = this;
  if(typeof options == 'function') callback = options, options = {};
  options = options || {};

  // If we have a callback fallback
  if(typeof callback == 'function') return ensureIndex(self, name, fieldOrSpec, options, callback);

  // Return a promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    ensureIndex(self, name, fieldOrSpec, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Db.prototype.eval"></a>[function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>eval (code, parameters, options, callback)](#apidoc.element.mongodb.Db.prototype.eval)
- description and source-code
```javascript
eval = function (code, parameters, options, callback) {
  var self = this;
  var args = Array.prototype.slice.call(arguments, 1);
  callback = args.pop();
  if(typeof callback != 'function') args.push(callback);
  parameters = args.length ? args.shift() : parameters;
  options = args.length ? args.shift() || {} : {};

  // Check if the callback is in fact a string
  if(typeof callback == 'function') return evaluate(self, code, parameters, options, callback);
  // Execute the command
  return new this.s.promiseLibrary(function(resolve, reject) {
    evaluate(self, code, parameters, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Db.prototype.executeDbAdminCommand"></a>[function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>executeDbAdminCommand (selector, options, callback)](#apidoc.element.mongodb.Db.prototype.executeDbAdminCommand)
- description and source-code
```javascript
executeDbAdminCommand = function (selector, options, callback) {
  var self = this;
  if(typeof options == 'function') callback = options, options = {};
  options = options || {};

  // Return the callback
  if(typeof callback == 'function') {
    // Convert read preference
    if(options.readPreference) {
      options.readPreference = convertReadPreference(options.readPreference)
    }

    return self.s.topology.command('admin.$cmd', selector, options, function(err, result) {
      // Did the user destroy the topology
      if(self.serverConfig && self.serverConfig.isDestroyed()) return callback(new MongoError('topology was destroyed'));
      if(err) return handleCallback(callback, err);
      handleCallback(callback, null, result.result);
    });
  }

  // Return promise
  return new self.s.promiseLibrary(function(resolve, reject) {
    self.s.topology.command('admin.$cmd', selector, options, function(err, result) {
      // Did the user destroy the topology
      if(self.serverConfig && self.serverConfig.isDestroyed()) return reject(new MongoError('topology was destroyed'));
      if(err) return reject(err);
      resolve(result.result);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Db.prototype.indexInformation"></a>[function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>indexInformation (name, options, callback)](#apidoc.element.mongodb.Db.prototype.indexInformation)
- description and source-code
```javascript
indexInformation = function (name, options, callback) {
  var self = this;
  if(typeof options == 'function') callback = options, options = {};
  options = options || {};

  // If we have a callback fallback
  if(typeof callback == 'function') return indexInformation(self, name, options, callback);

  // Return a promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    indexInformation(self, name, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Db.prototype.listCollections"></a>[function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>listCollections (filter, options)](#apidoc.element.mongodb.Db.prototype.listCollections)
- description and source-code
```javascript
listCollections = function (filter, options) {
  filter = filter || {};
  options = options || {};

  // Shallow clone the object
  options = shallowClone(options);
  // Set the promise library
  options.promiseLibrary = this.s.promiseLibrary;

  // Ensure valid readPreference
  if(options.readPreference) {
    options.readPreference = convertReadPreference(options.readPreference);
  }

  // We have a list collections command
  if(this.serverConfig.capabilities().hasListCollectionsCommand) {
    // Cursor options
    var cursor = options.batchSize ? {batchSize: options.batchSize} : {}
    // Build the command
    var command = { listCollections : true, filter: filter, cursor: cursor };
    // Set the AggregationCursor constructor
    options.cursorFactory = CommandCursor;
    // Create the cursor
    cursor = this.s.topology.cursor(f('%s.$cmd', this.s.databaseName), command, options);
    // Do we have a readPreference, apply it
    if(options.readPreference) {
      cursor.setReadPreference(options.readPreference);
    }
    // Return the cursor
    return cursor;
  }

  // We cannot use the listCollectionsCommand
  if(!this.serverConfig.capabilities().hasListCollectionsCommand) {
    // If we have legacy mode and have not provided a full db name filter it
    if(typeof filter.name == 'string' && !(new RegExp('^' + this.databaseName + '\\.').test(filter.name))) {
      filter = shallowClone(filter);
      filter.name = f('%s.%s', this.s.databaseName, filter.name);
    }
  }

  // No filter, filter by current database
  if(filter == null) {
    filter.name = f('/%s/', this.s.databaseName);
  }

  // Rewrite the filter to use $and to filter out indexes
  if(filter.name) {
    filter = {$and: [{name: filter.name}, {name:/^((?!\$).)*$/}]};
  } else {
    filter = {name:/^((?!\$).)*$/};
  }

  // Return options
  var _options = {transforms: listCollectionsTranforms(this.s.databaseName)}
  // Get the cursor
  cursor = this.collection(Db.SYSTEM_NAMESPACE_COLLECTION).find(filter, _options);
  // Do we have a readPreference, apply it
  if(options.readPreference) cursor.setReadPreference(options.readPreference);
  // Set the passed in batch size if one was provided
  if(options.batchSize) cursor = cursor.batchSize(options.batchSize);
  // We have a fallback mode using legacy systems collections
  return cursor;
}
```
- example usage
```shell
...
*   // Insert a bunch of documents
*   col.insert([{a:1, b:1}
*     , {a:2, b:2}, {a:3, b:3}
*     , {a:4, b:4}], {w:1}, function(err, result) {
*     test.equal(null, err);
*
*     // List the database collections available
*     db.listCollections().toArray(function(err, items) {
*       test.equal(null, err);
*       db.close();
*     });
*   });
* });
*/
...
```

#### <a name="apidoc.element.mongodb.Db.prototype.logout"></a>[function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>logout (options, callback)](#apidoc.element.mongodb.Db.prototype.logout)
- description and source-code
```javascript
logout = function (options, callback) {
  var self = this;
  if(typeof options == 'function') callback = options, options = {};
  options = options || {};

  // Establish the correct database name
  var dbName = this.s.authSource ? this.s.authSource : this.s.databaseName;
  dbName = options.dbName ? options.dbName : dbName;

  // If we have a callback
  if(typeof callback == 'function') {
    return self.s.topology.logout(dbName, function(err) {
      if(err) return callback(err);
      callback(null, true);
    });
  }

  // Return a promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    self.s.topology.logout(dbName, function(err) {
      if(err) return reject(err);
      resolve(true);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Db.prototype.open"></a>[function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>open (callback)](#apidoc.element.mongodb.Db.prototype.open)
- description and source-code
```javascript
open = function (callback) {
  var self = this;
  // We provided a callback leg
  if(typeof callback == 'function') return open(self, callback);
  // Return promise
  return new self.s.promiseLibrary(function(resolve, reject) {
    open(self, function(err, db) {
      if(err) return reject(err);
      resolve(db);
    })
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Db.prototype.removeUser"></a>[function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>removeUser (username, options, callback)](#apidoc.element.mongodb.Db.prototype.removeUser)
- description and source-code
```javascript
removeUser = function (username, options, callback) {
  // Unpack the parameters
  var self = this;
  var args = Array.prototype.slice.call(arguments, 1);
  callback = args.pop();
  if(typeof callback != 'function') args.push(callback);
  options = args.length ? args.shift() || {} : {};

  // If we have a callback fallback
  if(typeof callback == 'function') return removeUser(self, username, options, callback);

  // Return a promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    removeUser(self, username, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Db.prototype.renameCollection"></a>[function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>renameCollection (fromCollection, toCollection, options, callback)](#apidoc.element.mongodb.Db.prototype.renameCollection)
- description and source-code
```javascript
renameCollection = function (fromCollection, toCollection, options, callback) {
  var self = this;
  if(typeof options == 'function') callback = options, options = {};
  options = options || {};
  // Add return new collection
  options.new_collection = true;

  // Check if the callback is in fact a string
  if(typeof callback == 'function') {
    return this.collection(fromCollection).rename(toCollection, options, callback);
  }

  // Return a promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    self.collection(fromCollection).rename(toCollection, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Db.prototype.stats"></a>[function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>stats (options, callback)](#apidoc.element.mongodb.Db.prototype.stats)
- description and source-code
```javascript
stats = function (options, callback) {
  if(typeof options == 'function') callback = options, options = {};
  options = options || {};
  // Build command object
  var commandObject = { dbStats:true };
  // Check if we have the scale value
  if(options['scale'] != null) commandObject['scale'] = options['scale'];

  // If we have a readPreference set
  if(options.readPreference == null && this.s.readPreference) {
    options.readPreference = this.s.readPreference;
  }

  // Execute the command
  return this.command(commandObject, options, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Db.prototype.unref"></a>[function <span class="apidocSignatureSpan">mongodb.Db.prototype.</span>unref ()](#apidoc.element.mongodb.Db.prototype.unref)
- description and source-code
```javascript
unref = function () {
  this.s.topology.unref();
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.Decimal128"></a>[module mongodb.Decimal128](#apidoc.module.mongodb.Decimal128)

#### <a name="apidoc.element.mongodb.Decimal128.Decimal128"></a>[function <span class="apidocSignatureSpan">mongodb.</span>Decimal128 (bytes)](#apidoc.element.mongodb.Decimal128.Decimal128)
- description and source-code
```javascript
Decimal128 = function (bytes) {
  this._bsontype = 'Decimal128';
  this.bytes = bytes;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Decimal128.fromString"></a>[function <span class="apidocSignatureSpan">mongodb.Decimal128.</span>fromString (string)](#apidoc.element.mongodb.Decimal128.fromString)
- description and source-code
```javascript
fromString = function (string) {
  // Parse state tracking
  var isNegative = false;
  var sawRadix = false;
  var foundNonZero = false;

  // Total number of significant digits (no leading or trailing zero)
  var significantDigits = 0;
  // Total number of significand digits read
  var nDigitsRead = 0;
  // Total number of digits (no leading zeros)
  var nDigits = 0;
  // The number of the digits after radix
  var radixPosition = 0;
  // The index of the first non-zero in *str*
  var firstNonZero = 0;

  // Digits Array
  var digits = [0];
  // The number of digits in digits
  var nDigitsStored = 0;
  // Insertion pointer for digits
  var digitsInsert = 0;
  // The index of the first non-zero digit
  var firstDigit = 0;
  // The index of the last digit
  var lastDigit = 0;

  // Exponent
  var exponent = 0;
  // loop index over array
  var i = 0;
  // The high 17 digits of the significand
  var significandHigh = [0, 0];
  // The low 17 digits of the significand
  var significandLow = [0, 0];
  // The biased exponent
  var biasedExponent = 0;

  // Read index
  var index = 0;

  // Trim the string
  string = string.trim();

  // Results
  var stringMatch = string.match(PARSE_STRING_REGEXP);
  var infMatch = string.match(PARSE_INF_REGEXP);
  var nanMatch = string.match(PARSE_NAN_REGEXP);

  // Validate the string
  if(!stringMatch
    && ! infMatch
    && ! nanMatch || string.length == 0) {
      throw new Error("" + string + " not a valid Decimal128 string");
  }

  // Check if we have an illegal exponent format
  if(stringMatch && stringMatch[4] && stringMatch[2] === undefined) {
    throw new Error("" + string + " not a valid Decimal128 string");
  }

  // Get the negative or positive sign
  if(string[index] == '+' || string[index] == '-') {
    isNegative = string[index++] == '-';
  }

  // Check if user passed Infinity or NaN
  if(!isDigit(string[index]) && string[index] != '.') {
    if(string[index] == 'i' || string[index] == 'I') {
      return new Decimal128(new Buffer(isNegative ? INF_NEGATIVE_BUFFER : INF_POSITIVE_BUFFER));
    } else if(string[index] == 'N') {
      return new Decimal128(new Buffer(NAN_BUFFER));
    }
  }

  // Read all the digits
  while(isDigit(string[index]) || string[index] == '.') {
    if(string[index] == '.') {
      if(sawRadix) {
        return new Decimal128(new Buffer(NAN_BUFFER));
      }

      sawRadix = true;
      index = index + 1;
      continue;
    }

    if(nDigitsStored < 34) {
      if(string[index] != '0' || foundNonZero) {
        if(!foundNonZero) {
          firstNonZero = nDigitsRead;
        }

        foundNonZero = true;

        // Only store 34 digits
        digits[digitsInsert++] = parseInt(string[index], 10);
        nDigitsStored = nDigitsStored + 1;
      }
    }

    if(foundNonZero) {
      nDigits = nDigits + 1;
    }

    if(sawRadix) {
      radixPosition = radixPosition + 1;
    }

    nDigitsRead = nDigitsRead + 1;
    index = index + 1;
  }

  if(sawRadix && !nDigitsRead) {
    throw new Error("" + string + " not a valid Decimal128 string");
  }

  // Read exponent if exists
  if(string[index] == 'e' || string[index] == 'E') {
    // Read exponent digits
    var match = string.substr(++index).match(EXPONENT_REGEX);

    // No digits read
    if(!match || !match[2]) {
      return new Decimal128(new Buffer(NAN_BUFFER));
    }

    // Get exponent
    exponent = parseInt(match[0], 10);

    // Adjust the index
    index = index + match[0].length;
  }

  // Return not a number
  if(string[index]) {
    return new Decimal128(new Buffer(NAN_BUFFER));
  }

  // Done reading input
  // Find first non-zero digit in digits
  firstDigit = 0;

  if(!nDigitsStored) {
    firstDigit = 0;
    lastDigit = 0;
    digits[0] = 0;
    nDigits = 1;
    nDigitsStored = 1;
    significantDigits = 0;
  } else {
    lastDigit = nDigitsStored - 1;
    significantDigits = nDigits;

    if(exponent != 0 && significantDigits != 1) {
      while(string[firstNonZero + significantDigits - 1] == '0') {
        significantDigits = significantDigits - 1;
      }
    }
  }

  // Normalization of ...
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.Decimal128.prototype"></a>[module mongodb.Decimal128.prototype](#apidoc.module.mongodb.Decimal128.prototype)

#### <a name="apidoc.element.mongodb.Decimal128.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">mongodb.Decimal128.prototype.</span>toJSON ()](#apidoc.element.mongodb.Decimal128.prototype.toJSON)
- description and source-code
```javascript
toJSON = function () {
  return { "$numberDecimal": this.toString() };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Decimal128.prototype.toString"></a>[function <span class="apidocSignatureSpan">mongodb.Decimal128.prototype.</span>toString ()](#apidoc.element.mongodb.Decimal128.prototype.toString)
- description and source-code
```javascript
toString = function () {
  // Note: bits in this routine are referred to starting at 0,
  // from the sign bit, towards the coefficient.

  // bits 0 - 31
  var high;
  // bits 32 - 63
  var midh;
  // bits 64 - 95
  var midl;
  // bits 96 - 127
  var low;
  // bits 1 - 5
  var combination;
  // decoded biased exponent (14 bits)
  var biased_exponent;
  // the number of significand digits
  var significand_digits = 0;
  // the base-10 digits in the significand
  var significand = new Array(36);
  for(var i = 0; i < significand.length; i++) significand[i] = 0;
  // read pointer into significand
  var index = 0;

  // unbiased exponent
  var exponent;
  // the exponent if scientific notation is used
  var scientific_exponent;

  // true if the number is zero
  var is_zero = false;

  // the most signifcant significand bits (50-46)
  var significand_msb;
  // temporary storage for significand decoding
  var significand128 = {parts: new Array(4)};
  // indexing variables
  var i;
  var j, k;

  // Output string
  var string = [];

  // Unpack index
  var index = 0;

  // Buffer reference
  var buffer = this.bytes;

  // Unpack the low 64bits into a long
  low = buffer[index++] | buffer[index++] << 8 | buffer[index++] << 16 | buffer[index++] << 24;
  midl = buffer[index++] | buffer[index++] << 8 | buffer[index++] << 16 | buffer[index++] << 24;

  // Unpack the high 64bits into a long
  midh = buffer[index++] | buffer[index++] << 8 | buffer[index++] << 16 | buffer[index++] << 24;
  high = buffer[index++] | buffer[index++] << 8 | buffer[index++] << 16 | buffer[index++] << 24;

  // Unpack index
  var index = 0;

  // Create the state of the decimal
  var dec = {
    low: new Long(low, midl),
    high: new Long(midh, high) };

  if(dec.high.lessThan(Long.ZERO)) {
    string.push('-');
  }

  // Decode combination field and exponent
  combination = (high >> 26) & COMBINATION_MASK;

  if((combination >> 3) == 3) {
    // Check for 'special' values
    if(combination == COMBINATION_INFINITY) {
      return string.join('') + "Infinity";
    } else if(combination == COMBINATION_NAN) {
      return "NaN";
    } else {
      biased_exponent = (high >> 15) & EXPONENT_MASK;
      significand_msb = 0x08 + ((high >> 14) & 0x01);
    }
  } else {
    significand_msb = (high >> 14) & 0x07;
    biased_exponent = (high >> 17) & EXPONENT_MASK;
  }

  exponent = biased_exponent - EXPONENT_BIAS;

  // Create string of significand digits

  // Convert the 114-bit binary number represented by
  // (significand_high, significand_low) to at most 34 decimal
  // digits through modulo and division.
  significand128.parts[0] = (high & 0x3fff) + ((significand_msb & 0xf) << 14);
  significand128.parts[1] = midh;
  significand128.parts[2] = midl;
  significand128.parts[3] = low;

  if(significand128.parts[0] == 0 && significand128.parts[1] == 0
    && significand128.parts[2] == 0 && significand128.parts[3] == 0) {
      is_zero = true;
  } else {
    for(var k = 3; k >= 0; k--) {
      var least_digits = 0;
      // Peform the divide
      var result = divideu128(significand128);
      significand128 = result.quotient;
      least_digits = result.rem.low_;

      // We now have the 9 least significant digits (in base 2).
      // Convert and output to string.
      if(!least_digits) continue;

      for(var j = 8; j >= 0; j--) {
        // significand[k * 9 + j] = Math.round(least_digits % 10);
        significand[k * 9 + j] = least_digits % 10;
        // least_digits = Math.round(least_digits / 10);
        least_digits = Math.floor(least_digits / 10);
      }
    }
  }

  // Output format options:
  // Scientific - [-]d.dddE(+/-)dd or [-]dE(+/-)dd
  // Regular    - ddd.ddd

  if(is_zero) {
    significand_digits = 1;
    significand[index] = 0;
  } else {
    significand_digits = 36;
    var i = 0;

    while(!significand[index]) {
      i++;
      significand_digits = significand_digits - 1;
      index = index + 1;
    }
  }

  scientific_exponent = significand_digits - 1 + exponent;

  // The scientific exponent checks are dictated by the string conversion
  // ...
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.Double"></a>[module mongodb.Double](#apidoc.module.mongodb.Double)

#### <a name="apidoc.element.mongodb.Double.Double"></a>[function <span class="apidocSignatureSpan">mongodb.</span>Double (value)](#apidoc.element.mongodb.Double.Double)
- description and source-code
```javascript
function Double(value) {
  if(!(this instanceof Double)) return new Double(value);

  this._bsontype = 'Double';
  this.value = value;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.Double.prototype"></a>[module mongodb.Double.prototype](#apidoc.module.mongodb.Double.prototype)

#### <a name="apidoc.element.mongodb.Double.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">mongodb.Double.prototype.</span>toJSON ()](#apidoc.element.mongodb.Double.prototype.toJSON)
- description and source-code
```javascript
toJSON = function () {
  return this.value;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Double.prototype.valueOf"></a>[function <span class="apidocSignatureSpan">mongodb.Double.prototype.</span>valueOf ()](#apidoc.element.mongodb.Double.prototype.valueOf)
- description and source-code
```javascript
valueOf = function () {
  return this.value;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.GridFSBucket"></a>[module mongodb.GridFSBucket](#apidoc.module.mongodb.GridFSBucket)

#### <a name="apidoc.element.mongodb.GridFSBucket.GridFSBucket"></a>[function <span class="apidocSignatureSpan">mongodb.</span>GridFSBucket (db, options)](#apidoc.element.mongodb.GridFSBucket.GridFSBucket)
- description and source-code
```javascript
function GridFSBucket(db, options) {
  Emitter.apply(this);
  this.setMaxListeners(0);

  if (options && typeof options === 'object') {
    options = shallowClone(options);
    var keys = Object.keys(DEFAULT_GRIDFS_BUCKET_OPTIONS);
    for (var i = 0; i < keys.length; ++i) {
      if (!options[keys[i]]) {
        options[keys[i]] = DEFAULT_GRIDFS_BUCKET_OPTIONS[keys[i]];
      }
    }
  } else {
    options = DEFAULT_GRIDFS_BUCKET_OPTIONS;
  }

  this.s = {
    db: db,
    options: options,
    _chunksCollection: db.collection(options.bucketName + '.chunks'),
    _filesCollection: db.collection(options.bucketName + '.files'),
    checkedIndexes: false,
    calledOpenUploadStream: false,
    promiseLibrary: db.s.promiseLibrary ||
      (typeof global.Promise == 'function' ? global.Promise : require('es6-promise').Promise)
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.GridFSBucket.super_"></a>[function <span class="apidocSignatureSpan">mongodb.GridFSBucket.</span>super_ ()](#apidoc.element.mongodb.GridFSBucket.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.GridFSBucket.prototype"></a>[module mongodb.GridFSBucket.prototype](#apidoc.module.mongodb.GridFSBucket.prototype)

#### <a name="apidoc.element.mongodb.GridFSBucket.prototype.delete"></a>[function <span class="apidocSignatureSpan">mongodb.GridFSBucket.prototype.</span>delete (id, callback)](#apidoc.element.mongodb.GridFSBucket.prototype.delete)
- description and source-code
```javascript
delete = function (id, callback) {
  if (typeof callback === 'function') {
    return _delete(this, id, callback);
  }

  var _this = this;
  return new this.s.promiseLibrary(function(resolve, reject) {
    _delete(_this, id, function(error, res) {
      if (error) {
        reject(error);
      } else {
        resolve(res);
      }
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.GridFSBucket.prototype.drop"></a>[function <span class="apidocSignatureSpan">mongodb.GridFSBucket.prototype.</span>drop (callback)](#apidoc.element.mongodb.GridFSBucket.prototype.drop)
- description and source-code
```javascript
drop = function (callback) {
  if (typeof callback === 'function') {
    return _drop(this, callback);
  }

  var _this = this;
  return new this.s.promiseLibrary(function(resolve, reject) {
    _drop(_this, function(error, res) {
      if (error) {
        reject(error);
      } else {
        resolve(res);
      }
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.GridFSBucket.prototype.find"></a>[function <span class="apidocSignatureSpan">mongodb.GridFSBucket.prototype.</span>find (filter, options)](#apidoc.element.mongodb.GridFSBucket.prototype.find)
- description and source-code
```javascript
find = function (filter, options) {
  filter = filter || {};
  options = options || {};

  var cursor = this.s._filesCollection.find(filter);

  if (options.batchSize != null) {
    cursor.batchSize(options.batchSize);
  }
  if (options.limit != null) {
    cursor.limit(options.limit);
  }
  if (options.maxTimeMS != null) {
    cursor.maxTimeMS(options.maxTimeMS);
  }
  if (options.noCursorTimeout != null) {
    cursor.addCursorFlag('noCursorTimeout', options.noCursorTimeout);
  }
  if (options.skip != null) {
    cursor.skip(options.skip);
  }
  if (options.sort != null) {
    cursor.sort(options.sort);
  }

  return cursor;
}
```
- example usage
```shell
...
We will finish up the Quickstart CRUD methods by performing a simple query that returns all the documents matching the query.

'''js
var findDocuments = function(db, callback) {
  // Get the documents collection
  var collection = db.collection('documents');
  // Find some documents
  collection.find({}).toArray(function(err, docs) {
    assert.equal(err, null);
    assert.equal(2, docs.length);
    console.log("Found the following records");
    console.dir(docs);
    callback(docs);
  });
}
...
```

#### <a name="apidoc.element.mongodb.GridFSBucket.prototype.openDownloadStream"></a>[function <span class="apidocSignatureSpan">mongodb.GridFSBucket.prototype.</span>openDownloadStream (id, options)](#apidoc.element.mongodb.GridFSBucket.prototype.openDownloadStream)
- description and source-code
```javascript
openDownloadStream = function (id, options) {
  var filter = { _id: id };
  options = {
    start: options && options.start,
    end: options && options.end
  };

  return new GridFSBucketReadStream(this.s._chunksCollection,
    this.s._filesCollection, this.s.options.readPreference, filter, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.GridFSBucket.prototype.openDownloadStreamByName"></a>[function <span class="apidocSignatureSpan">mongodb.GridFSBucket.prototype.</span>openDownloadStreamByName (filename, options)](#apidoc.element.mongodb.GridFSBucket.prototype.openDownloadStreamByName)
- description and source-code
```javascript
openDownloadStreamByName = function (filename, options) {
  var sort = { uploadDate: -1 };
  var skip = null;
  if (options && options.revision != null) {
    if (options.revision >= 0) {
      sort = { uploadDate: 1 };
      skip = options.revision;
    } else {
      skip = -options.revision - 1;
    }
  }

  var filter = { filename: filename };
  options = {
    sort: sort,
    skip: skip,
    start: options && options.start,
    end: options && options.end
  };
  return new GridFSBucketReadStream(this.s._chunksCollection,
    this.s._filesCollection, this.s.options.readPreference, filter, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.GridFSBucket.prototype.openUploadStream"></a>[function <span class="apidocSignatureSpan">mongodb.GridFSBucket.prototype.</span>openUploadStream (filename, options)](#apidoc.element.mongodb.GridFSBucket.prototype.openUploadStream)
- description and source-code
```javascript
openUploadStream = function (filename, options) {
  if (options) {
    options = shallowClone(options);
  } else {
    options = {};
  }
  if (!options.chunkSizeBytes) {
    options.chunkSizeBytes = this.s.options.chunkSizeBytes;
  }
  return new GridFSBucketWriteStream(this, filename, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.GridFSBucket.prototype.openUploadStreamWithId"></a>[function <span class="apidocSignatureSpan">mongodb.GridFSBucket.prototype.</span>openUploadStreamWithId (id, filename, options)](#apidoc.element.mongodb.GridFSBucket.prototype.openUploadStreamWithId)
- description and source-code
```javascript
openUploadStreamWithId = function (id, filename, options) {
  if (options) {
    options = shallowClone(options);
  } else {
    options = {};
  }

  if (!options.chunkSizeBytes) {
    options.chunkSizeBytes = this.s.options.chunkSizeBytes;
  }

  options.id = id;

  return new GridFSBucketWriteStream(this, filename, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.GridFSBucket.prototype.rename"></a>[function <span class="apidocSignatureSpan">mongodb.GridFSBucket.prototype.</span>rename (id, filename, callback)](#apidoc.element.mongodb.GridFSBucket.prototype.rename)
- description and source-code
```javascript
rename = function (id, filename, callback) {
  if (typeof callback === 'function') {
    return _rename(this, id, filename, callback);
  }

  var _this = this;
  return new this.s.promiseLibrary(function(resolve, reject) {
    _rename(_this, id, filename, function(error, res) {
      if (error) {
        reject(error);
      } else {
        resolve(res);
      }
    });
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.GridStore"></a>[module mongodb.GridStore](#apidoc.module.mongodb.GridStore)

#### <a name="apidoc.element.mongodb.GridStore.GridStore"></a>[function <span class="apidocSignatureSpan">mongodb.</span>GridStore (db, id, filename, mode, options)](#apidoc.element.mongodb.GridStore.GridStore)
- description and source-code
```javascript
function GridStore(db, id, filename, mode, options) {
  if(!(this instanceof GridStore)) return new GridStore(db, id, filename, mode, options);
  this.db = db;

  // Handle options
  if(typeof options === 'undefined') options = {};
  // Handle mode
  if(typeof mode === 'undefined') {
    mode = filename;
    filename = undefined;
  } else if(typeof mode == 'object') {
    options = mode;
    mode = filename;
    filename = undefined;
  }

  if(id && id._bsontype == 'ObjectID') {
    this.referenceBy = REFERENCE_BY_ID;
    this.fileId = id;
    this.filename = filename;
  } else if(typeof filename == 'undefined') {
    this.referenceBy = REFERENCE_BY_FILENAME;
    this.filename = id;
    if (mode.indexOf('w') != null) {
      this.fileId = new ObjectID();
    }
  } else {
    this.referenceBy = REFERENCE_BY_ID;
    this.fileId = id;
    this.filename = filename;
  }

  // Set up the rest
  this.mode = mode == null ? "r" : mode;
  this.options = options || {};

  // Opened
  this.isOpen = false;

  // Set the root if overridden
  this.root = this.options['root'] == null ? GridStore.DEFAULT_ROOT_COLLECTION : this.options['root'];
  this.position = 0;
  this.readPreference = this.options.readPreference || db.options.readPreference || ReadPreference.PRIMARY;
  this.writeConcern = _getWriteConcern(db, this.options);
  // Set default chunk size
  this.internalChunkSize = this.options['chunkSize'] == null ? Chunk.DEFAULT_CHUNK_SIZE : this.options['chunkSize'];

  // Get the promiseLibrary
  var promiseLibrary = this.options.promiseLibrary;

  // No promise library selected fall back
  if(!promiseLibrary) {
    promiseLibrary = typeof global.Promise == 'function' ?
      global.Promise : require('es6-promise').Promise;
  }

  // Set the promiseLibrary
  this.promiseLibrary = promiseLibrary;

  Object.defineProperty(this, "chunkSize", { enumerable: true
   , get: function () {
       return this.internalChunkSize;
     }
   , set: function(value) {
       if(!(this.mode[0] == "w" && this.position == 0 && this.uploadDate == null)) {
         this.internalChunkSize = this.internalChunkSize;
       } else {
         this.internalChunkSize = value;
       }
     }
  });

  Object.defineProperty(this, "md5", { enumerable: true
   , get: function () {
       return this.internalMd5;
     }
  });

  Object.defineProperty(this, "chunkNumber", { enumerable: true
   , get: function () {
       return this.currentChunk && this.currentChunk.chunkNumber ? this.currentChunk.chunkNumber : null;
     }
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.GridStore.exist"></a>[function <span class="apidocSignatureSpan">mongodb.GridStore.</span>exist (db, fileIdObject, rootCollection, options, callback)](#apidoc.element.mongodb.GridStore.exist)
- description and source-code
```javascript
exist = function (db, fileIdObject, rootCollection, options, callback) {
  var args = Array.prototype.slice.call(arguments, 2);
  callback = args.pop();
  if(typeof callback != 'function') args.push(callback);
  rootCollection = args.length ? args.shift() : null;
  options = args.length ? args.shift() : {};
  options = options || {};

  // Get the promiseLibrary
  var promiseLibrary = options.promiseLibrary;

  // No promise library selected fall back
  if(!promiseLibrary) {
    promiseLibrary = typeof global.Promise == 'function' ?
      global.Promise : require('es6-promise').Promise;
  }

  // We provided a callback leg
  if(typeof callback == 'function') return exists(db, fileIdObject, rootCollection, options, callback);
  // Return promise
  return new promiseLibrary(function(resolve, reject) {
    exists(db, fileIdObject, rootCollection, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    })
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.GridStore.list"></a>[function <span class="apidocSignatureSpan">mongodb.GridStore.</span>list (db, rootCollection, options, callback)](#apidoc.element.mongodb.GridStore.list)
- description and source-code
```javascript
list = function (db, rootCollection, options, callback) {
  var args = Array.prototype.slice.call(arguments, 1);
  callback = args.pop();
  if(typeof callback != 'function') args.push(callback);
  rootCollection = args.length ? args.shift() : null;
  options = args.length ? args.shift() : {};
  options = options || {};

  // Get the promiseLibrary
  var promiseLibrary = options.promiseLibrary;

  // No promise library selected fall back
  if(!promiseLibrary) {
    promiseLibrary = typeof global.Promise == 'function' ?
      global.Promise : require('es6-promise').Promise;
  }

  // We provided a callback leg
  if(typeof callback == 'function') return list(db, rootCollection, options, callback);
  // Return promise
  return new promiseLibrary(function(resolve, reject) {
    list(db, rootCollection, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    })
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.GridStore.read"></a>[function <span class="apidocSignatureSpan">mongodb.GridStore.</span>read (db, name, length, offset, options, callback)](#apidoc.element.mongodb.GridStore.read)
- description and source-code
```javascript
read = function (db, name, length, offset, options, callback) {
  var args = Array.prototype.slice.call(arguments, 2);
  callback = args.pop();
  if(typeof callback != 'function') args.push(callback);
  length = args.length ? args.shift() : null;
  offset = args.length ? args.shift() : null;
  options = args.length ? args.shift() : null;
  options = options || {};

  // Get the promiseLibrary
  var promiseLibrary = options ? options.promiseLibrary : null;

  // No promise library selected fall back
  if(!promiseLibrary) {
    promiseLibrary = typeof global.Promise == 'function' ?
      global.Promise : require('es6-promise').Promise;
  }

  // We provided a callback leg
  if(typeof callback == 'function') return readStatic(db, name, length, offset, options, callback);
  // Return promise
  return new promiseLibrary(function(resolve, reject) {
    readStatic(db, name, length, offset, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    })
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.GridStore.readlines"></a>[function <span class="apidocSignatureSpan">mongodb.GridStore.</span>readlines (db, name, separator, options, callback)](#apidoc.element.mongodb.GridStore.readlines)
- description and source-code
```javascript
readlines = function (db, name, separator, options, callback) {
  var args = Array.prototype.slice.call(arguments, 2);
  callback = args.pop();
  if(typeof callback != 'function') args.push(callback);
  separator = args.length ? args.shift() : null;
  options = args.length ? args.shift() : null;
  options = options || {};

  // Get the promiseLibrary
  var promiseLibrary = options ? options.promiseLibrary : null;

  // No promise library selected fall back
  if(!promiseLibrary) {
    promiseLibrary = typeof global.Promise == 'function' ?
      global.Promise : require('es6-promise').Promise;
  }

  // We provided a callback leg
  if(typeof callback == 'function') return readlinesStatic(db, name, separator, options, callback);
  // Return promise
  return new promiseLibrary(function(resolve, reject) {
    readlinesStatic(db, name, separator, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    })
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.GridStore.unlink"></a>[function <span class="apidocSignatureSpan">mongodb.GridStore.</span>unlink (db, names, options, callback)](#apidoc.element.mongodb.GridStore.unlink)
- description and source-code
```javascript
unlink = function (db, names, options, callback) {
  var self = this;
  var args = Array.prototype.slice.call(arguments, 2);
  callback = args.pop();
  if(typeof callback != 'function') args.push(callback);
  options = args.length ? args.shift() : {};
  options = options || {};

  // Get the promiseLibrary
  var promiseLibrary = options.promiseLibrary;

  // No promise library selected fall back
  if(!promiseLibrary) {
    promiseLibrary = typeof global.Promise == 'function' ?
      global.Promise : require('es6-promise').Promise;
  }

  // We provided a callback leg
  if(typeof callback == 'function') return unlinkStatic(self, db, names, options, callback);

  // Return promise
  return new promiseLibrary(function(resolve, reject) {
    unlinkStatic(self, db, names, options, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    })
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.GridStore.define"></a>[module mongodb.GridStore.define](#apidoc.module.mongodb.GridStore.define)

#### <a name="apidoc.element.mongodb.GridStore.define.object"></a>[function <span class="apidocSignatureSpan">mongodb.GridStore.define.</span>object (db, id, filename, mode, options)](#apidoc.element.mongodb.GridStore.define.object)
- description and source-code
```javascript
function GridStore(db, id, filename, mode, options) {
  if(!(this instanceof GridStore)) return new GridStore(db, id, filename, mode, options);
  this.db = db;

  // Handle options
  if(typeof options === 'undefined') options = {};
  // Handle mode
  if(typeof mode === 'undefined') {
    mode = filename;
    filename = undefined;
  } else if(typeof mode == 'object') {
    options = mode;
    mode = filename;
    filename = undefined;
  }

  if(id && id._bsontype == 'ObjectID') {
    this.referenceBy = REFERENCE_BY_ID;
    this.fileId = id;
    this.filename = filename;
  } else if(typeof filename == 'undefined') {
    this.referenceBy = REFERENCE_BY_FILENAME;
    this.filename = id;
    if (mode.indexOf('w') != null) {
      this.fileId = new ObjectID();
    }
  } else {
    this.referenceBy = REFERENCE_BY_ID;
    this.fileId = id;
    this.filename = filename;
  }

  // Set up the rest
  this.mode = mode == null ? "r" : mode;
  this.options = options || {};

  // Opened
  this.isOpen = false;

  // Set the root if overridden
  this.root = this.options['root'] == null ? GridStore.DEFAULT_ROOT_COLLECTION : this.options['root'];
  this.position = 0;
  this.readPreference = this.options.readPreference || db.options.readPreference || ReadPreference.PRIMARY;
  this.writeConcern = _getWriteConcern(db, this.options);
  // Set default chunk size
  this.internalChunkSize = this.options['chunkSize'] == null ? Chunk.DEFAULT_CHUNK_SIZE : this.options['chunkSize'];

  // Get the promiseLibrary
  var promiseLibrary = this.options.promiseLibrary;

  // No promise library selected fall back
  if(!promiseLibrary) {
    promiseLibrary = typeof global.Promise == 'function' ?
      global.Promise : require('es6-promise').Promise;
  }

  // Set the promiseLibrary
  this.promiseLibrary = promiseLibrary;

  Object.defineProperty(this, "chunkSize", { enumerable: true
   , get: function () {
       return this.internalChunkSize;
     }
   , set: function(value) {
       if(!(this.mode[0] == "w" && this.position == 0 && this.uploadDate == null)) {
         this.internalChunkSize = this.internalChunkSize;
       } else {
         this.internalChunkSize = value;
       }
     }
  });

  Object.defineProperty(this, "md5", { enumerable: true
   , get: function () {
       return this.internalMd5;
     }
  });

  Object.defineProperty(this, "chunkNumber", { enumerable: true
   , get: function () {
       return this.currentChunk && this.currentChunk.chunkNumber ? this.currentChunk.chunkNumber : null;
     }
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.GridStore.prototype"></a>[module mongodb.GridStore.prototype](#apidoc.module.mongodb.GridStore.prototype)

#### <a name="apidoc.element.mongodb.GridStore.prototype.chunkCollection"></a>[function <span class="apidocSignatureSpan">mongodb.GridStore.prototype.</span>chunkCollection (callback)](#apidoc.element.mongodb.GridStore.prototype.chunkCollection)
- description and source-code
```javascript
chunkCollection = function (callback) {
  if(typeof callback == 'function')
    return this.db.collection((this.root + ".chunks"), callback);
  return this.db.collection((this.root + ".chunks"));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.GridStore.prototype.close"></a>[function <span class="apidocSignatureSpan">mongodb.GridStore.prototype.</span>close (callback)](#apidoc.element.mongodb.GridStore.prototype.close)
- description and source-code
```javascript
close = function (callback) {
  var self = this;
  // We provided a callback leg
  if(typeof callback == 'function') return close(self, callback);
  // Return promise
  return new self.promiseLibrary(function(resolve, reject) {
    close(self, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    })
  });
}
```
- example usage
```shell
...
// Connection URL
var url = 'mongodb://localhost:27017/myproject';
// Use connect method to connect to the Server
MongoClient.connect(url, function(err, db) {
  assert.equal(null, err);
  console.log("Connected correctly to server");

  db.close();
});
'''

Given that you booted up the **mongod** process earlier the application should connect successfully and print **Connected correctly
 to server** to the console.

Let's Add some code to show the different CRUD operations available.
...
```

#### <a name="apidoc.element.mongodb.GridStore.prototype.collection"></a>[function <span class="apidocSignatureSpan">mongodb.GridStore.prototype.</span>collection (callback)](#apidoc.element.mongodb.GridStore.prototype.collection)
- description and source-code
```javascript
collection = function (callback) {
  if(typeof callback == 'function')
    this.db.collection(this.root + ".files", callback);
  return this.db.collection(this.root + ".files");
}
```
- example usage
```shell
...
Inserting a Document
--------------------
Let's create a function that will insert some documents for us.

'''js
var insertDocuments = function(db, callback) {
// Get the documents collection
var collection = db.collection('documents');
// Insert some documents
collection.insertMany([
  {a : 1}, {a : 2}, {a : 3}
], function(err, result) {
  assert.equal(err, null);
  assert.equal(3, result.result.n);
  assert.equal(3, result.ops.length);
...
```

#### <a name="apidoc.element.mongodb.GridStore.prototype.destroy"></a>[function <span class="apidocSignatureSpan">mongodb.GridStore.prototype.</span>destroy ()](#apidoc.element.mongodb.GridStore.prototype.destroy)
- description and source-code
```javascript
function destroy() {
  // close and do not emit any more events. queued data is not sent.
  if(!this.writable) return;
  this.readable = false;
  if(this.writable) {
    this.writable = false;
    this._q.length = 0;
    this.emit('close');
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.GridStore.prototype.eof"></a>[function <span class="apidocSignatureSpan">mongodb.GridStore.prototype.</span>eof ()](#apidoc.element.mongodb.GridStore.prototype.eof)
- description and source-code
```javascript
eof = function () {
  return this.position == this.length ? true : false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.GridStore.prototype.getc"></a>[function <span class="apidocSignatureSpan">mongodb.GridStore.prototype.</span>getc (callback)](#apidoc.element.mongodb.GridStore.prototype.getc)
- description and source-code
```javascript
getc = function (callback) {
  var self = this;
  // We provided a callback leg
  if(typeof callback == 'function') return eof(self, callback);
  // Return promise
  return new self.promiseLibrary(function(resolve, reject) {
    eof(self, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    })
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.GridStore.prototype.open"></a>[function <span class="apidocSignatureSpan">mongodb.GridStore.prototype.</span>open (callback)](#apidoc.element.mongodb.GridStore.prototype.open)
- description and source-code
```javascript
open = function (callback) {
  var self = this;
  if( this.mode != "w" && this.mode != "w+" && this.mode != "r"){
    throw MongoError.create({message: "Illegal mode " + this.mode, driver:true});
  }

  // We provided a callback leg
  if(typeof callback == 'function') return open(self, callback);
  // Return promise
  return new self.promiseLibrary(function(resolve, reject) {
    open(self, function(err, store) {
      if(err) return reject(err);
      resolve(store);
    })
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.GridStore.prototype.puts"></a>[function <span class="apidocSignatureSpan">mongodb.GridStore.prototype.</span>puts (string, callback)](#apidoc.element.mongodb.GridStore.prototype.puts)
- description and source-code
```javascript
puts = function (string, callback) {
  var self = this;
  var finalString = string.match(/\n$/) == null ? string + "\n" : string;
  // We provided a callback leg
  if(typeof callback == 'function') return this.write(finalString, callback);
  // Return promise
  return new self.promiseLibrary(function(resolve, reject) {
    self.write(finalString, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    })
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.GridStore.prototype.read"></a>[function <span class="apidocSignatureSpan">mongodb.GridStore.prototype.</span>read (length, buffer, callback)](#apidoc.element.mongodb.GridStore.prototype.read)
- description and source-code
```javascript
read = function (length, buffer, callback) {
  var self = this;

  var args = Array.prototype.slice.call(arguments, 0);
  callback = args.pop();
  if(typeof callback != 'function') args.push(callback);
  length = args.length ? args.shift() : null;
  buffer = args.length ? args.shift() : null;
  // We provided a callback leg
  if(typeof callback == 'function') return read(self, length, buffer, callback);
  // Return promise
  return new self.promiseLibrary(function(resolve, reject) {
    read(self, length, buffer, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    })
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.GridStore.prototype.readlines"></a>[function <span class="apidocSignatureSpan">mongodb.GridStore.prototype.</span>readlines (separator, callback)](#apidoc.element.mongodb.GridStore.prototype.readlines)
- description and source-code
```javascript
readlines = function (separator, callback) {
  var self = this;
  var args = Array.prototype.slice.call(arguments, 0);
  callback = args.pop();
  if(typeof callback != 'function') args.push(callback);
  separator = args.length ? args.shift() : "\n";
  separator = separator || "\n";

  // We provided a callback leg
  if(typeof callback == 'function') return readlines(self, separator, callback);

  // Return promise
  return new self.promiseLibrary(function(resolve, reject) {
    readlines(self, separator, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    })
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.GridStore.prototype.rewind"></a>[function <span class="apidocSignatureSpan">mongodb.GridStore.prototype.</span>rewind (callback)](#apidoc.element.mongodb.GridStore.prototype.rewind)
- description and source-code
```javascript
rewind = function (callback) {
  var self = this;
  // We provided a callback leg
  if(typeof callback == 'function') return rewind(self, callback);
  // Return promise
  return new self.promiseLibrary(function(resolve, reject) {
    rewind(self, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    })
  });
}
```
- example usage
```shell
...
 * @param {object[]} documents All the documents the satisfy the cursor.
 */

/**
 * Returns an array of documents. The caller is responsible for making sure that there
 * is enough memory to store the results. Note that the array only contain partial
 * results when this cursor had been previouly accessed. In that case,
 * cursor.rewind() can be used to reset the cursor.
 * @method AggregationCursor.prototype.toArray
 * @param {AggregationCursor~toArrayResultCallback} [callback] The result callback.
 * @throws {MongoError}
 * @return {Promise} returns Promise if no callback passed
 */

/**
...
```

#### <a name="apidoc.element.mongodb.GridStore.prototype.seek"></a>[function <span class="apidocSignatureSpan">mongodb.GridStore.prototype.</span>seek (position, seekLocation, callback)](#apidoc.element.mongodb.GridStore.prototype.seek)
- description and source-code
```javascript
seek = function (position, seekLocation, callback) {
  var self = this;

  var args = Array.prototype.slice.call(arguments, 1);
  callback = args.pop();
  if(typeof callback != 'function') args.push(callback);
  seekLocation = args.length ? args.shift() : null;

  // We provided a callback leg
  if(typeof callback == 'function') return seek(self, position, seekLocation, callback);
  // Return promise
  return new self.promiseLibrary(function(resolve, reject) {
    seek(self, position, seekLocation, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    })
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.GridStore.prototype.stream"></a>[function <span class="apidocSignatureSpan">mongodb.GridStore.prototype.</span>stream ()](#apidoc.element.mongodb.GridStore.prototype.stream)
- description and source-code
```javascript
stream = function () {
  return new GridStoreStream(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.GridStore.prototype.tell"></a>[function <span class="apidocSignatureSpan">mongodb.GridStore.prototype.</span>tell (callback)](#apidoc.element.mongodb.GridStore.prototype.tell)
- description and source-code
```javascript
tell = function (callback) {
  var self = this;
  // We provided a callback leg
  if(typeof callback == 'function') return callback(null, this.position);
  // Return promise
  return new self.promiseLibrary(function(resolve) {
    resolve(self.position);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.GridStore.prototype.unlink"></a>[function <span class="apidocSignatureSpan">mongodb.GridStore.prototype.</span>unlink (callback)](#apidoc.element.mongodb.GridStore.prototype.unlink)
- description and source-code
```javascript
unlink = function (callback) {
  var self = this;
  // We provided a callback leg
  if(typeof callback == 'function') return unlink(self, callback);
  // Return promise
  return new self.promiseLibrary(function(resolve, reject) {
    unlink(self, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    })
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.GridStore.prototype.write"></a>[function <span class="apidocSignatureSpan">mongodb.GridStore.prototype.</span>write (data, close, callback)](#apidoc.element.mongodb.GridStore.prototype.write)
- description and source-code
```javascript
function write(data, close, callback) {
  var self = this;
  // We provided a callback leg
  if(typeof callback == 'function') return _writeNormal(this, data, close, callback);
  // Return promise
  return new self.promiseLibrary(function(resolve, reject) {
    _writeNormal(self, data, close, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    })
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.GridStore.prototype.writeFile"></a>[function <span class="apidocSignatureSpan">mongodb.GridStore.prototype.</span>writeFile (file, callback)](#apidoc.element.mongodb.GridStore.prototype.writeFile)
- description and source-code
```javascript
writeFile = function (file, callback) {
  var self = this;
  // We provided a callback leg
  if(typeof callback == 'function') return writeFile(self, file, callback);
  // Return promise
  return new self.promiseLibrary(function(resolve, reject) {
    writeFile(self, file, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    })
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.Int32"></a>[module mongodb.Int32](#apidoc.module.mongodb.Int32)

#### <a name="apidoc.element.mongodb.Int32.Int32"></a>[function <span class="apidocSignatureSpan">mongodb.</span>Int32 (value)](#apidoc.element.mongodb.Int32.Int32)
- description and source-code
```javascript
Int32 = function (value) {
  if(!(this instanceof Int32)) return new Int32(value);

  this._bsontype = 'Int32';
  this.value = value;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.Int32.prototype"></a>[module mongodb.Int32.prototype](#apidoc.module.mongodb.Int32.prototype)

#### <a name="apidoc.element.mongodb.Int32.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">mongodb.Int32.prototype.</span>toJSON ()](#apidoc.element.mongodb.Int32.prototype.toJSON)
- description and source-code
```javascript
toJSON = function () {
  return this.value;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Int32.prototype.valueOf"></a>[function <span class="apidocSignatureSpan">mongodb.Int32.prototype.</span>valueOf ()](#apidoc.element.mongodb.Int32.prototype.valueOf)
- description and source-code
```javascript
valueOf = function () {
  return this.value;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.Logger"></a>[module mongodb.Logger](#apidoc.module.mongodb.Logger)

#### <a name="apidoc.element.mongodb.Logger.Logger"></a>[function <span class="apidocSignatureSpan">mongodb.</span>Logger (className, options)](#apidoc.element.mongodb.Logger.Logger)
- description and source-code
```javascript
Logger = function (className, options) {
  if(!(this instanceof Logger)) return new Logger(className, options);
  options = options || {};

  // Current reference
  this.className = className;

  // Current logger
  if(options.logger) {
    currentLogger = options.logger;
  } else if(currentLogger == null) {
    currentLogger = console.log;
  }

  // Set level of logging, default is error
  if(options.loggerLevel) {
    level = options.loggerLevel || 'error';
  }

  // Add all class names
  if(filteredClasses[this.className] == null) classFilters[this.className] =  true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Logger.currentLogger"></a>[function <span class="apidocSignatureSpan">mongodb.Logger.</span>currentLogger ()](#apidoc.element.mongodb.Logger.currentLogger)
- description and source-code
```javascript
currentLogger = function () {
  return currentLogger;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Logger.filter"></a>[function <span class="apidocSignatureSpan">mongodb.Logger.</span>filter (type, values)](#apidoc.element.mongodb.Logger.filter)
- description and source-code
```javascript
filter = function (type, values) {
  if(type == 'class' && Array.isArray(values)) {
    filteredClasses = {};

    values.forEach(function(x) {
      filteredClasses[x] = true;
    });
  }
}
```
- example usage
```shell
...

    // No entry returned for duplicate servr
    if(deduplicatedServers[_host + "_" + _port]) return null;
    deduplicatedServers[_host + "_" + _port] = 1;

    // Return the mapped object
    return {host: _host, port: _port};
  }).filter(function(x) {
    return x != null;
  });
}

// Get the db name
object.dbName = dbName || 'admin';
// Split up all the options
...
```

#### <a name="apidoc.element.mongodb.Logger.reset"></a>[function <span class="apidocSignatureSpan">mongodb.Logger.</span>reset ()](#apidoc.element.mongodb.Logger.reset)
- description and source-code
```javascript
reset = function () {
  level = 'error';
  filteredClasses = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Logger.setCurrentLogger"></a>[function <span class="apidocSignatureSpan">mongodb.Logger.</span>setCurrentLogger (logger)](#apidoc.element.mongodb.Logger.setCurrentLogger)
- description and source-code
```javascript
setCurrentLogger = function (logger) {
  if(typeof logger != 'function') throw new MongoError("current logger must be a function");
  currentLogger = logger;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Logger.setLevel"></a>[function <span class="apidocSignatureSpan">mongodb.Logger.</span>setLevel (_level)](#apidoc.element.mongodb.Logger.setLevel)
- description and source-code
```javascript
setLevel = function (_level) {
  if(_level != 'info' && _level != 'error' && _level != 'debug' && _level != 'warn') {
    throw new Error(f("%s is an illegal logging level", _level));
  }

  level = _level;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.Logger.prototype"></a>[module mongodb.Logger.prototype](#apidoc.module.mongodb.Logger.prototype)

#### <a name="apidoc.element.mongodb.Logger.prototype.debug"></a>[function <span class="apidocSignatureSpan">mongodb.Logger.prototype.</span>debug (message, object)](#apidoc.element.mongodb.Logger.prototype.debug)
- description and source-code
```javascript
debug = function (message, object) {
  if(this.isDebug()
    && ((Object.keys(filteredClasses).length > 0 && filteredClasses[this.className])
      || (Object.keys(filteredClasses).length == 0 && classFilters[this.className]))) {
    var dateTime = new Date().getTime();
    var msg = f("[%s-%s:%s] %s %s", 'DEBUG', this.className, pid, dateTime, message);
    var state = {
      type: 'debug', message: message, className: this.className, pid: pid, date: dateTime
    };
    if(object) state.meta = object;
    currentLogger(msg, state);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Logger.prototype.error"></a>[function <span class="apidocSignatureSpan">mongodb.Logger.prototype.</span>error (message, object)](#apidoc.element.mongodb.Logger.prototype.error)
- description and source-code
```javascript
error = function (message, object) {
  if(this.isError()
    && ((Object.keys(filteredClasses).length > 0 && filteredClasses[this.className])
      || (Object.keys(filteredClasses).length == 0 && classFilters[this.className]))) {
    var dateTime = new Date().getTime();
    var msg = f("[%s-%s:%s] %s %s", 'ERROR', this.className, pid, dateTime, message);
    var state = {
      type: 'error', message: message, className: this.className, pid: pid, date: dateTime
    };
    if(object) state.meta = object;
    currentLogger(msg, state);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Logger.prototype.info"></a>[function <span class="apidocSignatureSpan">mongodb.Logger.prototype.</span>info (message, object)](#apidoc.element.mongodb.Logger.prototype.info)
- description and source-code
```javascript
info = function (message, object) {
  if(this.isInfo()
    && ((Object.keys(filteredClasses).length > 0 && filteredClasses[this.className])
      || (Object.keys(filteredClasses).length == 0 && classFilters[this.className]))) {
    var dateTime = new Date().getTime();
    var msg = f("[%s-%s:%s] %s %s", 'INFO', this.className, pid, dateTime, message);
    var state = {
      type: 'info', message: message, className: this.className, pid: pid, date: dateTime
    };
    if(object) state.meta = object;
    currentLogger(msg, state);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Logger.prototype.isDebug"></a>[function <span class="apidocSignatureSpan">mongodb.Logger.prototype.</span>isDebug ()](#apidoc.element.mongodb.Logger.prototype.isDebug)
- description and source-code
```javascript
isDebug = function () {
  return level == 'debug';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Logger.prototype.isError"></a>[function <span class="apidocSignatureSpan">mongodb.Logger.prototype.</span>isError ()](#apidoc.element.mongodb.Logger.prototype.isError)
- description and source-code
```javascript
isError = function () {
  return level == 'error' || level == 'info' || level == 'debug';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Logger.prototype.isInfo"></a>[function <span class="apidocSignatureSpan">mongodb.Logger.prototype.</span>isInfo ()](#apidoc.element.mongodb.Logger.prototype.isInfo)
- description and source-code
```javascript
isInfo = function () {
  return level == 'info' || level == 'debug';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Logger.prototype.isWarn"></a>[function <span class="apidocSignatureSpan">mongodb.Logger.prototype.</span>isWarn ()](#apidoc.element.mongodb.Logger.prototype.isWarn)
- description and source-code
```javascript
isWarn = function () {
  return level == 'error' || level == 'warn' || level == 'info' || level == 'debug';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Logger.prototype.warn"></a>[function <span class="apidocSignatureSpan">mongodb.Logger.prototype.</span>warn (message, object)](#apidoc.element.mongodb.Logger.prototype.warn)
- description and source-code
```javascript
warn = function (message, object) {
  if(this.isWarn()
    && ((Object.keys(filteredClasses).length > 0 && filteredClasses[this.className])
      || (Object.keys(filteredClasses).length == 0 && classFilters[this.className]))) {
    var dateTime = new Date().getTime();
    var msg = f("[%s-%s:%s] %s %s", 'WARN', this.className, pid, dateTime, message);
    var state = {
      type: 'warn', message: message, className: this.className, pid: pid, date: dateTime
    };
    if(object) state.meta = object;
    currentLogger(msg, state);
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.Long"></a>[module mongodb.Long](#apidoc.module.mongodb.Long)

#### <a name="apidoc.element.mongodb.Long.Long"></a>[function <span class="apidocSignatureSpan">mongodb.</span>Long (low, high)](#apidoc.element.mongodb.Long.Long)
- description and source-code
```javascript
function Long(low, high) {
  if(!(this instanceof Long)) return new Long(low, high);

  this._bsontype = 'Long';
<span class="apidocCodeCommentSpan">  /**
   * @type {number}
   * @ignore
   */
</span>  this.low_ = low | 0;  // force into 32 signed bits.

  /**
   * @type {number}
   * @ignore
   */
  this.high_ = high | 0;  // force into 32 signed bits.
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Long.fromBits"></a>[function <span class="apidocSignatureSpan">mongodb.Long.</span>fromBits (lowBits, highBits)](#apidoc.element.mongodb.Long.fromBits)
- description and source-code
```javascript
fromBits = function (lowBits, highBits) {
  return new Long(lowBits, highBits);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Long.fromInt"></a>[function <span class="apidocSignatureSpan">mongodb.Long.</span>fromInt (value)](#apidoc.element.mongodb.Long.fromInt)
- description and source-code
```javascript
fromInt = function (value) {
  if (-128 <= value && value < 128) {
    var cachedObj = Long.INT_CACHE_[value];
    if (cachedObj) {
      return cachedObj;
    }
  }

  var obj = new Long(value | 0, value < 0 ? -1 : 0);
  if (-128 <= value && value < 128) {
    Long.INT_CACHE_[value] = obj;
  }
  return obj;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Long.fromNumber"></a>[function <span class="apidocSignatureSpan">mongodb.Long.</span>fromNumber (value)](#apidoc.element.mongodb.Long.fromNumber)
- description and source-code
```javascript
fromNumber = function (value) {
  if (isNaN(value) || !isFinite(value)) {
    return Long.ZERO;
  } else if (value <= -Long.TWO_PWR_63_DBL_) {
    return Long.MIN_VALUE;
  } else if (value + 1 >= Long.TWO_PWR_63_DBL_) {
    return Long.MAX_VALUE;
  } else if (value < 0) {
    return Long.fromNumber(-value).negate();
  } else {
    return new Long(
               (value % Long.TWO_PWR_32_DBL_) | 0,
               (value / Long.TWO_PWR_32_DBL_) | 0);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Long.fromString"></a>[function <span class="apidocSignatureSpan">mongodb.Long.</span>fromString (str, opt_radix)](#apidoc.element.mongodb.Long.fromString)
- description and source-code
```javascript
fromString = function (str, opt_radix) {
  if (str.length == 0) {
    throw Error('number format error: empty string');
  }

  var radix = opt_radix || 10;
  if (radix < 2 || 36 < radix) {
    throw Error('radix out of range: ' + radix);
  }

  if (str.charAt(0) == '-') {
    return Long.fromString(str.substring(1), radix).negate();
  } else if (str.indexOf('-') >= 0) {
    throw Error('number format error: interior "-" character: ' + str);
  }

  // Do several (8) digits each time through the loop, so as to
  // minimize the calls to the very expensive emulated div.
  var radixToPower = Long.fromNumber(Math.pow(radix, 8));

  var result = Long.ZERO;
  for (var i = 0; i < str.length; i += 8) {
    var size = Math.min(8, str.length - i);
    var value = parseInt(str.substring(i, i + size), radix);
    if (size < 8) {
      var power = Long.fromNumber(Math.pow(radix, size));
      result = result.multiply(power).add(Long.fromNumber(value));
    } else {
      result = result.multiply(radixToPower);
      result = result.add(Long.fromNumber(value));
    }
  }
  return result;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.Long.prototype"></a>[module mongodb.Long.prototype](#apidoc.module.mongodb.Long.prototype)

#### <a name="apidoc.element.mongodb.Long.prototype.add"></a>[function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>add (other)](#apidoc.element.mongodb.Long.prototype.add)
- description and source-code
```javascript
add = function (other) {
  // Divide each number into 4 chunks of 16 bits, and then sum the chunks.

  var a48 = this.high_ >>> 16;
  var a32 = this.high_ & 0xFFFF;
  var a16 = this.low_ >>> 16;
  var a00 = this.low_ & 0xFFFF;

  var b48 = other.high_ >>> 16;
  var b32 = other.high_ & 0xFFFF;
  var b16 = other.low_ >>> 16;
  var b00 = other.low_ & 0xFFFF;

  var c48 = 0, c32 = 0, c16 = 0, c00 = 0;
  c00 += a00 + b00;
  c16 += c00 >>> 16;
  c00 &= 0xFFFF;
  c16 += a16 + b16;
  c32 += c16 >>> 16;
  c16 &= 0xFFFF;
  c32 += a32 + b32;
  c48 += c32 >>> 16;
  c32 &= 0xFFFF;
  c48 += a48 + b48;
  c48 &= 0xFFFF;
  return Long.fromBits((c16 << 16) | c00, (c48 << 16) | c32);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Long.prototype.and"></a>[function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>and (other)](#apidoc.element.mongodb.Long.prototype.and)
- description and source-code
```javascript
and = function (other) {
  return Long.fromBits(this.low_ & other.low_, this.high_ & other.high_);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Long.prototype.compare"></a>[function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>compare (other)](#apidoc.element.mongodb.Long.prototype.compare)
- description and source-code
```javascript
compare = function (other) {
  if (this.equals(other)) {
    return 0;
  }

  var thisNeg = this.isNegative();
  var otherNeg = other.isNegative();
  if (thisNeg && !otherNeg) {
    return -1;
  }
  if (!thisNeg && otherNeg) {
    return 1;
  }

  // at this point, the signs are the same, so subtraction will not overflow
  if (this.subtract(other).isNegative()) {
    return -1;
  } else {
    return 1;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Long.prototype.div"></a>[function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>div (other)](#apidoc.element.mongodb.Long.prototype.div)
- description and source-code
```javascript
div = function (other) {
  if (other.isZero()) {
    throw Error('division by zero');
  } else if (this.isZero()) {
    return Long.ZERO;
  }

  if (this.equals(Long.MIN_VALUE)) {
    if (other.equals(Long.ONE) ||
        other.equals(Long.NEG_ONE)) {
      return Long.MIN_VALUE;  // recall that -MIN_VALUE == MIN_VALUE
    } else if (other.equals(Long.MIN_VALUE)) {
      return Long.ONE;
    } else {
      // At this point, we have |other| >= 2, so |this/other| < |MIN_VALUE|.
      var halfThis = this.shiftRight(1);
      var approx = halfThis.div(other).shiftLeft(1);
      if (approx.equals(Long.ZERO)) {
        return other.isNegative() ? Long.ONE : Long.NEG_ONE;
      } else {
        var rem = this.subtract(other.multiply(approx));
        var result = approx.add(rem.div(other));
        return result;
      }
    }
  } else if (other.equals(Long.MIN_VALUE)) {
    return Long.ZERO;
  }

  if (this.isNegative()) {
    if (other.isNegative()) {
      return this.negate().div(other.negate());
    } else {
      return this.negate().div(other).negate();
    }
  } else if (other.isNegative()) {
    return this.div(other.negate()).negate();
  }

  // Repeat the following until the remainder is less than other:  find a
  // floating-point that approximates remainder / other *from below*, add this
  // into the result, and subtract it from the remainder.  It is critical that
  // the approximate value is less than or equal to the real value so that the
  // remainder never becomes negative.
  var res = Long.ZERO;
  var rem = this;
  while (rem.greaterThanOrEqual(other)) {
    // Approximate the result of division. This may be a little greater or
    // smaller than the actual value.
    var approx = Math.max(1, Math.floor(rem.toNumber() / other.toNumber()));

    // We will tweak the approximate result by changing it in the 48-th digit or
    // the smallest non-fractional digit, whichever is larger.
    var log2 = Math.ceil(Math.log(approx) / Math.LN2);
    var delta = (log2 <= 48) ? 1 : Math.pow(2, log2 - 48);

    // Decrease the approximation until it is smaller than the remainder.  Note
    // that if it is too large, the product overflows and is negative.
    var approxRes = Long.fromNumber(approx);
    var approxRem = approxRes.multiply(other);
    while (approxRem.isNegative() || approxRem.greaterThan(rem)) {
      approx -= delta;
      approxRes = Long.fromNumber(approx);
      approxRem = approxRes.multiply(other);
    }

    // We know the answer can't be zero... and actually, zero would cause
    // infinite recursion since we would make no progress.
    if (approxRes.isZero()) {
      approxRes = Long.ONE;
    }

    res = res.add(approxRes);
    rem = rem.subtract(approxRem);
  }
  return res;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Long.prototype.equals"></a>[function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>equals (other)](#apidoc.element.mongodb.Long.prototype.equals)
- description and source-code
```javascript
equals = function (other) {
  return (this.high_ == other.high_) && (this.low_ == other.low_);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Long.prototype.getHighBits"></a>[function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>getHighBits ()](#apidoc.element.mongodb.Long.prototype.getHighBits)
- description and source-code
```javascript
getHighBits = function () {
  return this.high_;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Long.prototype.getLowBits"></a>[function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>getLowBits ()](#apidoc.element.mongodb.Long.prototype.getLowBits)
- description and source-code
```javascript
getLowBits = function () {
  return this.low_;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Long.prototype.getLowBitsUnsigned"></a>[function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>getLowBitsUnsigned ()](#apidoc.element.mongodb.Long.prototype.getLowBitsUnsigned)
- description and source-code
```javascript
getLowBitsUnsigned = function () {
  return (this.low_ >= 0) ?
      this.low_ : Long.TWO_PWR_32_DBL_ + this.low_;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Long.prototype.getNumBitsAbs"></a>[function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>getNumBitsAbs ()](#apidoc.element.mongodb.Long.prototype.getNumBitsAbs)
- description and source-code
```javascript
getNumBitsAbs = function () {
  if (this.isNegative()) {
    if (this.equals(Long.MIN_VALUE)) {
      return 64;
    } else {
      return this.negate().getNumBitsAbs();
    }
  } else {
    var val = this.high_ != 0 ? this.high_ : this.low_;
    for (var bit = 31; bit > 0; bit--) {
      if ((val & (1 << bit)) != 0) {
        break;
      }
    }
    return this.high_ != 0 ? bit + 33 : bit + 1;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Long.prototype.greaterThan"></a>[function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>greaterThan (other)](#apidoc.element.mongodb.Long.prototype.greaterThan)
- description and source-code
```javascript
greaterThan = function (other) {
  return this.compare(other) > 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Long.prototype.greaterThanOrEqual"></a>[function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>greaterThanOrEqual (other)](#apidoc.element.mongodb.Long.prototype.greaterThanOrEqual)
- description and source-code
```javascript
greaterThanOrEqual = function (other) {
  return this.compare(other) >= 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Long.prototype.isNegative"></a>[function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>isNegative ()](#apidoc.element.mongodb.Long.prototype.isNegative)
- description and source-code
```javascript
isNegative = function () {
  return this.high_ < 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Long.prototype.isOdd"></a>[function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>isOdd ()](#apidoc.element.mongodb.Long.prototype.isOdd)
- description and source-code
```javascript
isOdd = function () {
  return (this.low_ & 1) == 1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Long.prototype.isZero"></a>[function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>isZero ()](#apidoc.element.mongodb.Long.prototype.isZero)
- description and source-code
```javascript
isZero = function () {
  return this.high_ == 0 && this.low_ == 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Long.prototype.lessThan"></a>[function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>lessThan (other)](#apidoc.element.mongodb.Long.prototype.lessThan)
- description and source-code
```javascript
lessThan = function (other) {
  return this.compare(other) < 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Long.prototype.lessThanOrEqual"></a>[function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>lessThanOrEqual (other)](#apidoc.element.mongodb.Long.prototype.lessThanOrEqual)
- description and source-code
```javascript
lessThanOrEqual = function (other) {
  return this.compare(other) <= 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Long.prototype.modulo"></a>[function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>modulo (other)](#apidoc.element.mongodb.Long.prototype.modulo)
- description and source-code
```javascript
modulo = function (other) {
  return this.subtract(this.div(other).multiply(other));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Long.prototype.multiply"></a>[function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>multiply (other)](#apidoc.element.mongodb.Long.prototype.multiply)
- description and source-code
```javascript
multiply = function (other) {
  if (this.isZero()) {
    return Long.ZERO;
  } else if (other.isZero()) {
    return Long.ZERO;
  }

  if (this.equals(Long.MIN_VALUE)) {
    return other.isOdd() ? Long.MIN_VALUE : Long.ZERO;
  } else if (other.equals(Long.MIN_VALUE)) {
    return this.isOdd() ? Long.MIN_VALUE : Long.ZERO;
  }

  if (this.isNegative()) {
    if (other.isNegative()) {
      return this.negate().multiply(other.negate());
    } else {
      return this.negate().multiply(other).negate();
    }
  } else if (other.isNegative()) {
    return this.multiply(other.negate()).negate();
  }

  // If both Longs are small, use float multiplication
  if (this.lessThan(Long.TWO_PWR_24_) &&
      other.lessThan(Long.TWO_PWR_24_)) {
    return Long.fromNumber(this.toNumber() * other.toNumber());
  }

  // Divide each Long into 4 chunks of 16 bits, and then add up 4x4 products.
  // We can skip products that would overflow.

  var a48 = this.high_ >>> 16;
  var a32 = this.high_ & 0xFFFF;
  var a16 = this.low_ >>> 16;
  var a00 = this.low_ & 0xFFFF;

  var b48 = other.high_ >>> 16;
  var b32 = other.high_ & 0xFFFF;
  var b16 = other.low_ >>> 16;
  var b00 = other.low_ & 0xFFFF;

  var c48 = 0, c32 = 0, c16 = 0, c00 = 0;
  c00 += a00 * b00;
  c16 += c00 >>> 16;
  c00 &= 0xFFFF;
  c16 += a16 * b00;
  c32 += c16 >>> 16;
  c16 &= 0xFFFF;
  c16 += a00 * b16;
  c32 += c16 >>> 16;
  c16 &= 0xFFFF;
  c32 += a32 * b00;
  c48 += c32 >>> 16;
  c32 &= 0xFFFF;
  c32 += a16 * b16;
  c48 += c32 >>> 16;
  c32 &= 0xFFFF;
  c32 += a00 * b32;
  c48 += c32 >>> 16;
  c32 &= 0xFFFF;
  c48 += a48 * b00 + a32 * b16 + a16 * b32 + a00 * b48;
  c48 &= 0xFFFF;
  return Long.fromBits((c16 << 16) | c00, (c48 << 16) | c32);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Long.prototype.negate"></a>[function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>negate ()](#apidoc.element.mongodb.Long.prototype.negate)
- description and source-code
```javascript
negate = function () {
  if (this.equals(Long.MIN_VALUE)) {
    return Long.MIN_VALUE;
  } else {
    return this.not().add(Long.ONE);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Long.prototype.not"></a>[function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>not ()](#apidoc.element.mongodb.Long.prototype.not)
- description and source-code
```javascript
not = function () {
  return Long.fromBits(~this.low_, ~this.high_);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Long.prototype.notEquals"></a>[function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>notEquals (other)](#apidoc.element.mongodb.Long.prototype.notEquals)
- description and source-code
```javascript
notEquals = function (other) {
  return (this.high_ != other.high_) || (this.low_ != other.low_);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Long.prototype.or"></a>[function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>or (other)](#apidoc.element.mongodb.Long.prototype.or)
- description and source-code
```javascript
or = function (other) {
  return Long.fromBits(this.low_ | other.low_, this.high_ | other.high_);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Long.prototype.shiftLeft"></a>[function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>shiftLeft (numBits)](#apidoc.element.mongodb.Long.prototype.shiftLeft)
- description and source-code
```javascript
shiftLeft = function (numBits) {
  numBits &= 63;
  if (numBits == 0) {
    return this;
  } else {
    var low = this.low_;
    if (numBits < 32) {
      var high = this.high_;
      return Long.fromBits(
                 low << numBits,
                 (high << numBits) | (low >>> (32 - numBits)));
    } else {
      return Long.fromBits(0, low << (numBits - 32));
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Long.prototype.shiftRight"></a>[function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>shiftRight (numBits)](#apidoc.element.mongodb.Long.prototype.shiftRight)
- description and source-code
```javascript
shiftRight = function (numBits) {
  numBits &= 63;
  if (numBits == 0) {
    return this;
  } else {
    var high = this.high_;
    if (numBits < 32) {
      var low = this.low_;
      return Long.fromBits(
                 (low >>> numBits) | (high << (32 - numBits)),
                 high >> numBits);
    } else {
      return Long.fromBits(
                 high >> (numBits - 32),
                 high >= 0 ? 0 : -1);
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Long.prototype.shiftRightUnsigned"></a>[function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>shiftRightUnsigned (numBits)](#apidoc.element.mongodb.Long.prototype.shiftRightUnsigned)
- description and source-code
```javascript
shiftRightUnsigned = function (numBits) {
  numBits &= 63;
  if (numBits == 0) {
    return this;
  } else {
    var high = this.high_;
    if (numBits < 32) {
      var low = this.low_;
      return Long.fromBits(
                 (low >>> numBits) | (high << (32 - numBits)),
                 high >>> numBits);
    } else if (numBits == 32) {
      return Long.fromBits(high, 0);
    } else {
      return Long.fromBits(high >>> (numBits - 32), 0);
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Long.prototype.subtract"></a>[function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>subtract (other)](#apidoc.element.mongodb.Long.prototype.subtract)
- description and source-code
```javascript
subtract = function (other) {
  return this.add(other.negate());
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Long.prototype.toInt"></a>[function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>toInt ()](#apidoc.element.mongodb.Long.prototype.toInt)
- description and source-code
```javascript
toInt = function () {
  return this.low_;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Long.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>toJSON ()](#apidoc.element.mongodb.Long.prototype.toJSON)
- description and source-code
```javascript
toJSON = function () {
  return this.toString();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Long.prototype.toNumber"></a>[function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>toNumber ()](#apidoc.element.mongodb.Long.prototype.toNumber)
- description and source-code
```javascript
toNumber = function () {
  return this.high_ * Long.TWO_PWR_32_DBL_ +
         this.getLowBitsUnsigned();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Long.prototype.toString"></a>[function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>toString (opt_radix)](#apidoc.element.mongodb.Long.prototype.toString)
- description and source-code
```javascript
toString = function (opt_radix) {
  var radix = opt_radix || 10;
  if (radix < 2 || 36 < radix) {
    throw Error('radix out of range: ' + radix);
  }

  if (this.isZero()) {
    return '0';
  }

  if (this.isNegative()) {
    if (this.equals(Long.MIN_VALUE)) {
      // We need to change the Long value before it can be negated, so we remove
      // the bottom-most digit in this base and then recurse to do the rest.
      var radixLong = Long.fromNumber(radix);
      var div = this.div(radixLong);
      var rem = div.multiply(radixLong).subtract(this);
      return div.toString(radix) + rem.toInt().toString(radix);
    } else {
      return '-' + this.negate().toString(radix);
    }
  }

  // Do several (6) digits each time through the loop, so as to
  // minimize the calls to the very expensive emulated div.
  var radixToPower = Long.fromNumber(Math.pow(radix, 6));

  var rem = this;
  var result = '';
  while (true) {
    var remDiv = rem.div(radixToPower);
    var intval = rem.subtract(remDiv.multiply(radixToPower)).toInt();
    var digits = intval.toString(radix);

    rem = remDiv;
    if (rem.isZero()) {
      return digits + result;
    } else {
      while (digits.length < 6) {
        digits = '0' + digits;
      }
      result = '' + digits + result;
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Long.prototype.xor"></a>[function <span class="apidocSignatureSpan">mongodb.Long.prototype.</span>xor (other)](#apidoc.element.mongodb.Long.prototype.xor)
- description and source-code
```javascript
xor = function (other) {
  return Long.fromBits(this.low_ ^ other.low_, this.high_ ^ other.high_);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.Map"></a>[module mongodb.Map](#apidoc.module.mongodb.Map)

#### <a name="apidoc.element.mongodb.Map.Map"></a>[function <span class="apidocSignatureSpan">mongodb.</span>Map ()](#apidoc.element.mongodb.Map.Map)
- description and source-code
```javascript
function Map() { [native code] }
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.MaxKey"></a>[module mongodb.MaxKey](#apidoc.module.mongodb.MaxKey)

#### <a name="apidoc.element.mongodb.MaxKey.MaxKey"></a>[function <span class="apidocSignatureSpan">mongodb.</span>MaxKey ()](#apidoc.element.mongodb.MaxKey.MaxKey)
- description and source-code
```javascript
function MaxKey() {
  if(!(this instanceof MaxKey)) return new MaxKey();

  this._bsontype = 'MaxKey';
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.MinKey"></a>[module mongodb.MinKey](#apidoc.module.mongodb.MinKey)

#### <a name="apidoc.element.mongodb.MinKey.MinKey"></a>[function <span class="apidocSignatureSpan">mongodb.</span>MinKey ()](#apidoc.element.mongodb.MinKey.MinKey)
- description and source-code
```javascript
function MinKey() {
  if(!(this instanceof MinKey)) return new MinKey();

  this._bsontype = 'MinKey';
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.MongoClient"></a>[module mongodb.MongoClient](#apidoc.module.mongodb.MongoClient)

#### <a name="apidoc.element.mongodb.MongoClient.MongoClient"></a>[function <span class="apidocSignatureSpan">mongodb.</span>MongoClient ()](#apidoc.element.mongodb.MongoClient.MongoClient)
- description and source-code
```javascript
function MongoClient() {
<span class="apidocCodeCommentSpan">  /**
   * The callback format for results
   * @callback MongoClient~connectCallback
   * @param {MongoError} error An error instance representing the error during the execution.
   * @param {Db} db The connected database.
   */
</span>
  /**
   * Connect to MongoDB using a url as documented at
   *
   *  docs.mongodb.org/manual/reference/connection-string/
   *
   * Note that for replicasets the replicaSet query parameter is required in the 2.0 driver
   *
   * @method
   * @param {string} url The connection URI string
   * @param {object} [options] Optional settings.
   * @param {number} [options.poolSize=5] poolSize The maximum size of the individual server pool.
   * @param {boolean} [options.ssl=false] Enable SSL connection.
   * @param {Buffer} [options.sslCA=undefined] SSL Certificate store binary buffer
   * @param {Buffer} [options.sslCRL=undefined] SSL Certificate revocation list binary buffer
   * @param {Buffer} [options.sslCert=undefined] SSL Certificate binary buffer
   * @param {Buffer} [options.sslKey=undefined] SSL Key file binary buffer
   * @param {string} [options.sslPass=undefined] SSL Certificate pass phrase
   * @param {boolean|function} [options.checkServerIdentity=true] Ensure we check server identify during SSL, set to false to disable
 checking. Only works for Node 0.12.x or higher. You can pass in a boolean or your own checkServerIdentity override function.
   * @param {boolean} [options.autoReconnect=true] Enable autoReconnect for single server instances
   * @param {boolean} [options.noDelay=true] TCP Connection no delay
   * @param {boolean} [options.keepAlive=0] The number of milliseconds to wait before initiating keepAlive on the TCP socket.
   * @param {number} [options.connectTimeoutMS=30000] TCP Connection timeout setting
   * @param {number} [options.socketTimeoutMS=30000] TCP Socket timeout setting
   * @param {number} [options.reconnectTries=30] Server attempt to reconnect #times
   * @param {number} [options.reconnectInterval=1000] Server will wait # milliseconds between retries
   * @param {boolean} [options.ha=true] Control if high availability monitoring runs for Replicaset or Mongos proxies.
   * @param {number} [options.haInterval=10000] The High availability period for replicaset inquiry
   * @param {string} [options.replicaSet=undefined] The Replicaset set name
   * @param {number} [options.secondaryAcceptableLatencyMS=15] Cutoff latency point in MS for Replicaset member selection
   * @param {number} [options.acceptableLatencyMS=15] Cutoff latency point in MS for Mongos proxies selection.
   * @param {boolean} [options.connectWithNoPrimary=false] Sets if the driver should connect even if no primary is available
   * @param {string} [options.authSource=undefined] Define the database to authenticate against
   * @param {(number|string)} [options.w=null] The write concern.
   * @param {number} [options.wtimeout=null] The write concern timeout.
   * @param {boolean} [options.j=false] Specify a journal write concern.
   * @param {boolean} [options.forceServerObjectId=false] Force server to assign _id values instead of driver.
   * @param {boolean} [options.serializeFunctions=false] Serialize functions on any object.
   * @param {Boolean} [options.ignoreUndefined=false] Specify if the BSON serializer should ignore undefined fields.
   * @param {boolean} [options.raw=false] Return document results as raw BSON buffers.
   * @param {boolean} [options.promoteLongs=true] Promotes Long values to number if they fit inside the 53 bits resolution.
   * @param {boolean} [options.promoteBuffers=false] Promotes Binary BSON values to native Node Buffers.
   * @param {boolean} [options.promoteValues=true] Promotes BSON values to native types where possible, set to false to only receive
 wrapper types.
   * @param {number} [options.bufferMaxEntries=-1] Sets a cap on how many operations the driver will buffer up before giving up
on getting a working connection, default is -1 which is unlimited.
   * @param {(ReadPreference|string)} [options.readPreference=null] The preferred ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.MongoClient.connect"></a>[function <span class="apidocSignatureSpan">mongodb.MongoClient.</span>connect (url, options, callback)](#apidoc.element.mongodb.MongoClient.connect)
- description and source-code
```javascript
connect = function (url, options, callback) {
  var args = Array.prototype.slice.call(arguments, 1);
  callback = typeof args[args.length - 1] == 'function' ? args.pop() : null;
  options = args.length ? args.shift() : null;
  options = options || {};

  // Validate options object
  var err = validOptions(options);

  // Get the promiseLibrary
  var promiseLibrary = options.promiseLibrary;

  // No promise library selected fall back
  if(!promiseLibrary) {
    promiseLibrary = typeof global.Promise == 'function' ?
      global.Promise : require('es6-promise').Promise;
  }

  // Return a promise
  if(typeof callback != 'function') {
    return new promiseLibrary(function(resolve, reject) {
      // Did we have a validation error
      if(err) return reject(err);
      // Attempt to connect
      connect(url, options, function(err, db) {
        if(err) return reject(err);
        resolve(db);
      });
    });
  }

  // Did we have a validation error
  if(err) return callback(err);
  // Fallback to callback based connect
  connect(url, options, callback);
}
```
- example usage
```shell
...
'''js
var MongoClient = require('mongodb').MongoClient
  , assert = require('assert');

// Connection URL
var url = 'mongodb://localhost:27017/myproject';
// Use connect method to connect to the Server
MongoClient.connect(url, function(err, db) {
  assert.equal(null, err);
  console.log("Connected correctly to server");

  db.close();
});
'''
...
```



# <a name="apidoc.module.mongodb.MongoClient.define"></a>[module mongodb.MongoClient.define](#apidoc.module.mongodb.MongoClient.define)

#### <a name="apidoc.element.mongodb.MongoClient.define.object"></a>[function <span class="apidocSignatureSpan">mongodb.MongoClient.define.</span>object ()](#apidoc.element.mongodb.MongoClient.define.object)
- description and source-code
```javascript
function MongoClient() {
<span class="apidocCodeCommentSpan">  /**
   * The callback format for results
   * @callback MongoClient~connectCallback
   * @param {MongoError} error An error instance representing the error during the execution.
   * @param {Db} db The connected database.
   */
</span>
  /**
   * Connect to MongoDB using a url as documented at
   *
   *  docs.mongodb.org/manual/reference/connection-string/
   *
   * Note that for replicasets the replicaSet query parameter is required in the 2.0 driver
   *
   * @method
   * @param {string} url The connection URI string
   * @param {object} [options] Optional settings.
   * @param {number} [options.poolSize=5] poolSize The maximum size of the individual server pool.
   * @param {boolean} [options.ssl=false] Enable SSL connection.
   * @param {Buffer} [options.sslCA=undefined] SSL Certificate store binary buffer
   * @param {Buffer} [options.sslCRL=undefined] SSL Certificate revocation list binary buffer
   * @param {Buffer} [options.sslCert=undefined] SSL Certificate binary buffer
   * @param {Buffer} [options.sslKey=undefined] SSL Key file binary buffer
   * @param {string} [options.sslPass=undefined] SSL Certificate pass phrase
   * @param {boolean|function} [options.checkServerIdentity=true] Ensure we check server identify during SSL, set to false to disable
 checking. Only works for Node 0.12.x or higher. You can pass in a boolean or your own checkServerIdentity override function.
   * @param {boolean} [options.autoReconnect=true] Enable autoReconnect for single server instances
   * @param {boolean} [options.noDelay=true] TCP Connection no delay
   * @param {boolean} [options.keepAlive=0] The number of milliseconds to wait before initiating keepAlive on the TCP socket.
   * @param {number} [options.connectTimeoutMS=30000] TCP Connection timeout setting
   * @param {number} [options.socketTimeoutMS=30000] TCP Socket timeout setting
   * @param {number} [options.reconnectTries=30] Server attempt to reconnect #times
   * @param {number} [options.reconnectInterval=1000] Server will wait # milliseconds between retries
   * @param {boolean} [options.ha=true] Control if high availability monitoring runs for Replicaset or Mongos proxies.
   * @param {number} [options.haInterval=10000] The High availability period for replicaset inquiry
   * @param {string} [options.replicaSet=undefined] The Replicaset set name
   * @param {number} [options.secondaryAcceptableLatencyMS=15] Cutoff latency point in MS for Replicaset member selection
   * @param {number} [options.acceptableLatencyMS=15] Cutoff latency point in MS for Mongos proxies selection.
   * @param {boolean} [options.connectWithNoPrimary=false] Sets if the driver should connect even if no primary is available
   * @param {string} [options.authSource=undefined] Define the database to authenticate against
   * @param {(number|string)} [options.w=null] The write concern.
   * @param {number} [options.wtimeout=null] The write concern timeout.
   * @param {boolean} [options.j=false] Specify a journal write concern.
   * @param {boolean} [options.forceServerObjectId=false] Force server to assign _id values instead of driver.
   * @param {boolean} [options.serializeFunctions=false] Serialize functions on any object.
   * @param {Boolean} [options.ignoreUndefined=false] Specify if the BSON serializer should ignore undefined fields.
   * @param {boolean} [options.raw=false] Return document results as raw BSON buffers.
   * @param {boolean} [options.promoteLongs=true] Promotes Long values to number if they fit inside the 53 bits resolution.
   * @param {boolean} [options.promoteBuffers=false] Promotes Binary BSON values to native Node Buffers.
   * @param {boolean} [options.promoteValues=true] Promotes BSON values to native types where possible, set to false to only receive
 wrapper types.
   * @param {number} [options.bufferMaxEntries=-1] Sets a cap on how many operations the driver will buffer up before giving up
on getting a working connection, default is -1 which is unlimited.
   * @param {(ReadPreference|string)} [options.readPreference=null] The preferred ...
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.MongoError"></a>[module mongodb.MongoError](#apidoc.module.mongodb.MongoError)

#### <a name="apidoc.element.mongodb.MongoError.MongoError"></a>[function <span class="apidocSignatureSpan">mongodb.</span>MongoError (message)](#apidoc.element.mongodb.MongoError.MongoError)
- description and source-code
```javascript
function MongoError(message) {
  this.name = 'MongoError';
  this.message = message;
  Error.captureStackTrace(this, MongoError);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.MongoError.create"></a>[function <span class="apidocSignatureSpan">mongodb.MongoError.</span>create (options)](#apidoc.element.mongodb.MongoError.create)
- description and source-code
```javascript
create = function (options) {
  var err = null;

  if(options instanceof Error) {
    err = new MongoError(options.message);
    err.stack = options.stack;
  } else if(typeof options == 'string') {
    err = new MongoError(options);
  } else {
    err = new MongoError(options.message || options.errmsg || options.$err || "n/a");
    // Other options
    for(var name in options) {
      err[name] = options[name];
    }
  }

  return err;
}
```
- example usage
```shell
...
 * Set the batch size for the cursor.
 * @method
 * @param {number} value The batchSize for the cursor.
 * @throws {MongoError}
 * @return {AggregationCursor}
 */
AggregationCursor.prototype.batchSize = function(value) {
  if(this.s.state == AggregationCursor.CLOSED || this.isDead()) throw MongoError.create({message: "Cursor is closed", driver:true
 });
  if(typeof value != 'number') throw MongoError.create({message: "batchSize requires an integer", drvier:true });
  if(this.s.cmd.cursor) this.s.cmd.cursor.batchSize = value;
  this.setCursorBatchSize(value);
  return this;
}

define.classMethod('batchSize', {callback: false, promise:false, returns: [AggregationCursor]});
...
```



# <a name="apidoc.module.mongodb.Mongos"></a>[module mongodb.Mongos](#apidoc.module.mongodb.Mongos)

#### <a name="apidoc.element.mongodb.Mongos.Mongos"></a>[function <span class="apidocSignatureSpan">mongodb.</span>Mongos (servers, options)](#apidoc.element.mongodb.Mongos.Mongos)
- description and source-code
```javascript
Mongos = function (servers, options) {
  if(!(this instanceof Mongos)) return new Mongos(servers, options);
  options = options || {};
  var self = this;

  // Filter the options
  options = filterOptions(options, legalOptionNames);

  // Ensure all the instances are Server
  for(var i = 0; i < servers.length; i++) {
    if(!(servers[i] instanceof Server)) {
      throw MongoError.create({message: "all seed list instances must be of the Server type", driver:true});
    }
  }

  // Stored options
  var storeOptions = {
      force: false
    , bufferMaxEntries: typeof options.bufferMaxEntries == 'number' ? options.bufferMaxEntries : MAX_JS_INT
  }

  // Shared global store
  var store = options.store || new Store(self, storeOptions);

  // Set up event emitter
  EventEmitter.call(this);

  // Build seed list
  var seedlist = servers.map(function(x) {
    return {host: x.host, port: x.port}
  });

  // Get the reconnect option
  var reconnect = typeof options.auto_reconnect == 'boolean' ? options.auto_reconnect : true;
  reconnect = typeof options.autoReconnect == 'boolean' ? options.autoReconnect : reconnect;

  // Clone options
  var clonedOptions = mergeOptions({}, {
    disconnectHandler: store,
    cursorFactory: Cursor,
    reconnect: reconnect,
    emitError: typeof options.emitError == 'boolean' ? options.emitError : true,
    size: typeof options.poolSize == 'number' ? options.poolSize : 5
  });

  // Translate any SSL options and other connectivity options
  clonedOptions = translateOptions(clonedOptions, options);

  // Socket options
  var socketOptions = options.socketOptions && Object.keys(options.socketOptions).length > 0
    ? options.socketOptions : options;

  // Translate all the options to the mongodb-core ones
  clonedOptions = translateOptions(clonedOptions, socketOptions);
  if(typeof clonedOptions.keepAlive == 'number') {
    clonedOptions.keepAliveInitialDelay = clonedOptions.keepAlive;
    clonedOptions.keepAlive = clonedOptions.keepAlive > 0;
  }

  // Build default client information
  this.clientInfo = {
    driver: {
      name: "nodejs",
      version: driverVersion
    },
    os: {
      type: type,
      name: name,
      architecture: architecture,
      version: release
    },
    platform: nodejsversion
  }

  // Build default client information
  clonedOptions.clientInfo = this.clientInfo;
  // Do we have an application specific string
  if(options.appname) {
    clonedOptions.clientInfo.application = { name: options.appname };
  }

  // Create the Mongos
  var mongos = new CMongos(seedlist, clonedOptions)
  // Server capabilities
  var sCapabilities = null;

  // Internal state
  this.s = {
    // Create the Mongos
      mongos: mongos
    // Server capabilities
    , sCapabilities: sCapabilities
    // Debug turned on
    , debug: clonedOptions.debug
    // Store option defaults
    , storeOptions: storeOptions
    // Cloned options
    , clonedOptions: clonedOptions
    // Actual store of callbacks
    , store: store
    // Options
    , options: options
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Mongos.super_"></a>[function <span class="apidocSignatureSpan">mongodb.Mongos.</span>super_ ()](#apidoc.element.mongodb.Mongos.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.Mongos.define"></a>[module mongodb.Mongos.define](#apidoc.module.mongodb.Mongos.define)

#### <a name="apidoc.element.mongodb.Mongos.define.object"></a>[function <span class="apidocSignatureSpan">mongodb.Mongos.define.</span>object (servers, options)](#apidoc.element.mongodb.Mongos.define.object)
- description and source-code
```javascript
object = function (servers, options) {
  if(!(this instanceof Mongos)) return new Mongos(servers, options);
  options = options || {};
  var self = this;

  // Filter the options
  options = filterOptions(options, legalOptionNames);

  // Ensure all the instances are Server
  for(var i = 0; i < servers.length; i++) {
    if(!(servers[i] instanceof Server)) {
      throw MongoError.create({message: "all seed list instances must be of the Server type", driver:true});
    }
  }

  // Stored options
  var storeOptions = {
      force: false
    , bufferMaxEntries: typeof options.bufferMaxEntries == 'number' ? options.bufferMaxEntries : MAX_JS_INT
  }

  // Shared global store
  var store = options.store || new Store(self, storeOptions);

  // Set up event emitter
  EventEmitter.call(this);

  // Build seed list
  var seedlist = servers.map(function(x) {
    return {host: x.host, port: x.port}
  });

  // Get the reconnect option
  var reconnect = typeof options.auto_reconnect == 'boolean' ? options.auto_reconnect : true;
  reconnect = typeof options.autoReconnect == 'boolean' ? options.autoReconnect : reconnect;

  // Clone options
  var clonedOptions = mergeOptions({}, {
    disconnectHandler: store,
    cursorFactory: Cursor,
    reconnect: reconnect,
    emitError: typeof options.emitError == 'boolean' ? options.emitError : true,
    size: typeof options.poolSize == 'number' ? options.poolSize : 5
  });

  // Translate any SSL options and other connectivity options
  clonedOptions = translateOptions(clonedOptions, options);

  // Socket options
  var socketOptions = options.socketOptions && Object.keys(options.socketOptions).length > 0
    ? options.socketOptions : options;

  // Translate all the options to the mongodb-core ones
  clonedOptions = translateOptions(clonedOptions, socketOptions);
  if(typeof clonedOptions.keepAlive == 'number') {
    clonedOptions.keepAliveInitialDelay = clonedOptions.keepAlive;
    clonedOptions.keepAlive = clonedOptions.keepAlive > 0;
  }

  // Build default client information
  this.clientInfo = {
    driver: {
      name: "nodejs",
      version: driverVersion
    },
    os: {
      type: type,
      name: name,
      architecture: architecture,
      version: release
    },
    platform: nodejsversion
  }

  // Build default client information
  clonedOptions.clientInfo = this.clientInfo;
  // Do we have an application specific string
  if(options.appname) {
    clonedOptions.clientInfo.application = { name: options.appname };
  }

  // Create the Mongos
  var mongos = new CMongos(seedlist, clonedOptions)
  // Server capabilities
  var sCapabilities = null;

  // Internal state
  this.s = {
    // Create the Mongos
      mongos: mongos
    // Server capabilities
    , sCapabilities: sCapabilities
    // Debug turned on
    , debug: clonedOptions.debug
    // Store option defaults
    , storeOptions: storeOptions
    // Cloned options
    , clonedOptions: clonedOptions
    // Actual store of callbacks
    , store: store
    // Options
    , options: options
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.Mongos.prototype"></a>[module mongodb.Mongos.prototype](#apidoc.module.mongodb.Mongos.prototype)

#### <a name="apidoc.element.mongodb.Mongos.prototype.auth"></a>[function <span class="apidocSignatureSpan">mongodb.Mongos.prototype.</span>auth ()](#apidoc.element.mongodb.Mongos.prototype.auth)
- description and source-code
```javascript
auth = function () {
  var args = Array.prototype.slice.call(arguments, 0);
  this.s.mongos.auth.apply(this.s.mongos, args);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Mongos.prototype.capabilities"></a>[function <span class="apidocSignatureSpan">mongodb.Mongos.prototype.</span>capabilities ()](#apidoc.element.mongodb.Mongos.prototype.capabilities)
- description and source-code
```javascript
capabilities = function () {
  if(this.s.sCapabilities) return this.s.sCapabilities;
  if(this.s.mongos.lastIsMaster() == null) return null;
  this.s.sCapabilities = new ServerCapabilities(this.s.mongos.lastIsMaster());
  return this.s.sCapabilities;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Mongos.prototype.close"></a>[function <span class="apidocSignatureSpan">mongodb.Mongos.prototype.</span>close (forceClosed)](#apidoc.element.mongodb.Mongos.prototype.close)
- description and source-code
```javascript
close = function (forceClosed) {
  this.s.mongos.destroy({
    force: typeof forceClosed == 'boolean' ? forceClosed : false,
  });
  // We need to wash out all stored processes
  if(forceClosed == true) {
    this.s.storeOptions.force = forceClosed;
    this.s.store.flush();
  }
}
```
- example usage
```shell
...
// Connection URL
var url = 'mongodb://localhost:27017/myproject';
// Use connect method to connect to the Server
MongoClient.connect(url, function(err, db) {
  assert.equal(null, err);
  console.log("Connected correctly to server");

  db.close();
});
'''

Given that you booted up the **mongod** process earlier the application should connect successfully and print **Connected correctly
 to server** to the console.

Let's Add some code to show the different CRUD operations available.
...
```

#### <a name="apidoc.element.mongodb.Mongos.prototype.command"></a>[function <span class="apidocSignatureSpan">mongodb.Mongos.prototype.</span>command (ns, cmd, options, callback)](#apidoc.element.mongodb.Mongos.prototype.command)
- description and source-code
```javascript
command = function (ns, cmd, options, callback) {
  this.s.mongos.command(ns, cmd, getReadPreference(options), callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Mongos.prototype.connect"></a>[function <span class="apidocSignatureSpan">mongodb.Mongos.prototype.</span>connect (db, _options, callback)](#apidoc.element.mongodb.Mongos.prototype.connect)
- description and source-code
```javascript
connect = function (db, _options, callback) {
  var self = this;
  if('function' === typeof _options) callback = _options, _options = {};
  if(_options == null) _options = {};
  if(!('function' === typeof callback)) callback = null;
  self.s.options = _options;

  // Update bufferMaxEntries
  self.s.storeOptions.bufferMaxEntries = db.bufferMaxEntries;

  // Error handler
  var connectErrorHandler = function() {
    return function(err) {
      // Remove all event handlers
      var events = ['timeout', 'error', 'close'];
      events.forEach(function(e) {
        self.removeListener(e, connectErrorHandler);
      });

      self.s.mongos.removeListener('connect', connectErrorHandler);

      // Try to callback
      try {
        callback(err);
      } catch(err) {
        process.nextTick(function() { throw err; })
      }
    }
  }

  // Actual handler
  var errorHandler = function(event) {
    return function(err) {
      if(event != 'error') {
        self.emit(event, err);
      }
    }
  }

  // Error handler
  var reconnectHandler = function() {
    self.emit('reconnect');
    self.s.store.execute();
  }

  // relay the event
  var relay = function(event) {
    return function(t, server) {
      self.emit(event, t, server);
    }
  }

  // Connect handler
  var connectHandler = function() {
    // Clear out all the current handlers left over
    ["timeout", "error", "close", 'serverOpening', 'serverDescriptionChanged', 'serverHeartbeatStarted',
      'serverHeartbeatSucceeded', 'serverHeartbeatFailed', 'serverClosed', 'topologyOpening',
      'topologyClosed', 'topologyDescriptionChanged'].forEach(function(e) {
      self.s.mongos.removeAllListeners(e);
    });

    // Set up listeners
    self.s.mongos.once('timeout', errorHandler('timeout'));
    self.s.mongos.once('error', errorHandler('error'));
    self.s.mongos.once('close', errorHandler('close'));

    // Set up SDAM listeners
    self.s.mongos.on('serverDescriptionChanged', relay('serverDescriptionChanged'));
    self.s.mongos.on('serverHeartbeatStarted', relay('serverHeartbeatStarted'));
    self.s.mongos.on('serverHeartbeatSucceeded', relay('serverHeartbeatSucceeded'));
    self.s.mongos.on('serverHeartbeatFailed', relay('serverHeartbeatFailed'));
    self.s.mongos.on('serverOpening', relay('serverOpening'));
    self.s.mongos.on('serverClosed', relay('serverClosed'));
    self.s.mongos.on('topologyOpening', relay('topologyOpening'));
    self.s.mongos.on('topologyClosed', relay('topologyClosed'));
    self.s.mongos.on('topologyDescriptionChanged', relay('topologyDescriptionChanged'));

    // Set up serverConfig listeners
    self.s.mongos.on('fullsetup', relay('fullsetup'));

    // Emit open event
    self.emit('open', null, self);

    // Return correctly
    try {
      callback(null, self);
    } catch(err) {
      process.nextTick(function() { throw err; })
    }
  }

  // Set up listeners
  self.s.mongos.once('timeout', connectErrorHandler('timeout'));
  self.s.mongos.once('error', connectErrorHandler('error'));
  self.s.mongos.once('close', connectErrorHandler('close'));
  self.s.mongos.once('connect', connectHandler);
  // Join and leave events
  self.s.mongos.on('joined', relay('joined'));
  self.s.mongos.on('left', relay('left'));

  // Reconnect server
  self.s.mongos.on('reconnect', reconnectHandler);

  // Start connection
  self.s.mongos.connect(_options);
}
```
- example usage
```shell
...
'''js
var MongoClient = require('mongodb').MongoClient
  , assert = require('assert');

// Connection URL
var url = 'mongodb://localhost:27017/myproject';
// Use connect method to connect to the Server
MongoClient.connect(url, function(err, db) {
  assert.equal(null, err);
  console.log("Connected correctly to server");

  db.close();
});
'''
...
```

#### <a name="apidoc.element.mongodb.Mongos.prototype.connections"></a>[function <span class="apidocSignatureSpan">mongodb.Mongos.prototype.</span>connections ()](#apidoc.element.mongodb.Mongos.prototype.connections)
- description and source-code
```javascript
connections = function () {
  return this.s.mongos.connections();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Mongos.prototype.cursor"></a>[function <span class="apidocSignatureSpan">mongodb.Mongos.prototype.</span>cursor (ns, cmd, options)](#apidoc.element.mongodb.Mongos.prototype.cursor)
- description and source-code
```javascript
cursor = function (ns, cmd, options) {
  options.disconnectHandler = this.s.store;
  return this.s.mongos.cursor(ns, cmd, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Mongos.prototype.insert"></a>[function <span class="apidocSignatureSpan">mongodb.Mongos.prototype.</span>insert (ns, ops, options, callback)](#apidoc.element.mongodb.Mongos.prototype.insert)
- description and source-code
```javascript
insert = function (ns, ops, options, callback) {
  this.s.mongos.insert(ns, ops, options, function(e, m) {
    callback(e, m)
  });
}
```
- example usage
```shell
...
* // Connection url
* var url = 'mongodb://localhost:27017/test';
* // Connect using MongoClient
* MongoClient.connect(url, function(err, db) {
*   // Create a collection we want to drop later
*   var col = db.collection('createIndexExample1');
*   // Insert a bunch of documents
*   col.insert([{a:1, b:1}
*     , {a:2, b:2}, {a:3, b:3}
*     , {a:4, b:4}], {w:1}, function(err, result) {
*     test.equal(null, err);
*     // Show that duplicate records got dropped
*     col.aggregation({}, {cursor: {}}).toArray(function(err, items) {
*       test.equal(null, err);
*       test.equal(4, items.length);
...
```

#### <a name="apidoc.element.mongodb.Mongos.prototype.isConnected"></a>[function <span class="apidocSignatureSpan">mongodb.Mongos.prototype.</span>isConnected ()](#apidoc.element.mongodb.Mongos.prototype.isConnected)
- description and source-code
```javascript
isConnected = function () {
  return this.s.mongos.isConnected();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Mongos.prototype.isDestroyed"></a>[function <span class="apidocSignatureSpan">mongodb.Mongos.prototype.</span>isDestroyed ()](#apidoc.element.mongodb.Mongos.prototype.isDestroyed)
- description and source-code
```javascript
isDestroyed = function () {
  return this.s.mongos.isDestroyed();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Mongos.prototype.lastIsMaster"></a>[function <span class="apidocSignatureSpan">mongodb.Mongos.prototype.</span>lastIsMaster ()](#apidoc.element.mongodb.Mongos.prototype.lastIsMaster)
- description and source-code
```javascript
lastIsMaster = function () {
  return this.s.mongos.lastIsMaster();
}
```
- example usage
```shell
...
/**
 * Add a maxTimeMS stage to the aggregation pipeline
 * @method
 * @param {number} value The state maxTimeMS value.
 * @return {AggregationCursor}
 */
AggregationCursor.prototype.maxTimeMS = function(value) {
  if(this.s.topology.lastIsMaster().minWireVersion > 2) {
    this.s.cmd.maxTimeMS = value;
  }
  return this;
}

define.classMethod('maxTimeMS', {callback: false, promise:false, returns: [AggregationCursor]});
...
```

#### <a name="apidoc.element.mongodb.Mongos.prototype.logout"></a>[function <span class="apidocSignatureSpan">mongodb.Mongos.prototype.</span>logout ()](#apidoc.element.mongodb.Mongos.prototype.logout)
- description and source-code
```javascript
logout = function () {
  var args = Array.prototype.slice.call(arguments, 0);
  this.s.mongos.logout.apply(this.s.mongos, args);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Mongos.prototype.remove"></a>[function <span class="apidocSignatureSpan">mongodb.Mongos.prototype.</span>remove (ns, ops, options, callback)](#apidoc.element.mongodb.Mongos.prototype.remove)
- description and source-code
```javascript
remove = function (ns, ops, options, callback) {
  this.s.mongos.remove(ns, ops, options, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Mongos.prototype.unref"></a>[function <span class="apidocSignatureSpan">mongodb.Mongos.prototype.</span>unref ()](#apidoc.element.mongodb.Mongos.prototype.unref)
- description and source-code
```javascript
unref = function () {
  return this.s.mongos.unref();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Mongos.prototype.update"></a>[function <span class="apidocSignatureSpan">mongodb.Mongos.prototype.</span>update (ns, ops, options, callback)](#apidoc.element.mongodb.Mongos.prototype.update)
- description and source-code
```javascript
update = function (ns, ops, options, callback) {
  this.s.mongos.update(ns, ops, options, callback);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.ObjectID"></a>[module mongodb.ObjectID](#apidoc.module.mongodb.ObjectID)

#### <a name="apidoc.element.mongodb.ObjectID.ObjectID"></a>[function <span class="apidocSignatureSpan">mongodb.</span>ObjectID (id)](#apidoc.element.mongodb.ObjectID.ObjectID)
- description and source-code
```javascript
function ObjectID(id) {
  // Duck-typing to support ObjectId from different npm packages
  if(id instanceof ObjectID) return id;
  if(!(this instanceof ObjectID)) return new ObjectID(id);

  this._bsontype = 'ObjectID';

  // The most common usecase (blank id, new objectId instance)
  if(id == null || typeof id == 'number') {
    // Generate a new id
    this.id = this.generate(id);
    // If we are caching the hex string
    if(ObjectID.cacheHexString) this.__id = this.toString('hex');
    // Return the object
    return;
  }

  // Check if the passed in id is valid
  var valid = ObjectID.isValid(id);

  // Throw an error if it's not a valid setup
  if(!valid && id != null){
    throw new Error("Argument passed in must be a single String of 12 bytes or a string of 24 hex characters");
  } else if(valid && typeof id == 'string' && id.length == 24 && hasBufferType) {
    return new ObjectID(new Buffer(id, 'hex'));
  } else if(valid && typeof id == 'string' && id.length == 24) {
    return ObjectID.createFromHexString(id);
  } else if(id != null && id.length === 12) {
    // assume 12 byte string
    this.id = id;
  } else if(id != null && id.toHexString) {
    // Duck-typing to support ObjectId from different npm packages
    return id;
  } else {
    throw new Error("Argument passed in must be a single String of 12 bytes or a string of 24 hex characters");
  }

  if(ObjectID.cacheHexString) this.__id = this.toString('hex');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.ObjectID.ObjectId"></a>[function <span class="apidocSignatureSpan">mongodb.ObjectID.</span>ObjectId (id)](#apidoc.element.mongodb.ObjectID.ObjectId)
- description and source-code
```javascript
function ObjectID(id) {
  // Duck-typing to support ObjectId from different npm packages
  if(id instanceof ObjectID) return id;
  if(!(this instanceof ObjectID)) return new ObjectID(id);

  this._bsontype = 'ObjectID';

  // The most common usecase (blank id, new objectId instance)
  if(id == null || typeof id == 'number') {
    // Generate a new id
    this.id = this.generate(id);
    // If we are caching the hex string
    if(ObjectID.cacheHexString) this.__id = this.toString('hex');
    // Return the object
    return;
  }

  // Check if the passed in id is valid
  var valid = ObjectID.isValid(id);

  // Throw an error if it's not a valid setup
  if(!valid && id != null){
    throw new Error("Argument passed in must be a single String of 12 bytes or a string of 24 hex characters");
  } else if(valid && typeof id == 'string' && id.length == 24 && hasBufferType) {
    return new ObjectID(new Buffer(id, 'hex'));
  } else if(valid && typeof id == 'string' && id.length == 24) {
    return ObjectID.createFromHexString(id);
  } else if(id != null && id.length === 12) {
    // assume 12 byte string
    this.id = id;
  } else if(id != null && id.toHexString) {
    // Duck-typing to support ObjectId from different npm packages
    return id;
  } else {
    throw new Error("Argument passed in must be a single String of 12 bytes or a string of 24 hex characters");
  }

  if(ObjectID.cacheHexString) this.__id = this.toString('hex');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.ObjectID.createFromHexString"></a>[function <span class="apidocSignatureSpan">mongodb.ObjectID.</span>createFromHexString (string)](#apidoc.element.mongodb.ObjectID.createFromHexString)
- description and source-code
```javascript
function createFromHexString(string) {
  // Throw an error if it's not a valid setup
  if(typeof string === 'undefined' || string != null && string.length != 24) {
    throw new Error("Argument passed in must be a single String of 12 bytes or a string of 24 hex characters");
  }

  // Use Buffer.from method if available
  if(hasBufferType) return new ObjectID(new Buffer(string, 'hex'));

  // Calculate lengths
  var array = new _Buffer(12);
  var n = 0;
  var i = 0;

  while (i < 24) {
    array[n++] = decodeLookup[string.charCodeAt(i++)] << 4 | decodeLookup[string.charCodeAt(i++)]
  }

  return new ObjectID(array);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.ObjectID.createFromTime"></a>[function <span class="apidocSignatureSpan">mongodb.ObjectID.</span>createFromTime (time)](#apidoc.element.mongodb.ObjectID.createFromTime)
- description and source-code
```javascript
function createFromTime(time) {
  var buffer = new Buffer([0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0]);
  // Encode time into first 4 bytes
  buffer[3] = time & 0xff;
  buffer[2] = (time >> 8) & 0xff;
  buffer[1] = (time >> 16) & 0xff;
  buffer[0] = (time >> 24) & 0xff;
  // Return the new objectId
  return new ObjectID(buffer);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.ObjectID.createPk"></a>[function <span class="apidocSignatureSpan">mongodb.ObjectID.</span>createPk ()](#apidoc.element.mongodb.ObjectID.createPk)
- description and source-code
```javascript
function createPk() {
  return new ObjectID();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.ObjectID.isValid"></a>[function <span class="apidocSignatureSpan">mongodb.ObjectID.</span>isValid (id)](#apidoc.element.mongodb.ObjectID.isValid)
- description and source-code
```javascript
function isValid(id) {
  if(id == null) return false;

  if(typeof id == 'number') {
    return true;
  }

  if(typeof id == 'string') {
    return id.length == 12 || (id.length == 24 && checkForHexRegExp.test(id));
  }

  if(id instanceof ObjectID) {
    return true;
  }

  if(id instanceof _Buffer) {
    return true;
  }

  // Duck-Typing detection of ObjectId like objects
  if(id.toHexString) {
    return id.id.length == 12 || (id.id.length == 24 && checkForHexRegExp.test(id.id));
  }

  return false;
}
```
- example usage
```shell
...
  if(typeof o.SERVICE_REALM == 'string') dbOptions.gssapiServiceRealm = o.SERVICE_REALM;
  if(typeof o.CANONICALIZE_HOST_NAME == 'string') dbOptions.gssapiCanonicalizeHostName = o.CANONICALIZE_HOST_NAME == 'true' ? true
 : false;
  break;
case 'wtimeoutMS':
  dbOptions.wtimeout = parseInt(value, 10);
  break;
case 'readPreference':
  if(!ReadPreference.isValid(value)) throw new Error("readPreference must be either primary/primaryPreferred/secondary/secondaryPreferred
/nearest");
  dbOptions.readPreference = value;
  break;
case 'maxStalenessSeconds':
  dbOptions.maxStalenessSeconds = parseInt(value, 10);
  break;
case 'readPreferenceTags':
  // Decode the value
...
```



# <a name="apidoc.module.mongodb.ObjectID.prototype"></a>[module mongodb.ObjectID.prototype](#apidoc.module.mongodb.ObjectID.prototype)

#### <a name="apidoc.element.mongodb.ObjectID.prototype.equals"></a>[function <span class="apidocSignatureSpan">mongodb.ObjectID.prototype.</span>equals (otherId)](#apidoc.element.mongodb.ObjectID.prototype.equals)
- description and source-code
```javascript
function equals(otherId) {
  var id;

  if(otherId instanceof ObjectID) {
    return this.toString() == otherId.toString();
  } else if(typeof otherId == 'string' && ObjectID.isValid(otherId) && otherId.length == 12 && this.id instanceof _Buffer) {
    return otherId === this.id.toString('binary');
  } else if(typeof otherId == 'string' && ObjectID.isValid(otherId) && otherId.length == 24) {
    return otherId.toLowerCase() === this.toHexString();
  } else if(typeof otherId == 'string' && ObjectID.isValid(otherId) && otherId.length == 12) {
    return otherId === this.id;
  } else if(otherId != null && (otherId instanceof ObjectID || otherId.toHexString)) {
    return otherId.toHexString() === this.toHexString();
  } else {
    return false;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.ObjectID.prototype.generate"></a>[function <span class="apidocSignatureSpan">mongodb.ObjectID.prototype.</span>generate (time)](#apidoc.element.mongodb.ObjectID.prototype.generate)
- description and source-code
```javascript
generate = function (time) {
  if ('number' != typeof time) {
    time = ~~(Date.now()/1000);
  }

  // Use pid
  var pid = (typeof process === 'undefined' ? Math.floor(Math.random() * 100000) : process.pid) % 0xFFFF;
  var inc = this.get_inc();
  // Buffer used
  var buffer = new Buffer(12);
  // Encode time
  buffer[3] = time & 0xff;
  buffer[2] = (time >> 8) & 0xff;
  buffer[1] = (time >> 16) & 0xff;
  buffer[0] = (time >> 24) & 0xff;
  // Encode machine
  buffer[6] = MACHINE_ID & 0xff;
  buffer[5] = (MACHINE_ID >> 8) & 0xff;
  buffer[4] = (MACHINE_ID >> 16) & 0xff;
  // Encode pid
  buffer[8] = pid & 0xff;
  buffer[7] = (pid >> 8) & 0xff;
  // Encode index
  buffer[11] = inc & 0xff;
  buffer[10] = (inc >> 8) & 0xff;
  buffer[9] = (inc >> 16) & 0xff;
  // Return the buffer
  return buffer;
}
```
- example usage
```shell
...
  // Classes to support
  var classes = [GridStore, OrderedBulkOperation, UnorderedBulkOperation,
    CommandCursor, AggregationCursor, Cursor, Collection, Db];

  // Add instrumentations to the available list
  for(var i = 0; i < classes.length; i++) {
    if(classes[i].define) {
      instrumentations.push(classes[i].define.generate());
    }
  }

  // Return the list of instrumentation points
  callback(null, instrumentations);
}
...
```

#### <a name="apidoc.element.mongodb.ObjectID.prototype.getInc"></a>[function <span class="apidocSignatureSpan">mongodb.ObjectID.prototype.</span>getInc ()](#apidoc.element.mongodb.ObjectID.prototype.getInc)
- description and source-code
```javascript
getInc = function () {
  return this.get_inc();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.ObjectID.prototype.getTimestamp"></a>[function <span class="apidocSignatureSpan">mongodb.ObjectID.prototype.</span>getTimestamp ()](#apidoc.element.mongodb.ObjectID.prototype.getTimestamp)
- description and source-code
```javascript
getTimestamp = function () {
  var timestamp = new Date();
  var time = this.id[3] | this.id[2] << 8 | this.id[1] << 16 | this.id[0] << 24;
  timestamp.setTime(Math.floor(time) * 1000);
  return timestamp;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.ObjectID.prototype.get_inc"></a>[function <span class="apidocSignatureSpan">mongodb.ObjectID.prototype.</span>get_inc ()](#apidoc.element.mongodb.ObjectID.prototype.get_inc)
- description and source-code
```javascript
get_inc = function () {
  return ObjectID.index = (ObjectID.index + 1) % 0xFFFFFF;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.ObjectID.prototype.inspect"></a>[function <span class="apidocSignatureSpan">mongodb.ObjectID.prototype.</span>inspect (format)](#apidoc.element.mongodb.ObjectID.prototype.inspect)
- description and source-code
```javascript
inspect = function (format) {
  // Is the id a buffer then use the buffer toString method to return the format
  if(this.id && this.id.copy) {
    return this.id.toString(typeof format === 'string' ? format : 'hex');
  }

  // if(this.buffer )
  return this.toHexString();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.ObjectID.prototype.toHexString"></a>[function <span class="apidocSignatureSpan">mongodb.ObjectID.prototype.</span>toHexString ()](#apidoc.element.mongodb.ObjectID.prototype.toHexString)
- description and source-code
```javascript
toHexString = function () {
  if(ObjectID.cacheHexString && this.__id) return this.__id;

  var hexString = '';
  if(!this.id || !this.id.length) {
    throw new Error('invalid ObjectId, ObjectId.id must be either a string or a Buffer, but is [' + JSON.stringify(this.id) + ']');
  }

  if(this.id instanceof _Buffer) {
    hexString = convertToHex(this.id);
    if(ObjectID.cacheHexString) this.__id = hexString;
    return hexString;
  }

  for (var i = 0; i < this.id.length; i++) {
    hexString += hexTable[this.id.charCodeAt(i)];
  }

  if(ObjectID.cacheHexString) this.__id = hexString;
  return hexString;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.ObjectID.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">mongodb.ObjectID.prototype.</span>toJSON ()](#apidoc.element.mongodb.ObjectID.prototype.toJSON)
- description and source-code
```javascript
toJSON = function () {
  return this.toHexString();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.ObjectID.prototype.toString"></a>[function <span class="apidocSignatureSpan">mongodb.ObjectID.prototype.</span>toString (format)](#apidoc.element.mongodb.ObjectID.prototype.toString)
- description and source-code
```javascript
toString = function (format) {
  // Is the id a buffer then use the buffer toString method to return the format
  if(this.id && this.id.copy) {
    return this.id.toString(typeof format === 'string' ? format : 'hex');
  }

  // if(this.buffer )
  return this.toHexString();
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.ReadPreference"></a>[module mongodb.ReadPreference](#apidoc.module.mongodb.ReadPreference)

#### <a name="apidoc.element.mongodb.ReadPreference.ReadPreference"></a>[function <span class="apidocSignatureSpan">mongodb.</span>ReadPreference (mode, tags, options)](#apidoc.element.mongodb.ReadPreference.ReadPreference)
- description and source-code
```javascript
ReadPreference = function (mode, tags, options) {
  if(!(this instanceof ReadPreference)) {
    return new ReadPreference(mode, tags, options);
  }

  this._type = 'ReadPreference';
  this.mode = mode;
  this.tags = tags;
  this.options =  options;

  // If no tags were passed in
  if(tags && typeof tags == 'object' && !Array.isArray(tags)) {
    if(tags.maxStalenessSeconds) {
      this.options = tags;
      this.tags = null;
    }
  }

  // Add the maxStalenessSeconds value to the read Preference
  if(this.options && this.options.maxStalenessSeconds) {
    this.maxStalenessSeconds = this.options.maxStalenessSeconds;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.ReadPreference.isValid"></a>[function <span class="apidocSignatureSpan">mongodb.ReadPreference.</span>isValid (_mode)](#apidoc.element.mongodb.ReadPreference.isValid)
- description and source-code
```javascript
isValid = function (_mode) {
  return (_mode == ReadPreference.PRIMARY || _mode == ReadPreference.PRIMARY_PREFERRED
    || _mode == ReadPreference.SECONDARY || _mode == ReadPreference.SECONDARY_PREFERRED
    || _mode == ReadPreference.NEAREST
    || _mode == true || _mode == false || _mode == null);
}
```
- example usage
```shell
...
  if(typeof o.SERVICE_REALM == 'string') dbOptions.gssapiServiceRealm = o.SERVICE_REALM;
  if(typeof o.CANONICALIZE_HOST_NAME == 'string') dbOptions.gssapiCanonicalizeHostName = o.CANONICALIZE_HOST_NAME == 'true' ? true
 : false;
  break;
case 'wtimeoutMS':
  dbOptions.wtimeout = parseInt(value, 10);
  break;
case 'readPreference':
  if(!ReadPreference.isValid(value)) throw new Error("readPreference must be either primary/primaryPreferred/secondary/secondaryPreferred
/nearest");
  dbOptions.readPreference = value;
  break;
case 'maxStalenessSeconds':
  dbOptions.maxStalenessSeconds = parseInt(value, 10);
  break;
case 'readPreferenceTags':
  // Decode the value
...
```



# <a name="apidoc.module.mongodb.ReadPreference.prototype"></a>[module mongodb.ReadPreference.prototype](#apidoc.module.mongodb.ReadPreference.prototype)

#### <a name="apidoc.element.mongodb.ReadPreference.prototype.isValid"></a>[function <span class="apidocSignatureSpan">mongodb.ReadPreference.prototype.</span>isValid (mode)](#apidoc.element.mongodb.ReadPreference.prototype.isValid)
- description and source-code
```javascript
isValid = function (mode) {
  var _mode = typeof mode == 'string' ? mode : this.mode;
  return ReadPreference.isValid(_mode);
}
```
- example usage
```shell
...
  if(typeof o.SERVICE_REALM == 'string') dbOptions.gssapiServiceRealm = o.SERVICE_REALM;
  if(typeof o.CANONICALIZE_HOST_NAME == 'string') dbOptions.gssapiCanonicalizeHostName = o.CANONICALIZE_HOST_NAME == 'true' ? true
 : false;
  break;
case 'wtimeoutMS':
  dbOptions.wtimeout = parseInt(value, 10);
  break;
case 'readPreference':
  if(!ReadPreference.isValid(value)) throw new Error("readPreference must be either primary/primaryPreferred/secondary/secondaryPreferred
/nearest");
  dbOptions.readPreference = value;
  break;
case 'maxStalenessSeconds':
  dbOptions.maxStalenessSeconds = parseInt(value, 10);
  break;
case 'readPreferenceTags':
  // Decode the value
...
```

#### <a name="apidoc.element.mongodb.ReadPreference.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">mongodb.ReadPreference.prototype.</span>toJSON ()](#apidoc.element.mongodb.ReadPreference.prototype.toJSON)
- description and source-code
```javascript
toJSON = function () {
  return this.toObject();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.ReadPreference.prototype.toObject"></a>[function <span class="apidocSignatureSpan">mongodb.ReadPreference.prototype.</span>toObject ()](#apidoc.element.mongodb.ReadPreference.prototype.toObject)
- description and source-code
```javascript
toObject = function () {
  var object = {mode:this.mode};

  if(this.tags != null) {
    object['tags'] = this.tags;
  }

  if(this.maxStalenessSeconds) {
    object['maxStalenessSeconds'] = this.maxStalenessSeconds;
  }

  return object;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.ReplSet"></a>[module mongodb.ReplSet](#apidoc.module.mongodb.ReplSet)

#### <a name="apidoc.element.mongodb.ReplSet.ReplSet"></a>[function <span class="apidocSignatureSpan">mongodb.</span>ReplSet (servers, options)](#apidoc.element.mongodb.ReplSet.ReplSet)
- description and source-code
```javascript
ReplSet = function (servers, options) {
  if(!(this instanceof ReplSet)) return new ReplSet(servers, options);
  options = options || {};
  var self = this;
  // Set up event emitter
  EventEmitter.call(this);

  // Filter the options
  options = filterOptions(options, legalOptionNames);

  // Ensure all the instances are Server
  for(var i = 0; i < servers.length; i++) {
    if(!(servers[i] instanceof Server)) {
      throw MongoError.create({message: "all seed list instances must be of the Server type", driver:true});
    }
  }

  // Stored options
  var storeOptions = {
      force: false
    , bufferMaxEntries: typeof options.bufferMaxEntries == 'number' ? options.bufferMaxEntries : MAX_JS_INT
  }

  // Shared global store
  var store = options.store || new Store(self, storeOptions);

  // Build seed list
  var seedlist = servers.map(function(x) {
    return {host: x.host, port: x.port}
  });

  // Clone options
  var clonedOptions = mergeOptions({}, {
    disconnectHandler: store,
    cursorFactory: Cursor,
    reconnect: false,
    emitError: typeof options.emitError == 'boolean' ? options.emitError : true,
    size: typeof options.poolSize == 'number' ? options.poolSize : 5
  });

  // Translate any SSL options and other connectivity options
  clonedOptions = translateOptions(clonedOptions, options);

  // Socket options
  var socketOptions = options.socketOptions && Object.keys(options.socketOptions).length > 0
    ? options.socketOptions : options;

  // Translate all the options to the mongodb-core ones
  clonedOptions = translateOptions(clonedOptions, socketOptions);
  if(typeof clonedOptions.keepAlive == 'number') {
    clonedOptions.keepAliveInitialDelay = clonedOptions.keepAlive;
    clonedOptions.keepAlive = clonedOptions.keepAlive > 0;
  }

  // Client info
  this.clientInfo = {
    driver: {
      name: "nodejs",
      version: driverVersion
    },
    os: {
      type: type,
      name: name,
      architecture: architecture,
      version: release
    },
    platform: nodejsversion
  }

  // Build default client information
  clonedOptions.clientInfo = this.clientInfo;
  // Do we have an application specific string
  if(options.appname) {
    clonedOptions.clientInfo.application = { name: options.appname };
  }

  // Create the ReplSet
  var replset = new CReplSet(seedlist, clonedOptions);

  // Listen to reconnect event
  replset.on('reconnect', function() {
    self.emit('reconnect');
    store.execute();
  });

  // Internal state
  this.s = {
    // Replicaset
    replset: replset
    // Server capabilities
    , sCapabilities: null
    // Debug tag
    , tag: options.tag
    // Store options
    , storeOptions: storeOptions
    // Cloned options
    , clonedOptions: clonedOptions
    // Store
    , store: store
    // Options
    , options: options
  }

  // Debug
  if(clonedOptions.debug) {
    // Last ismaster
    Object.defineProperty(this, 'replset', {
      enumerable:true, get: function() { return replset; }
    });
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.ReplSet.super_"></a>[function <span class="apidocSignatureSpan">mongodb.ReplSet.</span>super_ ()](#apidoc.element.mongodb.ReplSet.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.ReplSet.define"></a>[module mongodb.ReplSet.define](#apidoc.module.mongodb.ReplSet.define)

#### <a name="apidoc.element.mongodb.ReplSet.define.object"></a>[function <span class="apidocSignatureSpan">mongodb.ReplSet.define.</span>object (servers, options)](#apidoc.element.mongodb.ReplSet.define.object)
- description and source-code
```javascript
object = function (servers, options) {
  if(!(this instanceof ReplSet)) return new ReplSet(servers, options);
  options = options || {};
  var self = this;
  // Set up event emitter
  EventEmitter.call(this);

  // Filter the options
  options = filterOptions(options, legalOptionNames);

  // Ensure all the instances are Server
  for(var i = 0; i < servers.length; i++) {
    if(!(servers[i] instanceof Server)) {
      throw MongoError.create({message: "all seed list instances must be of the Server type", driver:true});
    }
  }

  // Stored options
  var storeOptions = {
      force: false
    , bufferMaxEntries: typeof options.bufferMaxEntries == 'number' ? options.bufferMaxEntries : MAX_JS_INT
  }

  // Shared global store
  var store = options.store || new Store(self, storeOptions);

  // Build seed list
  var seedlist = servers.map(function(x) {
    return {host: x.host, port: x.port}
  });

  // Clone options
  var clonedOptions = mergeOptions({}, {
    disconnectHandler: store,
    cursorFactory: Cursor,
    reconnect: false,
    emitError: typeof options.emitError == 'boolean' ? options.emitError : true,
    size: typeof options.poolSize == 'number' ? options.poolSize : 5
  });

  // Translate any SSL options and other connectivity options
  clonedOptions = translateOptions(clonedOptions, options);

  // Socket options
  var socketOptions = options.socketOptions && Object.keys(options.socketOptions).length > 0
    ? options.socketOptions : options;

  // Translate all the options to the mongodb-core ones
  clonedOptions = translateOptions(clonedOptions, socketOptions);
  if(typeof clonedOptions.keepAlive == 'number') {
    clonedOptions.keepAliveInitialDelay = clonedOptions.keepAlive;
    clonedOptions.keepAlive = clonedOptions.keepAlive > 0;
  }

  // Client info
  this.clientInfo = {
    driver: {
      name: "nodejs",
      version: driverVersion
    },
    os: {
      type: type,
      name: name,
      architecture: architecture,
      version: release
    },
    platform: nodejsversion
  }

  // Build default client information
  clonedOptions.clientInfo = this.clientInfo;
  // Do we have an application specific string
  if(options.appname) {
    clonedOptions.clientInfo.application = { name: options.appname };
  }

  // Create the ReplSet
  var replset = new CReplSet(seedlist, clonedOptions);

  // Listen to reconnect event
  replset.on('reconnect', function() {
    self.emit('reconnect');
    store.execute();
  });

  // Internal state
  this.s = {
    // Replicaset
    replset: replset
    // Server capabilities
    , sCapabilities: null
    // Debug tag
    , tag: options.tag
    // Store options
    , storeOptions: storeOptions
    // Cloned options
    , clonedOptions: clonedOptions
    // Store
    , store: store
    // Options
    , options: options
  }

  // Debug
  if(clonedOptions.debug) {
    // Last ismaster
    Object.defineProperty(this, 'replset', {
      enumerable:true, get: function() { return replset; }
    });
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.ReplSet.prototype"></a>[module mongodb.ReplSet.prototype](#apidoc.module.mongodb.ReplSet.prototype)

#### <a name="apidoc.element.mongodb.ReplSet.prototype.auth"></a>[function <span class="apidocSignatureSpan">mongodb.ReplSet.prototype.</span>auth ()](#apidoc.element.mongodb.ReplSet.prototype.auth)
- description and source-code
```javascript
auth = function () {
  var args = Array.prototype.slice.call(arguments, 0);
  this.s.replset.auth.apply(this.s.replset, args);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.ReplSet.prototype.capabilities"></a>[function <span class="apidocSignatureSpan">mongodb.ReplSet.prototype.</span>capabilities ()](#apidoc.element.mongodb.ReplSet.prototype.capabilities)
- description and source-code
```javascript
capabilities = function () {
  if(this.s.sCapabilities) return this.s.sCapabilities;
  if(this.s.replset.lastIsMaster() == null) return null;
  this.s.sCapabilities = new ServerCapabilities(this.s.replset.lastIsMaster());
  return this.s.sCapabilities;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.ReplSet.prototype.close"></a>[function <span class="apidocSignatureSpan">mongodb.ReplSet.prototype.</span>close (forceClosed)](#apidoc.element.mongodb.ReplSet.prototype.close)
- description and source-code
```javascript
close = function (forceClosed) {
  var self = this;
  // Call destroy on the topology
  this.s.replset.destroy({
    force: typeof forceClosed == 'boolean' ? forceClosed : false,
  });
  // We need to wash out all stored processes
  if(forceClosed == true) {
    this.s.storeOptions.force = forceClosed;
    this.s.store.flush();
  }

  var events = ['timeout', 'error', 'close', 'joined', 'left'];
  events.forEach(function(e) {
    self.removeAllListeners(e);
  });
}
```
- example usage
```shell
...
// Connection URL
var url = 'mongodb://localhost:27017/myproject';
// Use connect method to connect to the Server
MongoClient.connect(url, function(err, db) {
  assert.equal(null, err);
  console.log("Connected correctly to server");

  db.close();
});
'''

Given that you booted up the **mongod** process earlier the application should connect successfully and print **Connected correctly
 to server** to the console.

Let's Add some code to show the different CRUD operations available.
...
```

#### <a name="apidoc.element.mongodb.ReplSet.prototype.command"></a>[function <span class="apidocSignatureSpan">mongodb.ReplSet.prototype.</span>command (ns, cmd, options, callback)](#apidoc.element.mongodb.ReplSet.prototype.command)
- description and source-code
```javascript
command = function (ns, cmd, options, callback) {
  this.s.replset.command(ns, cmd, getReadPreference(options), callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.ReplSet.prototype.connect"></a>[function <span class="apidocSignatureSpan">mongodb.ReplSet.prototype.</span>connect (db, _options, callback)](#apidoc.element.mongodb.ReplSet.prototype.connect)
- description and source-code
```javascript
connect = function (db, _options, callback) {
  var self = this;
  if('function' === typeof _options) callback = _options, _options = {};
  if(_options == null) _options = {};
  if(!('function' === typeof callback)) callback = null;
  self.s.options = _options;

  // Update bufferMaxEntries
  self.s.storeOptions.bufferMaxEntries = db.bufferMaxEntries;

  // Actual handler
  var errorHandler = function(event) {
    return function(err) {
      if(event != 'error') {
        self.emit(event, err);
      }
    }
  }

  // Connect handler
  var connectHandler = function() {
    // Clear out all the current handlers left over
    ["timeout", "error", "close", 'serverOpening', 'serverDescriptionChanged', 'serverHeartbeatStarted',
      'serverHeartbeatSucceeded', 'serverHeartbeatFailed', 'serverClosed', 'topologyOpening',
      'topologyClosed', 'topologyDescriptionChanged'].forEach(function(e) {
      self.s.replset.removeAllListeners(e);
    });

    // Set up listeners
    self.s.replset.once('timeout', errorHandler('timeout'));
    self.s.replset.once('error', errorHandler('error'));
    self.s.replset.once('close', errorHandler('close'));

    // relay the event
    var relay = function(event) {
      return function(t, server) {
        self.emit(event, t, server);
      }
    }

    // Replset events relay
    var replsetRelay = function(event) {
      return function(t, server) {
        self.emit(event, t, server.lastIsMaster(), server);
      }
    }

    // Relay ha
    var relayHa = function(t, state) {
      self.emit('ha', t, state);

      if(t == 'start') {
        self.emit('ha_connect', t, state);
      } else if(t == 'end') {
        self.emit('ha_ismaster', t, state);
      }
    }

    // Set up serverConfig listeners
    self.s.replset.on('joined', replsetRelay('joined'));
    self.s.replset.on('left', relay('left'));
    self.s.replset.on('ping', relay('ping'));
    self.s.replset.on('ha', relayHa);

    // Set up SDAM listeners
    self.s.replset.on('serverDescriptionChanged', relay('serverDescriptionChanged'));
    self.s.replset.on('serverHeartbeatStarted', relay('serverHeartbeatStarted'));
    self.s.replset.on('serverHeartbeatSucceeded', relay('serverHeartbeatSucceeded'));
    self.s.replset.on('serverHeartbeatFailed', relay('serverHeartbeatFailed'));
    self.s.replset.on('serverOpening', relay('serverOpening'));
    self.s.replset.on('serverClosed', relay('serverClosed'));
    self.s.replset.on('topologyOpening', relay('topologyOpening'));
    self.s.replset.on('topologyClosed', relay('topologyClosed'));
    self.s.replset.on('topologyDescriptionChanged', relay('topologyDescriptionChanged'));

    self.s.replset.on('fullsetup', function() {
      self.emit('fullsetup', null, self);
    });

    self.s.replset.on('all', function() {
      self.emit('all', null, self);
    });

    // Emit open event
    self.emit('open', null, self);

    // Return correctly
    try {
      callback(null, self);
    } catch(err) {
      process.nextTick(function() { throw err; })
    }
  }

  // Error handler
  var connectErrorHandler = function() {
    return function(err) {
      ['timeout', 'error', 'close'].forEach(function(e) {
        self.s.replset.removeListener(e, connectErrorHandler);
      });

      self.s.replset.removeListener('connect', connectErrorHandler);
      // Destroy the replset
      self.s.replset.destroy();

      // Try to callback
      try {
        callback(err);
      } catch(err) {
        if(!self.s.replset.isConnected())
          process.nextTick(function() { throw err; })
      }
    }
  }

  // Set up listeners
  self.s.replset.once('timeout', connectErrorHandler('timeout'));
  self.s.replset.once('error', connectErrorHandler('error'));
  self.s.replset.once('close', connectErrorHandler('close'));
  self.s.replset.once('connect', connectHandler);

  // Start connection
  self.s.replset.connect(_options);
}
```
- example usage
```shell
...
'''js
var MongoClient = require('mongodb').MongoClient
  , assert = require('assert');

// Connection URL
var url = 'mongodb://localhost:27017/myproject';
// Use connect method to connect to the Server
MongoClient.connect(url, function(err, db) {
  assert.equal(null, err);
  console.log("Connected correctly to server");

  db.close();
});
'''
...
```

#### <a name="apidoc.element.mongodb.ReplSet.prototype.connections"></a>[function <span class="apidocSignatureSpan">mongodb.ReplSet.prototype.</span>connections ()](#apidoc.element.mongodb.ReplSet.prototype.connections)
- description and source-code
```javascript
connections = function () {
  return this.s.replset.connections();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.ReplSet.prototype.cursor"></a>[function <span class="apidocSignatureSpan">mongodb.ReplSet.prototype.</span>cursor (ns, cmd, options)](#apidoc.element.mongodb.ReplSet.prototype.cursor)
- description and source-code
```javascript
cursor = function (ns, cmd, options) {
  options = translateReadPreference(options);
  options.disconnectHandler = this.s.store;
  return this.s.replset.cursor(ns, cmd, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.ReplSet.prototype.insert"></a>[function <span class="apidocSignatureSpan">mongodb.ReplSet.prototype.</span>insert (ns, ops, options, callback)](#apidoc.element.mongodb.ReplSet.prototype.insert)
- description and source-code
```javascript
insert = function (ns, ops, options, callback) {
  this.s.replset.insert(ns, ops, options, callback);
}
```
- example usage
```shell
...
* // Connection url
* var url = 'mongodb://localhost:27017/test';
* // Connect using MongoClient
* MongoClient.connect(url, function(err, db) {
*   // Create a collection we want to drop later
*   var col = db.collection('createIndexExample1');
*   // Insert a bunch of documents
*   col.insert([{a:1, b:1}
*     , {a:2, b:2}, {a:3, b:3}
*     , {a:4, b:4}], {w:1}, function(err, result) {
*     test.equal(null, err);
*     // Show that duplicate records got dropped
*     col.aggregation({}, {cursor: {}}).toArray(function(err, items) {
*       test.equal(null, err);
*       test.equal(4, items.length);
...
```

#### <a name="apidoc.element.mongodb.ReplSet.prototype.isConnected"></a>[function <span class="apidocSignatureSpan">mongodb.ReplSet.prototype.</span>isConnected (options)](#apidoc.element.mongodb.ReplSet.prototype.isConnected)
- description and source-code
```javascript
isConnected = function (options) {
  options = options || {};

  // If we passed in a readPreference, translate to
  // a CoreReadPreference instance
  if(options.readPreference) {
    options.readPreference = translateReadPreference(options.readPreference);
  }

  return this.s.replset.isConnected(options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.ReplSet.prototype.isDestroyed"></a>[function <span class="apidocSignatureSpan">mongodb.ReplSet.prototype.</span>isDestroyed ()](#apidoc.element.mongodb.ReplSet.prototype.isDestroyed)
- description and source-code
```javascript
isDestroyed = function () {
  return this.s.replset.isDestroyed();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.ReplSet.prototype.lastIsMaster"></a>[function <span class="apidocSignatureSpan">mongodb.ReplSet.prototype.</span>lastIsMaster ()](#apidoc.element.mongodb.ReplSet.prototype.lastIsMaster)
- description and source-code
```javascript
lastIsMaster = function () {
  return this.s.replset.lastIsMaster();
}
```
- example usage
```shell
...
/**
 * Add a maxTimeMS stage to the aggregation pipeline
 * @method
 * @param {number} value The state maxTimeMS value.
 * @return {AggregationCursor}
 */
AggregationCursor.prototype.maxTimeMS = function(value) {
  if(this.s.topology.lastIsMaster().minWireVersion > 2) {
    this.s.cmd.maxTimeMS = value;
  }
  return this;
}

define.classMethod('maxTimeMS', {callback: false, promise:false, returns: [AggregationCursor]});
...
```

#### <a name="apidoc.element.mongodb.ReplSet.prototype.logout"></a>[function <span class="apidocSignatureSpan">mongodb.ReplSet.prototype.</span>logout ()](#apidoc.element.mongodb.ReplSet.prototype.logout)
- description and source-code
```javascript
logout = function () {
  var args = Array.prototype.slice.call(arguments, 0);
  this.s.replset.logout.apply(this.s.replset, args);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.ReplSet.prototype.remove"></a>[function <span class="apidocSignatureSpan">mongodb.ReplSet.prototype.</span>remove (ns, ops, options, callback)](#apidoc.element.mongodb.ReplSet.prototype.remove)
- description and source-code
```javascript
remove = function (ns, ops, options, callback) {
  this.s.replset.remove(ns, ops, options, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.ReplSet.prototype.unref"></a>[function <span class="apidocSignatureSpan">mongodb.ReplSet.prototype.</span>unref ()](#apidoc.element.mongodb.ReplSet.prototype.unref)
- description and source-code
```javascript
unref = function () {
  return this.s.replset.unref();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.ReplSet.prototype.update"></a>[function <span class="apidocSignatureSpan">mongodb.ReplSet.prototype.</span>update (ns, ops, options, callback)](#apidoc.element.mongodb.ReplSet.prototype.update)
- description and source-code
```javascript
update = function (ns, ops, options, callback) {
  this.s.replset.update(ns, ops, options, callback);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.Server"></a>[module mongodb.Server](#apidoc.module.mongodb.Server)

#### <a name="apidoc.element.mongodb.Server.Server"></a>[function <span class="apidocSignatureSpan">mongodb.</span>Server (host, port, options)](#apidoc.element.mongodb.Server.Server)
- description and source-code
```javascript
Server = function (host, port, options) {
  options = options || {};
  if(!(this instanceof Server)) return new Server(host, port, options);
  EventEmitter.call(this);
  var self = this;

  // Filter the options
  options = filterOptions(options, legalOptionNames);

  // Stored options
  var storeOptions = {
      force: false
    , bufferMaxEntries: typeof options.bufferMaxEntries == 'number' ? options.bufferMaxEntries : MAX_JS_INT
  }

  // Shared global store
  var store = options.store || new Store(self, storeOptions);

  // Detect if we have a socket connection
  if(host.indexOf('\/') != -1) {
    if(port != null && typeof port == 'object') {
      options = port;
      port = null;
    }
  } else if(port == null) {
    throw MongoError.create({message: 'port must be specified', driver:true});
  }

  // Get the reconnect option
  var reconnect = typeof options.auto_reconnect == 'boolean' ? options.auto_reconnect : true;
  reconnect = typeof options.autoReconnect == 'boolean' ? options.autoReconnect : reconnect;

  // Clone options
  var clonedOptions = mergeOptions({}, {
    host: host, port: port, disconnectHandler: store,
    cursorFactory: Cursor,
    reconnect: reconnect,
    emitError: typeof options.emitError == 'boolean' ? options.emitError : true,
    size: typeof options.poolSize == 'number' ? options.poolSize : 5
  });

  // Translate any SSL options and other connectivity options
  clonedOptions = translateOptions(clonedOptions, options);

  // Socket options
  var socketOptions = options.socketOptions && Object.keys(options.socketOptions).length > 0
    ? options.socketOptions : options;

  // Translate all the options to the mongodb-core ones
  clonedOptions = translateOptions(clonedOptions, socketOptions);
  if(typeof clonedOptions.keepAlive == 'number') {
    clonedOptions.keepAliveInitialDelay = clonedOptions.keepAlive;
    clonedOptions.keepAlive = clonedOptions.keepAlive > 0;
  }

  // Build default client information
  this.clientInfo = {
    driver: {
      name: "nodejs",
      version: driverVersion
    },
    os: {
      type: type,
      name: name,
      architecture: architecture,
      version: release
    },
    platform: nodejsversion
  }

  // Build default client information
  clonedOptions.clientInfo = this.clientInfo;
  // Do we have an application specific string
  if(options.appname) {
    clonedOptions.clientInfo.application = { name: options.appname };
  }

  // Create an instance of a server instance from mongodb-core
  var server = new CServer(clonedOptions);

  // Define the internal properties
  this.s = {
    // Create an instance of a server instance from mongodb-core
      server: server
    // Server capabilities
    , sCapabilities: null
    // Cloned options
    , clonedOptions: clonedOptions
    // Reconnect
    , reconnect: clonedOptions.reconnect
    // Emit error
    , emitError: clonedOptions.emitError
    // Pool size
    , poolSize: clonedOptions.size
    // Store Options
    , storeOptions: storeOptions
    // Store
    , store: store
    // Host
    , host: host
    // Port
    , port: port
    // Options
    , options: options
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Server.super_"></a>[function <span class="apidocSignatureSpan">mongodb.Server.</span>super_ ()](#apidoc.element.mongodb.Server.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.Server.define"></a>[module mongodb.Server.define](#apidoc.module.mongodb.Server.define)

#### <a name="apidoc.element.mongodb.Server.define.object"></a>[function <span class="apidocSignatureSpan">mongodb.Server.define.</span>object (host, port, options)](#apidoc.element.mongodb.Server.define.object)
- description and source-code
```javascript
object = function (host, port, options) {
  options = options || {};
  if(!(this instanceof Server)) return new Server(host, port, options);
  EventEmitter.call(this);
  var self = this;

  // Filter the options
  options = filterOptions(options, legalOptionNames);

  // Stored options
  var storeOptions = {
      force: false
    , bufferMaxEntries: typeof options.bufferMaxEntries == 'number' ? options.bufferMaxEntries : MAX_JS_INT
  }

  // Shared global store
  var store = options.store || new Store(self, storeOptions);

  // Detect if we have a socket connection
  if(host.indexOf('\/') != -1) {
    if(port != null && typeof port == 'object') {
      options = port;
      port = null;
    }
  } else if(port == null) {
    throw MongoError.create({message: 'port must be specified', driver:true});
  }

  // Get the reconnect option
  var reconnect = typeof options.auto_reconnect == 'boolean' ? options.auto_reconnect : true;
  reconnect = typeof options.autoReconnect == 'boolean' ? options.autoReconnect : reconnect;

  // Clone options
  var clonedOptions = mergeOptions({}, {
    host: host, port: port, disconnectHandler: store,
    cursorFactory: Cursor,
    reconnect: reconnect,
    emitError: typeof options.emitError == 'boolean' ? options.emitError : true,
    size: typeof options.poolSize == 'number' ? options.poolSize : 5
  });

  // Translate any SSL options and other connectivity options
  clonedOptions = translateOptions(clonedOptions, options);

  // Socket options
  var socketOptions = options.socketOptions && Object.keys(options.socketOptions).length > 0
    ? options.socketOptions : options;

  // Translate all the options to the mongodb-core ones
  clonedOptions = translateOptions(clonedOptions, socketOptions);
  if(typeof clonedOptions.keepAlive == 'number') {
    clonedOptions.keepAliveInitialDelay = clonedOptions.keepAlive;
    clonedOptions.keepAlive = clonedOptions.keepAlive > 0;
  }

  // Build default client information
  this.clientInfo = {
    driver: {
      name: "nodejs",
      version: driverVersion
    },
    os: {
      type: type,
      name: name,
      architecture: architecture,
      version: release
    },
    platform: nodejsversion
  }

  // Build default client information
  clonedOptions.clientInfo = this.clientInfo;
  // Do we have an application specific string
  if(options.appname) {
    clonedOptions.clientInfo.application = { name: options.appname };
  }

  // Create an instance of a server instance from mongodb-core
  var server = new CServer(clonedOptions);

  // Define the internal properties
  this.s = {
    // Create an instance of a server instance from mongodb-core
      server: server
    // Server capabilities
    , sCapabilities: null
    // Cloned options
    , clonedOptions: clonedOptions
    // Reconnect
    , reconnect: clonedOptions.reconnect
    // Emit error
    , emitError: clonedOptions.emitError
    // Pool size
    , poolSize: clonedOptions.size
    // Store Options
    , storeOptions: storeOptions
    // Store
    , store: store
    // Host
    , host: host
    // Port
    , port: port
    // Options
    , options: options
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.Server.prototype"></a>[module mongodb.Server.prototype](#apidoc.module.mongodb.Server.prototype)

#### <a name="apidoc.element.mongodb.Server.prototype.auth"></a>[function <span class="apidocSignatureSpan">mongodb.Server.prototype.</span>auth ()](#apidoc.element.mongodb.Server.prototype.auth)
- description and source-code
```javascript
auth = function () {
  var args = Array.prototype.slice.call(arguments, 0);
  this.s.server.auth.apply(this.s.server, args);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Server.prototype.capabilities"></a>[function <span class="apidocSignatureSpan">mongodb.Server.prototype.</span>capabilities ()](#apidoc.element.mongodb.Server.prototype.capabilities)
- description and source-code
```javascript
capabilities = function () {
  if(this.s.sCapabilities) return this.s.sCapabilities;
  if(this.s.server.lastIsMaster() == null) return null;
  this.s.sCapabilities = new ServerCapabilities(this.s.server.lastIsMaster());
  return this.s.sCapabilities;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Server.prototype.close"></a>[function <span class="apidocSignatureSpan">mongodb.Server.prototype.</span>close (forceClosed)](#apidoc.element.mongodb.Server.prototype.close)
- description and source-code
```javascript
close = function (forceClosed) {
  this.s.server.destroy();
  // We need to wash out all stored processes
  if(forceClosed == true) {
    this.s.storeOptions.force = forceClosed;
    this.s.store.flush();
  }
}
```
- example usage
```shell
...
// Connection URL
var url = 'mongodb://localhost:27017/myproject';
// Use connect method to connect to the Server
MongoClient.connect(url, function(err, db) {
  assert.equal(null, err);
  console.log("Connected correctly to server");

  db.close();
});
'''

Given that you booted up the **mongod** process earlier the application should connect successfully and print **Connected correctly
 to server** to the console.

Let's Add some code to show the different CRUD operations available.
...
```

#### <a name="apidoc.element.mongodb.Server.prototype.command"></a>[function <span class="apidocSignatureSpan">mongodb.Server.prototype.</span>command (ns, cmd, options, callback)](#apidoc.element.mongodb.Server.prototype.command)
- description and source-code
```javascript
command = function (ns, cmd, options, callback) {
  this.s.server.command(ns, cmd, getReadPreference(options), callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Server.prototype.connect"></a>[function <span class="apidocSignatureSpan">mongodb.Server.prototype.</span>connect (db, _options, callback)](#apidoc.element.mongodb.Server.prototype.connect)
- description and source-code
```javascript
connect = function (db, _options, callback) {
  var self = this;
  if('function' === typeof _options) callback = _options, _options = {};
  if(_options == null) _options = {};
  if(!('function' === typeof callback)) callback = null;
  self.s.options = _options;

  // Update bufferMaxEntries
  self.s.storeOptions.bufferMaxEntries = db.bufferMaxEntries;

  // Error handler
  var connectErrorHandler = function() {
    return function(err) {
      // Remove all event handlers
      var events = ['timeout', 'error', 'close'];
      events.forEach(function(e) {
        self.s.server.removeListener(e, connectHandlers[e]);
      });

      self.s.server.removeListener('connect', connectErrorHandler);

      // Try to callback
      try {
        callback(err);
      } catch(err) {
        process.nextTick(function() { throw err; })
      }
    }
  }

  // Actual handler
  var errorHandler = function(event) {
    return function(err) {
      if(event != 'error') {
        self.emit(event, err);
      }
    }
  }

  // Error handler
  var reconnectHandler = function() {
    self.emit('reconnect', self);
    self.s.store.execute();
  }

  // Reconnect failed
  var reconnectFailedHandler = function(err) {
    self.emit('reconnectFailed', err);
    self.s.store.flush(err);
  }

  // Destroy called on topology, perform cleanup
  var destroyHandler = function() {
    self.s.store.flush();
  }

  // Connect handler
  var connectHandler = function() {
    // Clear out all the current handlers left over
    ["timeout", "error", "close", 'serverOpening', 'serverDescriptionChanged', 'serverHeartbeatStarted',
      'serverHeartbeatSucceeded', 'serverHeartbeatFailed', 'serverClosed', 'topologyOpening',
      'topologyClosed', 'topologyDescriptionChanged'].forEach(function(e) {
      self.s.server.removeAllListeners(e);
    });

    // Set up listeners
    self.s.server.on('timeout', errorHandler('timeout'));
    self.s.server.once('error', errorHandler('error'));
    self.s.server.on('close', errorHandler('close'));
    // Only called on destroy
    self.s.server.on('destroy', destroyHandler);

    // relay the event
    var relay = function(event) {
      return function(t, server) {
        self.emit(event, t, server);
      }
    }

    // Set up SDAM listeners
    self.s.server.on('serverDescriptionChanged', relay('serverDescriptionChanged'));
    self.s.server.on('serverHeartbeatStarted', relay('serverHeartbeatStarted'));
    self.s.server.on('serverHeartbeatSucceeded', relay('serverHeartbeatSucceeded'));
    self.s.server.on('serverHeartbeatFailed', relay('serverHeartbeatFailed'));
    self.s.server.on('serverOpening', relay('serverOpening'));
    self.s.server.on('serverClosed', relay('serverClosed'));
    self.s.server.on('topologyOpening', relay('topologyOpening'));
    self.s.server.on('topologyClosed', relay('topologyClosed'));
    self.s.server.on('topologyDescriptionChanged', relay('topologyDescriptionChanged'));
    self.s.server.on('attemptReconnect', relay('attemptReconnect'));
    self.s.server.on('monitoring', relay('monitoring'));

    // Emit open event
    self.emit('open', null, self);

    // Return correctly
    try {
      callback(null, self);
    } catch(err) {
      console.log(err.stack)
      process.nextTick(function() { throw err; })
    }
  }

  // Set up listeners
  var connectHandlers = {
    timeout: connectErrorHandler('timeout'),
    error: connectErrorHandler('error'),
    close: connectErrorHandler('close')
  };

  // Add the event handlers
  self.s.server.once('timeout', connectHandlers.timeout);
  self.s.server.once('error', connectHandlers.error);
  self.s.server.once('close', connectHandlers.close);
  self.s.server.once('connect', connectHandler);
  // Reconnect server
  self.s.server.on('reconnect', reconnectHandler);
  self.s.server.on('reconnectFailed', reconnectFailedHandler);

  // Start connection
  self.s.server.connect(_options);
}
```
- example usage
```shell
...
'''js
var MongoClient = require('mongodb').MongoClient
  , assert = require('assert');

// Connection URL
var url = 'mongodb://localhost:27017/myproject';
// Use connect method to connect to the Server
MongoClient.connect(url, function(err, db) {
  assert.equal(null, err);
  console.log("Connected correctly to server");

  db.close();
});
'''
...
```

#### <a name="apidoc.element.mongodb.Server.prototype.connections"></a>[function <span class="apidocSignatureSpan">mongodb.Server.prototype.</span>connections ()](#apidoc.element.mongodb.Server.prototype.connections)
- description and source-code
```javascript
connections = function () {
  return this.s.server.connections();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Server.prototype.cursor"></a>[function <span class="apidocSignatureSpan">mongodb.Server.prototype.</span>cursor (ns, cmd, options)](#apidoc.element.mongodb.Server.prototype.cursor)
- description and source-code
```javascript
cursor = function (ns, cmd, options) {
  options.disconnectHandler = this.s.store;
  return this.s.server.cursor(ns, cmd, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Server.prototype.insert"></a>[function <span class="apidocSignatureSpan">mongodb.Server.prototype.</span>insert (ns, ops, options, callback)](#apidoc.element.mongodb.Server.prototype.insert)
- description and source-code
```javascript
insert = function (ns, ops, options, callback) {
  this.s.server.insert(ns, ops, options, callback);
}
```
- example usage
```shell
...
* // Connection url
* var url = 'mongodb://localhost:27017/test';
* // Connect using MongoClient
* MongoClient.connect(url, function(err, db) {
*   // Create a collection we want to drop later
*   var col = db.collection('createIndexExample1');
*   // Insert a bunch of documents
*   col.insert([{a:1, b:1}
*     , {a:2, b:2}, {a:3, b:3}
*     , {a:4, b:4}], {w:1}, function(err, result) {
*     test.equal(null, err);
*     // Show that duplicate records got dropped
*     col.aggregation({}, {cursor: {}}).toArray(function(err, items) {
*       test.equal(null, err);
*       test.equal(4, items.length);
...
```

#### <a name="apidoc.element.mongodb.Server.prototype.isConnected"></a>[function <span class="apidocSignatureSpan">mongodb.Server.prototype.</span>isConnected ()](#apidoc.element.mongodb.Server.prototype.isConnected)
- description and source-code
```javascript
isConnected = function () {
  return this.s.server.isConnected();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Server.prototype.isDestroyed"></a>[function <span class="apidocSignatureSpan">mongodb.Server.prototype.</span>isDestroyed ()](#apidoc.element.mongodb.Server.prototype.isDestroyed)
- description and source-code
```javascript
isDestroyed = function () {
  return this.s.server.isDestroyed();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Server.prototype.lastIsMaster"></a>[function <span class="apidocSignatureSpan">mongodb.Server.prototype.</span>lastIsMaster ()](#apidoc.element.mongodb.Server.prototype.lastIsMaster)
- description and source-code
```javascript
lastIsMaster = function () {
  return this.s.server.lastIsMaster();
}
```
- example usage
```shell
...
/**
 * Add a maxTimeMS stage to the aggregation pipeline
 * @method
 * @param {number} value The state maxTimeMS value.
 * @return {AggregationCursor}
 */
AggregationCursor.prototype.maxTimeMS = function(value) {
  if(this.s.topology.lastIsMaster().minWireVersion > 2) {
    this.s.cmd.maxTimeMS = value;
  }
  return this;
}

define.classMethod('maxTimeMS', {callback: false, promise:false, returns: [AggregationCursor]});
...
```

#### <a name="apidoc.element.mongodb.Server.prototype.logout"></a>[function <span class="apidocSignatureSpan">mongodb.Server.prototype.</span>logout ()](#apidoc.element.mongodb.Server.prototype.logout)
- description and source-code
```javascript
logout = function () {
  var args = Array.prototype.slice.call(arguments, 0);
  this.s.server.logout.apply(this.s.server, args);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Server.prototype.remove"></a>[function <span class="apidocSignatureSpan">mongodb.Server.prototype.</span>remove (ns, ops, options, callback)](#apidoc.element.mongodb.Server.prototype.remove)
- description and source-code
```javascript
remove = function (ns, ops, options, callback) {
  this.s.server.remove(ns, ops, options, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Server.prototype.unref"></a>[function <span class="apidocSignatureSpan">mongodb.Server.prototype.</span>unref ()](#apidoc.element.mongodb.Server.prototype.unref)
- description and source-code
```javascript
unref = function () {
  this.s.server.unref();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Server.prototype.update"></a>[function <span class="apidocSignatureSpan">mongodb.Server.prototype.</span>update (ns, ops, options, callback)](#apidoc.element.mongodb.Server.prototype.update)
- description and source-code
```javascript
update = function (ns, ops, options, callback) {
  this.s.server.update(ns, ops, options, callback);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.Symbol"></a>[module mongodb.Symbol](#apidoc.module.mongodb.Symbol)

#### <a name="apidoc.element.mongodb.Symbol.Symbol"></a>[function <span class="apidocSignatureSpan">mongodb.</span>Symbol (value)](#apidoc.element.mongodb.Symbol.Symbol)
- description and source-code
```javascript
function Symbol(value) {
  if(!(this instanceof Symbol)) return new Symbol(value);
  this._bsontype = 'Symbol';
  this.value = value;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.Symbol.prototype"></a>[module mongodb.Symbol.prototype](#apidoc.module.mongodb.Symbol.prototype)

#### <a name="apidoc.element.mongodb.Symbol.prototype.inspect"></a>[function <span class="apidocSignatureSpan">mongodb.Symbol.prototype.</span>inspect ()](#apidoc.element.mongodb.Symbol.prototype.inspect)
- description and source-code
```javascript
inspect = function () {
  return this.value;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Symbol.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">mongodb.Symbol.prototype.</span>toJSON ()](#apidoc.element.mongodb.Symbol.prototype.toJSON)
- description and source-code
```javascript
toJSON = function () {
  return this.value;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Symbol.prototype.toString"></a>[function <span class="apidocSignatureSpan">mongodb.Symbol.prototype.</span>toString ()](#apidoc.element.mongodb.Symbol.prototype.toString)
- description and source-code
```javascript
toString = function () {
  return this.value;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Symbol.prototype.valueOf"></a>[function <span class="apidocSignatureSpan">mongodb.Symbol.prototype.</span>valueOf ()](#apidoc.element.mongodb.Symbol.prototype.valueOf)
- description and source-code
```javascript
valueOf = function () {
  return this.value;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.Timestamp"></a>[module mongodb.Timestamp](#apidoc.module.mongodb.Timestamp)

#### <a name="apidoc.element.mongodb.Timestamp.Timestamp"></a>[function <span class="apidocSignatureSpan">mongodb.</span>Timestamp (low, high)](#apidoc.element.mongodb.Timestamp.Timestamp)
- description and source-code
```javascript
function Timestamp(low, high) {
  if(!(this instanceof Timestamp)) return new Timestamp(low, high);
  this._bsontype = 'Timestamp';
<span class="apidocCodeCommentSpan">  /**
   * @type {number}
   * @ignore
   */
</span>  this.low_ = low | 0;  // force into 32 signed bits.

  /**
   * @type {number}
   * @ignore
   */
  this.high_ = high | 0;  // force into 32 signed bits.
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Timestamp.fromBits"></a>[function <span class="apidocSignatureSpan">mongodb.Timestamp.</span>fromBits (lowBits, highBits)](#apidoc.element.mongodb.Timestamp.fromBits)
- description and source-code
```javascript
fromBits = function (lowBits, highBits) {
  return new Timestamp(lowBits, highBits);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Timestamp.fromInt"></a>[function <span class="apidocSignatureSpan">mongodb.Timestamp.</span>fromInt (value)](#apidoc.element.mongodb.Timestamp.fromInt)
- description and source-code
```javascript
fromInt = function (value) {
  if (-128 <= value && value < 128) {
    var cachedObj = Timestamp.INT_CACHE_[value];
    if (cachedObj) {
      return cachedObj;
    }
  }

  var obj = new Timestamp(value | 0, value < 0 ? -1 : 0);
  if (-128 <= value && value < 128) {
    Timestamp.INT_CACHE_[value] = obj;
  }
  return obj;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Timestamp.fromNumber"></a>[function <span class="apidocSignatureSpan">mongodb.Timestamp.</span>fromNumber (value)](#apidoc.element.mongodb.Timestamp.fromNumber)
- description and source-code
```javascript
fromNumber = function (value) {
  if (isNaN(value) || !isFinite(value)) {
    return Timestamp.ZERO;
  } else if (value <= -Timestamp.TWO_PWR_63_DBL_) {
    return Timestamp.MIN_VALUE;
  } else if (value + 1 >= Timestamp.TWO_PWR_63_DBL_) {
    return Timestamp.MAX_VALUE;
  } else if (value < 0) {
    return Timestamp.fromNumber(-value).negate();
  } else {
    return new Timestamp(
               (value % Timestamp.TWO_PWR_32_DBL_) | 0,
               (value / Timestamp.TWO_PWR_32_DBL_) | 0);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Timestamp.fromString"></a>[function <span class="apidocSignatureSpan">mongodb.Timestamp.</span>fromString (str, opt_radix)](#apidoc.element.mongodb.Timestamp.fromString)
- description and source-code
```javascript
fromString = function (str, opt_radix) {
  if (str.length == 0) {
    throw Error('number format error: empty string');
  }

  var radix = opt_radix || 10;
  if (radix < 2 || 36 < radix) {
    throw Error('radix out of range: ' + radix);
  }

  if (str.charAt(0) == '-') {
    return Timestamp.fromString(str.substring(1), radix).negate();
  } else if (str.indexOf('-') >= 0) {
    throw Error('number format error: interior "-" character: ' + str);
  }

  // Do several (8) digits each time through the loop, so as to
  // minimize the calls to the very expensive emulated div.
  var radixToPower = Timestamp.fromNumber(Math.pow(radix, 8));

  var result = Timestamp.ZERO;
  for (var i = 0; i < str.length; i += 8) {
    var size = Math.min(8, str.length - i);
    var value = parseInt(str.substring(i, i + size), radix);
    if (size < 8) {
      var power = Timestamp.fromNumber(Math.pow(radix, size));
      result = result.multiply(power).add(Timestamp.fromNumber(value));
    } else {
      result = result.multiply(radixToPower);
      result = result.add(Timestamp.fromNumber(value));
    }
  }
  return result;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.Timestamp.prototype"></a>[module mongodb.Timestamp.prototype](#apidoc.module.mongodb.Timestamp.prototype)

#### <a name="apidoc.element.mongodb.Timestamp.prototype.add"></a>[function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>add (other)](#apidoc.element.mongodb.Timestamp.prototype.add)
- description and source-code
```javascript
add = function (other) {
  // Divide each number into 4 chunks of 16 bits, and then sum the chunks.

  var a48 = this.high_ >>> 16;
  var a32 = this.high_ & 0xFFFF;
  var a16 = this.low_ >>> 16;
  var a00 = this.low_ & 0xFFFF;

  var b48 = other.high_ >>> 16;
  var b32 = other.high_ & 0xFFFF;
  var b16 = other.low_ >>> 16;
  var b00 = other.low_ & 0xFFFF;

  var c48 = 0, c32 = 0, c16 = 0, c00 = 0;
  c00 += a00 + b00;
  c16 += c00 >>> 16;
  c00 &= 0xFFFF;
  c16 += a16 + b16;
  c32 += c16 >>> 16;
  c16 &= 0xFFFF;
  c32 += a32 + b32;
  c48 += c32 >>> 16;
  c32 &= 0xFFFF;
  c48 += a48 + b48;
  c48 &= 0xFFFF;
  return Timestamp.fromBits((c16 << 16) | c00, (c48 << 16) | c32);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Timestamp.prototype.and"></a>[function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>and (other)](#apidoc.element.mongodb.Timestamp.prototype.and)
- description and source-code
```javascript
and = function (other) {
  return Timestamp.fromBits(this.low_ & other.low_, this.high_ & other.high_);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Timestamp.prototype.compare"></a>[function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>compare (other)](#apidoc.element.mongodb.Timestamp.prototype.compare)
- description and source-code
```javascript
compare = function (other) {
  if (this.equals(other)) {
    return 0;
  }

  var thisNeg = this.isNegative();
  var otherNeg = other.isNegative();
  if (thisNeg && !otherNeg) {
    return -1;
  }
  if (!thisNeg && otherNeg) {
    return 1;
  }

  // at this point, the signs are the same, so subtraction will not overflow
  if (this.subtract(other).isNegative()) {
    return -1;
  } else {
    return 1;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Timestamp.prototype.div"></a>[function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>div (other)](#apidoc.element.mongodb.Timestamp.prototype.div)
- description and source-code
```javascript
div = function (other) {
  if (other.isZero()) {
    throw Error('division by zero');
  } else if (this.isZero()) {
    return Timestamp.ZERO;
  }

  if (this.equals(Timestamp.MIN_VALUE)) {
    if (other.equals(Timestamp.ONE) ||
        other.equals(Timestamp.NEG_ONE)) {
      return Timestamp.MIN_VALUE;  // recall that -MIN_VALUE == MIN_VALUE
    } else if (other.equals(Timestamp.MIN_VALUE)) {
      return Timestamp.ONE;
    } else {
      // At this point, we have |other| >= 2, so |this/other| < |MIN_VALUE|.
      var halfThis = this.shiftRight(1);
      var approx = halfThis.div(other).shiftLeft(1);
      if (approx.equals(Timestamp.ZERO)) {
        return other.isNegative() ? Timestamp.ONE : Timestamp.NEG_ONE;
      } else {
        var rem = this.subtract(other.multiply(approx));
        var result = approx.add(rem.div(other));
        return result;
      }
    }
  } else if (other.equals(Timestamp.MIN_VALUE)) {
    return Timestamp.ZERO;
  }

  if (this.isNegative()) {
    if (other.isNegative()) {
      return this.negate().div(other.negate());
    } else {
      return this.negate().div(other).negate();
    }
  } else if (other.isNegative()) {
    return this.div(other.negate()).negate();
  }

  // Repeat the following until the remainder is less than other:  find a
  // floating-point that approximates remainder / other *from below*, add this
  // into the result, and subtract it from the remainder.  It is critical that
  // the approximate value is less than or equal to the real value so that the
  // remainder never becomes negative.
  var res = Timestamp.ZERO;
  var rem = this;
  while (rem.greaterThanOrEqual(other)) {
    // Approximate the result of division. This may be a little greater or
    // smaller than the actual value.
    var approx = Math.max(1, Math.floor(rem.toNumber() / other.toNumber()));

    // We will tweak the approximate result by changing it in the 48-th digit or
    // the smallest non-fractional digit, whichever is larger.
    var log2 = Math.ceil(Math.log(approx) / Math.LN2);
    var delta = (log2 <= 48) ? 1 : Math.pow(2, log2 - 48);

    // Decrease the approximation until it is smaller than the remainder.  Note
    // that if it is too large, the product overflows and is negative.
    var approxRes = Timestamp.fromNumber(approx);
    var approxRem = approxRes.multiply(other);
    while (approxRem.isNegative() || approxRem.greaterThan(rem)) {
      approx -= delta;
      approxRes = Timestamp.fromNumber(approx);
      approxRem = approxRes.multiply(other);
    }

    // We know the answer can't be zero... and actually, zero would cause
    // infinite recursion since we would make no progress.
    if (approxRes.isZero()) {
      approxRes = Timestamp.ONE;
    }

    res = res.add(approxRes);
    rem = rem.subtract(approxRem);
  }
  return res;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Timestamp.prototype.equals"></a>[function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>equals (other)](#apidoc.element.mongodb.Timestamp.prototype.equals)
- description and source-code
```javascript
equals = function (other) {
  return (this.high_ == other.high_) && (this.low_ == other.low_);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Timestamp.prototype.getHighBits"></a>[function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>getHighBits ()](#apidoc.element.mongodb.Timestamp.prototype.getHighBits)
- description and source-code
```javascript
getHighBits = function () {
  return this.high_;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Timestamp.prototype.getLowBits"></a>[function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>getLowBits ()](#apidoc.element.mongodb.Timestamp.prototype.getLowBits)
- description and source-code
```javascript
getLowBits = function () {
  return this.low_;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Timestamp.prototype.getLowBitsUnsigned"></a>[function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>getLowBitsUnsigned ()](#apidoc.element.mongodb.Timestamp.prototype.getLowBitsUnsigned)
- description and source-code
```javascript
getLowBitsUnsigned = function () {
  return (this.low_ >= 0) ?
      this.low_ : Timestamp.TWO_PWR_32_DBL_ + this.low_;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Timestamp.prototype.getNumBitsAbs"></a>[function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>getNumBitsAbs ()](#apidoc.element.mongodb.Timestamp.prototype.getNumBitsAbs)
- description and source-code
```javascript
getNumBitsAbs = function () {
  if (this.isNegative()) {
    if (this.equals(Timestamp.MIN_VALUE)) {
      return 64;
    } else {
      return this.negate().getNumBitsAbs();
    }
  } else {
    var val = this.high_ != 0 ? this.high_ : this.low_;
    for (var bit = 31; bit > 0; bit--) {
      if ((val & (1 << bit)) != 0) {
        break;
      }
    }
    return this.high_ != 0 ? bit + 33 : bit + 1;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Timestamp.prototype.greaterThan"></a>[function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>greaterThan (other)](#apidoc.element.mongodb.Timestamp.prototype.greaterThan)
- description and source-code
```javascript
greaterThan = function (other) {
  return this.compare(other) > 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Timestamp.prototype.greaterThanOrEqual"></a>[function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>greaterThanOrEqual (other)](#apidoc.element.mongodb.Timestamp.prototype.greaterThanOrEqual)
- description and source-code
```javascript
greaterThanOrEqual = function (other) {
  return this.compare(other) >= 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Timestamp.prototype.isNegative"></a>[function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>isNegative ()](#apidoc.element.mongodb.Timestamp.prototype.isNegative)
- description and source-code
```javascript
isNegative = function () {
  return this.high_ < 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Timestamp.prototype.isOdd"></a>[function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>isOdd ()](#apidoc.element.mongodb.Timestamp.prototype.isOdd)
- description and source-code
```javascript
isOdd = function () {
  return (this.low_ & 1) == 1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Timestamp.prototype.isZero"></a>[function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>isZero ()](#apidoc.element.mongodb.Timestamp.prototype.isZero)
- description and source-code
```javascript
isZero = function () {
  return this.high_ == 0 && this.low_ == 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Timestamp.prototype.lessThan"></a>[function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>lessThan (other)](#apidoc.element.mongodb.Timestamp.prototype.lessThan)
- description and source-code
```javascript
lessThan = function (other) {
  return this.compare(other) < 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Timestamp.prototype.lessThanOrEqual"></a>[function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>lessThanOrEqual (other)](#apidoc.element.mongodb.Timestamp.prototype.lessThanOrEqual)
- description and source-code
```javascript
lessThanOrEqual = function (other) {
  return this.compare(other) <= 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Timestamp.prototype.modulo"></a>[function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>modulo (other)](#apidoc.element.mongodb.Timestamp.prototype.modulo)
- description and source-code
```javascript
modulo = function (other) {
  return this.subtract(this.div(other).multiply(other));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Timestamp.prototype.multiply"></a>[function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>multiply (other)](#apidoc.element.mongodb.Timestamp.prototype.multiply)
- description and source-code
```javascript
multiply = function (other) {
  if (this.isZero()) {
    return Timestamp.ZERO;
  } else if (other.isZero()) {
    return Timestamp.ZERO;
  }

  if (this.equals(Timestamp.MIN_VALUE)) {
    return other.isOdd() ? Timestamp.MIN_VALUE : Timestamp.ZERO;
  } else if (other.equals(Timestamp.MIN_VALUE)) {
    return this.isOdd() ? Timestamp.MIN_VALUE : Timestamp.ZERO;
  }

  if (this.isNegative()) {
    if (other.isNegative()) {
      return this.negate().multiply(other.negate());
    } else {
      return this.negate().multiply(other).negate();
    }
  } else if (other.isNegative()) {
    return this.multiply(other.negate()).negate();
  }

  // If both Timestamps are small, use float multiplication
  if (this.lessThan(Timestamp.TWO_PWR_24_) &&
      other.lessThan(Timestamp.TWO_PWR_24_)) {
    return Timestamp.fromNumber(this.toNumber() * other.toNumber());
  }

  // Divide each Timestamp into 4 chunks of 16 bits, and then add up 4x4 products.
  // We can skip products that would overflow.

  var a48 = this.high_ >>> 16;
  var a32 = this.high_ & 0xFFFF;
  var a16 = this.low_ >>> 16;
  var a00 = this.low_ & 0xFFFF;

  var b48 = other.high_ >>> 16;
  var b32 = other.high_ & 0xFFFF;
  var b16 = other.low_ >>> 16;
  var b00 = other.low_ & 0xFFFF;

  var c48 = 0, c32 = 0, c16 = 0, c00 = 0;
  c00 += a00 * b00;
  c16 += c00 >>> 16;
  c00 &= 0xFFFF;
  c16 += a16 * b00;
  c32 += c16 >>> 16;
  c16 &= 0xFFFF;
  c16 += a00 * b16;
  c32 += c16 >>> 16;
  c16 &= 0xFFFF;
  c32 += a32 * b00;
  c48 += c32 >>> 16;
  c32 &= 0xFFFF;
  c32 += a16 * b16;
  c48 += c32 >>> 16;
  c32 &= 0xFFFF;
  c32 += a00 * b32;
  c48 += c32 >>> 16;
  c32 &= 0xFFFF;
  c48 += a48 * b00 + a32 * b16 + a16 * b32 + a00 * b48;
  c48 &= 0xFFFF;
  return Timestamp.fromBits((c16 << 16) | c00, (c48 << 16) | c32);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Timestamp.prototype.negate"></a>[function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>negate ()](#apidoc.element.mongodb.Timestamp.prototype.negate)
- description and source-code
```javascript
negate = function () {
  if (this.equals(Timestamp.MIN_VALUE)) {
    return Timestamp.MIN_VALUE;
  } else {
    return this.not().add(Timestamp.ONE);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Timestamp.prototype.not"></a>[function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>not ()](#apidoc.element.mongodb.Timestamp.prototype.not)
- description and source-code
```javascript
not = function () {
  return Timestamp.fromBits(~this.low_, ~this.high_);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Timestamp.prototype.notEquals"></a>[function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>notEquals (other)](#apidoc.element.mongodb.Timestamp.prototype.notEquals)
- description and source-code
```javascript
notEquals = function (other) {
  return (this.high_ != other.high_) || (this.low_ != other.low_);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Timestamp.prototype.or"></a>[function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>or (other)](#apidoc.element.mongodb.Timestamp.prototype.or)
- description and source-code
```javascript
or = function (other) {
  return Timestamp.fromBits(this.low_ | other.low_, this.high_ | other.high_);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Timestamp.prototype.shiftLeft"></a>[function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>shiftLeft (numBits)](#apidoc.element.mongodb.Timestamp.prototype.shiftLeft)
- description and source-code
```javascript
shiftLeft = function (numBits) {
  numBits &= 63;
  if (numBits == 0) {
    return this;
  } else {
    var low = this.low_;
    if (numBits < 32) {
      var high = this.high_;
      return Timestamp.fromBits(
                 low << numBits,
                 (high << numBits) | (low >>> (32 - numBits)));
    } else {
      return Timestamp.fromBits(0, low << (numBits - 32));
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Timestamp.prototype.shiftRight"></a>[function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>shiftRight (numBits)](#apidoc.element.mongodb.Timestamp.prototype.shiftRight)
- description and source-code
```javascript
shiftRight = function (numBits) {
  numBits &= 63;
  if (numBits == 0) {
    return this;
  } else {
    var high = this.high_;
    if (numBits < 32) {
      var low = this.low_;
      return Timestamp.fromBits(
                 (low >>> numBits) | (high << (32 - numBits)),
                 high >> numBits);
    } else {
      return Timestamp.fromBits(
                 high >> (numBits - 32),
                 high >= 0 ? 0 : -1);
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Timestamp.prototype.shiftRightUnsigned"></a>[function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>shiftRightUnsigned (numBits)](#apidoc.element.mongodb.Timestamp.prototype.shiftRightUnsigned)
- description and source-code
```javascript
shiftRightUnsigned = function (numBits) {
  numBits &= 63;
  if (numBits == 0) {
    return this;
  } else {
    var high = this.high_;
    if (numBits < 32) {
      var low = this.low_;
      return Timestamp.fromBits(
                 (low >>> numBits) | (high << (32 - numBits)),
                 high >>> numBits);
    } else if (numBits == 32) {
      return Timestamp.fromBits(high, 0);
    } else {
      return Timestamp.fromBits(high >>> (numBits - 32), 0);
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Timestamp.prototype.subtract"></a>[function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>subtract (other)](#apidoc.element.mongodb.Timestamp.prototype.subtract)
- description and source-code
```javascript
subtract = function (other) {
  return this.add(other.negate());
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Timestamp.prototype.toInt"></a>[function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>toInt ()](#apidoc.element.mongodb.Timestamp.prototype.toInt)
- description and source-code
```javascript
toInt = function () {
  return this.low_;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Timestamp.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>toJSON ()](#apidoc.element.mongodb.Timestamp.prototype.toJSON)
- description and source-code
```javascript
toJSON = function () {
  return this.toString();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Timestamp.prototype.toNumber"></a>[function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>toNumber ()](#apidoc.element.mongodb.Timestamp.prototype.toNumber)
- description and source-code
```javascript
toNumber = function () {
  return this.high_ * Timestamp.TWO_PWR_32_DBL_ +
         this.getLowBitsUnsigned();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Timestamp.prototype.toString"></a>[function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>toString (opt_radix)](#apidoc.element.mongodb.Timestamp.prototype.toString)
- description and source-code
```javascript
toString = function (opt_radix) {
  var radix = opt_radix || 10;
  if (radix < 2 || 36 < radix) {
    throw Error('radix out of range: ' + radix);
  }

  if (this.isZero()) {
    return '0';
  }

  if (this.isNegative()) {
    if (this.equals(Timestamp.MIN_VALUE)) {
      // We need to change the Timestamp value before it can be negated, so we remove
      // the bottom-most digit in this base and then recurse to do the rest.
      var radixTimestamp = Timestamp.fromNumber(radix);
      var div = this.div(radixTimestamp);
      var rem = div.multiply(radixTimestamp).subtract(this);
      return div.toString(radix) + rem.toInt().toString(radix);
    } else {
      return '-' + this.negate().toString(radix);
    }
  }

  // Do several (6) digits each time through the loop, so as to
  // minimize the calls to the very expensive emulated div.
  var radixToPower = Timestamp.fromNumber(Math.pow(radix, 6));

  var rem = this;
  var result = '';
  while (true) {
    var remDiv = rem.div(radixToPower);
    var intval = rem.subtract(remDiv.multiply(radixToPower)).toInt();
    var digits = intval.toString(radix);

    rem = remDiv;
    if (rem.isZero()) {
      return digits + result;
    } else {
      while (digits.length < 6) {
        digits = '0' + digits;
      }
      result = '' + digits + result;
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.Timestamp.prototype.xor"></a>[function <span class="apidocSignatureSpan">mongodb.Timestamp.prototype.</span>xor (other)](#apidoc.element.mongodb.Timestamp.prototype.xor)
- description and source-code
```javascript
xor = function (other) {
  return Timestamp.fromBits(this.low_ ^ other.low_, this.high_ ^ other.high_);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.aggregation_cursor"></a>[module mongodb.aggregation_cursor](#apidoc.module.mongodb.aggregation_cursor)

#### <a name="apidoc.element.mongodb.aggregation_cursor.aggregation_cursor"></a>[function <span class="apidocSignatureSpan">mongodb.</span>aggregation_cursor (bson, ns, cmd, options, topology, topologyOptions)](#apidoc.element.mongodb.aggregation_cursor.aggregation_cursor)
- description and source-code
```javascript
aggregation_cursor = function (bson, ns, cmd, options, topology, topologyOptions) {
  CoreCursor.apply(this, Array.prototype.slice.call(arguments, 0));
  var state = AggregationCursor.INIT;
  var streamOptions = {};

  // MaxTimeMS
  var maxTimeMS = null;

  // Get the promiseLibrary
  var promiseLibrary = options.promiseLibrary;

  // No promise library selected fall back
  if(!promiseLibrary) {
    promiseLibrary = typeof global.Promise == 'function' ?
      global.Promise : require('es6-promise').Promise;
  }

  // Set up
  Readable.call(this, {objectMode: true});

  // Internal state
  this.s = {
    // MaxTimeMS
      maxTimeMS: maxTimeMS
    // State
    , state: state
    // Stream options
    , streamOptions: streamOptions
    // BSON
    , bson: bson
    // Namespace
    , ns: ns
    // Command
    , cmd: cmd
    // Options
    , options: options
    // Topology
    , topology: topology
    // Topology Options
    , topologyOptions: topologyOptions
    // Promise library
    , promiseLibrary: promiseLibrary
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.super_"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.</span>super_ (options)](#apidoc.element.mongodb.aggregation_cursor.super_)
- description and source-code
```javascript
function Readable(options) {
  if (!(this instanceof Readable))
    return new Readable(options);

  this._readableState = new ReadableState(options, this);

  // legacy
  this.readable = true;

  if (options && typeof options.read === 'function')
    this._read = options.read;

  Stream.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.aggregation_cursor.prototype"></a>[module mongodb.aggregation_cursor.prototype](#apidoc.module.mongodb.aggregation_cursor.prototype)

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype._find"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>_find (callback)](#apidoc.element.mongodb.aggregation_cursor.prototype._find)
- description and source-code
```javascript
_find = function (callback) {
  var self = this;

  if(self.logger.isDebug()) {
    self.logger.debug(f('issue initial query [%s] with flags [%s]'
      , JSON.stringify(self.cmd)
      , JSON.stringify(self.query)));
  }

  var queryCallback = function(err, r) {
    if(err) return callback(err);

    // Get the raw message
    var result = r.message;

    // Query failure bit set
    if(result.queryFailure) {
      return callback(MongoError.create(result.documents[0]), null);
    }

    // Check if we have a command cursor
    if(Array.isArray(result.documents) && result.documents.length == 1
      && (!self.cmd.find || (self.cmd.find && self.cmd.virtual == false))
      && (result.documents[0].cursor != 'string'
        || result.documents[0]['$err']
        || result.documents[0]['errmsg']
        || Array.isArray(result.documents[0].result))
      ) {

      // We have a an error document return the error
      if(result.documents[0]['$err']
        || result.documents[0]['errmsg']) {
        return callback(MongoError.create(result.documents[0]), null);
      }

      // We have a cursor document
      if(result.documents[0].cursor != null
        && typeof result.documents[0].cursor != 'string') {
          var id = result.documents[0].cursor.id;
          // If we have a namespace change set the new namespace for getmores
          if(result.documents[0].cursor.ns) {
            self.ns = result.documents[0].cursor.ns;
          }
          // Promote id to long if needed
          self.cursorState.cursorId = typeof id == 'number' ? Long.fromNumber(id) : id;
          self.cursorState.lastCursorId = self.cursorState.cursorId;
          // If we have a firstBatch set it
          if(Array.isArray(result.documents[0].cursor.firstBatch)) {
            self.cursorState.documents = result.documents[0].cursor.firstBatch;//.reverse();
          }

          // Return after processing command cursor
          return callback(null, null);
      }

      if(Array.isArray(result.documents[0].result)) {
        self.cursorState.documents = result.documents[0].result;
        self.cursorState.cursorId = Long.ZERO;
        return callback(null, null);
      }
    }

    // Otherwise fall back to regular find path
    self.cursorState.cursorId = result.cursorId;
    self.cursorState.documents = result.documents;
    self.cursorState.lastCursorId = result.cursorId;

    // Transform the results with passed in transformation method if provided
    if(self.cursorState.transforms && typeof self.cursorState.transforms.query == 'function') {
      self.cursorState.documents = self.cursorState.transforms.query(result);
    }

    // Return callback
    callback(null, null);
  }

  // Options passed to the pool
  var queryOptions = {};

  // If we have a raw query decorate the function
  if(self.options.raw || self.cmd.raw) {
    // queryCallback.raw = self.options.raw || self.cmd.raw;
    queryOptions.raw = self.options.raw || self.cmd.raw;
  }

  // Do we have documentsReturnedIn set on the query
  if(typeof self.query.documentsReturnedIn == 'string') {
    // queryCallback.documentsReturnedIn = self.query.documentsReturnedIn;
    queryOptions.documentsReturnedIn = self.query.documentsReturnedIn;
  }

  // Add promote Long value if defined
  if(typeof self.cursorState.promoteLongs == 'boolean') {
    queryOptions.promoteLongs = self.cursorState.promoteLongs;
  }

  // Add promote values if defined
  if(typeof self.cursorState.promoteValues == 'boolean') {
    queryOptions.promoteValues = self.cursorState.promoteValues;
  }

  // Add promote values if defined
  if(typeof self.cursorState.promoteBuffers == 'boolean') {
    queryOptions.promoteBuffers = self.cursorState.promoteBuffers;
  }
  // Write the initial command out
  self.server.s.pool.write(self.query, queryOptions, queryCallback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype._getmore"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>_getmore (callback)](#apidoc.element.mongodb.aggregation_cursor.prototype._getmore)
- description and source-code
```javascript
_getmore = function (callback) {
  if(this.logger.isDebug()) this.logger.debug(f('schedule getMore call for query [%s]', JSON.stringify(this.query)))
  // Determine if it's a raw query
  var raw = this.options.raw || this.cmd.raw;

  // Set the current batchSize
  var batchSize = this.cursorState.batchSize;
  if(this.cursorState.limit > 0
    && ((this.cursorState.currentLimit + batchSize) > this.cursorState.limit)) {
    batchSize = this.cursorState.limit - this.cursorState.currentLimit;
  }

  // Default pool
  var pool = this.server.s.pool;

  // We have a wire protocol handler
  this.server.wireProtocolHandler.getMore(this.bson, this.ns, this.cursorState, batchSize, raw, pool, this.options, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype._killcursor"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>_killcursor (callback)](#apidoc.element.mongodb.aggregation_cursor.prototype._killcursor)
- description and source-code
```javascript
_killcursor = function (callback) {
  // Set cursor to dead
  this.cursorState.dead = true;
  this.cursorState.killed = true;
  // Remove documents
  this.cursorState.documents = [];

  // If no cursor id just return
  if(this.cursorState.cursorId == null || this.cursorState.cursorId.isZero() || this.cursorState.init == false) {
    if(callback) callback(null, null);
    return;
  }

  // Default pool
  var pool = this.server.s.pool;
  // Execute command
  this.server.wireProtocolHandler.killCursor(this.bson, this.ns, this.cursorState.cursorId, pool, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype._next"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>_next (callback)](#apidoc.element.mongodb.aggregation_cursor.prototype._next)
- description and source-code
```javascript
_next = function (callback) {
  nextFunction(this, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype._read"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>_read ()](#apidoc.element.mongodb.aggregation_cursor.prototype._read)
- description and source-code
```javascript
_read = function () {
  var self = this;
  if(self.s.state == Cursor.CLOSED || self.isDead()) {
    return self.push(null);
  }

  // Get the next item
  self.nextObject(function(err, result) {
    if(err) {
      if(self.listeners('error') && self.listeners('error').length > 0) {
        self.emit('error', err);
      }
      if(!self.isDead()) self.close();

      // Emit end event
      self.emit('end');
      return self.emit('finish');
    }

    // If we provided a transformation method
    if(typeof self.s.streamOptions.transform == 'function' && result != null) {
      return self.push(self.s.streamOptions.transform(result));
    }

    // If we provided a map function
    if(self.cursorState.transforms && typeof self.cursorState.transforms.doc == 'function' && result != null) {
      return self.push(self.cursorState.transforms.doc(result));
    }

    // Return the result
    self.push(result);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.addCursorFlag"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>addCursorFlag (flag, value)](#apidoc.element.mongodb.aggregation_cursor.prototype.addCursorFlag)
- description and source-code
```javascript
addCursorFlag = function (flag, value) {
  if(this.s.state == Cursor.CLOSED || this.s.state == Cursor.OPEN || this.isDead()) throw MongoError.create({message: "Cursor is
 closed", driver:true});
  if(flags.indexOf(flag) == -1) throw MongoError.create({message: f("flag %s not a supported flag %s", flag, flags), driver:true
 });
  if(typeof value != 'boolean') throw MongoError.create({message: f("flag %s must be a boolean value", flag), driver:true});
  this.s.cmd[flag] = value;
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.addListener"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>addListener (ev, fn)](#apidoc.element.mongodb.aggregation_cursor.prototype.addListener)
- description and source-code
```javascript
addListener = function (ev, fn) {
  const res = Stream.prototype.on.call(this, ev, fn);

  if (ev === 'data') {
    // Start flowing on next tick if stream isn't explicitly paused
    if (this._readableState.flowing !== false)
      this.resume();
  } else if (ev === 'readable') {
    const state = this._readableState;
    if (!state.endEmitted && !state.readableListening) {
      state.readableListening = state.needReadable = true;
      state.emittedReadable = false;
      if (!state.reading) {
        process.nextTick(nReadingNextTick, this);
      } else if (state.length) {
        emitReadable(this, state);
      }
    }
  }

  return res;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.addQueryModifier"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>addQueryModifier (name, value)](#apidoc.element.mongodb.aggregation_cursor.prototype.addQueryModifier)
- description and source-code
```javascript
addQueryModifier = function (name, value) {
  if(this.s.state == Cursor.CLOSED || this.s.state == Cursor.OPEN || this.isDead()) throw MongoError.create({message: "Cursor is
 closed", driver:true});
  if(name[0] != '$') throw MongoError.create({message: f("%s is not a valid query modifier"), driver:true});
  // Strip of the $
  var field = name.substr(1);
  // Set on the command
  this.s.cmd[field] = value;
  // Deal with the special case for sort
  if(field == 'orderby') this.s.cmd.sort = this.s.cmd[field];
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.batchSize"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>batchSize (value)](#apidoc.element.mongodb.aggregation_cursor.prototype.batchSize)
- description and source-code
```javascript
batchSize = function (value) {
  if(this.s.state == AggregationCursor.CLOSED || this.isDead()) throw MongoError.create({message: "Cursor is closed", driver:true
 });
  if(typeof value != 'number') throw MongoError.create({message: "batchSize requires an integer", drvier:true });
  if(this.s.cmd.cursor) this.s.cmd.cursor.batchSize = value;
  this.setCursorBatchSize(value);
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.bufferedCount"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>bufferedCount ()](#apidoc.element.mongodb.aggregation_cursor.prototype.bufferedCount)
- description and source-code
```javascript
bufferedCount = function () {
  return this.cursorState.documents.length - this.cursorState.cursorIndex;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.clone"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>clone ()](#apidoc.element.mongodb.aggregation_cursor.prototype.clone)
- description and source-code
```javascript
clone = function () {
  return this.topology.cursor(this.ns, this.cmd, this.options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.close"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>close (callback)](#apidoc.element.mongodb.aggregation_cursor.prototype.close)
- description and source-code
```javascript
close = function (callback) {
  this.s.state = Cursor.CLOSED;
  // Kill the cursor
  this.kill();
  // Emit the close event for the cursor
  this.emit('close');
  // Callback if provided
  if(typeof callback == 'function') return handleCallback(callback, null, this);
  // Return a Promise
  return new this.s.promiseLibrary(function(resolve) {
    resolve();
  });
}
```
- example usage
```shell
...
// Connection URL
var url = 'mongodb://localhost:27017/myproject';
// Use connect method to connect to the Server
MongoClient.connect(url, function(err, db) {
  assert.equal(null, err);
  console.log("Connected correctly to server");

  db.close();
});
'''

Given that you booted up the **mongod** process earlier the application should connect successfully and print **Connected correctly
 to server** to the console.

Let's Add some code to show the different CRUD operations available.
...
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.collation"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>collation (value)](#apidoc.element.mongodb.aggregation_cursor.prototype.collation)
- description and source-code
```javascript
collation = function (value) {
  this.s.cmd.collation = value;
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.comment"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>comment (value)](#apidoc.element.mongodb.aggregation_cursor.prototype.comment)
- description and source-code
```javascript
comment = function (value) {
  if(this.s.state == Cursor.CLOSED || this.s.state == Cursor.OPEN || this.isDead()) throw MongoError.create({message: "Cursor is
 closed", driver:true});
  this.s.cmd.comment = value;
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.count"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>count (applySkipLimit, opts, callback)](#apidoc.element.mongodb.aggregation_cursor.prototype.count)
- description and source-code
```javascript
count = function (applySkipLimit, opts, callback) {
  var self = this;
  if(self.s.cmd.query == null) throw MongoError.create({message: "count can only be used with find command", driver:true});
  if(typeof opts == 'function') callback = opts, opts = {};
  opts = opts || {};

  // Execute using callback
  if(typeof callback == 'function') return count(self, applySkipLimit, opts, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    count(self, applySkipLimit, opts, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.cursorBatchSize"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>cursorBatchSize ()](#apidoc.element.mongodb.aggregation_cursor.prototype.cursorBatchSize)
- description and source-code
```javascript
cursorBatchSize = function () {
  return this.cursorState.batchSize;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.cursorLimit"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>cursorLimit ()](#apidoc.element.mongodb.aggregation_cursor.prototype.cursorLimit)
- description and source-code
```javascript
cursorLimit = function () {
  return this.cursorState.limit;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.cursorSkip"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>cursorSkip ()](#apidoc.element.mongodb.aggregation_cursor.prototype.cursorSkip)
- description and source-code
```javascript
cursorSkip = function () {
  return this.cursorState.skip;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.destroy"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>destroy (err)](#apidoc.element.mongodb.aggregation_cursor.prototype.destroy)
- description and source-code
```javascript
destroy = function (err) {
  if(err) this.emit('error', err);
  this.pause();
  this.close();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.each"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>each (callback)](#apidoc.element.mongodb.aggregation_cursor.prototype.each)
- description and source-code
```javascript
each = function (callback) {
  // Rewind cursor state
  this.rewind();
  // Set current cursor to INIT
  this.s.state = Cursor.INIT;
  // Run the query
  _each(this, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.emit"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>emit (type)](#apidoc.element.mongodb.aggregation_cursor.prototype.emit)
- description and source-code
```javascript
function emit(type) {
  var er, handler, len, args, i, events, domain;
  var needDomainExit = false;
  var doError = (type === 'error');

  events = this._events;
  if (events)
    doError = (doError && events.error == null);
  else if (!doError)
    return false;

  domain = this.domain;

  // If there is no 'error' event listener then throw.
  if (doError) {
    er = arguments[1];
    if (domain) {
      if (!er)
        er = new Error('Uncaught, unspecified "error" event');
      er.domainEmitter = this;
      er.domain = domain;
      er.domainThrown = false;
      domain.emit('error', er);
    } else if (er instanceof Error) {
      throw er; // Unhandled 'error' event
    } else {
      // At least give some kind of context to the user
      var err = new Error('Uncaught, unspecified "error" event. (' + er + ')');
      err.context = er;
      throw err;
    }
    return false;
  }

  handler = events[type];

  if (!handler)
    return false;

  if (domain && this !== process) {
    domain.enter();
    needDomainExit = true;
  }

  var isFn = typeof handler === 'function';
  len = arguments.length;
  switch (len) {
    // fast cases
    case 1:
      emitNone(handler, isFn, this);
      break;
    case 2:
      emitOne(handler, isFn, this, arguments[1]);
      break;
    case 3:
      emitTwo(handler, isFn, this, arguments[1], arguments[2]);
      break;
    case 4:
      emitThree(handler, isFn, this, arguments[1], arguments[2], arguments[3]);
      break;
    // slower
    default:
      args = new Array(len - 1);
      for (i = 1; i < len; i++)
        args[i - 1] = arguments[i];
      emitMany(handler, isFn, this, args);
  }

  if (needDomainExit)
    domain.exit();

  return true;
}
```
- example usage
```shell
...
// Filter out any sensitive commands
if(senstiveCommands.indexOf(commandName.toLowerCase()) != -1) {
  command.commandObj = {};
  command.commandObj[commandName] = true;
}

// Emit the started event
self.emit('started', command)

// Start time
var startTime = timestampGenerator.current();

// Push our handler callback
args.push(function(err, r) {
  var endTime = timestampGenerator.current();
...
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.eventNames"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>eventNames ()](#apidoc.element.mongodb.aggregation_cursor.prototype.eventNames)
- description and source-code
```javascript
function eventNames() {
  return this._eventsCount > 0 ? Reflect.ownKeys(this._events) : [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.explain"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>explain (callback)](#apidoc.element.mongodb.aggregation_cursor.prototype.explain)
- description and source-code
```javascript
explain = function (callback) {
  var self = this;
  this.s.cmd.explain = true;

  // Do we have a readConcern
  if(this.s.cmd.readConcern) {
    delete this.s.cmd['readConcern'];
  }

  // Execute using callback
  if(typeof callback == 'function') return this._next(callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    self._next(function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.filter"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>filter (filter)](#apidoc.element.mongodb.aggregation_cursor.prototype.filter)
- description and source-code
```javascript
filter = function (filter) {
  if(this.s.state == Cursor.CLOSED || this.s.state == Cursor.OPEN || this.isDead()) throw MongoError.create({message: "Cursor is
 closed", driver:true});
  this.s.cmd.query = filter;
  return this;
}
```
- example usage
```shell
...

    // No entry returned for duplicate servr
    if(deduplicatedServers[_host + "_" + _port]) return null;
    deduplicatedServers[_host + "_" + _port] = 1;

    // Return the mapped object
    return {host: _host, port: _port};
  }).filter(function(x) {
    return x != null;
  });
}

// Get the db name
object.dbName = dbName || 'admin';
// Split up all the options
...
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.forEach"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>forEach (iterator, callback)](#apidoc.element.mongodb.aggregation_cursor.prototype.forEach)
- description and source-code
```javascript
forEach = function (iterator, callback) {
  this.each(function(err, doc){
    if(err) { callback(err); return false; }
    if(doc != null) { iterator(doc); return true; }
    if(doc == null && callback) {
      var internalCallback = callback;
      callback = null;
      internalCallback(null);
      return false;
    }
  });
}
```
- example usage
```shell
...
  // Reference
  var self = this;
  // Names of methods we need to wrap
  var methods = ['command', 'insert', 'update', 'remove'];
  // Prototype
  var proto = core.Server.prototype;
  // Core server method we are going to wrap
  methods.forEach(function(x) {
var func = proto[x];

// Add to overloaded methods
self.overloads.push({proto: proto, name:x, func:func});

// The actual prototype
proto[x] = function() {
...
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.geoNear"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>geoNear (document)](#apidoc.element.mongodb.aggregation_cursor.prototype.geoNear)
- description and source-code
```javascript
geoNear = function (document) {
  this.s.cmd.pipeline.push({$geoNear: document});
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.get"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>get (callback)](#apidoc.element.mongodb.aggregation_cursor.prototype.get)
- description and source-code
```javascript
get = function (callback) {
  var self = this;
  if(self.s.options.tailable) throw MongoError.create({message: 'Tailable cursor cannot be converted to array', driver:true});

  // Execute using callback
  if(typeof callback == 'function') return toArray(self, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    toArray(self, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
...
// Get the callback
var callback = args.pop();
// Set current callback operation id from the current context or create
// a new one
var ourOpId = callback.operationId || operationIdGenerator.next();

// Get a connection reference for this server instance
var connection = this.s.pool.get()

// Emit the start event for the command
var command = {
  // Returns the command.
  command: commandObj,
  // Returns the database name.
  databaseName: db,
...
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.getMaxListeners"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>getMaxListeners ()](#apidoc.element.mongodb.aggregation_cursor.prototype.getMaxListeners)
- description and source-code
```javascript
function getMaxListeners() {
  return $getMaxListeners(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.group"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>group (document)](#apidoc.element.mongodb.aggregation_cursor.prototype.group)
- description and source-code
```javascript
group = function (document) {
  this.s.cmd.pipeline.push({$group: document});
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.hasNext"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>hasNext (callback)](#apidoc.element.mongodb.aggregation_cursor.prototype.hasNext)
- description and source-code
```javascript
hasNext = function (callback) {
  var self = this;

  // Execute using callback
  if(typeof callback == 'function') {
    if(self.s.currentDoc){
      return callback(null, true);
    } else {
      return nextObject(self, function(err, doc) {
        if(!doc) return callback(null, false);
        self.s.currentDoc = doc;
        callback(null, true);
      });
    }
  }

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    if(self.s.currentDoc){
      resolve(true);
    } else {
      nextObject(self, function(err, doc) {
        if(self.s.state == Cursor.CLOSED || self.isDead()) return resolve(false);
        if(err) return reject(err);
        if(!doc) return resolve(false);
        self.s.currentDoc = doc;
        resolve(true);
      });
    }
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.hint"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>hint (hint)](#apidoc.element.mongodb.aggregation_cursor.prototype.hint)
- description and source-code
```javascript
hint = function (hint) {
  if(this.s.state == Cursor.CLOSED || this.s.state == Cursor.OPEN || this.isDead()) throw MongoError.create({message: "Cursor is
 closed", driver:true});
  this.s.cmd.hint = hint;
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.isClosed"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>isClosed ()](#apidoc.element.mongodb.aggregation_cursor.prototype.isClosed)
- description and source-code
```javascript
isClosed = function () {
  return this.isDead();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.isDead"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>isDead ()](#apidoc.element.mongodb.aggregation_cursor.prototype.isDead)
- description and source-code
```javascript
isDead = function () {
  return this.cursorState.dead == true;
}
```
- example usage
```shell
...
 * Set the batch size for the cursor.
 * @method
 * @param {number} value The batchSize for the cursor.
 * @throws {MongoError}
 * @return {AggregationCursor}
 */
AggregationCursor.prototype.batchSize = function(value) {
  if(this.s.state == AggregationCursor.CLOSED || this.isDead()) throw MongoError.create({message: "Cursor is closed", driver:true
 });
  if(typeof value != 'number') throw MongoError.create({message: "batchSize requires an integer", drvier:true });
  if(this.s.cmd.cursor) this.s.cmd.cursor.batchSize = value;
  this.setCursorBatchSize(value);
  return this;
}

define.classMethod('batchSize', {callback: false, promise:false, returns: [AggregationCursor]});
...
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.isKilled"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>isKilled ()](#apidoc.element.mongodb.aggregation_cursor.prototype.isKilled)
- description and source-code
```javascript
isKilled = function () {
  return this.cursorState.killed == true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.isNotified"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>isNotified ()](#apidoc.element.mongodb.aggregation_cursor.prototype.isNotified)
- description and source-code
```javascript
isNotified = function () {
  return this.cursorState.notified == true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.isPaused"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>isPaused ()](#apidoc.element.mongodb.aggregation_cursor.prototype.isPaused)
- description and source-code
```javascript
isPaused = function () {
  return this._readableState.flowing === false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.kill"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>kill (callback)](#apidoc.element.mongodb.aggregation_cursor.prototype.kill)
- description and source-code
```javascript
kill = function (callback) {
  this._killcursor(callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.limit"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>limit (value)](#apidoc.element.mongodb.aggregation_cursor.prototype.limit)
- description and source-code
```javascript
limit = function (value) {
  this.s.cmd.pipeline.push({$limit: value});
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.listenerCount"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>listenerCount (type)](#apidoc.element.mongodb.aggregation_cursor.prototype.listenerCount)
- description and source-code
```javascript
function listenerCount(type) {
  const events = this._events;

  if (events) {
    const evlistener = events[type];

    if (typeof evlistener === 'function') {
      return 1;
    } else if (evlistener) {
      return evlistener.length;
    }
  }

  return 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.listeners"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>listeners (type)](#apidoc.element.mongodb.aggregation_cursor.prototype.listeners)
- description and source-code
```javascript
function listeners(type) {
  var evlistener;
  var ret;
  var events = this._events;

  if (!events)
    ret = [];
  else {
    evlistener = events[type];
    if (!evlistener)
      ret = [];
    else if (typeof evlistener === 'function')
      ret = [evlistener];
    else
      ret = arrayClone(evlistener, evlistener.length);
  }

  return ret;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.lookup"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>lookup (document)](#apidoc.element.mongodb.aggregation_cursor.prototype.lookup)
- description and source-code
```javascript
lookup = function (document) {
  this.s.cmd.pipeline.push({$lookup: document});
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.map"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>map (transform)](#apidoc.element.mongodb.aggregation_cursor.prototype.map)
- description and source-code
```javascript
map = function (transform) {
  this.cursorState.transforms = { doc: transform };
  return this;
}
```
- example usage
```shell
...
  } else {
// Split up the db
hostPart = connection_part;
// Deduplicate servers
var deduplicatedServers = {};

// Parse all server results
servers = hostPart.split(',').map(function(h) {
  var _host, _port, ipv6match;
  //check if it matches [IPv6]:port, where the port number is optional
  if ((ipv6match = /\[([^\]]+)\](?:\:(.+))?/.exec(h))) {
    _host = ipv6match[1];
    _port = parseInt(ipv6match[2], 10) || 27017;
  } else {
    //otherwise assume it's IPv4, or plain hostname
...
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.match"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>match (document)](#apidoc.element.mongodb.aggregation_cursor.prototype.match)
- description and source-code
```javascript
match = function (document) {
  this.s.cmd.pipeline.push({$match: document});
  return this;
}
```
- example usage
```shell
...
// Add server options to final object
object.server_options = serverOptions;
object.db_options = dbOptions;
object.rs_options = replSetServersOptions;
object.mongos_options = mongosOptions;

// Let's check if we are using a domain socket
if(url.match(/\.sock/)) {
  // Split out the socket part
  var domainSocket = url.substring(
      url.indexOf("mongodb://") + "mongodb://".length
    , url.lastIndexOf(".sock") + ".sock".length);
  // Clean out any auth stuff if any
  if(domainSocket.indexOf("@") != -1) domainSocket = domainSocket.split("@")[1];
  servers = [{domain_socket: domainSocket}];
...
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.max"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>max (max)](#apidoc.element.mongodb.aggregation_cursor.prototype.max)
- description and source-code
```javascript
max = function (max) {
  if(this.s.state == Cursor.CLOSED || this.s.state == Cursor.OPEN || this.isDead()) throw MongoError.create({message: "Cursor is
 closed", driver:true});
  this.s.cmd.max = max;
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.maxAwaitTimeMS"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>maxAwaitTimeMS (value)](#apidoc.element.mongodb.aggregation_cursor.prototype.maxAwaitTimeMS)
- description and source-code
```javascript
maxAwaitTimeMS = function (value) {
  if(typeof value != 'number') throw MongoError.create({message: "maxAwaitTimeMS must be a number", driver:true});
  if(this.s.state == Cursor.CLOSED || this.s.state == Cursor.OPEN || this.isDead()) throw MongoError.create({message: "Cursor is
 closed", driver:true});
  this.s.cmd.maxAwaitTimeMS = value;
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.maxScan"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>maxScan (maxScan)](#apidoc.element.mongodb.aggregation_cursor.prototype.maxScan)
- description and source-code
```javascript
maxScan = function (maxScan) {
  if(this.s.state == Cursor.CLOSED || this.s.state == Cursor.OPEN || this.isDead()) throw MongoError.create({message: "Cursor is
 closed", driver:true});
  this.s.cmd.maxScan = maxScan;
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.maxTimeMS"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>maxTimeMS (value)](#apidoc.element.mongodb.aggregation_cursor.prototype.maxTimeMS)
- description and source-code
```javascript
maxTimeMS = function (value) {
  if(this.s.topology.lastIsMaster().minWireVersion > 2) {
    this.s.cmd.maxTimeMS = value;
  }
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.maxTimeMs"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>maxTimeMs (value)](#apidoc.element.mongodb.aggregation_cursor.prototype.maxTimeMs)
- description and source-code
```javascript
maxTimeMs = function (value) {
  if(typeof value != 'number') throw MongoError.create({message: "maxTimeMS must be a number", driver:true});
  if(this.s.state == Cursor.CLOSED || this.s.state == Cursor.OPEN || this.isDead()) throw MongoError.create({message: "Cursor is
 closed", driver:true});
  this.s.cmd.maxTimeMS = value;
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.min"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>min (min)](#apidoc.element.mongodb.aggregation_cursor.prototype.min)
- description and source-code
```javascript
min = function (min) {
  if(this.s.state == Cursor.CLOSED || this.s.state == Cursor.OPEN || this.isDead()) throw MongoError.create({message: "Cursor is
 closed", driver:true});
  this.s.cmd.min = min;
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.next"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>next (callback)](#apidoc.element.mongodb.aggregation_cursor.prototype.next)
- description and source-code
```javascript
next = function (callback) {
  var self = this;

  // Execute using callback
  if(typeof callback == 'function') {
    // Return the currentDoc if someone called hasNext first
    if(self.s.currentDoc) {
      var doc = self.s.currentDoc;
      self.s.currentDoc = null;
      return callback(null, doc);
    }

    // Return the next object
    return nextObject(self, callback)
  }

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    // Return the currentDoc if someone called hasNext first
    if(self.s.currentDoc) {
      var doc = self.s.currentDoc;
      self.s.currentDoc = null;
      return resolve(doc);
    }

    nextObject(self, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
...
  commandObj.ordered = options.ordered != undefined ? options.ordered : true;
}

// Get the callback
var callback = args.pop();
// Set current callback operation id from the current context or create
// a new one
var ourOpId = callback.operationId || operationIdGenerator.next();

// Get a connection reference for this server instance
var connection = this.s.pool.get()

// Emit the start event for the command
var command = {
  // Returns the command.
...
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.nextObject"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>nextObject (callback)](#apidoc.element.mongodb.aggregation_cursor.prototype.nextObject)
- description and source-code
```javascript
nextObject = function (callback) {
  var self = this;

  // Execute using callback
  if(typeof callback == 'function') {
    // Return the currentDoc if someone called hasNext first
    if(self.s.currentDoc) {
      var doc = self.s.currentDoc;
      self.s.currentDoc = null;
      return callback(null, doc);
    }

    // Return the next object
    return nextObject(self, callback)
  }

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    // Return the currentDoc if someone called hasNext first
    if(self.s.currentDoc) {
      var doc = self.s.currentDoc;
      self.s.currentDoc = null;
      return resolve(doc);
    }

    nextObject(self, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.on"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>on (ev, fn)](#apidoc.element.mongodb.aggregation_cursor.prototype.on)
- description and source-code
```javascript
on = function (ev, fn) {
  const res = Stream.prototype.on.call(this, ev, fn);

  if (ev === 'data') {
    // Start flowing on next tick if stream isn't explicitly paused
    if (this._readableState.flowing !== false)
      this.resume();
  } else if (ev === 'readable') {
    const state = this._readableState;
    if (!state.endEmitted && !state.readableListening) {
      state.readableListening = state.needReadable = true;
      state.emittedReadable = false;
      if (!state.reading) {
        process.nextTick(nReadingNextTick, this);
      } else if (state.length) {
        emitReadable(this, state);
      }
    }
  }

  return res;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.once"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>once (type, listener)](#apidoc.element.mongodb.aggregation_cursor.prototype.once)
- description and source-code
```javascript
function once(type, listener) {
  if (typeof listener !== 'function')
    throw new TypeError('"listener" argument must be a function');
  this.on(type, _onceWrap(this, type, listener));
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.out"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>out (destination)](#apidoc.element.mongodb.aggregation_cursor.prototype.out)
- description and source-code
```javascript
out = function (destination) {
  this.s.cmd.pipeline.push({$out: destination});
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.pause"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>pause ()](#apidoc.element.mongodb.aggregation_cursor.prototype.pause)
- description and source-code
```javascript
pause = function () {
  debug('call pause flowing=%j', this._readableState.flowing);
  if (false !== this._readableState.flowing) {
    debug('pause');
    this._readableState.flowing = false;
    this.emit('pause');
  }
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.pipe"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>pipe (dest, pipeOpts)](#apidoc.element.mongodb.aggregation_cursor.prototype.pipe)
- description and source-code
```javascript
pipe = function (dest, pipeOpts) {
  var src = this;
  var state = this._readableState;

  switch (state.pipesCount) {
    case 0:
      state.pipes = dest;
      break;
    case 1:
      state.pipes = [state.pipes, dest];
      break;
    default:
      state.pipes.push(dest);
      break;
  }
  state.pipesCount += 1;
  debug('pipe count=%d opts=%j', state.pipesCount, pipeOpts);

  var doEnd = (!pipeOpts || pipeOpts.end !== false) &&
              dest !== process.stdout &&
              dest !== process.stderr;

  var endFn = doEnd ? onend : cleanup;
  if (state.endEmitted)
    process.nextTick(endFn);
  else
    src.once('end', endFn);

  dest.on('unpipe', onunpipe);
  function onunpipe(readable) {
    debug('onunpipe');
    if (readable === src) {
      cleanup();
    }
  }

  function onend() {
    debug('onend');
    dest.end();
  }

  // when the dest drains, it reduces the awaitDrain counter
  // on the source.  This would be more elegant with a .once()
  // handler in flow(), but adding and removing repeatedly is
  // too slow.
  var ondrain = pipeOnDrain(src);
  dest.on('drain', ondrain);

  var cleanedUp = false;
  function cleanup() {
    debug('cleanup');
    // cleanup event handlers once the pipe is broken
    dest.removeListener('close', onclose);
    dest.removeListener('finish', onfinish);
    dest.removeListener('drain', ondrain);
    dest.removeListener('error', onerror);
    dest.removeListener('unpipe', onunpipe);
    src.removeListener('end', onend);
    src.removeListener('end', cleanup);
    src.removeListener('data', ondata);

    cleanedUp = true;

    // if the reader is waiting for a drain event from this
    // specific writer, then it would cause it to never start
    // flowing again.
    // So, if this is awaiting a drain, then we just call it now.
    // If we don't know, then assume that we are waiting for one.
    if (state.awaitDrain &&
        (!dest._writableState || dest._writableState.needDrain))
      ondrain();
  }

  // If the user pushes more data while we're writing to dest then we'll end up
  // in ondata again. However, we only want to increase awaitDrain once because
  // dest will only emit one 'drain' event for the multiple writes.
  // => Introduce a guard on increasing awaitDrain.
  var increasedAwaitDrain = false;
  src.on('data', ondata);
  function ondata(chunk) {
    debug('ondata');
    increasedAwaitDrain = false;
    var ret = dest.write(chunk);
    if (false === ret && !increasedAwaitDrain) {
      // If the user unpiped during 'dest.write()', it is possible
      // to get stuck in a permanently paused state if that write
      // also returned false.
      // => Check whether 'dest' is still a piping destination.
      if (((state.pipesCount === 1 && state.pipes === dest) ||
           (state.pipesCount > 1 && state.pipes.indexOf(dest) !== -1)) &&
          !cleanedUp) {
        debug('false write response, pause', src._readableState.awaitDrain);
        src._readableState.awaitDrain++;
        increasedAwaitDrain = true;
      }
      src.pause();
    }
  }

  // if the dest has an error, then stop piping into it.
  // however, don't suppress the throwing behavior for this.
  function onerror(er) {
    debug('onerror', er);
    unpipe();
    dest.removeListener('error', onerror);
    if (EE.listenerCount(dest, 'error') === 0)
      dest.emit('error', er);
  }

  // Make sure our error handler is attached before userland ones.
  prependListener(dest, 'error', onerror);

  // Both close and finish should trigger unpipe, but only once.
  function onclose() {
    dest.removeListener('finish', onfinish);
    unpipe();
  }
  dest.once('close', onclose);
  function onfinish() {
    debug('onfinish');
    dest.removeListener('close', onclose);
    unpipe();
  }
  dest.once('finish', onfinish);

  function unpipe() {
    debug('unpipe');
    src.unpipe(dest);
  }

  // tell the dest that it's being piped to
  dest.emit('pipe', src);

  // start the flow if it hasn't been started already.
  if (!state.flowing) {
    debug('pipe resume');
    src.resume();
  }

  return dest; ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.prependListener"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>prependListener (type, listener)](#apidoc.element.mongodb.aggregation_cursor.prototype.prependListener)
- description and source-code
```javascript
function prependListener(type, listener) {
  return _addListener(this, type, listener, true);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.prependOnceListener"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>prependOnceListener (type, listener)](#apidoc.element.mongodb.aggregation_cursor.prototype.prependOnceListener)
- description and source-code
```javascript
function prependOnceListener(type, listener) {
  if (typeof listener !== 'function')
    throw new TypeError('"listener" argument must be a function');
  this.prependListener(type, _onceWrap(this, type, listener));
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.project"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>project (document)](#apidoc.element.mongodb.aggregation_cursor.prototype.project)
- description and source-code
```javascript
project = function (document) {
  this.s.cmd.pipeline.push({$project: document});
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.push"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>push (chunk, encoding)](#apidoc.element.mongodb.aggregation_cursor.prototype.push)
- description and source-code
```javascript
push = function (chunk, encoding) {
  var state = this._readableState;

  if (!state.objectMode && typeof chunk === 'string') {
    encoding = encoding || state.defaultEncoding;
    if (encoding !== state.encoding) {
      chunk = Buffer.from(chunk, encoding);
      encoding = '';
    }
  }

  return readableAddChunk(this, state, chunk, encoding, false);
}
```
- example usage
```shell
...
/**
* Add a geoNear stage to the aggregation pipeline
* @method
* @param {object} document The geoNear stage document.
* @return {AggregationCursor}
*/
AggregationCursor.prototype.geoNear = function(document) {
 this.s.cmd.pipeline.push({$geoNear: document});
 return this;
}

define.classMethod('geoNear', {callback: false, promise:false, returns: [AggregationCursor]});

/**
* Add a group stage to the aggregation pipeline
...
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.read"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>read (n)](#apidoc.element.mongodb.aggregation_cursor.prototype.read)
- description and source-code
```javascript
read = function (n) {
  debug('read', n);
  n = parseInt(n, 10);
  var state = this._readableState;
  var nOrig = n;

  if (n !== 0)
    state.emittedReadable = false;

  // if we're doing read(0) to trigger a readable event, but we
  // already have a bunch of data in the buffer, then just trigger
  // the 'readable' event and move on.
  if (n === 0 &&
      state.needReadable &&
      (state.length >= state.highWaterMark || state.ended)) {
    debug('read: emitReadable', state.length, state.ended);
    if (state.length === 0 && state.ended)
      endReadable(this);
    else
      emitReadable(this);
    return null;
  }

  n = howMuchToRead(n, state);

  // if we've ended, and we're now clear, then finish it up.
  if (n === 0 && state.ended) {
    if (state.length === 0)
      endReadable(this);
    return null;
  }

  // All the actual chunk generation logic needs to be
  // *below* the call to _read.  The reason is that in certain
  // synthetic stream cases, such as passthrough streams, _read
  // may be a completely synchronous operation which may change
  // the state of the read buffer, providing enough data when
  // before there was *not* enough.
  //
  // So, the steps are:
  // 1. Figure out what the state of things will be after we do
  // a read from the buffer.
  //
  // 2. If that resulting state will trigger a _read, then call _read.
  // Note that this may be asynchronous, or synchronous.  Yes, it is
  // deeply ugly to write APIs this way, but that still doesn't mean
  // that the Readable class should behave improperly, as streams are
  // designed to be sync/async agnostic.
  // Take note if the _read call is sync or async (ie, if the read call
  // has returned yet), so that we know whether or not it's safe to emit
  // 'readable' etc.
  //
  // 3. Actually pull the requested chunks out of the buffer and return.

  // if we need a readable event, then we need to do some reading.
  var doRead = state.needReadable;
  debug('need readable', doRead);

  // if we currently have less than the highWaterMark, then also read some
  if (state.length === 0 || state.length - n < state.highWaterMark) {
    doRead = true;
    debug('length less than watermark', doRead);
  }

  // however, if we've ended, then there's no point, and if we're already
  // reading, then it's unnecessary.
  if (state.ended || state.reading) {
    doRead = false;
    debug('reading or ended', doRead);
  } else if (doRead) {
    debug('do read');
    state.reading = true;
    state.sync = true;
    // if the length is currently zero, then we *need* a readable event.
    if (state.length === 0)
      state.needReadable = true;
    // call internal read method
    this._read(state.highWaterMark);
    state.sync = false;
    // If _read pushed data synchronously, then 'reading' will be false,
    // and we need to re-evaluate how much data we can return to the user.
    if (!state.reading)
      n = howMuchToRead(nOrig, state);
  }

  var ret;
  if (n > 0)
    ret = fromList(n, state);
  else
    ret = null;

  if (ret === null) {
    state.needReadable = true;
    n = 0;
  } else {
    state.length -= n;
  }

  if (state.length === 0) {
    // If we have nothing in the buffer, then we want to know
    // as soon as we *do* get something into the buffer.
    if (!state.ended)
      state.needReadable = true;

    // If we tried to read() past the EOF, then emit end on the next tick.
    if (nOrig !== n && state.ended)
      endReadable(this);
  }

  if (ret !== null)
    this.emit('data', ret);

  return ret;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.readBufferedDocuments"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>readBufferedDocuments (number)](#apidoc.element.mongodb.aggregation_cursor.prototype.readBufferedDocuments)
- description and source-code
```javascript
readBufferedDocuments = function (number) {
  var unreadDocumentsLength = this.cursorState.documents.length - this.cursorState.cursorIndex;
  var length = number < unreadDocumentsLength ? number : unreadDocumentsLength;
  var elements = this.cursorState.documents.slice(this.cursorState.cursorIndex, this.cursorState.cursorIndex + length);

  // Transform the doc with passed in transformation method if provided
  if(this.cursorState.transforms && typeof this.cursorState.transforms.doc == 'function') {
    // Transform all the elements
    for(var i = 0; i < elements.length; i++) {
      elements[i] = this.cursorState.transforms.doc(elements[i]);
    }
  }

  // Ensure we do not return any more documents than the limit imposed
  // Just return the number of elements up to the limit
  if(this.cursorState.limit > 0 && (this.cursorState.currentLimit + elements.length) > this.cursorState.limit) {
    elements = elements.slice(0, (this.cursorState.limit - this.cursorState.currentLimit));
    this.kill();
  }

  // Adjust current limit
  this.cursorState.currentLimit = this.cursorState.currentLimit + elements.length;
  this.cursorState.cursorIndex = this.cursorState.cursorIndex + elements.length;

  // Return elements
  return elements;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.redact"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>redact (document)](#apidoc.element.mongodb.aggregation_cursor.prototype.redact)
- description and source-code
```javascript
redact = function (document) {
  this.s.cmd.pipeline.push({$redact: document});
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.removeAllListeners"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>removeAllListeners (type)](#apidoc.element.mongodb.aggregation_cursor.prototype.removeAllListeners)
- description and source-code
```javascript
function removeAllListeners(type) {
  var listeners, events;

  events = this._events;
  if (!events)
    return this;

  // not listening for removeListener, no need to emit
  if (!events.removeListener) {
    if (arguments.length === 0) {
      this._events = new EventHandlers();
      this._eventsCount = 0;
    } else if (events[type]) {
      if (--this._eventsCount === 0)
        this._events = new EventHandlers();
      else
        delete events[type];
    }
    return this;
  }

  // emit removeListener for all listeners on all events
  if (arguments.length === 0) {
    var keys = Object.keys(events);
    for (var i = 0, key; i < keys.length; ++i) {
      key = keys[i];
      if (key === 'removeListener') continue;
      this.removeAllListeners(key);
    }
    this.removeAllListeners('removeListener');
    this._events = new EventHandlers();
    this._eventsCount = 0;
    return this;
  }

  listeners = events[type];

  if (typeof listeners === 'function') {
    this.removeListener(type, listeners);
  } else if (listeners) {
    // LIFO order
    do {
      this.removeListener(type, listeners[listeners.length - 1]);
    } while (listeners[0]);
  }

  return this;
}
```
- example usage
```shell
...
Instrumentation.prototype.uninstrument = function() {
  for(var i = 0; i < this.overloads.length; i++) {
    var obj = this.overloads[i];
    obj.proto[obj.name] = obj.func;
  }

  // Remove all listeners
  this.removeAllListeners('started');
  this.removeAllListeners('succeeded');
  this.removeAllListeners('failed');
}

module.exports = Instrumentation;
...
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.removeListener"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>removeListener (type, listener)](#apidoc.element.mongodb.aggregation_cursor.prototype.removeListener)
- description and source-code
```javascript
function removeListener(type, listener) {
  var list, events, position, i, originalListener;

  if (typeof listener !== 'function')
    throw new TypeError('"listener" argument must be a function');

  events = this._events;
  if (!events)
    return this;

  list = events[type];
  if (!list)
    return this;

  if (list === listener || list.listener === listener) {
    if (--this._eventsCount === 0)
      this._events = new EventHandlers();
    else {
      delete events[type];
      if (events.removeListener)
        this.emit('removeListener', type, list.listener || listener);
    }
  } else if (typeof list !== 'function') {
    position = -1;

    for (i = list.length; i-- > 0;) {
      if (list[i] === listener || list[i].listener === listener) {
        originalListener = list[i].listener;
        position = i;
        break;
      }
    }

    if (position < 0)
      return this;

    if (list.length === 1) {
      list[0] = undefined;
      if (--this._eventsCount === 0) {
        this._events = new EventHandlers();
        return this;
      } else {
        delete events[type];
      }
    } else {
      spliceOne(list, position);
    }

    if (events.removeListener)
      this.emit('removeListener', type, originalListener || listener);
  }

  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.resume"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>resume ()](#apidoc.element.mongodb.aggregation_cursor.prototype.resume)
- description and source-code
```javascript
resume = function () {
  var state = this._readableState;
  if (!state.flowing) {
    debug('resume');
    state.flowing = true;
    resume(this, state);
  }
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.returnKey"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>returnKey (value)](#apidoc.element.mongodb.aggregation_cursor.prototype.returnKey)
- description and source-code
```javascript
returnKey = function (value) {
  if(this.s.state == Cursor.CLOSED || this.s.state == Cursor.OPEN || this.isDead()) throw MongoError.create({message: "Cursor is
 closed", driver:true});
  this.s.cmd.returnKey = value;
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.rewind"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>rewind ()](#apidoc.element.mongodb.aggregation_cursor.prototype.rewind)
- description and source-code
```javascript
rewind = function () {
  if(this.cursorState.init) {
    if(!this.cursorState.dead) {
      this.kill();
    }

    this.cursorState.currentLimit = 0;
    this.cursorState.init = false;
    this.cursorState.dead = false;
    this.cursorState.killed = false;
    this.cursorState.notified = false;
    this.cursorState.documents = [];
    this.cursorState.cursorId = null;
    this.cursorState.cursorIndex = 0;
  }
}
```
- example usage
```shell
...
 * @param {object[]} documents All the documents the satisfy the cursor.
 */

/**
 * Returns an array of documents. The caller is responsible for making sure that there
 * is enough memory to store the results. Note that the array only contain partial
 * results when this cursor had been previouly accessed. In that case,
 * cursor.rewind() can be used to reset the cursor.
 * @method AggregationCursor.prototype.toArray
 * @param {AggregationCursor~toArrayResultCallback} [callback] The result callback.
 * @throws {MongoError}
 * @return {Promise} returns Promise if no callback passed
 */

/**
...
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.setCursorBatchSize"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>setCursorBatchSize (value)](#apidoc.element.mongodb.aggregation_cursor.prototype.setCursorBatchSize)
- description and source-code
```javascript
setCursorBatchSize = function (value) {
  this.cursorState.batchSize = value;
}
```
- example usage
```shell
...
* @throws {MongoError}
* @return {AggregationCursor}
*/
AggregationCursor.prototype.batchSize = function(value) {
 if(this.s.state == AggregationCursor.CLOSED || this.isDead()) throw MongoError.create({message: "Cursor is closed", driver:true
 });
 if(typeof value != 'number') throw MongoError.create({message: "batchSize requires an integer", drvier:true });
 if(this.s.cmd.cursor) this.s.cmd.cursor.batchSize = value;
 this.setCursorBatchSize(value);
 return this;
}

define.classMethod('batchSize', {callback: false, promise:false, returns: [AggregationCursor]});

/**
* Add a geoNear stage to the aggregation pipeline
...
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.setCursorLimit"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>setCursorLimit (value)](#apidoc.element.mongodb.aggregation_cursor.prototype.setCursorLimit)
- description and source-code
```javascript
setCursorLimit = function (value) {
  this.cursorState.limit = value;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.setCursorOption"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>setCursorOption (field, value)](#apidoc.element.mongodb.aggregation_cursor.prototype.setCursorOption)
- description and source-code
```javascript
setCursorOption = function (field, value) {
  if(this.s.state == Cursor.CLOSED || this.s.state == Cursor.OPEN || this.isDead()) throw MongoError.create({message: "Cursor is
 closed", driver:true});
  if(fields.indexOf(field) == -1) throw MongoError.create({message: f("option %s not a supported option %s", field, fields), driver
:true });
  this.s[field] = value;
  if(field == 'numberOfRetries')
    this.s.currentNumberOfRetries = value;
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.setCursorSkip"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>setCursorSkip (value)](#apidoc.element.mongodb.aggregation_cursor.prototype.setCursorSkip)
- description and source-code
```javascript
setCursorSkip = function (value) {
  this.cursorState.skip = value;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.setEncoding"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>setEncoding (enc)](#apidoc.element.mongodb.aggregation_cursor.prototype.setEncoding)
- description and source-code
```javascript
setEncoding = function (enc) {
  if (!StringDecoder)
    StringDecoder = require('string_decoder').StringDecoder;
  this._readableState.decoder = new StringDecoder(enc);
  this._readableState.encoding = enc;
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.setMaxListeners"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>setMaxListeners (n)](#apidoc.element.mongodb.aggregation_cursor.prototype.setMaxListeners)
- description and source-code
```javascript
function setMaxListeners(n) {
  if (typeof n !== 'number' || n < 0 || isNaN(n))
    throw new TypeError('"n" argument must be a positive number');
  this._maxListeners = n;
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.setReadPreference"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>setReadPreference (r)](#apidoc.element.mongodb.aggregation_cursor.prototype.setReadPreference)
- description and source-code
```javascript
setReadPreference = function (r) {
  if(this.s.state != Cursor.INIT) throw MongoError.create({message: 'cannot change cursor readPreference after cursor has been accessed
', driver:true});
  if(r instanceof ReadPreference) {
    this.s.options.readPreference = new CoreReadPreference(r.mode, r.tags, {maxStalenessSeconds: r.maxStalenessSeconds});
  } else if(typeof r == 'string'){
    this.s.options.readPreference = new CoreReadPreference(r);
  } else if(r instanceof CoreReadPreference) {
    this.s.options.readPreference = r;
  }

  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.showRecordId"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>showRecordId (value)](#apidoc.element.mongodb.aggregation_cursor.prototype.showRecordId)
- description and source-code
```javascript
showRecordId = function (value) {
  if(this.s.state == Cursor.CLOSED || this.s.state == Cursor.OPEN || this.isDead()) throw MongoError.create({message: "Cursor is
 closed", driver:true});
  this.s.cmd.showDiskLoc = value;
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.skip"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>skip (value)](#apidoc.element.mongodb.aggregation_cursor.prototype.skip)
- description and source-code
```javascript
skip = function (value) {
  this.s.cmd.pipeline.push({$skip: value});
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.snapshot"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>snapshot (value)](#apidoc.element.mongodb.aggregation_cursor.prototype.snapshot)
- description and source-code
```javascript
snapshot = function (value) {
  if(this.s.state == Cursor.CLOSED || this.s.state == Cursor.OPEN || this.isDead()) throw MongoError.create({message: "Cursor is
 closed", driver:true});
  this.s.cmd.snapshot = value;
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.sort"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>sort (document)](#apidoc.element.mongodb.aggregation_cursor.prototype.sort)
- description and source-code
```javascript
sort = function (document) {
  this.s.cmd.pipeline.push({$sort: document});
  return this;
}
```
- example usage
```shell
...
this.name = name;
this.object = object;
this.stream = typeof stream == 'boolean' ? stream : false;
this.instrumentations = {};
}

Define.prototype.classMethod = function(name, options) {
var keys = Object.keys(options).sort();
var key = generateKey(keys, options);

// Add a list of instrumentations
if(this.instrumentations[key] == null) {
  this.instrumentations[key] = {
    methods: [], options: options
  }
...
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.stream"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>stream (options)](#apidoc.element.mongodb.aggregation_cursor.prototype.stream)
- description and source-code
```javascript
stream = function (options) {
  this.s.streamOptions = options || {};
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.toArray"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>toArray (callback)](#apidoc.element.mongodb.aggregation_cursor.prototype.toArray)
- description and source-code
```javascript
toArray = function (callback) {
  var self = this;
  if(self.s.options.tailable) throw MongoError.create({message: 'Tailable cursor cannot be converted to array', driver:true});

  // Execute using callback
  if(typeof callback == 'function') return toArray(self, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    toArray(self, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
...
We will finish up the Quickstart CRUD methods by performing a simple query that returns all the documents matching the query.

'''js
var findDocuments = function(db, callback) {
  // Get the documents collection
  var collection = db.collection('documents');
  // Find some documents
  collection.find({}).toArray(function(err, docs) {
    assert.equal(err, null);
    assert.equal(2, docs.length);
    console.log("Found the following records");
    console.dir(docs);
    callback(docs);
  });
}
...
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.unpipe"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>unpipe (dest)](#apidoc.element.mongodb.aggregation_cursor.prototype.unpipe)
- description and source-code
```javascript
unpipe = function (dest) {
  var state = this._readableState;

  // if we're not piping anywhere, then do nothing.
  if (state.pipesCount === 0)
    return this;

  // just one destination.  most common case.
  if (state.pipesCount === 1) {
    // passed in one, but it's not the right one.
    if (dest && dest !== state.pipes)
      return this;

    if (!dest)
      dest = state.pipes;

    // got a match.
    state.pipes = null;
    state.pipesCount = 0;
    state.flowing = false;
    if (dest)
      dest.emit('unpipe', this);
    return this;
  }

  // slow case. multiple pipe destinations.

  if (!dest) {
    // remove all.
    var dests = state.pipes;
    var len = state.pipesCount;
    state.pipes = null;
    state.pipesCount = 0;
    state.flowing = false;

    for (var i = 0; i < len; i++)
      dests[i].emit('unpipe', this);
    return this;
  }

  // try to find the right one.
  const index = state.pipes.indexOf(dest);
  if (index === -1)
    return this;

  state.pipes.splice(index, 1);
  state.pipesCount -= 1;
  if (state.pipesCount === 1)
    state.pipes = state.pipes[0];

  dest.emit('unpipe', this);

  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.unshift"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>unshift (chunk)](#apidoc.element.mongodb.aggregation_cursor.prototype.unshift)
- description and source-code
```javascript
unshift = function (chunk) {
  var state = this._readableState;
  return readableAddChunk(this, state, chunk, '', true);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.unwind"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>unwind (field)](#apidoc.element.mongodb.aggregation_cursor.prototype.unwind)
- description and source-code
```javascript
unwind = function (field) {
  this.s.cmd.pipeline.push({$unwind: field});
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.aggregation_cursor.prototype.wrap"></a>[function <span class="apidocSignatureSpan">mongodb.aggregation_cursor.prototype.</span>wrap (stream)](#apidoc.element.mongodb.aggregation_cursor.prototype.wrap)
- description and source-code
```javascript
wrap = function (stream) {
  var state = this._readableState;
  var paused = false;

  var self = this;
  stream.on('end', function() {
    debug('wrapped end');
    if (state.decoder && !state.ended) {
      var chunk = state.decoder.end();
      if (chunk && chunk.length)
        self.push(chunk);
    }

    self.push(null);
  });

  stream.on('data', function(chunk) {
    debug('wrapped data');
    if (state.decoder)
      chunk = state.decoder.write(chunk);

    // don't skip over falsy values in objectMode
    if (state.objectMode && (chunk === null || chunk === undefined))
      return;
    else if (!state.objectMode && (!chunk || !chunk.length))
      return;

    var ret = self.push(chunk);
    if (!ret) {
      paused = true;
      stream.pause();
    }
  });

  // proxy all the other methods.
  // important when wrapping filters and duplexes.
  for (var i in stream) {
    if (this[i] === undefined && typeof stream[i] === 'function') {
      this[i] = function(method) {
        return function() {
          return stream[method].apply(stream, arguments);
        };
      }(i);
    }
  }

  // proxy certain important events.
  const events = ['error', 'close', 'destroy', 'pause', 'resume'];
  events.forEach(function(ev) {
    stream.on(ev, self.emit.bind(self, ev));
  });

  // when we try to consume some more bytes, simply unpause the
  // underlying stream.
  self._read = function(n) {
    debug('wrapped _read', n);
    if (paused) {
      paused = false;
      stream.resume();
    }
  };

  return self;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.apm"></a>[module mongodb.apm](#apidoc.module.mongodb.apm)

#### <a name="apidoc.element.mongodb.apm.apm"></a>[function <span class="apidocSignatureSpan">mongodb.</span>apm (core, options, callback)](#apidoc.element.mongodb.apm.apm)
- description and source-code
```javascript
apm = function (core, options, callback) {
  options = options || {};

  // Optional id generators
  var operationIdGenerator = options.operationIdGenerator || basicOperationIdGenerator;
  // Optional timestamp generator
  var timestampGenerator = options.timestampGenerator || basicTimestampGenerator;
  // Extend with event emitter functionality
  EventEmitter.call(this);

  // Contains all the instrumentation overloads
  this.overloads = [];

  // ---------------------------------------------------------
  //
  // Instrument prototype
  //
  // ---------------------------------------------------------

  var instrumentPrototype = function(callback) {
    var instrumentations = []

    // Classes to support
    var classes = [GridStore, OrderedBulkOperation, UnorderedBulkOperation,
      CommandCursor, AggregationCursor, Cursor, Collection, Db];

    // Add instrumentations to the available list
    for(var i = 0; i < classes.length; i++) {
      if(classes[i].define) {
        instrumentations.push(classes[i].define.generate());
      }
    }

    // Return the list of instrumentation points
    callback(null, instrumentations);
  }

  // Did the user want to instrument the prototype
  if(typeof callback == 'function') {
    instrumentPrototype(callback);
  }

  // ---------------------------------------------------------
  //
  // Server
  //
  // ---------------------------------------------------------

  // Reference
  var self = this;
  // Names of methods we need to wrap
  var methods = ['command', 'insert', 'update', 'remove'];
  // Prototype
  var proto = core.Server.prototype;
  // Core server method we are going to wrap
  methods.forEach(function(x) {
    var func = proto[x];

    // Add to overloaded methods
    self.overloads.push({proto: proto, name:x, func:func});

    // The actual prototype
    proto[x] = function() {
      var requestId = core.Query.nextRequestId();
      // Get the aruments
      var args = Array.prototype.slice.call(arguments, 0);
      var ns = args[0];
      var commandObj = args[1];
      var options = args[2] || {};
      var keys = Object.keys(commandObj);
      var commandName = keys[0];
      var db = ns.split('.')[0];

      // Get the collection
      var col = ns.split('.');
      col.shift();
      col = col.join('.');

      // Do we have a legacy insert/update/remove command
      if(x == 'insert') { //} && !this.lastIsMaster().maxWireVersion) {
        commandName = 'insert';

        // Re-write the command
        commandObj = {
          insert: col, documents: commandObj
        }

        if(options.writeConcern && Object.keys(options.writeConcern).length > 0)  {
          commandObj.writeConcern = options.writeConcern;
        }

        commandObj.ordered = options.ordered != undefined ? options.ordered : true;
      } else if(x == 'update') { // && !this.lastIsMaster().maxWireVersion) {
        commandName = 'update';

        // Re-write the command
        commandObj = {
          update: col, updates: commandObj
        }

        if(options.writeConcern && Object.keys(options.writeConcern).length > 0) {
          commandObj.writeConcern = options.writeConcern;
        }

        commandObj.ordered = options.ordered != undefined ? options.ordered : true;
      } else if(x == 'remove') { //&& !this.lastIsMaster().maxWireVersion) {
        commandName = 'delete';

        // Re-write the command
        commandObj = {
          delete: col, deletes: commandObj
        }

        if(options.writeConcern && Object.keys(options.writeConcern).length > 0) {
          commandObj.writeConcern = options.writeConcern;
        }

        commandObj.ordered = options.ordered != undefined ? options.ordered : true;
      }

      // Get the callback
      var callback = args.pop();
      // Set current callback operation id from the current context or create
      // a new one
      var ourOpId = callback.operationId || operationIdGenerator.next();

      // Get a connection reference for this server instance
      var connection = this.s.pool.get()

      // Emit the start event ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.apm.super_"></a>[function <span class="apidocSignatureSpan">mongodb.apm.</span>super_ ()](#apidoc.element.mongodb.apm.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.apm.prototype"></a>[module mongodb.apm.prototype](#apidoc.module.mongodb.apm.prototype)

#### <a name="apidoc.element.mongodb.apm.prototype.uninstrument"></a>[function <span class="apidocSignatureSpan">mongodb.apm.prototype.</span>uninstrument ()](#apidoc.element.mongodb.apm.prototype.uninstrument)
- description and source-code
```javascript
uninstrument = function () {
  for(var i = 0; i < this.overloads.length; i++) {
    var obj = this.overloads[i];
    obj.proto[obj.name] = obj.func;
  }

  // Remove all listeners
  this.removeAllListeners('started');
  this.removeAllListeners('succeeded');
  this.removeAllListeners('failed');
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.command_cursor"></a>[module mongodb.command_cursor](#apidoc.module.mongodb.command_cursor)

#### <a name="apidoc.element.mongodb.command_cursor.command_cursor"></a>[function <span class="apidocSignatureSpan">mongodb.</span>command_cursor (bson, ns, cmd, options, topology, topologyOptions)](#apidoc.element.mongodb.command_cursor.command_cursor)
- description and source-code
```javascript
command_cursor = function (bson, ns, cmd, options, topology, topologyOptions) {
  CoreCursor.apply(this, Array.prototype.slice.call(arguments, 0));
  var state = CommandCursor.INIT;
  var streamOptions = {};

  // MaxTimeMS
  var maxTimeMS = null;

  // Get the promiseLibrary
  var promiseLibrary = options.promiseLibrary;

  // No promise library selected fall back
  if(!promiseLibrary) {
    promiseLibrary = typeof global.Promise == 'function' ?
      global.Promise : require('es6-promise').Promise;
  }

  // Set up
  Readable.call(this, {objectMode: true});

  // Internal state
  this.s = {
    // MaxTimeMS
      maxTimeMS: maxTimeMS
    // State
    , state: state
    // Stream options
    , streamOptions: streamOptions
    // BSON
    , bson: bson
    // Namespace
    , ns: ns
    // Command
    , cmd: cmd
    // Options
    , options: options
    // Topology
    , topology: topology
    // Topology Options
    , topologyOptions: topologyOptions
    // Promise library
    , promiseLibrary: promiseLibrary
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.command_cursor.super_"></a>[function <span class="apidocSignatureSpan">mongodb.command_cursor.</span>super_ (options)](#apidoc.element.mongodb.command_cursor.super_)
- description and source-code
```javascript
function Readable(options) {
  if (!(this instanceof Readable))
    return new Readable(options);

  this._readableState = new ReadableState(options, this);

  // legacy
  this.readable = true;

  if (options && typeof options.read === 'function')
    this._read = options.read;

  Stream.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.command_cursor.prototype"></a>[module mongodb.command_cursor.prototype](#apidoc.module.mongodb.command_cursor.prototype)

#### <a name="apidoc.element.mongodb.command_cursor.prototype._find"></a>[function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>_find (callback)](#apidoc.element.mongodb.command_cursor.prototype._find)
- description and source-code
```javascript
_find = function (callback) {
  var self = this;

  if(self.logger.isDebug()) {
    self.logger.debug(f('issue initial query [%s] with flags [%s]'
      , JSON.stringify(self.cmd)
      , JSON.stringify(self.query)));
  }

  var queryCallback = function(err, r) {
    if(err) return callback(err);

    // Get the raw message
    var result = r.message;

    // Query failure bit set
    if(result.queryFailure) {
      return callback(MongoError.create(result.documents[0]), null);
    }

    // Check if we have a command cursor
    if(Array.isArray(result.documents) && result.documents.length == 1
      && (!self.cmd.find || (self.cmd.find && self.cmd.virtual == false))
      && (result.documents[0].cursor != 'string'
        || result.documents[0]['$err']
        || result.documents[0]['errmsg']
        || Array.isArray(result.documents[0].result))
      ) {

      // We have a an error document return the error
      if(result.documents[0]['$err']
        || result.documents[0]['errmsg']) {
        return callback(MongoError.create(result.documents[0]), null);
      }

      // We have a cursor document
      if(result.documents[0].cursor != null
        && typeof result.documents[0].cursor != 'string') {
          var id = result.documents[0].cursor.id;
          // If we have a namespace change set the new namespace for getmores
          if(result.documents[0].cursor.ns) {
            self.ns = result.documents[0].cursor.ns;
          }
          // Promote id to long if needed
          self.cursorState.cursorId = typeof id == 'number' ? Long.fromNumber(id) : id;
          self.cursorState.lastCursorId = self.cursorState.cursorId;
          // If we have a firstBatch set it
          if(Array.isArray(result.documents[0].cursor.firstBatch)) {
            self.cursorState.documents = result.documents[0].cursor.firstBatch;//.reverse();
          }

          // Return after processing command cursor
          return callback(null, null);
      }

      if(Array.isArray(result.documents[0].result)) {
        self.cursorState.documents = result.documents[0].result;
        self.cursorState.cursorId = Long.ZERO;
        return callback(null, null);
      }
    }

    // Otherwise fall back to regular find path
    self.cursorState.cursorId = result.cursorId;
    self.cursorState.documents = result.documents;
    self.cursorState.lastCursorId = result.cursorId;

    // Transform the results with passed in transformation method if provided
    if(self.cursorState.transforms && typeof self.cursorState.transforms.query == 'function') {
      self.cursorState.documents = self.cursorState.transforms.query(result);
    }

    // Return callback
    callback(null, null);
  }

  // Options passed to the pool
  var queryOptions = {};

  // If we have a raw query decorate the function
  if(self.options.raw || self.cmd.raw) {
    // queryCallback.raw = self.options.raw || self.cmd.raw;
    queryOptions.raw = self.options.raw || self.cmd.raw;
  }

  // Do we have documentsReturnedIn set on the query
  if(typeof self.query.documentsReturnedIn == 'string') {
    // queryCallback.documentsReturnedIn = self.query.documentsReturnedIn;
    queryOptions.documentsReturnedIn = self.query.documentsReturnedIn;
  }

  // Add promote Long value if defined
  if(typeof self.cursorState.promoteLongs == 'boolean') {
    queryOptions.promoteLongs = self.cursorState.promoteLongs;
  }

  // Add promote values if defined
  if(typeof self.cursorState.promoteValues == 'boolean') {
    queryOptions.promoteValues = self.cursorState.promoteValues;
  }

  // Add promote values if defined
  if(typeof self.cursorState.promoteBuffers == 'boolean') {
    queryOptions.promoteBuffers = self.cursorState.promoteBuffers;
  }
  // Write the initial command out
  self.server.s.pool.write(self.query, queryOptions, queryCallback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.command_cursor.prototype._getmore"></a>[function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>_getmore (callback)](#apidoc.element.mongodb.command_cursor.prototype._getmore)
- description and source-code
```javascript
_getmore = function (callback) {
  if(this.logger.isDebug()) this.logger.debug(f('schedule getMore call for query [%s]', JSON.stringify(this.query)))
  // Determine if it's a raw query
  var raw = this.options.raw || this.cmd.raw;

  // Set the current batchSize
  var batchSize = this.cursorState.batchSize;
  if(this.cursorState.limit > 0
    && ((this.cursorState.currentLimit + batchSize) > this.cursorState.limit)) {
    batchSize = this.cursorState.limit - this.cursorState.currentLimit;
  }

  // Default pool
  var pool = this.server.s.pool;

  // We have a wire protocol handler
  this.server.wireProtocolHandler.getMore(this.bson, this.ns, this.cursorState, batchSize, raw, pool, this.options, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.command_cursor.prototype._killcursor"></a>[function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>_killcursor (callback)](#apidoc.element.mongodb.command_cursor.prototype._killcursor)
- description and source-code
```javascript
_killcursor = function (callback) {
  // Set cursor to dead
  this.cursorState.dead = true;
  this.cursorState.killed = true;
  // Remove documents
  this.cursorState.documents = [];

  // If no cursor id just return
  if(this.cursorState.cursorId == null || this.cursorState.cursorId.isZero() || this.cursorState.init == false) {
    if(callback) callback(null, null);
    return;
  }

  // Default pool
  var pool = this.server.s.pool;
  // Execute command
  this.server.wireProtocolHandler.killCursor(this.bson, this.ns, this.cursorState.cursorId, pool, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.command_cursor.prototype._next"></a>[function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>_next (callback)](#apidoc.element.mongodb.command_cursor.prototype._next)
- description and source-code
```javascript
_next = function (callback) {
  nextFunction(this, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.command_cursor.prototype.batchSize"></a>[function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>batchSize (value)](#apidoc.element.mongodb.command_cursor.prototype.batchSize)
- description and source-code
```javascript
batchSize = function (value) {
  if(this.s.state == CommandCursor.CLOSED || this.isDead()) throw MongoError.create({message: "Cursor is closed", driver:true});
  if(typeof value != 'number') throw MongoError.create({message: "batchSize requires an integer", driver:true});
  if(this.s.cmd.cursor) this.s.cmd.cursor.batchSize = value;
  this.setCursorBatchSize(value);
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.command_cursor.prototype.bufferedCount"></a>[function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>bufferedCount ()](#apidoc.element.mongodb.command_cursor.prototype.bufferedCount)
- description and source-code
```javascript
bufferedCount = function () {
  return this.cursorState.documents.length - this.cursorState.cursorIndex;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.command_cursor.prototype.close"></a>[function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>close (callback)](#apidoc.element.mongodb.command_cursor.prototype.close)
- description and source-code
```javascript
close = function (callback) {
  this.s.state = Cursor.CLOSED;
  // Kill the cursor
  this.kill();
  // Emit the close event for the cursor
  this.emit('close');
  // Callback if provided
  if(typeof callback == 'function') return handleCallback(callback, null, this);
  // Return a Promise
  return new this.s.promiseLibrary(function(resolve) {
    resolve();
  });
}
```
- example usage
```shell
...
// Connection URL
var url = 'mongodb://localhost:27017/myproject';
// Use connect method to connect to the Server
MongoClient.connect(url, function(err, db) {
  assert.equal(null, err);
  console.log("Connected correctly to server");

  db.close();
});
'''

Given that you booted up the **mongod** process earlier the application should connect successfully and print **Connected correctly
 to server** to the console.

Let's Add some code to show the different CRUD operations available.
...
```

#### <a name="apidoc.element.mongodb.command_cursor.prototype.each"></a>[function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>each (callback)](#apidoc.element.mongodb.command_cursor.prototype.each)
- description and source-code
```javascript
each = function (callback) {
  // Rewind cursor state
  this.rewind();
  // Set current cursor to INIT
  this.s.state = Cursor.INIT;
  // Run the query
  _each(this, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.command_cursor.prototype.explain"></a>[function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>explain (callback)](#apidoc.element.mongodb.command_cursor.prototype.explain)
- description and source-code
```javascript
explain = function (callback) {
  var self = this;
  this.s.cmd.explain = true;

  // Do we have a readConcern
  if(this.s.cmd.readConcern) {
    delete this.s.cmd['readConcern'];
  }

  // Execute using callback
  if(typeof callback == 'function') return this._next(callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    self._next(function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.command_cursor.prototype.forEach"></a>[function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>forEach (iterator, callback)](#apidoc.element.mongodb.command_cursor.prototype.forEach)
- description and source-code
```javascript
forEach = function (iterator, callback) {
  this.each(function(err, doc){
    if(err) { callback(err); return false; }
    if(doc != null) { iterator(doc); return true; }
    if(doc == null && callback) {
      var internalCallback = callback;
      callback = null;
      internalCallback(null);
      return false;
    }
  });
}
```
- example usage
```shell
...
  // Reference
  var self = this;
  // Names of methods we need to wrap
  var methods = ['command', 'insert', 'update', 'remove'];
  // Prototype
  var proto = core.Server.prototype;
  // Core server method we are going to wrap
  methods.forEach(function(x) {
var func = proto[x];

// Add to overloaded methods
self.overloads.push({proto: proto, name:x, func:func});

// The actual prototype
proto[x] = function() {
...
```

#### <a name="apidoc.element.mongodb.command_cursor.prototype.get"></a>[function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>get (callback)](#apidoc.element.mongodb.command_cursor.prototype.get)
- description and source-code
```javascript
get = function (callback) {
  var self = this;
  if(self.s.options.tailable) throw MongoError.create({message: 'Tailable cursor cannot be converted to array', driver:true});

  // Execute using callback
  if(typeof callback == 'function') return toArray(self, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    toArray(self, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
...
// Get the callback
var callback = args.pop();
// Set current callback operation id from the current context or create
// a new one
var ourOpId = callback.operationId || operationIdGenerator.next();

// Get a connection reference for this server instance
var connection = this.s.pool.get()

// Emit the start event for the command
var command = {
  // Returns the command.
  command: commandObj,
  // Returns the database name.
  databaseName: db,
...
```

#### <a name="apidoc.element.mongodb.command_cursor.prototype.isClosed"></a>[function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>isClosed ()](#apidoc.element.mongodb.command_cursor.prototype.isClosed)
- description and source-code
```javascript
isClosed = function () {
  return this.isDead();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.command_cursor.prototype.isDead"></a>[function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>isDead ()](#apidoc.element.mongodb.command_cursor.prototype.isDead)
- description and source-code
```javascript
isDead = function () {
  return this.cursorState.dead == true;
}
```
- example usage
```shell
...
 * Set the batch size for the cursor.
 * @method
 * @param {number} value The batchSize for the cursor.
 * @throws {MongoError}
 * @return {AggregationCursor}
 */
AggregationCursor.prototype.batchSize = function(value) {
  if(this.s.state == AggregationCursor.CLOSED || this.isDead()) throw MongoError.create({message: "Cursor is closed", driver:true
 });
  if(typeof value != 'number') throw MongoError.create({message: "batchSize requires an integer", drvier:true });
  if(this.s.cmd.cursor) this.s.cmd.cursor.batchSize = value;
  this.setCursorBatchSize(value);
  return this;
}

define.classMethod('batchSize', {callback: false, promise:false, returns: [AggregationCursor]});
...
```

#### <a name="apidoc.element.mongodb.command_cursor.prototype.isKilled"></a>[function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>isKilled ()](#apidoc.element.mongodb.command_cursor.prototype.isKilled)
- description and source-code
```javascript
isKilled = function () {
  return this.cursorState.killed == true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.command_cursor.prototype.isNotified"></a>[function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>isNotified ()](#apidoc.element.mongodb.command_cursor.prototype.isNotified)
- description and source-code
```javascript
isNotified = function () {
  return this.cursorState.notified == true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.command_cursor.prototype.kill"></a>[function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>kill (callback)](#apidoc.element.mongodb.command_cursor.prototype.kill)
- description and source-code
```javascript
kill = function (callback) {
  this._killcursor(callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.command_cursor.prototype.maxTimeMS"></a>[function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>maxTimeMS (value)](#apidoc.element.mongodb.command_cursor.prototype.maxTimeMS)
- description and source-code
```javascript
maxTimeMS = function (value) {
  if(this.s.topology.lastIsMaster().minWireVersion > 2) {
    this.s.cmd.maxTimeMS = value;
  }
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.command_cursor.prototype.next"></a>[function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>next (callback)](#apidoc.element.mongodb.command_cursor.prototype.next)
- description and source-code
```javascript
next = function (callback) {
  var self = this;

  // Execute using callback
  if(typeof callback == 'function') {
    // Return the currentDoc if someone called hasNext first
    if(self.s.currentDoc) {
      var doc = self.s.currentDoc;
      self.s.currentDoc = null;
      return callback(null, doc);
    }

    // Return the next object
    return nextObject(self, callback)
  }

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    // Return the currentDoc if someone called hasNext first
    if(self.s.currentDoc) {
      var doc = self.s.currentDoc;
      self.s.currentDoc = null;
      return resolve(doc);
    }

    nextObject(self, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
...
  commandObj.ordered = options.ordered != undefined ? options.ordered : true;
}

// Get the callback
var callback = args.pop();
// Set current callback operation id from the current context or create
// a new one
var ourOpId = callback.operationId || operationIdGenerator.next();

// Get a connection reference for this server instance
var connection = this.s.pool.get()

// Emit the start event for the command
var command = {
  // Returns the command.
...
```

#### <a name="apidoc.element.mongodb.command_cursor.prototype.readBufferedDocuments"></a>[function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>readBufferedDocuments (number)](#apidoc.element.mongodb.command_cursor.prototype.readBufferedDocuments)
- description and source-code
```javascript
readBufferedDocuments = function (number) {
  var unreadDocumentsLength = this.cursorState.documents.length - this.cursorState.cursorIndex;
  var length = number < unreadDocumentsLength ? number : unreadDocumentsLength;
  var elements = this.cursorState.documents.slice(this.cursorState.cursorIndex, this.cursorState.cursorIndex + length);

  // Transform the doc with passed in transformation method if provided
  if(this.cursorState.transforms && typeof this.cursorState.transforms.doc == 'function') {
    // Transform all the elements
    for(var i = 0; i < elements.length; i++) {
      elements[i] = this.cursorState.transforms.doc(elements[i]);
    }
  }

  // Ensure we do not return any more documents than the limit imposed
  // Just return the number of elements up to the limit
  if(this.cursorState.limit > 0 && (this.cursorState.currentLimit + elements.length) > this.cursorState.limit) {
    elements = elements.slice(0, (this.cursorState.limit - this.cursorState.currentLimit));
    this.kill();
  }

  // Adjust current limit
  this.cursorState.currentLimit = this.cursorState.currentLimit + elements.length;
  this.cursorState.cursorIndex = this.cursorState.cursorIndex + elements.length;

  // Return elements
  return elements;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.command_cursor.prototype.rewind"></a>[function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>rewind ()](#apidoc.element.mongodb.command_cursor.prototype.rewind)
- description and source-code
```javascript
rewind = function () {
  if(this.cursorState.init) {
    if(!this.cursorState.dead) {
      this.kill();
    }

    this.cursorState.currentLimit = 0;
    this.cursorState.init = false;
    this.cursorState.dead = false;
    this.cursorState.killed = false;
    this.cursorState.notified = false;
    this.cursorState.documents = [];
    this.cursorState.cursorId = null;
    this.cursorState.cursorIndex = 0;
  }
}
```
- example usage
```shell
...
 * @param {object[]} documents All the documents the satisfy the cursor.
 */

/**
 * Returns an array of documents. The caller is responsible for making sure that there
 * is enough memory to store the results. Note that the array only contain partial
 * results when this cursor had been previouly accessed. In that case,
 * cursor.rewind() can be used to reset the cursor.
 * @method AggregationCursor.prototype.toArray
 * @param {AggregationCursor~toArrayResultCallback} [callback] The result callback.
 * @throws {MongoError}
 * @return {Promise} returns Promise if no callback passed
 */

/**
...
```

#### <a name="apidoc.element.mongodb.command_cursor.prototype.setCursorBatchSize"></a>[function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>setCursorBatchSize (value)](#apidoc.element.mongodb.command_cursor.prototype.setCursorBatchSize)
- description and source-code
```javascript
setCursorBatchSize = function (value) {
  this.cursorState.batchSize = value;
}
```
- example usage
```shell
...
* @throws {MongoError}
* @return {AggregationCursor}
*/
AggregationCursor.prototype.batchSize = function(value) {
 if(this.s.state == AggregationCursor.CLOSED || this.isDead()) throw MongoError.create({message: "Cursor is closed", driver:true
 });
 if(typeof value != 'number') throw MongoError.create({message: "batchSize requires an integer", drvier:true });
 if(this.s.cmd.cursor) this.s.cmd.cursor.batchSize = value;
 this.setCursorBatchSize(value);
 return this;
}

define.classMethod('batchSize', {callback: false, promise:false, returns: [AggregationCursor]});

/**
* Add a geoNear stage to the aggregation pipeline
...
```

#### <a name="apidoc.element.mongodb.command_cursor.prototype.setReadPreference"></a>[function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>setReadPreference (r)](#apidoc.element.mongodb.command_cursor.prototype.setReadPreference)
- description and source-code
```javascript
setReadPreference = function (r) {
  if(this.s.state == CommandCursor.CLOSED || this.isDead()) throw MongoError.create({message: "Cursor is closed", driver:true});
  if(this.s.state != CommandCursor.INIT) throw MongoError.create({message: 'cannot change cursor readPreference after cursor has
 been accessed', driver:true});

  if(r instanceof ReadPreference) {
    this.s.options.readPreference = new CoreReadPreference(r.mode, r.tags, {maxStalenessSeconds: r.maxStalenessSeconds});
  } else if(typeof r == 'string') {
    this.s.options.readPreference = new CoreReadPreference(r);
  } else if(r instanceof CoreReadPreference) {
    this.s.options.readPreference = r;
  }

  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.command_cursor.prototype.toArray"></a>[function <span class="apidocSignatureSpan">mongodb.command_cursor.prototype.</span>toArray (callback)](#apidoc.element.mongodb.command_cursor.prototype.toArray)
- description and source-code
```javascript
toArray = function (callback) {
  var self = this;
  if(self.s.options.tailable) throw MongoError.create({message: 'Tailable cursor cannot be converted to array', driver:true});

  // Execute using callback
  if(typeof callback == 'function') return toArray(self, callback);

  // Return a Promise
  return new this.s.promiseLibrary(function(resolve, reject) {
    toArray(self, function(err, r) {
      if(err) return reject(err);
      resolve(r);
    });
  });
}
```
- example usage
```shell
...
We will finish up the Quickstart CRUD methods by performing a simple query that returns all the documents matching the query.

'''js
var findDocuments = function(db, callback) {
  // Get the documents collection
  var collection = db.collection('documents');
  // Find some documents
  collection.find({}).toArray(function(err, docs) {
    assert.equal(err, null);
    assert.equal(2, docs.length);
    console.log("Found the following records");
    console.dir(docs);
    callback(docs);
  });
}
...
```



# <a name="apidoc.module.mongodb.metadata"></a>[module mongodb.metadata](#apidoc.module.mongodb.metadata)

#### <a name="apidoc.element.mongodb.metadata.metadata"></a>[function <span class="apidocSignatureSpan">mongodb.</span>metadata (name, object, stream)](#apidoc.element.mongodb.metadata.metadata)
- description and source-code
```javascript
metadata = function (name, object, stream) {
  this.name = name;
  this.object = object;
  this.stream = typeof stream == 'boolean' ? stream : false;
  this.instrumentations = {};
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.metadata.prototype"></a>[module mongodb.metadata.prototype](#apidoc.module.mongodb.metadata.prototype)

#### <a name="apidoc.element.mongodb.metadata.prototype.classMethod"></a>[function <span class="apidocSignatureSpan">mongodb.metadata.prototype.</span>classMethod (name, options)](#apidoc.element.mongodb.metadata.prototype.classMethod)
- description and source-code
```javascript
classMethod = function (name, options) {
  var keys = Object.keys(options).sort();
  var key = generateKey(keys, options);

  // Add a list of instrumentations
  if(this.instrumentations[key] == null) {
    this.instrumentations[key] = {
      methods: [], options: options
    }
  }

  // Push to list of method for this instrumentation
  this.instrumentations[key].methods.push(name);
}
```
- example usage
```shell
...
 if(this.s.state == AggregationCursor.CLOSED || this.isDead()) throw MongoError.create({message: "Cursor is closed", driver:true
 });
 if(typeof value != 'number') throw MongoError.create({message: "batchSize requires an integer", drvier:true });
 if(this.s.cmd.cursor) this.s.cmd.cursor.batchSize = value;
 this.setCursorBatchSize(value);
 return this;
}

define.classMethod('batchSize', {callback: false, promise:false, returns: [AggregationCursor]});

/**
* Add a geoNear stage to the aggregation pipeline
* @method
* @param {object} document The geoNear stage document.
* @return {AggregationCursor}
*/
...
```

#### <a name="apidoc.element.mongodb.metadata.prototype.generate"></a>[function <span class="apidocSignatureSpan">mongodb.metadata.prototype.</span>generate ()](#apidoc.element.mongodb.metadata.prototype.generate)
- description and source-code
```javascript
generate = function () {
  // Generate the return object
  var object = {
    name: this.name, obj: this.object, stream: this.stream,
    instrumentations: []
  }

  for(var name in this.instrumentations) {
    object.instrumentations.push(this.instrumentations[name]);
  }

  return object;
}
```
- example usage
```shell
...
  // Classes to support
  var classes = [GridStore, OrderedBulkOperation, UnorderedBulkOperation,
    CommandCursor, AggregationCursor, Cursor, Collection, Db];

  // Add instrumentations to the available list
  for(var i = 0; i < classes.length; i++) {
    if(classes[i].define) {
      instrumentations.push(classes[i].define.generate());
    }
  }

  // Return the list of instrumentation points
  callback(null, instrumentations);
}
...
```

#### <a name="apidoc.element.mongodb.metadata.prototype.staticMethod"></a>[function <span class="apidocSignatureSpan">mongodb.metadata.prototype.</span>staticMethod (name, options)](#apidoc.element.mongodb.metadata.prototype.staticMethod)
- description and source-code
```javascript
staticMethod = function (name, options) {
  options.static = true;
  var keys = Object.keys(options).sort();
  var key = generateKey(keys, options);

  // Add a list of instrumentations
  if(this.instrumentations[key] == null) {
    this.instrumentations[key] = {
      methods: [], options: options
    }
  }

  // Push to list of method for this instrumentation
  this.instrumentations[key].methods.push(name);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.topology_base"></a>[module mongodb.topology_base](#apidoc.module.mongodb.topology_base)

#### <a name="apidoc.element.mongodb.topology_base.ServerCapabilities"></a>[function <span class="apidocSignatureSpan">mongodb.topology_base.</span>ServerCapabilities (ismaster)](#apidoc.element.mongodb.topology_base.ServerCapabilities)
- description and source-code
```javascript
ServerCapabilities = function (ismaster) {
  var setup_get_property = function(object, name, value) {
    Object.defineProperty(object, name, {
        enumerable: true
      , get: function () { return value; }
    });
  }

  // Capabilities
  var aggregationCursor = false;
  var writeCommands = false;
  var textSearch = false;
  var authCommands = false;
  var listCollections = false;
  var listIndexes = false;
  var maxNumberOfDocsInBatch = ismaster.maxWriteBatchSize || 1000;
  var commandsTakeWriteConcern = false;
  var commandsTakeCollation = false;

  if(ismaster.minWireVersion >= 0) {
    textSearch = true;
  }

  if(ismaster.maxWireVersion >= 1) {
    aggregationCursor = true;
    authCommands = true;
  }

  if(ismaster.maxWireVersion >= 2) {
    writeCommands = true;
  }

  if(ismaster.maxWireVersion >= 3) {
    listCollections = true;
    listIndexes = true;
  }

  if(ismaster.maxWireVersion >= 5) {
    commandsTakeWriteConcern = true;
    commandsTakeCollation = true;
  }

  // If no min or max wire version set to 0
  if(ismaster.minWireVersion == null) {
    ismaster.minWireVersion = 0;
  }

  if(ismaster.maxWireVersion == null) {
    ismaster.maxWireVersion = 0;
  }

  // Map up read only parameters
  setup_get_property(this, "hasAggregationCursor", aggregationCursor);
  setup_get_property(this, "hasWriteCommands", writeCommands);
  setup_get_property(this, "hasTextSearch", textSearch);
  setup_get_property(this, "hasAuthCommands", authCommands);
  setup_get_property(this, "hasListCollectionsCommand", listCollections);
  setup_get_property(this, "hasListIndexesCommand", listIndexes);
  setup_get_property(this, "minWireVersion", ismaster.minWireVersion);
  setup_get_property(this, "maxWireVersion", ismaster.maxWireVersion);
  setup_get_property(this, "maxNumberOfDocsInBatch", maxNumberOfDocsInBatch);
  setup_get_property(this, "commandsTakeWriteConcern", commandsTakeWriteConcern);
  setup_get_property(this, "commandsTakeCollation", commandsTakeCollation);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.topology_base.Store"></a>[function <span class="apidocSignatureSpan">mongodb.topology_base.</span>Store (topology, storeOptions)](#apidoc.element.mongodb.topology_base.Store)
- description and source-code
```javascript
Store = function (topology, storeOptions) {
  var self = this;
  var storedOps = [];
  storeOptions = storeOptions || {force:false, bufferMaxEntries: -1}

  // Internal state
  this.s = {
      storedOps: storedOps
    , storeOptions: storeOptions
    , topology: topology
  }

  Object.defineProperty(this, 'length', {
    enumerable:true, get: function() { return self.s.storedOps.length; }
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mongodb.utils"></a>[module mongodb.utils](#apidoc.module.mongodb.utils)

#### <a name="apidoc.element.mongodb.utils.assign"></a>[function <span class="apidocSignatureSpan">mongodb.utils.</span>assign ()](#apidoc.element.mongodb.utils.assign)
- description and source-code
```javascript
function assign() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.utils.checkCollectionName"></a>[function <span class="apidocSignatureSpan">mongodb.utils.</span>checkCollectionName (collectionName)](#apidoc.element.mongodb.utils.checkCollectionName)
- description and source-code
```javascript
function checkCollectionName(collectionName) {
  if('string' !== typeof collectionName) {
    throw Error("collection name must be a String");
  }

  if(!collectionName || collectionName.indexOf('..') != -1) {
    throw Error("collection names cannot be empty");
  }

  if(collectionName.indexOf('$') != -1 &&
      collectionName.match(/((^\$cmd)|(oplog\.\$main))/) == null) {
    throw Error("collection names must not contain '$'");
  }

  if(collectionName.match(/^\.|\.$/) != null) {
    throw Error("collection names must not start or end with '.'");
  }

  // Validate that we are not passing 0x00 in the colletion name
  if(!!~collectionName.indexOf("\x00")) {
    throw new Error("collection names cannot contain a null character");
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.utils.debugOptions"></a>[function <span class="apidocSignatureSpan">mongodb.utils.</span>debugOptions (debugFields, options)](#apidoc.element.mongodb.utils.debugOptions)
- description and source-code
```javascript
debugOptions = function (debugFields, options) {
  var finaloptions = {};
  debugFields.forEach(function(n) {
    finaloptions[n] = options[n];
  });

  return finaloptions;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.utils.decorateCommand"></a>[function <span class="apidocSignatureSpan">mongodb.utils.</span>decorateCommand (command, options, exclude)](#apidoc.element.mongodb.utils.decorateCommand)
- description and source-code
```javascript
decorateCommand = function (command, options, exclude) {
  for(var name in options) {
    if(exclude[name] == null) command[name] = options[name];
  }

  return command;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.utils.filterOptions"></a>[function <span class="apidocSignatureSpan">mongodb.utils.</span>filterOptions (options, names)](#apidoc.element.mongodb.utils.filterOptions)
- description and source-code
```javascript
filterOptions = function (options, names) {
  var filterOptions =  {};

  for(var name in options) {
    if(names.indexOf(name) != -1) filterOptions[name] = options[name];
  }

  // Filtered options
  return filterOptions;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.utils.formatSortValue"></a>[function <span class="apidocSignatureSpan">mongodb.utils.</span>formatSortValue (sortDirection)](#apidoc.element.mongodb.utils.formatSortValue)
- description and source-code
```javascript
formatSortValue = function (sortDirection) {
  var value = ("" + sortDirection).toLowerCase();

  switch (value) {
    case 'ascending':
    case 'asc':
    case '1':
      return 1;
    case 'descending':
    case 'desc':
    case '-1':
      return -1;
    default:
      throw new Error("Illegal sort clause, must be of the form "
                    + "[['field1', '(ascending|descending)'], "
                    + "['field2', '(ascending|descending)']]");
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.utils.formattedOrderClause"></a>[function <span class="apidocSignatureSpan">mongodb.utils.</span>formattedOrderClause (sortValue)](#apidoc.element.mongodb.utils.formattedOrderClause)
- description and source-code
```javascript
formattedOrderClause = function (sortValue) {
  var orderBy = {};
  if(sortValue == null) return null;
  if (Array.isArray(sortValue)) {
    if(sortValue.length === 0) {
      return null;
    }

    for(var i = 0; i < sortValue.length; i++) {
      if(sortValue[i].constructor == String) {
        orderBy[sortValue[i]] = 1;
      } else {
        orderBy[sortValue[i][0]] = formatSortValue(sortValue[i][1]);
      }
    }
  } else if(sortValue != null && typeof sortValue == 'object') {
    orderBy = sortValue;
  } else if (typeof sortValue == 'string') {
    orderBy[sortValue] = 1;
  } else {
    throw new Error("Illegal sort clause, must be of the form " +
      "[['field1', '(ascending|descending)'], ['field2', '(ascending|descending)']]");
  }

  return orderBy;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.utils.getReadPreference"></a>[function <span class="apidocSignatureSpan">mongodb.utils.</span>getReadPreference (options)](#apidoc.element.mongodb.utils.getReadPreference)
- description and source-code
```javascript
getReadPreference = function (options) {
  var r = null
  if(options.readPreference) {
    r = options.readPreference
  } else {
    return options;
  }

  if(r instanceof ReadPreference) {
    options.readPreference = new CoreReadPreference(r.mode, r.tags, {maxStalenessSeconds: r.maxStalenessSeconds});
  } else if(typeof r == 'string') {
    options.readPreference = new CoreReadPreference(r);
  } else if(r && !(r instanceof ReadPreference) && typeof r == 'object') {
    var mode = r.mode || r.preference;
    if (mode && typeof mode == 'string') {
      options.readPreference = new CoreReadPreference(mode, r.tags, {maxStalenessSeconds: r.maxStalenessSeconds});
    }
  }

  return options;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.utils.getSingleProperty"></a>[function <span class="apidocSignatureSpan">mongodb.utils.</span>getSingleProperty (obj, name, value)](#apidoc.element.mongodb.utils.getSingleProperty)
- description and source-code
```javascript
getSingleProperty = function (obj, name, value) {
  Object.defineProperty(obj, name, {
    enumerable:true,
    get: function() {
      return value
    }
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.utils.handleCallback"></a>[function <span class="apidocSignatureSpan">mongodb.utils.</span>handleCallback (callback, err, value1, value2)](#apidoc.element.mongodb.utils.handleCallback)
- description and source-code
```javascript
handleCallback = function (callback, err, value1, value2) {
  try {
    if(callback == null) return;
    if(callback) {
      return value2 ? callback(err, value1, value2) :  callback(err, value1);
    }
  } catch(err) {
    process.nextTick(function() { throw err; });
    return false;
  }

  return true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.utils.isObject"></a>[function <span class="apidocSignatureSpan">mongodb.utils.</span>isObject (arg)](#apidoc.element.mongodb.utils.isObject)
- description and source-code
```javascript
isObject = function (arg) {
  return '[object Object]' == Object.prototype.toString.call(arg)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.utils.mergeOptions"></a>[function <span class="apidocSignatureSpan">mongodb.utils.</span>mergeOptions (target, source)](#apidoc.element.mongodb.utils.mergeOptions)
- description and source-code
```javascript
mergeOptions = function (target, source) {
  for(var name in source) {
    target[name] = source[name];
  }

  return target;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.utils.normalizeHintField"></a>[function <span class="apidocSignatureSpan">mongodb.utils.</span>normalizeHintField (hint)](#apidoc.element.mongodb.utils.normalizeHintField)
- description and source-code
```javascript
function normalizeHintField(hint) {
  var finalHint = null;

  if(typeof hint == 'string') {
    finalHint = hint;
  } else if(Array.isArray(hint)) {
    finalHint = {};

    hint.forEach(function(param) {
      finalHint[param] = 1;
    });
  } else if(hint != null && typeof hint == 'object') {
    finalHint = {};
    for (var name in hint) {
      finalHint[name] = hint[name];
    }
  }

  return finalHint;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.utils.parseIndexOptions"></a>[function <span class="apidocSignatureSpan">mongodb.utils.</span>parseIndexOptions (fieldOrSpec)](#apidoc.element.mongodb.utils.parseIndexOptions)
- description and source-code
```javascript
parseIndexOptions = function (fieldOrSpec) {
  var fieldHash = {};
  var indexes = [];
  var keys;

  // Get all the fields accordingly
  if('string' == typeof fieldOrSpec) {
    // 'type'
    indexes.push(fieldOrSpec + '_' + 1);
    fieldHash[fieldOrSpec] = 1;
  } else if(Array.isArray(fieldOrSpec)) {
    fieldOrSpec.forEach(function(f) {
      if('string' == typeof f) {
        // [{location:'2d'}, 'type']
        indexes.push(f + '_' + 1);
        fieldHash[f] = 1;
      } else if(Array.isArray(f)) {
        // [['location', '2d'],['type', 1]]
        indexes.push(f[0] + '_' + (f[1] || 1));
        fieldHash[f[0]] = f[1] || 1;
      } else if(isObject(f)) {
        // [{location:'2d'}, {type:1}]
        keys = Object.keys(f);
        keys.forEach(function(k) {
          indexes.push(k + '_' + f[k]);
          fieldHash[k] = f[k];
        });
      } else {
        // undefined (ignore)
      }
    });
  } else if(isObject(fieldOrSpec)) {
    // {location:'2d', type:1}
    keys = Object.keys(fieldOrSpec);
    keys.forEach(function(key) {
      indexes.push(key + '_' + fieldOrSpec[key]);
      fieldHash[key] = fieldOrSpec[key];
    });
  }

  return {
    name: indexes.join("_"), keys: keys, fieldHash: fieldHash
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.utils.shallowClone"></a>[function <span class="apidocSignatureSpan">mongodb.utils.</span>shallowClone (obj)](#apidoc.element.mongodb.utils.shallowClone)
- description and source-code
```javascript
shallowClone = function (obj) {
  var copy = {};
  for(var name in obj) copy[name] = obj[name];
  return copy;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.utils.toError"></a>[function <span class="apidocSignatureSpan">mongodb.utils.</span>toError (error)](#apidoc.element.mongodb.utils.toError)
- description and source-code
```javascript
toError = function (error) {
  if (error instanceof Error) return error;

  var msg = error.err || error.errmsg || error.errMessage || error;
  var e = MongoError.create({message: msg, driver:true});

  // Get all object keys
  var keys = typeof error == 'object'
    ? Object.keys(error)
    : [];

  for(var i = 0; i < keys.length; i++) {
    try {
      e[keys[i]] = error[keys[i]];
    } catch(err) {
      // continue
    }
  }

  return e;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mongodb.utils.translateOptions"></a>[function <span class="apidocSignatureSpan">mongodb.utils.</span>translateOptions (target, source)](#apidoc.element.mongodb.utils.translateOptions)
- description and source-code
```javascript
translateOptions = function (target, source) {
  var translations = {
    // SSL translation options
    'sslCA': 'ca', 'sslCRL': 'crl', 'sslValidate': 'rejectUnauthorized', 'sslKey': 'key',
    'sslCert': 'cert', 'sslPass': 'passphrase',
    // SocketTimeout translation options
    'socketTimeoutMS': 'socketTimeout', 'connectTimeoutMS': 'connectionTimeout',
    // Replicaset options
    'replicaSet': 'setName', 'rs_name': 'setName', 'secondaryAcceptableLatencyMS': 'acceptableLatency',
    'connectWithNoPrimary': 'secondaryOnlyConnectionAllowed',
    // Mongos options
    'acceptableLatencyMS': 'localThresholdMS'
  }

  for(var name in source) {
    if(translations[name]) {
      target[translations[name]] = source[name];
    } else {
      target[name] = source[name];
    }
  }

  return target;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
