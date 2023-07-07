# prefix-tagging
prototype of crowdsourcing the tagging of prefixes.

Sometimes prefixes have a special function, sometimes these can be inferred (anycast, ixp use), but other times it is useful to identify a specific function for a prefix, but it's not inferrable. Example: prefixes that have rpki invalid key material on purpose, so to make it possible to test rpki/rov deployment.

This repo is an attempt to tag these prefixes

There is a single pipe-separated-values (PSV) file. Fields are:
* tag
* prefix
* contributor (github id)

Please describe new tags here:

## tag: rpki-invalid-on-purpose

This tag identifies prefixes that on purpose have rpki invalid key material. These prefixes can be used to monitor rpki/rov deployment, because a router deploying route origin validation filtering will not propagate a route with associated rpki invalid key material.
