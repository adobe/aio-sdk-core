<!-- 
Copyright 2019 Adobe. All rights reserved.
This file is licensed to you under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License. You may obtain a copy
of the License at http://www.apache.org/licenses/LICENSE-2.0
Unless required by applicable law or agreed to in writing, software distributed under
the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR REPRESENTATIONS
OF ANY KIND, either express or implied. See the License for the specific language
governing permissions and limitations under the License.
-->
@adobe/aio-sdk-core
====================

[![Version](https://img.shields.io/npm/v/@adobe/aio-sdk-core.svg)](https://npmjs.org/package/@adobe/aio-sdk-core)
[![Downloads/week](https://img.shields.io/npm/dw/@adobe/aio-sdk-core.svg)](https://npmjs.org/package/@adobe/aio-sdk-core)
[![Build Status](https://travis-ci.com/adobe/aio-sdk-core.svg?branch=master)](https://travis-ci.com/adobe/aio-sdk-core)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0) [![Greenkeeper badge](https://badges.greenkeeper.io/adobe/aio-sdk-core.svg)](https://greenkeeper.io/)
[![Codecov Coverage](https://img.shields.io/codecov/c/github/adobe/aio-sdk-core/master.svg?style=flat-square)](https://codecov.io/gh/adobe/aio-sdk-core/)

This is the Adobe I/O Core SDK. This contains:
- [Core Config Library](https://github.com/adobe/aio-lib-core-config)
- [Core Errors Library](https://github.com/adobe/aio-lib-core-errors)
- [Core Logger Library](https://github.com/adobe/aio-lib-core-logging)
- [Core TVM Library](https://github.com/adobe/aio-lib-core-tvm)

[SDK Health](./health.md)

The module can be added to your project with:

```javascript
npm install @adobe/aio-sdk-core --save
```

Here is a snippet:

```javascript
const CoreSdk = require('@adobe/aio-sdk-core')
// OR ...
const { Config, Errors, TVMClient, Logger } = require('@adobe/aio-sdk-core')

// set a Config key value
CoreSdk.Config.set('my.token', 1234)

// get all stored config values
CoreSdk.Config.get()

// create your own Error wrapper here, see @adobe/aio-lib-core-error docs
const { AioCoreSDKError, AioCoreSDKErrorWrapper } = CoreSdk.Errors

// init the TVM client for further use
const tvm = await CoreSdk.TvmClient.init({ ow: { auth: '<myauth>', namespace: '<mynamespace>' } })

// create a Logger
const myAppLogger = CoreSdk.Logger('MyApp')
myAppLogger.info('Hello, Dave.')
```

## Explore

`goto` [API](./doc/api.md)

## Contributing

Contributions are welcomed! Read the [Contributing Guide](./.github/CONTRIBUTING.md) for more information.

## Licensing

This project is licensed under the Apache V2 License. See [LICENSE](LICENSE) for more information.