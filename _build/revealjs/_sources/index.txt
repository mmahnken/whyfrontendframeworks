==============================
Front End Frameworks: But why?
==============================

Disclaimer
==========

A Disclaimer
------------
On learning your first JavaScript Framework

.. container:: item-incremental
    
    - first know JavaScript
    - first master a web framework
    - don't try to do it in 1 day
    - HB Fellows: probably don't do it for your Hackbright project

JavaScript History
==================

A Storied Past
--------------
.. container:: item-incremental

    - 1998-early 2000s JavaScript gets standardized for multiple browsers
    - 2006- jQuery released, ends up winning the battle of the JS libraries for the timebeing

Front End Frameworks Come on the Scene
--------------------------------------

.. image:: new-js-fw.png

.. container:: item-incremental

    * 2009- AngularJS (Brat Tech LLC, Google and community)
    * 2010- Backbone (Jeremy Ashkenas)
    * 2011- Ember.js (Yehuda Katz, Tom Dale, community)
    * 2013- React.js (Facebook, Instagram, community)

The Case for Front End Frameworks
=================================

Why FEFs, Apparently
--------------------
.. container:: item-incremental

    * Easily testable
    * More maintainable
    * Safer
    * Faster
    * Easy on the eyes

Designing an Application Without a Front End Framework
======================================================

Let's talk about
----------------

.. container:: item-incremental

    * Database design
    * Designing your controllers (a.k.a. *routes*)
    * Designing page behavior with JavaScript

Database Design - elegant?
--------------------------
.. container:: compare
    
    .. image:: database_schema.jpg
        :width: 70%

    .. image:: coco.jpg
        :width: 20%

Designing Your Controllers - elegant?
-------------------------------------

.. container:: one-incremental
    
    .. code-block:: python
        :emphasize-lines: 1

        @app.route('/submit')
        def submit_form():
            pass

        @app.route('/process_form')
        def process_profile():
            pass

        @app.route('/form')
        def process_async_form():
            pass

Designing Your Controllers - elegant?
-------------------------------------
(Cont.)

.. container:: compare

    .. code-block:: python

        @app.route('/users/<int:user_id>/save')
        def create_user():
            pass

        @app.route('/users/<int:user_id>/profile')
        def profile():
            pass

        @app.route('/save_profile')
        def save_profile_async():
            pass

    .. image:: audrey.jpg
        :width: 20%

Designing Page Behavior with JavaScript - elegant?
--------------------------------------------------

.. image:: computer-shoe.jpg


Getting Acquainted with React.js
================================

React.js
--------

.. image:: logo.png
    :width: 50%


Component lifecycles
--------------------

.. code-block:: javascript

    var TextBox = React.createClass({
        getInitialState: function(){
            // pass
        },
        componentDidMount: function(){
            // pass
        },
        componentShouldUpdate: function(){
            // pass
        },
        render: function(){
            // pass
        }
    });

No More HTML (kind of.)
-----------------------

.. code-block:: javascript

    var TextBox = React.createClass({
        render: function() {
            return (<input type="text">);
        }

    });

No More HTML (kind of.)
-----------------------
(Cont.)

.. image:: not-mad.jpg

Components Composed of Other Components
---------------------------------------

.. code-block:: javascript

    var TextBox = React.createClass({
        render: function() {
            return (<input type="text" />);
        }

    });

.. code-block:: javascript

    var MeggiesForm = React.createClass({
        render: function(){
            return (
                <form action="/profile" method="post">
                    <TextBox />
                    <input type="submit" />
                </form>
                )        
        }
    });


React is Quick.
---------------
.. container:: nest-incremental

   - React changes the HTML using your instructions.
   - Everything becomes a lot more hypothetical.

     - No longer think of your code as directly changing the HTML.
   - React batches change events efficiently.
   

.. container:: one-incremental

    .. image:: ghost-dom.png
        :width: 70%

Gotchas
-------
Come to this slide when you do your first React.js tutorial. We'll skip it now unless people have questions.

.. container:: item-incremental

    - ``componentDidMount`` means the render function got called.
    - you can't use ``class="blah"`` in JSX because ``class`` is a reserved word in JavaScript.
        - use ``className`` instead.
    - Always use this.setState to change a component's state. Other than that function, state should be thought of as being immutable.

It's not all kittens and pizza.
-------------------------------

.. container:: nest-incremental
    
    - React is hard on designer workflows.
    - JSX is hard to look at.
    - The error messages are hella cryptic. Debugging React.js is horrible.

     - Facebook React developers, if you can hear me, please make this better.


FEF Patterns
============

FEF Patterns
------------
.. container:: item-incremental

    * Independent modules or units that have their own behaviors
    * An interest in fewer "pages"
    * Faster development and faster onboarding
    * Declarative is better than imperative
    * HTML, CSS, Bootstrap, and JQuery are still welcome to the party
    * When the data in the browser (user interacts) or the server (someone likes a page, some requests to be your friend) changes, the FEF "does the heavy lifting for you". 


Resources/ bibliography
=======================

Resources
---------

.. image:: react-book.png

Other Resources
---------------
.. container:: item-incremental

    - AngularJS: Up and Running (by Shyam Seshadri and Brad Green)
    - https://gist.github.com/dypsilon/5819504


