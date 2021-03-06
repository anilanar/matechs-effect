# Introduction

[![codecov.io](http://codecov.io/github/mikearnaldi/matechs-effect/coverage.svg?branch=master)](http://codecov.io/github/mikearnaldi/matechs-effect) [![Greenkeeper badge](https://badges.greenkeeper.io/mikearnaldi/matechs-effect.svg)](https://greenkeeper.io/)

Matechs Effect is a Fully-fledged functional effect system for typescript with a rich standard library including modules for http server & client, logger, orm, cqrs+es, zookeeper leader election, next.js, apollo, rxjs, redux-observables and more.

Docs at [https://arnaldimichael.gitbook.io/matechs-effect/](https://arnaldimichael.gitbook.io/matechs-effect/)

## Note on Docs
Docs are meant to be only for introduction to the architecture but are still outdated, for proper usage refer to the test & demo packages in each package

## Details

For details about the additional types and overloads please refer to documentation in `packages/effect`

## Notes

This package is a work in progress syntax and functions might change, feedback are welcome and contributions even more!

## Videos
26-03-2020 Introduction call, basic explaination of the effect library and showcase of examples:
[https://vimeo.com/401143293](https://vimeo.com/401143293)

## License
The library is released with an MIT license and the codebase is fully open-source please read: 
[LICENSE.md](https://github.com/mikearnaldi/matechs-effect/blob/master/LICENSE.md)

As with any good library there is a commercial project that support the development and maintainance, if you want to know more find us at [https://www.matechs.com/](https://www.matechs.com/) we are a digital accelerator looking for smart founders!

## Stability Grid
|      Package                  | API Stage  | Used in Prod |                            Description                            |                                 Weekly NPM                                 |
|-------------------------------|------------|--------------|-------------------------------------------------------------------|----------------------------------------------------------------------------|
| @matechs/effect               |   stable   |      yes     | Core package provides all the primitives for effect management.   |![weekly-downloads](https://badgen.net/npm/dw/@matechs/effect)              |
| @matechs/http-client          |   stable   |      yes     | Http client specification and shared utilities for http requests. |![weekly-downloads](https://badgen.net/npm/dw/@matechs/http-client)         |
| @matechs/http-client-fetch    |   stable   |      yes     | Http client implementation using a generic fetch instance.        |![weekly-downloads](https://badgen.net/npm/dw/@matechs/http-client-fetch)   |
| @matechs/http-client-libcurl  |   stable   |      yes     | Http client implementation using libcurl, supports http2 on node. |![weekly-downloads](https://badgen.net/npm/dw/@matechs/http-client-libcurl) |
| @matechs/browser              |   stable   |      yes     | Deals with reading and writing to browser local & sesstion store. |![weekly-downloads](https://badgen.net/npm/dw/@matechs/browser)             |
| @matechs/console              |   stable   |      yes     | Effectified version of node & browser console.                    |![weekly-downloads](https://badgen.net/npm/dw/@matechs/console)             |
| @matechs/rxjs                 |   stable   |      yes     | Integrates RxJS with streams, effect and rx pipe operators.       |![weekly-downloads](https://badgen.net/npm/dw/@matechs/rxjs)                |
| @matechs/epics                |   beta     |      no      | Integrate redux-observable epics in terms of effectful streams.   |![weekly-downloads](https://badgen.net/npm/dw/@matechs/epics)               |
| @matechs/rpc                  |   beta     |      yes     | Wire serializable free modules to express for remote consumption. |![weekly-downloads](https://badgen.net/npm/dw/@matechs/rpc)                 |
| @matechs/rpc-client           |   beta     |      yes     | Implement server RPC defined free modules in terms of http client.|![weekly-downloads](https://badgen.net/npm/dw/@matechs/rpc-client)          |
| @matechs/orm                  |   stable   |      yes     | Integrates with TypeORM allowing multi database manage smoothly.  |![weekly-downloads](https://badgen.net/npm/dw/@matechs/orm)                 |
| @matechs/cqrs                 |   beta     |      no      | Embeds feature complete CQRS+ES utility to ORM for PostgreSQL.    |![weekly-downloads](https://badgen.net/npm/dw/@matechs/cqrs)                |
| @matechs/cqrs-es              |   beta     |      no      | Integrates cqrs aggregates with EventStore.                       |![weekly-downloads](https://badgen.net/npm/dw/@matechs/cqrs-es)             |
| @matechs/express              |   beta     |      yes     | Integrates with express and provide utilities to define routes.   |![weekly-downloads](https://badgen.net/npm/dw/@matechs/express)             |
| @matechs/tracing              |   beta     |      yes     | Integrates with opentracing-js featuring auto tracing of free mod.|![weekly-downloads](https://badgen.net/npm/dw/@matechs/tracing)             |
| @matechs/graceful             |   beta     |      yes     | Utility to register callbacks to improve graceful exit scenarios. |![weekly-downloads](https://badgen.net/npm/dw/@matechs/graceful)            |
| @matechs/logger               |   stable   |      yes     | Define a generic logger interface and provide a console interpret.|![weekly-downloads](https://badgen.net/npm/dw/@matechs/logger)              |
| @matechs/logger-winston       |   stable   |      yes     | Integrates logger with a winston based interpreter.               |![weekly-downloads](https://badgen.net/npm/dw/@matechs/logger-winston)      |
| @matechs/uuid                 |   beta     |      yes     | Generates v4 uuids with different encodings, classic & short.     |![weekly-downloads](https://badgen.net/npm/dw/@matechs/uuid)                |
| @matechs/zoo                  |   beta     |      yes     | Integrates zookeeper for leader elections.                        |![weekly-downloads](https://badgen.net/npm/dw/@matechs/zoo)                 |
| @matechs/fancy                |   beta     |      no      | Full blown integration with Next.js / React & Mobx.               |![weekly-downloads](https://badgen.net/npm/dw/@matechs/fancy)               |
| @matechs/apollo               |   beta     |      no      | Integrates with apollo-server with full env support in resolvers  |![weekly-downloads](https://badgen.net/npm/dw/@matechs/apollo)              |
| @matechs/test                 |   beta     |      no      | Port of ZIO Test, integrates fast-check & customizable runner.    |![weekly-downloads](https://badgen.net/npm/dw/@matechs/test)                |
| @matechs/test-jest            |   beta     |      no      | Integrates jest as runner for `@matechs/test`.                    |![weekly-downloads](https://badgen.net/npm/dw/@matechs/test-jest)           |

## Performance
Currently we run only minor benchmarks in ci where we test against `@qio` and `waveguide` as they represent a similar feature-set, the benchmarks may be affected by environmental conditions and they are not necessarily a representation of the production performance where we can expect all those libraries to perform similarly.

Running on ci:
```
$ /home/runner/work/matechs-effect/matechs-effect/node_modules/.bin/ts-node bench/index.ts
effect x 25,179 ops/sec ±1.52% (82 runs sampled)
effect-fluent x 15,655 ops/sec ±1.43% (80 runs sampled)
qio x 23,223 ops/sec ±2.31% (80 runs sampled)
wave x 12,233 ops/sec ±6.35% (77 runs sampled)
lerna success - @matechs/effect
promise x 4,236 ops/sec ±1.91% (77 runs sampled)
native x 26,099 ops/sec ±5.12% (79 runs sampled)
Fastest is native

$ /home/runner/work/matechs-effect/matechs-effect/node_modules/.bin/ts-node bench/nestedMap.ts
effect x 12,189 ops/sec ±1.49% (80 runs sampled)
effect-fluent x 5,373 ops/sec ±1.87% (79 runs sampled)
wave x 2,771 ops/sec ±1.80% (77 runs sampled)
qio x 10,443 ops/sec ±2.33% (77 runs sampled)
Fastest is effect

$ /home/runner/work/matechs-effect/matechs-effect/node_modules/.bin/ts-node bench/nestedChain.ts
effect x 1,171 ops/sec ±1.87% (77 runs sampled)
effect-fluent x 715 ops/sec ±8.69% (74 runs sampled)
wave x 352 ops/sec ±9.17% (76 runs sampled)
qio x 1,186 ops/sec ±1.47% (79 runs sampled)
Fastest is qio,effect
```

## Thanks

This library would have not been feasibly possible without the strong foundations of [fp-ts](https://github.com/gcanti/fp-ts) and [Waveguide](https://github.com/rzeigler/waveguide) from which we have forked the base bifunctor and execution runtime, huge thanks to the Authors.

This library was initially based on Fluture, huge thanks to the Authors.

Another huge thanks goes to both the scala community (ZIO in specific) and the haskell community (RIO & Polysemy) from which inspiration is taken.

All of the above projects are advised!

## Get in touch
The best place to reach out would be either in https://fpchat-invite.herokuapp.com (FP Chat, @Michael Arnaldi) or for italians https://italiajs.herokuapp.com/ (Italia JS, @Michael Arnaldi or channel #fp)
