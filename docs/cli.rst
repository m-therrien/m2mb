.. _cli:

==================
Command line usage
==================

This package provides a command line to run the server.

To run the server, use the ``m2mbd`` command.

.. code:: bash

    $ m2mbd localhost 8225 http://mattermost/hooks/abcdefg

Parameters
==========

Required parameters
+++++++++++++++++++

``hostname``
    local hostname or ip address interface on which the server runs

``port``
    the port on which the server listens

``webhook_url``
    the Slack/Mattermost compatible webhook url to which send the messages

Optional parameters
+++++++++++++++++++

``-h``, ``--help``
    show help and exit

``--sieve_rules_files``
    the path to the file containing :doc:`sieve <sieve>` rules to filter
    incoming messages
    **NB**: ending lines must be ``<CRLF>``
    *defaults to sending all mails to default channel*

``--default_channel``
    default channel to send messages to
    *defaults to webhook defined channel*

``--username`` [1]_
    displayed username on messages
    *defaults to the username who created the webhook*

``--icon_url`` [1]_
    url used to displayed icon on messages
    *defaults to Slack/Mattermost default webhook icon*

``-d``, ``--debug``
    increase debugging info
    can be provided up to three times

.. [1] Username and icon overwrite must be allowed by Slack/Mattermost
    configuration