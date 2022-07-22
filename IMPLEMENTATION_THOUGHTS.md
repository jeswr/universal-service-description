## This file is for my thoughts around implementation path.

1. One good initial test of this USD would be to see if we can add metadata to various Comunica configs so that each engine configuration setup as a SPARQL endpoint can advertise the services available on that particular endpoint.

## How to expose a service instance

There are a few options around exposing a service instance that need to be discussed, the options are:
1. Use one or more "rel" links in order to link to a USD
2. Expose some RDF through various rel links *within* the OPTIONS header (avoids traversing multiple documents => improve performance). I believe this should be optional, and always *in addition to* the publisihing of a single dereferencable document to limit the amount of things that need to be implemented by the client, and instead this is an optional implementation to improve performance.

TODO: Read up on the Web Linking RFC in relation to this point https://datatracker.ietf.org/doc/html/rfc5988
Service description is even mentioned within this document (https://datatracker.ietf.org/doc/html/rfc5988#section-4)
[x] Didn't seem useful at all after reading - TODO: Read up on the Atom Publishing Protocol https://datatracker.ietf.org/doc/html/rfc5023 which seems fairly similar to what is trying to be achieved here.

In order to effectively, and securely achieve phase (which is declaratively describing endpoint customisations so that a client can adjust) we should probably look to the function ontologies that were being researched in the last couple of ISWCs


