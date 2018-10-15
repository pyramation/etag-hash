# ETag Hash

Es6 class that generates ETag using the same algorithm as S3 via MD5 sum.

## Installation

```sh
npm install etag-hash
```

## Usage

```js
const createHash = require('etag-hash').createHash;
const etag = createHash().update(contents).digest();
```

ETags compatible with s3, API similar to the crypto module to be compatible with streams. Thanks to the author of [this post](https://stackoverflow.com/questions/12186993/what-is-the-algorithm-to-compute-the-amazon-s3-etag-for-a-file-larger-than-5gb#answer-19896823) for the breakdown of the algorithm.