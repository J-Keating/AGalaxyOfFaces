# Ask

This file controls the booking section, enquiry form, contact details, and form delivery. Never put an email password, API secret, or SMTP credential here.

## Section introduction

- **Navigation label:** Ask
- **Eyebrow:** Bookings and questions
- **Headline:** Tell me what you're planning.
- **Description:** Share the date, location, and approximate number of guests. I'll reply with availability and the details you need.
- **Submit button:** Send enquiry
- **Success message:** Thanks! Your enquiry has been sent.
- **Error message:** That did not send. Please try again or email us directly.

## Contact details

- **Business email:** [Email address]
- **Public phone:** [Optional]
- **Typical response time:** [For example: Usually within two working days]

## Form delivery

- **Mode:** Formspree
- **Formspree endpoint:** [For example: https://formspree.io/f/xxxxxxx]
- **Hosted form URL:** https://j-keating.github.io/AGalaxyOfFaces/ask.html
- **Email subject:** Face painting enquiry from {name}

The Canva website should link its **Check availability** call to the hosted form URL. Formspree sends submissions from that page without opening an email application.

## Form fields

### Name

- **Label:** Your name
- **Type:** Text
- **Required:** Yes

### Email

- **Label:** Email
- **Type:** Email
- **Required:** Yes

### Event date

- **Label:** Event date
- **Type:** Date
- **Required:** No

### Event type

- **Label:** Event type
- **Type:** Select
- **Required:** No
- **Options:** Birthday party; Festival or fair; School or community event; Other

### Event details

- **Label:** Tell me about the event
- **Type:** Long text
- **Required:** Yes
- **Placeholder:** Location, number of guests, timing, and anything else that would be helpful...

## Privacy note

- **Show below form:** [Optional short note explaining how enquiry details are used]
