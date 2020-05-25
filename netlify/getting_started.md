# Overview

I've been working on my own personal website for a few months, but I haven't deployed it yet.
I'm far from happy with it, but I think making it available to the public will add some pressure to improve the site.
If that doesn't work I'll start linking to it and that should really put my feet to the fire.

Including the wait for my DNS settings to propagate, my website was up and running on my new custom domain in less than 30 minutes! It's only costing me the \$12/yr for my domain name.

Why did I wait so long to do this?!

# First Impressions from Setup

- Connecting to an existing GitHub repo was crazy easy via the setup wizard.
- Quick build config allows me to automatically deploy when pushing to master.
- It immediately knew how to handle deploying a Gatsby site. I didn't need to give it any additional information.
- Able to quickly change my \*.netlify.app domain.
- Free tier allows me to work without uploading any payment information.
- My background image (2.5MB) takes a long time on initial load.
- Took me 10 minutes to see my existing app deployed to my own \*.netlify.app domain.

# Custom Domain

Netlify offered the option to buy my .dev domain directly through them at $16.99 for the first year and $18.99 for the second year After looking around at domain services, I found this to be on the expensive side.

Google Domains offered my domain at \$12/yr. There were some cheaper options ($1-$2 less) at domain hosts I had never heard of, so I stuck with Google.

These were the steps to set up a custom domain on Netlify:

- Bought the domain from Google Domains
- Verified my email for Google Domains
- In Netlify's Domain management page I added the custom domain I just bought from Google
- After adding my custom domain, Netlify automatically scrolled me down to an error saying they could not provision a Let's Encrypt cert for my custom domain, meaning my site wasn't using HTTPS (uh oh)
- I looked around for some articles on how to set up a custom domain, and quickly found how to [Connect my Google Domain to a third party web host](https://support.google.com/domains/answer/6353515?hl=en), but I struggled to find an article on how to find the necessary values from Netlify to add into the Custom Resource records on Google Domains.
- Then I looked at my Domain management page on Netlify again and scrolled back up to where I added my custom domain. There were some alert icons there! In the options dropdown I found the values that needed to bet set in Google Domains!
- I set the instructed A type and CNAME type in Google Domains
- Waited 10 minutes for all of this to propagate
- Done!
