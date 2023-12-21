=====================
Neutralized databases
=====================

What is a neutralized database?
===============================

A neutralized database is a non-production database on which several parameters are deactivated. This enables one to
carry out tests without the risk of launching specific automated processes that could impact production data (e.g.,
sending emails to customers). Live access is then removed and turned into a testing environment.

.. note::
   **Any testing database created is a neutralized database:**
   - testing backup databases
   - duplicate databases
   - For Odoo.sh: staging and development databases

.. warning::
   A database can also be neutralized when upgrading, as it is vital to do some tests before switching to a new version.

The consequences of a neutralized database
==========================================

Here is a non-exhaustive list of the deactivated parameters:
- all planned actions (where many flows are generated, e.g., automatic invoicing of subscriptions, mass mailing, etc.)
- the outgoing e-mail server (so that no e-mails are sent to anyone, especially customers, as it would be inappropriate
for them to receive requests for payment of duplicate or incorrect invoices)
- bank synchronization
- payment providers
- delivery methods
- IAP (In-App Purchase) tokens

How does one know when the database is neutralized?
===================================================

A red banner at the top of the screen is displayed on the neutralized database so that it can be seen immediately.
