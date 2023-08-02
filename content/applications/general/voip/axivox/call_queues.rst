===========
Call queues
===========

A call queue is a system that organizes sand routes incoming calls. When customers call a business
and all of the agents are busy, the call queue lines up the callers in sequential order based on the
time they called in. The callers then wait on hold, to be connected to the next available call
center agent.

By implementing a call queue system in place, this reduces stress for employees, and helps build
brand trust with customers. Many companies use call queues to help set expectations, distribute the
workload evenly amongst the team thus lowering call abandonment rates.

This document covers configuring call queues (with advanced settings), as well as how to log into a
call queue from the Odoo database.

Add a queue
===========

To add a call queue in Axivox navigate to the `Axivox management console
<https://manage.axivox.com>`_. In the left menu click on :guilabel:`Queues`. Next, click on
:guilabel:`Add a queue`.

Name
----

Once the :menuselection:`New queue` page appears, enter the
:guilabel:`Name` of the queue.

Internal extension
------------------

Choose an :guilabel:`Internal extension` for the queue. This is an
number to be dialed by users of the database to reach the login prompt for the queue.

Strategy
--------

Following the :guilabel:`Internal extension` field, is a field called :guilabel:`Strategy`. This
field is very important, in that it determines the call routing of received calls into this queue.
The following choices are available in the :guilabel:`Strategy` dropdown:

- Call all available agents
- Call the agent who has received the call for the longest time
- Call the agent who received the last call
- Call a random agent
- Call agents one after another
- Call agents one after another starting with the first in the list

Choose a strategy that meets the company's needs for customers calling into the queue. Each choice
results in a different strategy for choosing a agent to receive the incoming call.

Maximum waiting time in seconds
-------------------------------

The :guilabel:`Maximum waiting time in seconds` is the longest time the customer waits in the queue
before going to a voicemail, or wherever else they are directed to in a dial plan. Enter a time in
seconds.

Maximum duration of ringing at an agent
---------------------------------------

The :guilabel:`Maximum duration of ringing at an agent` is the longest time an individual agent's
line rings before moving on to another agent or the next step in the dial plan. Enter a time in
seconds.

.. seealso::
   For more information on dial plans visit:
   - :doc:`dial_plan_basics`
   - :doc:`dial_plan_advanced`

Adding agents
-------------

Adding :guilabel:`Static agents` and adding :guilabel:`Dynamic agents` are two pre-configured
methods for adding agents onto the call queue during the configuration.

.. _axivox/static-agents:

Static agents
~~~~~~~~~~~~~

Add :guilabel:`Static agents` to the :menuselection:`Queue configuration` page and these agents are
automatically added to the queue without the need to log in to receive calls.

.. _axivox/dynamic-agents:

Dynamic agents
~~~~~~~~~~~~~~

Add :guilabel:`Dynamic agents` to the :menuselection:`Queue configuration` page and these agents
have the ability to log into this queue. They are not logged in automatically and need to log in, to
receive calls.

.. tip::
   Be sure to :guilabel:`Save` the changes, and :guilabel:`Apply changes` in the upper right to
   implement the change in production.

Agent connection
================

There are three ways that call agents can connect to a Axivox call queue:

#. Dynamic agents connect automatically.
#. Manager logs agent(s) in via the `Axivox management console <https://manage.axivox.com>`_.
#. Agent connects to the queue in Odoo via the VoIP widget.

.. seealso::
   See the documentation on setting :guilabel:`Dynamic agents` in the `Axivox management console
   <https://manage.axivox.com>`_. :ref:`axivox/dynamic-agents`

Connect via Axivox queue
------------------------

After the initial configuration of the call queue is completed on the :menuselection:`Queue
configuration` page, and the changes are saved and implemented, then a manager can log into the
`Axivox management console <https://manage.axivox.com>`_ and connect :guilabel:`Static agents` to
the queue manually.

To connect :guilabel:`Static agents manually` navigate and click on the :guilabel:`Queues` menu in
the left hand column. The ::menuselection:`Queues` dashboard appears with a few different columns
listed.

When agents are connected to the queue or live with a customer, they’ll show under
:guilabel:`Connected Agents`. If they are Static agents, then they will always show up as connected.
Connect an agent by clicking the orange button labeled :guilabel:`Connect an agent`. Then select
their name from the drop-down menu, and click “Connect”.

.. image:: call_queues/call-queue.png
   :align: center
   :alt: Call queue with connected agents column highlighted and connect an agent and report buttons
         highlighted.

.. seealso::
   For more information on static and dynamic agents see this documentation:
   - :ref:`axivox/static-agents`
   - :ref:`axivox/dynamic-agents`

Report
~~~~~~

Click on :guilabel:`Report` to check on the reporting for a particular queue in order see who
connected when, and what phone calls came in and out of the queue. Reports can be customized by
date (:guilabel:`From` and :guilabel:`To`), :guilabel:`Event type`, and :guilabel:`Caller ID`. Each
report can be exported to a CSV (comma separated value) file for further use and analysis.

The :guilabel:`Event type` breakdown includes:

- The caller quit
- An agent is connecting
- An agent is disconnecting
- The call was terminated (agent hangs up)
- The call was terminated (caller hangs up)
- The caller is connected to an agent.
- Someone is entering the queue
- The caller exits the queue (no agent is connected)
- The caller exits the queue (timeout)
- No one is answering
- No one in answering, the caller hangs up
- Transfer
- Blind Transfer

.. image:: call_queues/event-type.png
   :align: center
   :alt: Event types in the Axivox queue reporting feature.

Different :guilabel:`Event type` can be selected or unselected by clicking :guilabel:`Check all` or
:guilabel:`Uncheck all` in the dropdown. To select an individual :guilabel:`Event type`, first click
:guilabel:`Uncheck all` and then click on the specific :guilabel:`Event type` in the dropdown.

Connecting to a queue on Odoo
-----------------------------

Agents can connect manually to the Axivox call queue from the Odoo VoIP widget once VoIP is
configured for the individual the user.

.. seealso::
   :doc:`axivox_config`

.. tip::
   In order to find out the :guilabel:`Agent connection` number and :guilabel:`Agent disconnection`
   number navigate to the `Axivox management console <https://manage.axivox.com>`_ and click on
   :guilabel:`Queues` in the left hand column. Under the :guilabel:`Agent Connection` column is the
   number that agents dial to connect to the queue. Under :guilabel:`Agent Disconnection` is the
   number an agent dials to be disconnected from the queue.

In order for an agent to connect to the call queue simply dial the :guilabel:`Agent connection`
number and press the green call button (phone icon [ 📞 ]). Then the agents hears a short two-second
message indicating that the agent is logged in. The call automatically ends.

.. tip::
   To view the connected agents in a call queue navigate to the `Axivox management console
   <https://manage.axivox.com>`_ and click on :guilabel:`Queue` in the left hand column. Click
   the green :guilabel:`Refresh` button at the top of the :guilabel:`Connected agents` column. Any
   agent (static or dynamic) that is connected to the queue currently, appear in the column next to
   the queue they are logged into.

To log out of the queue, simply open the Odoo VoIP widget and dial the :guilabel:`Agent
disconnection` number and press the green call button (phone icon [ 📞 ]). The agent will be
disconnected from the queue after a short two-second message.

.. tip::
   To view the connected agents in a call queue navigate to the `Axivox management console
   <https://manage.axivox.com>`_ and click on :guilabel:`Queue` in the left hand column. Click
   the green :guilabel:`Refresh` button at the top of the :guilabel:`Connected agents` column. To
   disconnect an agent manually click on the red :guilabel:`Disconnect` button and they are
   immediately disconnected. This can be helpful in situations where agents forget to log out at the
   end of the day.

.. seealso::
   For more information on the Odoo VoIp widget see this documentation: :doc:`../voip_widget`
