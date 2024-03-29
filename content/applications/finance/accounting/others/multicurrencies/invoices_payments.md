# Manage invoices and payment in multiple currencies

## Overview

Odoo provides multi-currency support with automatic currency gross or
loss entry adjustment. There are a few things Odoo has been to ease the
user's life.

All the account transactions will be done using the company currency.
However you can see two extra fields with the journal entry where
secondary currency and amount will visible. You can create
multi-currency journals of force a specific currency.

When creating an invoice, the currency can be changed very easily;
however Odoo takes the company currency as a default assignment. It will
convert all the amounts automatically using that currency.

## Configuration

### Enable Multi-Currency

For information about enabling Multi-Currency, please read the document:
`how_it_works`

### Configure your journal

In order to register payments in other currencies, you have to remove
the currency constraint on the journal. Go to the accounting
application, on the journal, click on `More --> Settings`.

![image](invoices_payments/invoice01.png)

Check if the currency field is empty or in the foreign currency in which
you will register the payments. If a currency is filled in, it means
that you can register payments only in this currency.

![image](invoices_payments/invoice02.png)

## Multi-currency invoices & Vendor Bills

Now that you are working in a multi-currency environment, all
accountable items will be linked to a currency, domestic or foreign.

### Invoices

You are now able to set a different currency than the company one on
your sale orders and on your invoices. The currency is set for the whole
document.

![image](invoices_payments/invoice03.png)

### Vendor Bills

You are now able to set a different currency than the company one on
your purchase orders and on your vendor bills. The currency is set for
the whole document.

![image](invoices_payments/invoice04.png)

## Multi-currency Payments

In the accounting application, go to `Sales --> Payments`. Register the
payment and indicate that it was done in the foreign currency. Then
click on **Confirm**.

![image](invoices_payments/invoice05.png)

The journal entry has been posted but not allocated.

Go back to your invoice (`Sales --> Customer Invoices`) and click on
**Add** to allocate the payment.

![image](invoices_payments/invoice06.png)

## Multi- Currency Bank Statements

When creating or importing bank statements, the amount is in the company
currency. But there are now two complementary fields, the amount that
was actually paid and the currency in which it was paid.

![image](invoices_payments/invoice07.png)

When reconciling it, Odoo will directly match the payment with the right
invoice. You will get the invoice price in the invoice currency and the
amount in your company currency.

![image](invoices_payments/invoice08.png)

## Exchange Rate Journal

Go to `Adviser --> Journal Entries` and look for the **Exchange
Difference** journal entries. All the exchange rates differences are
recorded in it.

![image](invoices_payments/invoice09.png)

<div class="seealso">

\* `how_it_works` \* `exchange`

</div>
