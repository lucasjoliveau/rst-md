# FAQ

This document contains an explanation of the most recurring mailing
concerns.

We will start by addressing issues of outgoing emails (ex: my client has
not received my email), and then, of incoming emails (ex: I do not
receive responses from my customers in the database).

## Outgoing emails

### What do you have to check if your email is not sent?

The first indicator showing you that the email has not been sent is the
red envelope next to the date and time of the message.

![Red envelope displayed in chatter](faq/red-envelop.png)

#### Common error messages

##### You reached your daily limit:

![Warning in Odoo upon email limit reached](faq/email-limit.png)

Each email service provider has its own email sending limits. The limits
may be daily, hourly, and sometimes even per minute. This is the same
for Odoo, we have to limit our customers to prevent our e-mail servers
from being blacklisted.

Here are the default limits for new databases:

  - 200 emails/day for Odoo Online and Odoo.sh databases with an active
    subscription,
  - 20 emails/day for one-app free databases,
  - 50 emails/day for trial databases,
  - in case of migration, your daily limit might be reset to 50 emails a
    day.

In case you hit the limit, you can:

  - Ask our support team to increase your daily limit. We will analyze
    the situation of your database depending on (non-exhaustive list):
      - How many users in your database,
      - Which apps are installed,
      - Your bounce rate: the percentage of email addresses that did not
        receive your emails because it was returned by a mail server on
        its way to the final recipient. You can contact the
        [support](https://www.odoo.com/help).
  - Use your own outgoing email server to be independent of Odoo’s mail
    limit (please refer to `the corresponding documentation
    </applications/general/email_communication/email_servers>`),
  - Wait until 11pm UTC for the reset and click on the retry button: The
    `Developer mode <developer-mode>` must be activated. Then, go to
    `Settings --> Technical --> Emails`

![Retry button of an emails](faq/email-retry-technical.png)

<div class="warning">

<div class="title">

Warning

</div>

The daily limit is global to your database and can rise quickly\! By
default an internal message, a notification, a note, etc. counts as an
email in your daily limit if it notifies someone.

</div>

You can mitigate this by receiving your `notifications in Odoo
<discuss_app/notification_preferences>` instead of by emails.

##### SMTP Error

You can find out why an email wasn't transmitted successfully by
reviewing the Simple Mail Transport Protocol (SMTP) error messages. SMTP
is a protocol to describe the email structure and transmit it over the
Internet, and the error messages generated by email services are helpful
tools to diagnose and troubleshoot email problems.

##### No Error

Odoo is not always capable of providing information for the reason it
failed. The different providers implement a personalized policy of the
bounce emails and it is not always possible for Odoo to interpret it
correctly.

If you have this problem on a recurring basis with the same client or
the same domain, please do not hesitate to contact [Odoo
Support](https://www.odoo.com/help) for help in finding a reason.

Note: in such case, one of the most common reasons is related to `SPF
<email_communication/spf_compliant>` and/or `DKIM
<email_communication/DKIM_compliant>` configuration.

##### Why is my email sent late?

It may happen that you schedule an email campaign but it is not sent on
time. We know that we use a delayed job to send emails that we consider
as not urgent (Newsletters concept such as mass mailing, marketing
automation, events). The system utility **cron** can be used to schedule
programs to run automatically at predetermined intervals. We use that
policy in order to avoid cluttering the mail servers and prioritize the
communication.

The emails considered urgent (communication from one person to another
one such as Sales Orders, Invoices, Purchase Orders, etc.) are sent
directly.

![Email scheduled to be sent later.](faq/email-scheduled-later.png)

By default, the Mass Mailing cron runs every 60 minutes. So, you should
wait maximum an hour before the campaign is actually sent.

## Incoming emails

When you have an issue with incoming emails, there might not be an
indication per se in Odoo. This is the client who tries to contact a
database who will get a bounce (most of the time 550: mailbox
unavailable).

### Emails are not received

Depending on the platform you are using:

  - The **Odoo.sh** users can find their live logs on the folder
    `~/logs/`.
  - The folder `~/logs/` (preferably accessed by the command line) of an
    Odoo.sh contains a list of files containing the logs of the
    database. The log files are created everyday at 5:00 AM UTC. The two
    last days are not compressed, while the older ones are, in order to
    gain space. The naming of the files for Today and Yesterday are
    `odoo.log` and `odoo.log.1`. For the following, they are named with
    their dates and compressed. See the Odoo.sh documentation about
    `logs <odoosh/logs>`. Use the command `grep` and `zgrep` (for the
    compressed ones) to search through the files.
  - **Odoo Online** users won’t have access to their logs. However you
    can still contact [Odoo Support](https://www.odoo.com/help) , if you
    have a recurring issue with the same client or domain.

### Get help from support

In order to get helped efficiently, please provide as much information
as possible. Here is a list of what can be helpful:

  - The **EML** of the email, stating for *Electronic Mail*, is the file
    format containing all the technical information required for an
    investigation. The documentation of your own email provider might
    help you on how to get your EML files. Once you get the EML of the
    email, adding it in the attachment of your ticket is the most
    efficient way for us to investigate. The support will mainly focus
    on redundant issues.
    
    <div class="seealso">
    
    \- [Gmail
    documentation](https://support.google.com/mail/answer/29436)
    
    \- [Outlook
    documentation](https://support.microsoft.com/en-us/office/view-internet-message-headers-in-outlook-cd039382-dc6e-4264-ac74-c048563d212c#tab=Web)
    
    </div>

  - The exact flow you are following in order to normally receive those
    emails in Odoo. Here are examples of questions whose answers can be
    useful:
    
      - Is this simply a reply from an email going out from Odoo ?
      - Are you using an incoming email server or somehow redirecting?
      - Can you provide us with an example of an email that has been
        correctly forwarded ?

  - Providing answers to the following questions:
    
      - Is it a generic issue or is it specific to a use case? If yes,
        which one exactly?
      - Is it working as expected? In case the email is sent using Odoo,
        the bounce email should reach the Odoo database and display the
        `red envelope <red_envelop>`.
