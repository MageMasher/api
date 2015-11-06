## #_ ignore



 <table border="1">
<tr>
<td>syntax</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> clj doc](http://clojure.org/reader#toc2)
</td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/I8uNXHv.png"> edn doc](https://github.com/edn-format/edn#discard)
</td>
</tr>
</table>



Causes the following form to be completely skipped by the reader.  This is a
more complete removal than the `comment` macro which yields nil.



---

###### Examples:

```clj
{:foo #_bar 2}
;;=> {:foo 2}
```

To comment out the last line of a function without worrying about commenting out
the trailing parentheses:

```clj
(defn foo []
  (println "hello")
  #_(println "world"))
```



---

###### See Also:

[`; comment`](../syntax/comment.md)<br>
[`cljs.core/comment`](../cljs.core/comment.md)<br>

---




 @ [github](https://github.com/clojure/clojure/blob/clojure-1.3.0/src/jvm/clojure/lang/LispReader.java#L):

```clj

```

<!--
Repo - tag - source tree - lines:

 <pre>
clojure @ clojure-1.3.0
└── src
    └── jvm
        └── clojure
            └── lang
                └── <ins>[LispReader.java:](https://github.com/clojure/clojure/blob/clojure-1.3.0/src/jvm/clojure/lang/LispReader.java#L)</ins>
</pre>

-->

---




 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/syntax/ignore.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "Causes the following form to be completely skipped by the reader.  This is a\nmore complete removal than the `comment` macro which yields nil.",
 :ns "syntax",
 :name "ignore",
 :history [["+" "0.0-927"]],
 :type "syntax",
 :related ["syntax/comment" "cljs.core/comment"],
 :full-name-encode "syntax/ignore",
 :source {:repo "clojure",
          :tag "clojure-1.3.0",
          :filename "src/jvm/clojure/lang/LispReader.java",
          :lines [nil]},
 :examples [{:id "f36d7a",
             :content "```clj\n{:foo #_bar 2}\n;;=> {:foo 2}\n```\n\nTo comment out the last line of a function without worrying about commenting out\nthe trailing parentheses:\n\n```clj\n(defn foo []\n  (println \"hello\")\n  #_(println \"world\"))\n```"}],
 :edn-doc "https://github.com/edn-format/edn#discard",
 :full-name "syntax/ignore",
 :display "#_ ignore",
 :clj-doc "http://clojure.org/reader#toc2"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "syntax/ignore"]))
```

-->