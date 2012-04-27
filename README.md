node-jscoverage-executer
========================
helps you to get the code coverage in your node.js scripts.


Installation
============
1, clone from github

    $ git clone git@github.com:Shanon/node-jscoverage-executer.git

2, install using npm

    $ npm [-g] install /path/to/your/git/clone/directory


Usage
=====
1, generate the source code for the coverage from your source code using the jscoverage.

    $ jscoverage [--encoding=utf8] /path/to/your/source target_dir

2.a, execute your script with jscoverage-executer in jscoverage's output directory;

    $ cd target_dir
    $ jscoverage-executer your_script.js

2.b, execute your script with NODE_PATH env and jscoverage-executer.

    $ NODE_PATH=target_dir jscoverage-executer your_script.js

When your script is finished, the coverage data will be output to the 'cover' directory.
If you want to change the output directory, set the environment variable 'COVERAGE_DIRECTORY'

3, output code coverage using 'whiskey'

    $ whiskey --coverage-dir /path/to/coverage/output/dir \
      --coverage-files `echo target_dir/cover/[0-9]*.json` [--coverage-reporter html]




License
=======
[The MIT License](http://www.opensource.org/licenses/mit-license.php)