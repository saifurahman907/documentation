================
Conference calls
================

Conference calls help to connect employees quickly and efficiently, so that matters can be discussed
in a open forum of sorts. Attendees can be limited via a sign in code, so that confidential matters
stay private.

This document will cover the configuration of conference calls in Axivox for use in Odoo *VoIP*.

Add conference
==============

To add a a virtual conference room, first, navigate to the `Axivox management console
<https://manage.axivox.com>`_. After logging in, click on :guilabel:`Conferences` in the left hand
menu. Next, click the green button labeled, :guilabel:`Add a conference` and a form will appear.

Fill in the :guilabel:`Name` field and set an :guilabel:`Internal extension`. The internal extension
is what everyone in the network (users) will use to quickly dial into the conference call, instead
of typing in the whole phone number.

.. tip::
   Try picking a number between three and five digits long, this way it can easily be dialed and
   remembered.

Next, set the :guilabel:`Access code` if the conference room requires security. This is a password
to get into the conference, once the extension for the conference is dialed. Immediately after
dialing the extension a digital receptionist will prompt for the :guilabel:`Access code`.

Under the :guilabel:`Administrator extension` click the dropdown and select the user's extension
that will manage the call. Finally, under :guilabel:`Wait for the administrator to start the
conference`, click the dropdown and select :guilabel:`Yes` or :guilabel:`No`. Should the selection
be :guilabel:`Yes`, then nobody will be allowed to utilize the virtual conference room until the
administrator is present and logged into the :guilabel:`Conference`.

Be sure to :guilabel:`Save` the changes, and :guilabel:`Apply changes` in the upper right to
implement the change in production. The conference has now be added and the Axivox administrator has
the option to :guilabel:`Delete` or :guilabel:`Edit` the :guilabel:`Conference` from the
Axivox :guilabel:`Conference` main dashboard.

To invite a Axivox user to a specific :guilabel:`Conference` simply click :guilabel:`Invite` and
enter the extension or phone number of the invitee. Once the extension or number is added into the
field, then click the green :guilabel:`Invite` button and the recipient will immediately receive a
phone call linking them to the conference automatically.

Incoming numbers
================

To open a conference to a wider audience, an Axivox :guilabel:`Conference` can be linked to
:guilabel:`Incoming numbers`. Log into the `Axivox management console <https://manage.axivox.com>`_
and click on :guilabel:`Incoming numbers`. Next, click :guilabel:`Edit` to the far right side of the
*incoming number* that the conference should be attached to. Now, under the first field, labeled,
:guilabel:`Destination type for voice call` click the dropdown and select :guilabel:`Conference`.
Finally, under :guilabel:`Conference`, click the dropdown and select the specific conference that
should be attached to this incoming number.

Now, whenever this incoming number is dialed the caller is let into the conference if there isn't an
:guilabel:`Access code`, or, the caller will be prompted to enter the :guilabel:`Access code` should
one be set.

Starting call in Odoo
=====================

In the Odoo database, click on the VoIP widget in the upper right corner (represented by a phone
[ ☎️ ] icon). Dial the specific extension number for the :guilabel:`Conference` and click the phone
receiver [ 📞 ] icon.

.. image:: conference_calls/phone-widget.png
    :align: center
    :alt: Connecting to a conference extension using the Odoo VoIP widget.

Once the digital receptionist answers, then dial the :guilabel:`Access code` and press the pound
[ # ] icon/key.
