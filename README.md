BitcoinAuth
===========

Could the Bitcoin platform have more use cases than payments? Can we imagine other use cases
leveraging the crypto that powers bitcoin? This is one first idea, hopefully more to come.

Concept
-------

You have a personal domain (e.g. mine is htt://eschnou.com). You add on this page a link to one
of your bitcoin addresses with a `rel="me"` relation. You can now easily login in web services
with your 'domain' as your identity and bitcoin signature for authentication.

How it works
------------

1. You land on a website asking you to login.
2. You enter your domain as identity
3. The website prompts you with a challenge that has the form `thewebsite.com:Wg5qpk1oLmwqnt4z`
4. You sign the challenge with the bitcoin key associated to your domain
5. You provide the signature to the site which can easily verify it against your public key discovered on your site.

Important details to think about
--------------------------------

*The format of the challenge is important*: We want to avoid malicious sites tricking users in signing 
arbitrary content and also signing a token to login somewhere else. This is why there is a recognizable
format including the target domain.

Discuss
-------

Please discuss through the issue tracker.




