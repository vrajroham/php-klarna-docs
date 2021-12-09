Config
=====

.. _installation:

Installation
------------

To use Lumache, first install it using pip:

.. code-block:: console

   (.venv) $ pip install lumache

Creating recipes
----------------

To retrieve a list of random ingredients,
you can use the ``lumache.get_random_ingredients()`` function:

.. autofunction:: lumache.get_random_ingredients

The ``kind`` parameter should be either ``"meat"``, ``"fish"``,
or ``"veggies"``. Otherwise, :php:func:`get_random_ingredients`
will raise an exception.

.. autoexception:: lumache.InvalidKindError

For example:

>>> import lumache
>>> lumache.get_random_ingredients()
['shells', 'gorgonzola', 'parsley']

.. code-block:: PHP
    <?php

    namespace Api\Core\Helpers;

    class Helpers
    {
        /**
        * Get the current logged in user.
        *
        * @return User|mixed
        */
        public static function getLoggedInUser(): User
        {
            $user = \Auth::user();

            if ($user === null) {
                throw new InvariantViolationException('No logged in user bound');
            }

            return $user;
        }
    }

