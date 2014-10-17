==========================
Askbot-Heroku - Q&A forum
==========================

This is a fork of the Askbot project - open source Q&A system, like StackOverflow, Yahoo Answers and some others.

This fork consists of an initialized Askbot installation containing the necessary modifications to deploy in heroku with a PostgreSQL database.

To deploy in heroku:

1. Create the heroku app with ``heroku create``
2. Push to the heroku repository: ``git push heroku master``
3. Set environment variables in heroku::

   $ heroku config:set DJANGO_SETTINGS_MODULE=app.settings
   $ heroku config:set SECRET_KEY="some_random_value"

4. ``syncdb`` and ``migrate``::

   $ heroku run python ./manage.py syncdb
   $ heroku run python ./manage.py migrate

To get a value for SECRET_KEY you can use the linux utility ``apg``.

I will try to keep this repository synced with https://github.com/ASKBOT/askbot-devel.git but this is not guaranteed.

The rest of this README comes from the original project.

=======
This is Askbot project - open source Q&A system, like StackOverflow, Yahoo Answers and some others.
Askbot is based on code of CNPROG, originally created by Mike Chen 
and Sailing Cai and some code written for OSQA.

Demos and hosting are available at http://askbot.com.

How to contribute
=================

**Translators: DO NOT use git to contribute translations!!!** instead - translate at https://www.transifex.com/projects/p/askbot/.

All documentation is in the directory askbot/doc

Askbot is based on code of CNPROG, originally created by Mike Chen 
and Sailing Cai and some code written for OSQA
=======
To contribute code, please fork and make pull requests.

If you are planning to add a new feature, please bring it up for discussion at our forum
(http://askbot.org/en/questions/) and mention that you are willing to develop this feature.

We will merge obvious bug fixes without questions, for more complex fixes
please add a test case that fails before and passes after applying your fix.

**Notes on using git for Askbot.** Please use topic branches only - one per feature or bugfix.
Do not add multiple features and fixes into the same branch -
those are much harder to understand and merge.

Follow https://help.github.com/articles/fork-a-repo to to learn how to use
`fetch` and `push` as well as other help on using git.

License, copyright and trademarks
=================================
Askbot software is licensed under GPL, version 3.

Copyright Askbot S.p.A and the project contributors, 2010-2013.

"Askbot" is a trademark and service mark registered in the United States, number 4323777.
