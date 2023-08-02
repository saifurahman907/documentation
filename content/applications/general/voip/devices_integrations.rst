========================
Devices and integrations
========================

:abbr:`VoIP (Voice over Internet Protocol)` can be used on many different devices, ranging from, a
computer, tablet, smartphone and many more. This is helpful in that it reduces costs, and employees
can work from anywhere in the world with a broadband internet connection.

Odoo *VoIP* is SIP (Session Initiation Protocol) compatible, which means that it can be used with
*any* :abbr:`SIP (Session Initiation Protocol)` compatible application. This document will cover
setting up Odoo *VoIP* across different devices and integrations.

Odoo is fully integrated with all Odoo apps, users can click into any app and schedule a call as an
activity in the chatter.

.. example::
   For example, in the *CRM* app a user can click into an opportunity and click on
   :guilabel:`Activities` in the chatter. Next, choose :guilabel:`Call` and under :guilabel:`Due
   Date` select a date. Click :guilabel:`Save` and now in the chatter an activity will show up.
   Should the :guilabel:`Due Date` be for today's date, then the activity will show up in the
   :abbr:`VoIP (Voice over Internet Protocol)` widget.

   .. image:: devices_integrations/crm-voip-widget.png
      :align: center
      :alt: View of crm leads and the option to schedule an activity for Odoo Discuss

   .. seealso::
      :doc:`voip_widget`

Odoo VoIP (laptop/desktop computer)
===================================

Odoo :abbr:`VoIP (Voice over Internet Protocol)` app and widget can be used from any browser on a
laptop or desktop device. Simply click on the phone icon in the upper right corner and the widget
will appear.

.. seealso::
   To see use of the :abbr:`VoIP (Voice over Internet Protocol)` widget on a desktop/laptop computer
   see this documentation: :doc:`voip_widget`.

Odoo VoIP (tablet/mobile device)
================================

Odoo :abbr:`VoIP (Voice over Internet Protocol)` app can be used on tablets and mobile phones
through the Odoo Android or Apple IOS applications. Additionally the mobile web browser can be used
to access the database.

.. warning::
   Odoo android and Apple IOS applications are no longer being maintained by Odoo on the android and
   Apple portals. This means that Odoo support will only be able to handle limited scope of Odoo
   android or Apple IOS support tickets.

While in the mobile application on a mobile/tablet access the :abbr:`VoIP (Voice over Internet
Protocol)` widget by tapping on the phone icon in the upper right corner. The widget will appear in
the lower left corner.

When first making a call from the tablet using the mobile application, the user will be prompted to
:guilabel:`Allow` for the database to use the microphone. Click :guilabel:`Allow` when prompted to
continue with the call using the microphone. This step is necessary whether using the mobile Odoo
application or web browser.

.. image:: devices_integrations/voip-phone.png
    :align: center
    :alt: Window prompt to choose whether to use VOIP or the devices phone to make the call.

Odoo will then ask how to make the call. The two options will be: :guilabel:`VOIP` or
:guilabel:`Phone` (should the tablet be enabled for calling). Click the box next to
:guilabel:`Remember ?` should this decision be the default moving forward.

.. image:: devices_integrations/allow-mic.png
    :align: center
    :alt: Allow the database to access the microphone.

Here is the layout of what the :abbr:`VoIP (Voice over Internet Protocol)` app looks like on the
a mobile device:

.. image:: devices_integrations/voip-odoo-dashboard.png
    :align: center
    :alt: Layout of what the VoIP app looks like on the a mobile device.

Zoiper Lite
===========

Zoiper Lite is a free :abbr:`VoIP (Voice over Internet Protocol)` :abbr:`SIP (Session Initiation
Protocol)` dialer with voice and video.

To start using the Zoiper app, first download it to the device via the `Zoiper download page
<https://www.zoiper.com/en/voip-softphone/download/current>`_.

A mobile device is the most common installation, and this document will cover setup on the Zoiper
IOS application. Screenshots and steps may differ depending on the setup.

After installing the Zoiper application on the Apple iPhone open the application and tap on
:guilabel:`Settings`. Navigate to :guilabel:`Accounts` and tap on the plus [+] icon to add an
account.

If the :abbr:`VoIP (Voice over Internet Protocol)` account is already setup, then click
:guilabel:`Yes`.

.. image:: devices_integrations/account-settings-zoiper-group.png
   :align: center
   :alt: Zoiper account setup, shown in the view from a mobile device.

Next, tap on :guilabel:`Select a provider`. On the screen that populates tap on :guilabel:`Country`
in the upper right corner to narrow the providers down to a specific country. Choose the country for
the provider that is being configured and then find the :guilabel:`Provider` and select it.

.. example::
   If the provider being configured is *Axivox* then select :guilabel:`Belgium`. Choose
   :guilabel:`Axivox` as the provider.

.. image:: devices_integrations/provider-zoiper-odoo.png
   :align: center
   :alt: Zoiper account setup, choosing the provider.

Then, under :abbr:`SIP (Session Initiation Protocol)` options, enter the :guilabel:`Account name`,
:guilabel:`Domain`, :guilabel:`Username`, and :guilabel:`Password`. All this information will vary
based on the account.

.. tip::
   To access this information via the *Axivox* portal, navigate to :menuselection:`Users --> Choose
   user --> Edit --> SIP Identifiers tab`. The :guilabel:`SIP username`, :guilabel:`Domain`,
   :guilabel:`SIP password`, and :guilabel:`Address of the proxy server` are all present in this
   tab.

.. list-table::
   :header-rows: 1

   * - Zoiper Field
     - Axivox Field
   * - Account name
     - *Can be anything*
   * - Domain
     - Domain
   * - Username
     - SIP username
   * - Password
     - SIP password

Once this account information is entered in click the green :guilabel:`Register` button at the top
of the screen. Once the registration information is checked Zioper will populate a message stating
:guilabel:`Registration Status: OK`. Zoiper is now setup to make phone calls using the :abbr:`VoIP
(Voice over Internet Protocol)` service.

.. image:: devices_integrations/sip-options-zoiper.png
   :align: center
   :alt: Zoiper account setup, registration successful.

Linphone
========

Linphone is an open-source :abbr:`VoIP (Voice over Internet Protocol)` :abbr:`SIP (Session
Initiation Protocol)` softphone used for voice, video, messaging (group and individual), as well as
conference calls.

To start using the Linphone app, first download it to the device via the `Linphone download page
<https://new.linphone.org/technical-corner/linphone?qt-technical_corner=2#qt-technical_corner>`_.

A mobile device is the most common installation, and this document will cover setup on the Linphone
IOS application. Screenshots and steps may differ depending on the setup.

To begin configuring Linphone for use with a :abbr:`SIP (Session Initiation Protocol)` provider
first open Linphone and a assistant screen will appear. From this screen select :guilabel:`Use SIP
Account`. Then on the following screen enter the username, password, domain, and display name. Then
press :guilabel:`Login`. Linphone will be ready to start making calls once there is a green button
at the top of the application screen that reads :guilabel:`Connected`.

.. image:: devices_integrations/linphone-odoo-setup.png
   :align: center
   :alt: Linphone account setup, registration successful.

.. tip::
   Linphone makes a variety of applications for mobile and desktop devices in operating systems,
   such as Windows, Linux, Apple, and Android. Because Linphone is an open source project, many new
   updates are released on a regular basis. See `Linphone's wiki-documentation page
   <https://wiki.linphone.org/xwiki/wiki/public/view/Linphone/>`_.
