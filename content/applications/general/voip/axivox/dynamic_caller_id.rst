=================
Dynamic caller ID
=================

Caller ID will identify the caller when they make a phone call. The recipient of the call can see
what number the caller is calling from. Caller ID show users and clients, who is calling, so they
can choose to pick up or decline the call.

Axivox offers a dynamic caller ID to choose which number is displayed on outgoing calls.
International numbers can be purchased to do business transactions internationally, via a phone call
from a number that has an area code or country code of the destination. By displaying a local
number, this can increase customer engagement.

Some companies have many employees making calls from a call center, these employees are not always
available to receive a return phone call back from a prospective customer. In this case, :abbr:`VoIP
(Voice over Internet Protocol)` can be configured in such a way that dynamic caller ID shows the
main company phone number so that any number of employees in the group can answer the call. This way
a call is never missed.

.. _dynamic-caller-id/default:

Default outgoing number
=======================

In Axivox a *default number* can be set. This is a company's main number. This means when anyone
from the company (user/employeee) calls a number outside the company, the default number will show
up by default on the caller ID. If someone from outside the company tries to call back a user/
employee then they are funneled back through the main line (default number). If there is a dial plan
set up they will be prompted to make selections. This is especially helpful in cases that employees
change positions or if they leave the company.

.. seealso::
   - :doc:`dial_plan_basics`
   - :doc:`dial_plan_advanced`

To access the default number go to the `Axivox management console <https://manage.axivox.com>`_  and
log in. Click into :guilabel:`Settings` in the left menu and navigate to :guilabel:`Default
outgoing number`. Change the :guilabel:`Default outgoing number` by clicking the dropdown and making
a selection from the incoming phone numbers available on Axivox.

Be sure to :guilabel:`Save` the changes, and :guilabel:`Apply changes` in the upper right to
implement the change in production.

The :guilabel:`Default outgoing number` is what shows up by default in the Axivox management portal.
However, the outgoing number can also be configured differently at the user level.

Users
-----

To configure the outgoing number at the user level, first log in to the `Axivox management console
<https://manage.axivox.com>`_. Click into :guilabel:`Users` in the left side menu, and then click
:guilabel:`Edit` to the right of the user that is to be configured. Under :guilabel:`Outgoing
number` click the dropdown to select either the :guilabel:`Default outgoing number` (as specified
here: :ref:`dynamic-caller-id/default`), or any of the :guilabel:`Incoming numbers` on the Axivox
account.

Choosing the :guilabel:`Default` selection in the :guilabel:`Outgoing number` dropdown will ensure
that this user will have the :guilabel:`Default outgoing number` show on their caller ID when making
calls. If a specific number is chosen and this number is assigned to this user under
:guilabel:`Incoming numbers` (in the Axivox console's left menu), then this user will have a direct
line for customer to reach them on.

Be sure to :guilabel:`Save` the changes, and :guilabel:`Apply changes` in the upper right to
implement the change in production.

.. tip::
   By default in Axivox when creating a new user, the :guilabel:`Outgoing number` will automatically
   be set to :guilabel:`Default`.

Advanced options
----------------

To access the :guilabel:`Advanced options` navigate to the :guilabel:`Settings` option in the left
menu of the `Axivox management console <https://manage.axivox.com>`_. Then, click
:guilabel:`Advanced options` to the right of :guilabel:`Default outgoing number`. By default there
aren't any advanced rules set, so to create one, click the green :guilabel:`Plus [+]` icon. Here,
different caller IDs can be set up depending on what location the user/employee is calling from.

To create a rule, first set the :guilabel:`Destination prefeix`. This is the country code complete
with zero(s) in front of it. Then select the *phone number* that should be used for calling out from
that country code.

.. important::
   Check the box for :guilabel:`Apply advanced rules even for users with a default outgoing number
   configured.` to allow these rules to trump all other outgoing configurations.

.. tip::
   The rules order can be modified with a mouse by dragging into another order. The first matching
   rule is applied.

.. example::
   For example, a company would like all users/employees to utilize the configured number for Great
   Britain when calling from the `0044` country code (Great Britain). Simply type in `0044` into the
   :guilabel:`Destination prefeix` and select the number starting with the `+44` country code. Order
   the rules as necessary and select the checkbox to supersede all other rules if needed.

   .. image:: dynamic_caller_id/advanced-callerid.png
      :align: center
      :alt: Advanced options for the default outgoing number.

Be sure to :guilabel:`Save` the changes, and :guilabel:`Apply changes` in the upper right to
implement the change in production.
