Typesetting Notes with restructuredText
=======================================

Oh this is pretty hard.

Do you want some irrelevant theorems?
-------------------------------------

Here is an irrelevent theorem (`source <https://www.sciencedirect.com/science/article/pii/S1570868310000455>`__) to show that theorems can be referenced from the same page (:numref:`Theorem {number} <selfpromotion>`) or from other pages (:numref:`Theorem {number} <righttriangle>`).

.. _selfpromotion:

.. proof:theorem::

   #. If :math:`\Lambda` is a canonical modal logic, then the class of all frames that validate :math:`\Lambda` is quasimodal.
   #. A class of frames closed under the three fundamental frame constructions and ultraproducts is quasimodal.
   #. A modally definable elementary class of frames is quasimodal.

And here are others, without any label, or without title.

.. proof:theorem::

   Let :math:`\Lambda` be the modal logic of the quasimodal class K of frames, and let L be a class of frames containing K and having the same modal logic :math:`\Lambda`.

   #. K and L have the same hybrid logic.
   #. L is quasimodal

.. proof:corollary:: Non-quasimodal class of frames

   Let K be a class of frames, and :math:`\varphi` a hybrid formula valid in K. If :math:`\varphi` is not valid in the closure of K under the three fundamental operations and ultraroots, then K is not quasimodal.

.. _gammastar:

.. proof:conjecture:: Fake :math:`\Gamma^*` conjecture

   This is a dummy conjecture to illustrate that one can use math in theorem titles.

   Note that math typesetting is lost when referencing the theorem: :ref:`gammastar`.

Code Blocks
-------------------------------------

Swift code?

.. code-block:: swift
   :linenos:
   
   func someFunctionWithNonescapingClosure(closure: () -> Void) {
      closure()
   }

   class SomeClass {
      var x = 10
      func doSomething() {
         someFunctionWithEscapingClosure { self.x = 100 }
         someFunctionWithNonescapingClosure { x = 200 }
      }
   }

   let instance = SomeClass()
   instance.doSomething()
   print(instance.x)
   // Prints "200"

   completionHandlers.first?()
   print(instance.x)
   // Prints "100"

Does it work?
