API reference
=============


PHP public API
--------------

The public API is contained in the OCP namespace. See the `OCP API reference
<https://nextcloud-server.netlify.app/>`_ for further details.


PHP testing API
---------------

To avoid releasing incomplete public API, it is possible to release a
testing version of the future API in the NCT namespace, following these rules:

- Code quality, comments, tests and psalm check are expected to be identical to the OCP namespace.
- Classes must be tag as `@experimental`, including the current version of Nextcloud.
- An API can only live in this testing namespace for one major release.
- During this testing phase, the code and the API can be modified/restructured without limitation.
- Once tested, the API will be removed entirely or copied to the OCP public namespace.
- If the API is not removed, the version from the NCT namespace will be marked as deprecated.
- Deprecated API from the NCT namespace are kept for 2 major releases.

.. note::
  - API within the testing namespace might not have documentation other than in-code comments.
