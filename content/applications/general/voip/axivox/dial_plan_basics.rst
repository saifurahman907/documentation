================
Dial plan basics
================

When someone calls a business, they might need to get in touch with customer support, a sales team,
or even one person's direct line. The caller might also be in search of some information about the
business, such as store hours, or they might want to leave a voicemail, so someone from the company
can call them back. With dial plans in Axivox a company can manage how incoming calls are handled.

Using call architecture through a dial plan, callers get directed to the right people or to the
right information. This document will cover basic configuration of dial plans in Axivox.

.. seealso::
   For more information on advanced dial plans visit :doc:`dial_plan_advanced`.

Dial plans
==========

Access dial plans by navigating to `Axivox management console <https://manage.axivox.com>`_ and
clicking on :guilabel:`Dial plans`. To add a new dial plan, click on the green button labeled,
:guilabel:`Add a new dial plan`.

.. tip::
   Axivox has no limit to the number of dial plans created. These can be added and improved upon at
   a later time. This allows for sandboxes to be created with many different configurations.

.. image:: dial_plan_basics/dial-plan-edits.png
   :align: center
   :alt: Dial plan dashboard with the edit features and Add a dial plan button highlighted.

To edit an existing dial plan, choose one of the following options to the right of the saved dial
plan:

#. :guilabel:`Delete` - This action deletes the attached dial plan.
#. :guilabel:`Edit` - This action allows the user to edit the :guilabel:`Name` and
   :guilabel:`Extension`.
#. :guilabel:`Visual Editor` - This action opens a visual editor window where the dial plan
   architecture can be edited.
#. :guilabel:`Duplicate` - This action duplicates the dial plan and puts it at the bottom of the
   list with an extension of +1 larger than the original extension.

Dial plan editor
----------------

The dial plan editor is the primary place where the architecture or structure of the dial plan is
configured. A separate window with a GUI (graphical user interface) appears where various dial plan
elements can be configured and linked together.

.. image:: dial_plan_basics/dial-plan-visual.png
   :align: center
   :alt: Visual editor for an example dial plan, with the New element, Add, and Save buttons
         highlighted.

New dial plans come blank with the option to :guilabel:`Add` :guilabel:`New elements` and
:guilabel:`Save` the progress. This method for saving is different from saving any other edits in
the Axiovx management console in that a separate :guilabel:`Save` button must be pressed before
closing the :menuselection:`Visual editor`. Again, like all other changes before these changes to
take place on the Axivox platform, the user must click :guilabel:`Apply changes` in the upper right
corner.

To add a new element from the :guilabel:`New element` dropdown, click and select the :guilabel:`New
element`. Then click :guilabel:`Add`. Connect elements by dragging outward from the circle on the
right or left side of the element. An :guilabel:`arrow` will appear and drag this :guilabel:`arrow`
to the next element in the dial plan. Connect the :guilabel:`arrow` to the circle on the right or
left side of the element.

.. important::
   All elements must have a final destination to close a loop. This can be the :guilabel:`hang up`
   element or looping the element back to a :guilabel:`menu` element or :guilabel:`digital
   receptionist`.

   .. image:: dial_plan_basics/loop-back.png
      :align: center
      :alt: Dial plan, shown with highlight looping open end back to the beginning of the menu
            element.

Remember to click :guilabel:`Save` before exiting the :menuselection:`Visual editor`.

Dial plan elements
------------------

The following :guilabel:`New elements` are available for use in a dial plan:

**Basic element**

- :guilabel:`Call` - Call an extension or queue.
- :guilabel:`Play a file` - Play an audio file or voice greeting.
- :guilabel:`Voicemail` - Forward to a voicemail (terminal).
- :guilabel:`Hang up` - Hang up the call (terminal).
- :guilabel:`Queue` - Attach a call queue with a group of users to answer a call.
- :guilabel:`Conference` - Add a conference room for a caller to connect to.

**Basic routing element**

- :guilabel:`Menu` - Add a dial-by-number directory and configured downstream actions (not
  terminal).
- :guilabel:`Switch` - A switch is a manually on/off control that can turn divert traffic based on
  whether it's opened (On) or closed (off).
- :guilabel:`Digital Receptionist` - Attached a virtual dispatcher to listen for extensions to
  connect to.

**Advanced routing element**

- :guilabel:`Dispatcher` - Create a call filter to route traffic based on geo-location of the caller
  ID.
- :guilabel:`Access list` - Create a tailored access list with VIP customer preference. Advanced
  routing mechanism.
- :guilabel:`Time condition` - Create time conditions to route incoming traffic around holidays or
  other sensitive time-frames.
- :guilabel:`Multi-Switch` - A mechanism to create paths and turn them on and off to divert incoming
  calls.

**Advanced element**

- :guilabel:`Record` - Recording feature is enabled (requires plan change, enabled in Settings).
- :guilabel:`Caller ID` - Replace the caller ID by the called number or free text.

Attach to incoming number
=========================

To attach an existing dial plan to an incoming number go to `Axivox management console
<https://manage.axivox.com>`_ and clicking on :guilabel:`Incoming numbers`. Next, click
:guilabel:`Edit` next to the number which the dial plan should be attached. This means that when
that number is dialed into, that the dial plan is activated and run through the prompts to properly
route the caller.

After selecting :guilabel:`Edit` click the drop-down menu next to the :guilabel:`Destination type
for voice call` field and select :guilabel:`Dial plan`. Then, a drop-down menu called
:guilabel:`Dial plan` will appear. Use the drop-down menu next to the :guilabel:`Dial plan` field to
find and select the appropriate dial plan to be activated on this :guilabel:`Incoming number`.

Finally :guilabel:`Save` the changes and :guilabel:`Apply changes` in the upper right corner.

.. seealso::
   :doc:`dial_plan_advanced`

Basic dial plan scenarios
-------------------------

The following setup is a basic dial plan scenario for call routing, many more elements can be added
on to complete the setup. The basic dial plan elements include: :guilabel:`Call`,
:guilabel:`Voicemail`, :guilabel:`Play a file`, :guilabel:`Menu`, :guilabel:`Queue`,
:guilabel:`Conference`, and :guilabel:`Hangup`.

.. image:: dial_plan_basics/basic-scenario.png
   :align: center
   :alt: Basic dial plan configuration

.. seealso::
   This setup does not include any basic or advanced call routing. For more information on call
   routing reference this documentation: :doc:`dial_plan_advanced`.
