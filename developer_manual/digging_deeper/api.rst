API reference
=============


PHP public API
--------------

The public API is contained in the OCP namespace. See the `OCP API reference
<https://nextcloud-server.netlify.app/>`_ for further details.


PHP testing API
---------------

To avoid releasing uncompleted public API, it is possible to release a
testing version of the future API in the NCT namespace, following those rules:

- An API can only be nested in this testing namespace for 1 (one) major release,
- Once tested the API will be removed or copied to the OCP public namespace,
- If the API is not removed, the version from the NCT namespace will be marked as deprecated,
- Deprecated API from the NCT namespace are kept for 2 major releases,
- Code quality, comments, tests and psalm check are expected to be identical than in the OCP namespace.

.. note::
  - API within the testing namespace might not have documentation other than in-code comments.
