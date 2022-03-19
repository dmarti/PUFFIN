**Does PUFFIN prevent some transactions from taking place based on what happened on another site?**

Yes, the PUFFIN is based on previous ad transactions that may have happened on any site.

However, a bidding function is never made aware of whether it lost an auction due to PUFFIN or due to being outbid on the current site.

**Is the PUFFIN available to parties in the client-side auction?**

No. Making PUFFIN available here [could encourage sites to add too many marginal people to the interest group and then rely on PUFFIN to only bid on some of them](https://github.com/dmarti/PUFFIN/issues/3).

**Is PUFFIN a privacy protection measure?**

A significant risk for browser-enabled advertising is that deceptive and fraudulent sites will be able to monetize ad impressions from desirable users.

Each high-value user will be carrying around a bunch of high-revenue ads in their browser, and all that a deceptive site has to do is somehow get one of those ads to bid.

In-browser ads give bad actors a powerful incentive to send out a large number of links to their sites in hopes of getting some high-value traffic.
This could take the form of:

 * harmless but annoying tactics like chumboxes

 * ToS-violating but legal techniques like email and forum spam

 * Malware

Without revenue protection for high-engagement sites, TURTLEDOVE/FLEDGE help support malware by making it easier to monetize.


**When is the PUFFIN applied?**

In the FLEDGE origin trial, [the contextual clearing price can be used as a floor for the FLEDGE auction, and the contextual ad can be rendered in a regular iframe if the FLEDGE auction returns no...results that beat the floor](https://github.com/WICG/turtledove/issues/260#issuecomment-1072887938). The PUFFIN would be applied as an additional floor at this stage: the interest group ad would need to beat both the current winning contextual ad and the PUFFIN.
