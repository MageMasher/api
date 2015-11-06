## cljs.core/map-indexed



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/map-indexed</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/map-indexed)
</td>
</tr>
</table>


 <samp>
(__map-indexed__ f coll)<br>
</samp>

---

Returns a lazy sequence consisting of the result of applying `f` to 0 and the
first item of `coll`, followed by applying `f` to 1 and the second item in
`coll`, etc, until `coll` is exhausted.

Function `f` should accept 2 arguments, index and item.



---


###### See Also:

[`cljs.core/map`](../cljs.core/map.md)<br>
[`cljs.core/keep-indexed`](../cljs.core/keep-indexed.md)<br>

---


Source docstring:

```
Returns a lazy sequence consisting of the result of applying f to 0
and the first item of coll, followed by applying f to 1 and the second
item in coll, etc, until coll is exhausted. Thus function f should
accept 2 arguments, index and item.
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r927/src/cljs/cljs/core.cljs#L1522-L1533):

```clj
(defn map-indexed
  [f coll]
  (let [mapi (fn mpi [idx coll]
               (lazy-seq
                (when-let [s (seq coll)]
                  (cons (f idx (first s))
                        (mpi (inc idx) (rest s))))))]
    (mapi 0 coll)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r927
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:1522-1533](https://github.com/clojure/clojurescript/blob/r927/src/cljs/cljs/core.cljs#L1522-L1533)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.core/map-indexed` @ clojuredocs](http://clojuredocs.org/clojure.core/map-indexed)<br>
[`clojure.core/map-indexed` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/map-indexed/)<br>
[`clojure.core/map-indexed` @ crossclj](http://crossclj.info/fun/clojure.core/map-indexed.html)<br>
[`cljs.core/map-indexed` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/map-indexed.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core/map-indexed.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "Returns a lazy sequence consisting of the result of applying `f` to 0 and the\nfirst item of `coll`, followed by applying `f` to 1 and the second item in\n`coll`, etc, until `coll` is exhausted.\n\nFunction `f` should accept 2 arguments, index and item.",
 :ns "cljs.core",
 :name "map-indexed",
 :signature ["[f coll]"],
 :history [["+" "0.0-927"]],
 :type "function",
 :related ["cljs.core/map" "cljs.core/keep-indexed"],
 :full-name-encode "cljs.core/map-indexed",
 :source {:code "(defn map-indexed\n  [f coll]\n  (let [mapi (fn mpi [idx coll]\n               (lazy-seq\n                (when-let [s (seq coll)]\n                  (cons (f idx (first s))\n                        (mpi (inc idx) (rest s))))))]\n    (mapi 0 coll)))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r927",
          :filename "src/cljs/cljs/core.cljs",
          :lines [1522 1533]},
 :full-name "cljs.core/map-indexed",
 :clj-symbol "clojure.core/map-indexed",
 :docstring "Returns a lazy sequence consisting of the result of applying f to 0\nand the first item of coll, followed by applying f to 1 and the second\nitem in coll, etc, until coll is exhausted. Thus function f should\naccept 2 arguments, index and item."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/map-indexed"]))
```

-->