# Exponential Backoff [![GoDoc][godoc image]][godoc] [![Coverage Status][coveralls image]][coveralls]

This is a Go port of the exponential backoff algorithm from [Google's HTTP Client Library for Java][google-http-java-client].

[Exponential backoff][exponential backoff wiki]
is an algorithm that uses feedback to multiplicatively decrease the rate of some process,
in order to gradually find an acceptable rate.
The retries exponentially increase and stop increasing when a certain threshold is met.

## Usage

Import path is `github.com/cenkalti/backoff/v5`. Please note the version part at the end.

For most cases, use [`Retry`][retry-doc] function. See [example_test.go][example] for an example.

If you have specific needs, copy the [`Retry`][retry-src] function into your code and modify it as needed.

## Contributing

* I would like to keep this library as small as possible.
* Please don't send a PR without opening an issue and discussing it first.
* If proposed change is not a common use case, I will probably not accept it.

[godoc]: https://pkg.go.dev/github.com/cenkalti/backoff/v5
[godoc image]: https://godoc.org/github.com/cenkalti/backoff?status.png
[coveralls]: https://coveralls.io/github/cenkalti/backoff?branch=master
[coveralls image]: https://coveralls.io/repos/github/cenkalti/backoff/badge.svg?branch=master

[google-http-java-client]: https://github.com/google/google-http-java-client/blob/da1aa993e90285ec18579f1553339b00e19b3ab5/google-http-client/src/main/java/com/google/api/client/util/ExponentialBackOff.java
[exponential backoff wiki]: http://en.wikipedia.org/wiki/Exponential_backoff

[retry-doc]: https://pkg.go.dev/github.com/cenkalti/backoff/v5#Retry
[retry-src]: https://github.com/cenkalti/backoff/blob/v5/retry.go
[example]: https://github.com/cenkalti/backoff/blob/v5/example_test.go
