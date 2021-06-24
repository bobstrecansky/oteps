# API and SDK separation not necessary for all languages

API and SDK separation may not be strictly mandatory and may be cumbersome to implement for specific languages.

## Motivation

There are languages that have difficulty separating API and SDK packages for consumption.  PHP usually includes the 
API and SDK for a package in the same metapackage, so it's simpler for the most prominent PHP dependency management 
tool, 
[Composer](https://getcomposer.org/), to download and use.  Separating APIs and SDKs is not as prominent in PHP as 
it is in other languages like Go/Java/Python et. al.

## Explanation
PHP doesn't really have an intrinsic need to separate the API and the SDK. This would most likely be a very strange use
case in PHP.

The current wording of the [specification](https://github.com/open-telemetry/opentelemetry-specification/blob/main/specification/library-guidelines.md#expected-usage) states that

`The API and the SDK are split into multiple packages, based on signal type` 

I'm not certain that should be a hard requirement, as this sort of implementation step can be difficult for specific 
languages.

## Internal details

## Trade-offs and mitigations

The most obvious known tradeoff is not following the same explicit pattern as the rest of the language SIGs for 
API/SDK separation.  Not being able to replace the SDK in the future is also another known limitation.  This 
practice is not very commonplace in PHP, so I think this would be very unlikely to happen.

## Prior art and alternatives

There is no prior art or alternative solutions for this particular problem that come to mind; very happy to hear 
others' opinions here.

## Open questions

No current open questions on the OTEP if we are able to change the language of the specification slightly.

## Future possibilities

No future possibilities need to be listed.