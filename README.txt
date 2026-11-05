CaRe Bounce - holding page
==========================
Updated 5 November 2026. These files are served by GitHub Pages at
carebounce.co.za.

This is NOT the real site. It is one page that says "opening soon" and
pushes people to WhatsApp. It goes up first to prove the domain, the SSL
and the Zoho mail all survive the move, before the real site replaces it.

WHAT IS IN HERE
  index.html   The holding page. No images, no video, no JavaScript.
  robots.txt   Search engines may index it.
  sitemap.xml  Points Google at the homepage.

WHY GITHUB PAGES AND NOT NETLIFY
  Netlify's free plan prints a "Powered by Netlify" badge on the site and
  only removes it on a paid plan (about R350 a month). GitHub Pages serves
  our files exactly as uploaded and adds nothing. Both are free.

  Cloudflare Pages was the other option. It only offers a CNAME record for
  a custom domain, and a CNAME cannot sit on carebounce.co.za because our
  Zoho MX records are already there - it would have killed our email.
  GitHub Pages gives A records, which sit alongside MX happily.

TO CHANGE THE PAGE
  Edit index.html, then upload it over the old one in the repository.
  GitHub republishes within about a minute.

  There is no countdown any more. The page says "Opening soon" in plain
  HTML - one line, near the top of the body. There is no JavaScript in
  this file at all, so nothing can break and it works everywhere.

WHY NOT "UNDER MAINTENANCE"
  Maintenance means something broke. Nothing has broken - this business
  has not opened yet. "Opening soon" is the truthful version and it does
  not make a first-time visitor think the company is unreliable.

DNS - WHAT POINTS WHERE
  The domain is registered at HostAfrica and stays there (R109 a year,
  renews 25 October 2027). Only these records concern the website:

    A      @     185.199.108.153    GitHub Pages
    A      @     185.199.109.153    four, so the site survives one
    A      @     185.199.110.153    GitHub datacentre going down
    A      @     185.199.111.153
    CNAME  www   carebounceenquiries.github.io

  DO NOT TOUCH the 3 MX records or the 2 TXT records. Those are the Zoho
  email. Changing them stops info@carebounce.co.za receiving mail.

  After any DNS change, send a test email to info@carebounce.co.za from a
  different address and confirm it still arrives.

THERE IS NO FORM ON THIS PAGE, AND THAT IS DELIBERATE
  GitHub Pages only hands out files. It cannot receive a form submission.
  This page uses a WhatsApp button instead, which needs no server.

  The real site does have a quote form. Before it launches, that form must
  be pointed at something that can catch it - Zoho Forms (free: 3 forms,
  500 submissions a month, and we already have Zoho), or a WhatsApp
  pre-fill that needs no service at all.

WHEN THE REAL SITE IS READY
  Upload the contents of ..\netlify-site over this repository. Before you
  do, that folder still needs:
    - six real photographs for the gallery
    - the two [PRICE] values on the Love Experiences page
    - share.jpg for WhatsApp and Facebook link previews
    - the quote form rewired away from Netlify Forms
