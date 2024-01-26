# Sign

**Odoo Sign** allows you to send, sign and approve documents online.

You can upload any PDF file and add drag-and-dropping fields on it.
These fields are automatically filled out with the user's detail if they
are logged in.

<div class="seealso">

\- [Odoo Sign: product page](https://www.odoo.com/app/sign) - [Odoo
Tutorials: Sign](https://www.odoo.com/slides/sign-61)

</div>

## Validity of electronic signatures

The legal validity of electronic signatures generated by Odoo depends on
the legislation of your country. Companies doing business abroad should
consider electronic signature laws of other countries as well.

### In the European Union

The [eIDAS regulation](http://data.europa.eu/eli/reg/2014/910/oj)
establishes the framework for electronic signatures in all [27 member
states of the European
Union](https://europa.eu/european-union/about-eu/countries_en).

It distinguishes three types of electronic signatures:

1.  Electronic signatures
2.  Advanced electronic signatures
3.  Qualified electronic signatures

Odoo generates the first type, regular electronic signatures, and these
signatures can produce legal effects in the EU, as the regulation states
that “an electronic signature shall not be denied legal effect and
admissibility as evidence in legal proceedings solely on the grounds
that it is in an electronic form or that it does not meet the
requirements for qualified electronic signatures.”

Note that electronic signatures may not be automatically recognized as
valid. You may need to bring supporting evidence of a signature’s
validity.

### In the United States of America

The [ESIGN Act (Electronic Signatures in Global and National Commerce
Act)](https://www.fdic.gov/regulations/compliance/manual/10/X-3.1.pdf),
at the interstate and international levels, and the [UETA (Uniform
Electronic Transactions
Act)](https://www.uniformlaws.org/committees/community-home/librarydocuments?communitykey=2c04b76c-2b7d-4399-977e-d5876ba7e034&tab=librarydocuments),
at the state level, provide the legal framework for electronic
signatures. Note that
[Illinois](https://www.ilga.gov/legislation/ilcs/ilcs5.asp?ActID=89&)
and [New
York](https://its.ny.gov/electronic-signatures-and-records-act-esra)
have not adopted the UETA, but similar acts instead.

Overall, to be recognized as valid, electronic signatures have to meet
five criteria:

1.  A signer must show a clear intent to sign. For example, using a
    mouse to draw a signature can show intent. The signer must also have
    the option to opt-out of electronically signing a document.
2.  A signer must first express or imply their consent to conduct
    business electronically.
3.  The signature must be clearly attributed. In Odoo, metadata, such as
    the signer’s IP address, is added to the signature, which can be
    used as supporting evidence.
4.  The signature must be associated with the document being signed, for
    example, by keeping a record detailing how the signature was
    captured.
5.  Electronically signed documents need to be retained and available
    for later reference by all parties involved, for example, by
    providing the signer either a fully-executed copy or the option to
    download a copy.

<div class="note">

<div class="title">

Note

</div>

The information provided here does not constitute legal advice; it is
provided for general informational purposes only. As laws governing
electronic signatures rapidly evolve, we cannot guarantee whether all
information is up to date or not. We advise contacting a local attorney
for legal advice regarding electronic signature compliance and validity.

</div>

## Field Types

By configuring your own *Field Types*, also known as *Signature Item
Types*, you can make the signing process even faster for your customers,
partners, and employees.

To create and customize fields, activate the `developer mode
<developer-mode>`. Then head to `Documents --> Configuration --> Field
Types` and click on *Create*.

After giving your new field a name, select one of the six *Types*
available:

  - **Signature**: users are prompted to enter their signature either by
    drawing it, automatically generating one based on their name, or
    uploading a local file (usually an image). Each subsequent
    *Signature* field then reuses the data entered in the first field.
  - **Initial**: users are prompted to enter their initials, in a
    similar way to the *Signature* field.
  - **Text**: users enter text on a single line.
  - **Multiline Text**: users enter text on multiple lines.
  - **Checkbox**: users can tick a box (e.g.,to mark their approval or
    consent).
  - **Selection**: users choose a single option from a variety of
    options.

Next, you have the option to auto-complete fields for users based on
their Odoo profile information by using *Automatic Partner Field*. To
this end, the *Name*, *Email*, *Phone*, and *Company* fields are
preconfigured in your database.

<div class="note">

<div class="title">

Note

</div>

Users can freely edit auto-completed fields.

</div>

![Company field example in Odoo Sign](sign/field-example.png)

You can then change the size of the field by editing the *Default Width*
and *Default Height*. Both sizes are defined as a percentage of the
full-page expressed as a decimal, with 1 equalling the full-page's width
or height. By default, the width of new fields you create is set to 15%
(0.150) of a full-page's width, while their height is set to 1.5%
(0.015) of a full-page's height.

Next, write a *Tip*. Tips are displayed inside arrows on the left-hand
side of the user's screen during the signing process. You can also use a
*Placeholder* text to be displayed inside the field before it is
completed.

![Tip and placeholder example in Odoo Sign](sign/tip-placeholder.png)