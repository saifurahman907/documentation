==================
Dial plan advanced
==================

Companies have a lot of incoming calls every day, but many don't want their teams to answer calls
24 hours a day, 7 days a week. Using Axivox advanced dial plan features, the process can be
automated and routing can be setup for all scenarios. This way customers are never left waiting or
frustrated because they could not get in touch with anyone.

Using the advanced elements in dial plans, companies can automate call routing for certain days or
times, like company holidays. Companies can also allow callers to enter extensions themselves and
transferred automatically using a digital receptionist, so an administrative team does not have to
be available around the clock. There is even the option, to route callers depending on where they
are calling from in the world, to maximize efficiently.

.. seealso::
   For more information on basic dial plans visit :doc:`dial_plan_basics`.

Basic routing elements
======================

- :guilabel:`Menu` - Add a dial-by-number directory and configured downstream actions (not
  terminal).

- :guilabel:`Digital Receptionist` - Attached a virtual dispatcher to listen for extensions to
  connect to.

Digital receptionist scenario
-----------------------------

Advanced routing elements
=========================

- :guilabel:`Dispatcher` - Create a call filter to route traffic based on geo-location of the caller
  ID.
- :guilabel:`Access list` - Create a tailored access list with VIP customer preference. Advanced
  routing mechanism.
- :guilabel:`Time condition` - Create time conditions to route incoming traffic around holidays or
  other sensitive time-frames.
- :guilabel:`Multi-Switch` - A mechanism to create paths and turn them on and off to divert incoming
  calls.

Dispatcher scenario
-------------------

Time condition scenario
-----------------------

Access list scenario
--------------------

Switches
========

- :guilabel:`Switch` - A switch is a manually on/off control that can turn divert traffic based on
  whether it's opened (On) or closed (off).

Basic switch
------------

A switch in Axivox is a simple activated / deactivated. :guilabel:`Switches` can be set in the
`Axivox management console <https://manage.axivox.com>`_ by navigating to :guilabel:`Switches`in
the left menu. To create a new switch click :guilabel:`Add a switch` and then configure a
:guilabel:`Name` for it.

Toggle the :guilabel:`Switch` :guilabel:`On` and :guilabel:`Off` from the :guilabel:`State` column
in the Switches dashboard (click :guilabel:`Switches` in the left menu).

This :guilabel:`On` / :guilabel:`Off` state will automatically route traffic in a dial plan in which
this switch is set. The traffic travels to the :guilabel:`Active` route when :guilabel:`On` is
toggled in the switch. The call traffic travels to the :guilabel:`Inactivate` route when
:guilabel:`Off` is toggled in the switch. Changes can be made on the fly, just be sure to
:guilabel:`Apply changes`.

Add a switch to dial plan
~~~~~~~~~~~~~~~~~~~~~~~~~

To add a :guilabel:`Switch` to a dial plan, first, navigate to `Axivox management
console <https://manage.axivox.com>`_ and click on :guilabel:`Dial plans` in the left menu. Then
select or create a dial plan, and click on the drop-down menu. Select :guilabel:`Switch` and then
click :guilabel:`Add`. Double click on the element to set the :guilabel:`Switch`.

.. image:: dial_plan_advanced/switch.png
   :align: center
   :alt: Switch configuration in a dial plan, with inactive and active routes highlighted.

Multi-switch
------------

A :guilabel:`Multi-switch` in Axivox is a switch where multiple paths can be configured and switched
between. To configure and set a :guilabel:`Multi-switch` first, navigate to `Axivox management
console <https://manage.axivox.com>`_. Then, click on the :guilabel:`Switches` menu item in the left
menu. Toggle to the :guilabel:`Multi-switch` tab to create or set a pre-configured
:guilabel:`Multi-switch`.

To create a new :guilabel:`Multi-switch` click :guilabel:`Create new`. Enter a :guilabel:`Name` for
the :guilabel:`Multi-switch` and then enter the :guilabel:`Available choice`(s). Enter one
:guilabel:`Available choice` per line and do not duplicate any.

To select the :guilabel:`State` of the :guilabel:`Multi-switch` click the drop-down menu next to the
:guilabel:`Multi-switch` name. Whichever :guilabel:`State` is choose is the route that is followed
in the dial plan. The :guilabel:`State` can be edited on the fly, just be sure to :guilabel:`Apply
changes`.

Add a multi-switch to dial plan
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

To add a :guilabel:`Multi-switch` to a dial plan, first, navigate to `Axivox management
console <https://manage.axivox.com>`_ and click on :guilabel:`Dial plans` in the left menu. Then
select or create a dial plan, and click on the drop-down menu. Select :guilabel:`Multi-switch` and
then click :guilabel:`Add`. Double click on the element to set the :guilabel:`Switch`.

.. image:: dial_plan_advanced/multi-switch.png
   :align: center
   :alt: Multi-switch configuration in a dial plan, with chosen route highlighted.
