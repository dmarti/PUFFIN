# PUFFIN

PUFFIN, Personal User Floor For Impression Negotiations, is an enhancement
of TURTLEDOVE and related proposals, intended to enable users to 
incentivize the production and distribution of desired ad-supported content.


## Motivation

New proposals for enabling interest group based advertising are likely to have
two key effects on the advertising market.

 * Additional ad revenue for sites because of increased advertiser knowledge
   of audience composition in real time, similar to the effect shown by 
   Johnson et al. for the third-party cookie.

 * Leakage of ad revenue from high-engagement, high-reputation sites to
   lower-engagement sites where the same audience appears to be available.

While proposed post-cookie ad systems can address the leakage of _data_ away
from high-reputation sites, the _revenue_ leakage is still a 
problem for web users who are members of the audience for that content
and prefer to see more of it produced.


## Incentives for ecosystem participants

The advertising literature generally focuses on the
use of advertising by the _seller_ of a good
or service to produce desired behavior in the _buyer_.
Today's web advertising ecosystem, however, is
more complex.  Advertising placement decisions are encoded in
software run in the _buyer_'s browser, under control of
the buyer, and can therefore be designed to produce
desired behavior in the _seller_.

The browser
user seeks to obtain more value, in the form of
ad-supported content of interest, for a given "cost"
in advertising exposure.  Browser-based ad auctions
are an opportunity for users to choose to receive
interest-group advertising selectively.


# Proposal

In TURTLEDOVE and related proposals, a contextual ad and an interest-group ad
participate in an auction, and the interest-based ad wins (and is displayed to the user)
if it can outbid the highest-bidding contextual ad.

PUFFIN is a persistent per-browser floor price that the interest-group ad bid must
also exceeed in order to win the auction.

PUFFIN is calculated as an exponentially weighted rolling average of
contextual ad bids.  The interest-based ad must beat not only the highest-bidding
contextual ad, but also the average contextual ad displayed in the same browser.

This presents no problem for the positive, revenue-enhancing uses of interest-based
advertising, but limits revenue leakage effects.

Because PUFFIN is intended to incentivize production of high-engagement content, 
browsers may choose to adjust PUFFIN based on site engagement score, with a lower
effective PUFFIN applied to high-engagement pages.


## Example flow

FIXME

## Reporting

PUFFIN provides for no additional reporting beyond
what is available in the existing ad auction.
The PUFFIN is confidential and per-browser, and is
not available to any script.

## Fraud considerations

FIXME

## Fingerprinting

FIXME


# Related work

[WICG/turtledove: TURTLEDOVE](https://github.com/WICG/turtledove)

Johnson, Garrett and Shriver, Scott and Du, Shaoyin, Consumer Privacy Choice in Online Advertising: Who Opts Out and at What Cost to Industry? (June 19, 2019). Simon Business School Working Paper No. FR 17-19, Available at SSRN: https://ssrn.com/abstract=3020503 or http://dx.doi.org/10.2139/ssrn.3020503 

[Site Engagement - The Chromium Projects](https://www.chromium.org/developers/design-documents/site-engagement)
