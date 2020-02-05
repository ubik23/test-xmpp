Created two accounts to test: 
frederic@jabbers.one
other@jabbers.one

Started by going through some examples on the Strophe.js Github page:
https://github.com/strophe/strophejs/tree/master/examples

I played with basic.html with basic.js:

I used a CDN for Strophe instead of handling it locally for the test.
I plugged the conversjs.com/http-bind as the BOSH_SERVICE to get it working.  Was able to login and get a response. But this script didn’t handle messages…

At this point I took the time to learn more. I watched a video by Jack Moffit on XMPP and Strophe.js and two videos by JC Brand on XMPP and Converse.js. At this point I’m getting a clearer picture of how the pieces fit together.

I’m now understanding how xmpp and http are different and how they require BOSH and Strophe for the XMPP to function in the browser. 

I checked out the xmpp-bosh-client, specifically the function that sends out the message:
https://github.com/kdcro101/xmpp-bosh-client/blob/a29c383de06b4f29857094810083c11098344fc9/node-ts/index.ts#L360

Then I found a live version with the code:
http://embed.plnkr.co/EhQHDsYpDhrECmaaIlZO/

I copied it locally as ‘chat.html’ and changed the BOSH_SERVICE and the CDN for Strophe and was able to get it to send a message over XMPP (tested in two instances of the page, with my two XMPP adresses).

For the purpose of the test, I'm running a local php server like so : php -S localhost:1234


