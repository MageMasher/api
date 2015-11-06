## cljs.repl.browser/server-state



 <table border="1">
<tr>
<td>var</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
</tr>
</table>









Source code @ [github](https://github.com/clojure/clojurescript/blob/r927/src/clj/cljs/repl/browser.clj#L24-L28):

```clj
(defonce server-state (atom {:socket nil
                             :connection nil
                             :promised-conn nil
                             :return-value-fn nil
                             :client-js nil}))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r927
└── src
    └── clj
        └── cljs
            └── repl
                └── <ins>[browser.clj:24-28](https://github.com/clojure/clojurescript/blob/r927/src/clj/cljs/repl/browser.clj#L24-L28)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.repl.browser/server-state` @ crossclj](http://crossclj.info/fun/cljs.repl.browser/server-state.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.repl.browser/server-state.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.repl.browser",
 :name "server-state",
 :type "var",
 :source {:code "(defonce server-state (atom {:socket nil\n                             :connection nil\n                             :promised-conn nil\n                             :return-value-fn nil\n                             :client-js nil}))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r927",
          :filename "src/clj/cljs/repl/browser.clj",
          :lines [24 28]},
 :full-name "cljs.repl.browser/server-state",
 :full-name-encode "cljs.repl.browser/server-state",
 :history [["+" "0.0-927"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.repl.browser/server-state"]))
```

-->