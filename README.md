# zk-web

zk-web is a Web UI of [Zookeeper](http://zookeeper.apache.org), just making it easier to use. Sometimes I really get tired of the command line.
zk-web is written in [clojure](http://clojure.org) with [noir](http://webnoir.org) and [boostrap](http://twitter.github.com/bootstrap/). Currently there're just less than 450 lines clojure code at all. Clojure is really so simple and so elegent!

## Usage

To use zk-web, you need [leiningen](https://github.com/technomancy/leiningen) and git currentlly. (And I'll make a stand-alone package later).
Run the following command:

```bash
git clone git://github.com/qiuxiafei/zk-web.git
cd zk-web
lein deps # run this if you're using lein 1.x
lein run
```
Meet with zk-web at [http://localhost:8080](http://localhost:8080)! I'am sure it's super easy!

## Configuration

zk-web is also easy to configurate too. It reads $HOME/.zk-web-conf.clj when it starts up. As you already seen, the configuration file is also clojure code. Let's see a example:

```clojure
{
 :server-port 8989
 :users {
         "admin" "hello"
         ;; more users here
         }
 }
```

## Features
* Jump to ancesters of a node in navigation bar.
* List children of a node with link to them.
* Show stat and data of a node.
* Remember last 3 zookeepers you visit in cookie.
* Create/edit/delete/rmr a node.
* Simple authority management.

## TODO
* Data Format - Format json, xml and so on.

## License

Copyright (C) 2012

Distributed under the Eclipse Public License, the same as Clojure.
