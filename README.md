BitcoinID and BitcoinAuth
==========================

Could the Bitcoin platform have more use cases than payments? Can we imagine other use cases
leveraging the crypto that powers bitcoin? This is one first idea, hopefully more to come.

BitcoinID
---------

You have a personal domain (e.g. mine is htt://eschnou.com). You add on this page a link to one
of your bitcoin addresses with a `rel="me"` relation. This simple additions enable new use cases:

- You can now easily login in web services with your 'domain' as your identity and bitcoin signature for authentication.
- You can send/receive payments to/from other URLs without the need to know the recipient bitcoin address

BitcoinAuth flow
----------------

1. You land on a website asking you to login.
2. You enter your domain as identity
3. The website prompts you with a challenge that has the form `thewebsite.com:Wg5qpk1oLmwqnt4z`
4. You sign the challenge with the bitcoin key associated to your domain
5. You provide the signature to the site which can easily verify it against your public key discovered on your site.

*The format of the challenge is important*: We want to avoid malicious sites tricking users in signing 
arbitrary content and also signing a token to login somewhere else. This is why there is a recognizable
format including the target domain.


Using BitcoinID to tip a user/post on the #indieweb
---------------------------------------------------

1. Let's say you want to tip me 0.01 BTC for this awesome idea :-)
2. The tip client fetches the page at htt://eschnou.com
3. The client parse the page and search for an anchor with rel=me pointing to a bitcoin uri
4. The client sends the payment to the bitcoin address

In addition, the user could post a 'tip mention' on his own site, linking to the post/user
being tipped with a rel='tip' mention and send a pingback to the target URI.

Discuss
-------

Please discuss through the issue tracker.
