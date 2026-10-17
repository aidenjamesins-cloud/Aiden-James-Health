# Aiden James Health

Website for Aiden James Health, an independent health insurance advisor in Tampa, FL.

## How it's set up

- `public/` holds the website itself. `public/index.html` is the homepage.
- `wrangler.jsonc` tells Cloudflare to serve everything in `public/`.

## Making changes

Edit files in `public/` (on GitHub: open the file, click the pencil icon, save with "Commit changes").
Cloudflare redeploys the site automatically after every commit.

## Quote form

The "See what you'd actually pay" form emails each request to ajh@aidenjameshealth.us through FormSubmit (formsubmit.co).
The very first submission sends an activation email to that inbox; click the link in it once, and every request after that arrives as an email.

The form has two steps (situation and state, then name, phone and optional ages). Business card QR codes open `https://aidenjameshealth.us/?card=NNNN#quote`; the form then shows the card number, and the email subject and "Came from" line name the card that brought the request in.

To test the form without sending anything, set `var DRAFT = false;` to `true` near the top of the script in `public/index.html`.

## Still to add

- Your Florida license number in the footer, if you want it shown
- Your agency appointment disclosure, if your agency requires one
- A client reviews section, once you have real reviews to share (a placeholder comment marks the spot in `public/index.html`)
- Your Google rating in the hero stat row, once your Google Business Profile has reviews
