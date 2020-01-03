# httpfactory
PSR-17 plus methods for clients and emitters.

This makes use of guzzlehttp/psr7, laminas-laminashttphandlerunner, and socialconnect/http-client to provide a simple factory that should handle most HTTP needs. Additionally it contains static methods for retrieving the names of the classes used in each implementation.

---
### Usage

```
<?php

use Prim\HttpFactory\HttpFactory;

// PSR-17 creating objects implementing PSR-7
$response = (new HttpFactory)->createResponse();
$responseClass = HttpFactory::responseClass();

// PSR-18 HTTP client factory.
$client = (new HttpFactory)->createClient();
$clientClass = HttpFactory::clientClass();

// SAPI emitter factory.
$emitter = (new HttpFactory)->createEmitter();
$emitterClass = HttpFactory::emitterClass();

// PSR-7 server request from globals.
$request = (new HttpFactory)->createServerRequestFromGlobals();
```
