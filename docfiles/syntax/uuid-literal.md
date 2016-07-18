---
name: syntax/uuid-literal
display as: "#uuid literal"
see also:
  - cljs.core/uuid
  - cljs.core/random-uuid
---

## Summary

## Details

Creates a universally unique identifier (UUID), using the [doc:cljs.core/UUID] type.

The format is `#uuid "8-4-4-4-12"`, where the numbers represent the number of hex digits.

Representing UUIDs with `#uuid` rather than just a plain string has the following benefits:

- the reader will throw an exception on malformed UUIDs
- its UUID type is preserved and shown when serialized to [edn].

To create a UUID from an evaluated expression, use [doc:cljs.core/uuid].

[edn]:https://github.com/edn-format/edn

## Examples

```clj
#uuid "00000000-0000-0000-0000-000000000000"
;;=> #uuid "00000000-0000-0000-0000-000000000000"

#uuid "97bda55b-6175-4c39-9e04-7c0205c709dc"
;;=> #uuid "97bda55b-6175-4c39-9e04-7c0205c709dc"

#uuid "asdf"
;; clojure.lang.ExceptionInfo: Invalid UUID string: asdf
```

Get as a string:

```clj
(def foo #uuid "97bda55b-6175-4c39-9e04-7c0205c709dc")
(str foo)
;;=> "97bda55b-6175-4c39-9e04-7c0205c709dc"
```

## Usage
#uuid "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"

<!-- AUTO-GENERATED docfile links for github -->
[doc:cljs.core/UUID]:https://github.com/cljs/api/blob/master/docfiles/cljs.core/UUID.md
[doc:cljs.core/uuid]:https://github.com/cljs/api/blob/master/docfiles/cljs.core/uuid.md