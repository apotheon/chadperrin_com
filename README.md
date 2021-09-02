# chadperrin.com

This is my Zola-based rewrite of the chadperrin.com site.

To view work in progress in a browser:

    $ zola serve                # load localhost:1111

I typically ensure rebuild of a deployable version after viewing locally in a
browser by using this:

    $ zola serve; zola build    # load localhost:1111

This is the process for deploying:

    $ zola build
    $ cd public
    $ git clone git@github.com:apotheon/chadperrindeploy.git
    $ mv chadperrindeploy/.git ./
    $ rm -rf chadperrindeploy/
    $ git add *
    $ git commit -m 'compose reasonable commit message'
    $ git push

[Zola documentation][zoladoc]

[zoladoc]: https://www.getzola.org/documentation/getting-started/directory-structure/
