RTD Tool Chain
==============
Instructions on creating and using the tool chain for generating documentation on ReadTheDocs

References
-----------------
* `RTD Destination Website <https://readthedocs.org/projects/rtdtutorialkroki/>`_
* `Sphinx Quickstart Tutorial <https://sphinx-rtd-tutorial.readthedocs.io/en/latest/install.html>`_
* `Continuous Deployment <https://docs.readthedocs.io/en/stable/integrations.html>`_

Process Outlines
----------------
* create repositories
   * local repository for editing
        * add RTD config `Config <https://docs.readthedocs.io/en/stable/config-file/index.html>`_
   * github repository for editing
   * read the docs repository for reading and publishing
        * Import project
        * add rtd conf
        * build
        * view
* transfer processes
   * update local repository
   * build local site
   * transfer local site to github
   * transfer github site to read the docs
   * update github site
   * pull github back to local site

Commands
--------
* Push to github
    * git remote -v
    * git remote rm origin
    * git log --pretty=oneline --abbrev-commit --all
    * git remote add origin git@github.com:unixgeexen/compinfo.rtd.git
    * git push origin master
* Errors in rtd build
.. code-block:: console
 python -m sphinx -T -b html -d _build/doctrees -D language=en . $READTHEDOCS_OUTPUT/html
Running Sphinx v7.2.6

Traceback (most recent call last):
  File "/home/docs/checkouts/readthedocs.org/user_builds/compinfortd/envs/latest/lib/python3.12/site-packages/sphinx/registry.py", line 447, in load_extension
    mod = import_module(extname)
          ^^^^^^^^^^^^^^^^^^^^^^
  File "/home/docs/.asdf/installs/python/3.12.0/lib/python3.12/importlib/__init__.py", line 90, in import_module
    return _bootstrap._gcd_import(name[level:], package, level)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "<frozen importlib._bootstrap>", line 1381, in _gcd_import
  File "<frozen importlib._bootstrap>", line 1354, in _find_and_load
  File "<frozen importlib._bootstrap>", line 1318, in _find_and_load_unlocked
ModuleNotFoundError: No module named 'sphinxcontrib.kroki'

The above exception was the direct cause of the following exception:

Traceback (most recent call last):
  File "/home/docs/checkouts/readthedocs.org/user_builds/compinfortd/envs/latest/lib/python3.12/site-packages/sphinx/cmd/build.py", line 293, in build_main
    app = Sphinx(args.sourcedir, args.confdir, args.outputdir,
          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/docs/checkouts/readthedocs.org/user_builds/compinfortd/envs/latest/lib/python3.12/site-packages/sphinx/application.py", line 233, in __init__
    self.setup_extension(extension)
  File "/home/docs/checkouts/readthedocs.org/user_builds/compinfortd/envs/latest/lib/python3.12/site-packages/sphinx/application.py", line 406, in setup_extension
    self.registry.load_extension(self, extname)
  File "/home/docs/checkouts/readthedocs.org/user_builds/compinfortd/envs/latest/lib/python3.12/site-packages/sphinx/registry.py", line 450, in load_extension
    raise ExtensionError(__('Could not import extension %s') % extname,
sphinx.errors.ExtensionError: Could not import extension sphinxcontrib.kroki (exception: No module named 'sphinxcontrib.kroki')

Extension error:
Could not import extension sphinxcontrib.kroki (exception: No module named 'sphinxcontrib.krok
