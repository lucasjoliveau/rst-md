# VIES VAT numbers validation

**VAT Information Exchange System** - abbreviated **VIES** - is a tool
provided by the European Commission that allows you to check the
validity of VAT numbers of companies registered in the European Union.

Odoo provides a feature to **Verify VAT Numbers** when you save a
contact. This helps you make sure that your contacts provided you with a
valid VAT number without leaving Odoo interface.

## Configuration

To enable this feature, go to `Accounting --> Configuration --> Settings
--> Taxes`, enable the **Verify VAT Numbers** feature, and click on
*Save*.

![Enable "Verify VAT Numbers" in Odoo
Accounting](vat_validation/vat-validation-configuration.png)

## VAT Number validation

Whenever you create or modify a contact, make sure to fill out the
**Country** and **VAT** fields.

![Fill out the contact form with the country and VAT number before
clicking on \*Save\*](vat_validation/vat-validation-contact-form.png)

When you click on *Save*, Odoo runs a VIES VAT number check, and
displays an error message if the VAT number is invalid.

![Odoo displays an error message instead of saving when the VAT number
is invalid](vat_validation/vat-validation-error.png)

<div class="important">

<div class="title">

Important

</div>

This tool checks the VAT number's validity but does not check the other
fields' validity.

</div>

<div class="seealso">

  - [European Commission: VIES search
    engine](https://ec.europa.eu/taxation_customs/vies/vatRequest.html)

</div>
