# om with figwheel

Project with om and figwheel

Latest versions

Clojure 1.7

## Setup

To get an interactive development environment run:

optional:- brew install rlwrap

    rlwrap lein figwheel

and open your browser at [localhost:3449](http://localhost:3449/).
This will auto compile and send all changes to the browser without the
need to reload. After the compilation process is complete, you will
get a Browser Connected REPL. An easy way to try it is:

    (js/alert "Am I connected?")

and you should see an alert in the browser window.


Update the text using the REPL.

    (in-ns 'omwithfigwheel.client) ;; change into namespace

    (swap! app-state assoc :text "Changed it!") ;; associate the text to "Changed it!"

The Browser should update as the app state is modified.

To clean all compiled files:

    lein clean

To create a production build run:

    lein cljsbuild once min

And open your browser in `resources/public/index.html`. 

## License

Distributed under the Eclipse Public License either version 1.0 or (at your option) any later version.
