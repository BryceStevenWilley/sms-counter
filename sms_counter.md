# Text message (SMS) counter for the GetYourRefund Hub 

**ONLY CONTINUE IF YOU TRUST THE SOURCE OF THIS CODE (me)**. You can verify my identity with Billy and Kelly.

<div id="the_bookmarklet" style="padding: 1em; background: rgb(200, 240, 240); border: 1px solid black; border-radius: 4px">
Drag this link into your browser's toolbar:<br/>
<a href="javascript: (function() {
    var gyr_msg_counter_js = document.createElement( 'script' );
    gyr_msg_counter_js.setAttribute( 'src', 'https://plocket.github.io/sms-counter/sms_counter.js' );
    document.body.appendChild( gyr_msg_counter_js );
})();">SMS Counter for GYR Hub</a>
</div>
<br/>
This bookmarklet lets you see an estimate of how many inidividual text messages (sms) your words might send.

Phones split up messages into separate chunks. The charge per message. Some phones mix up the order in which the chunks appear.

### Other prototypes we have made

* You can see a client's images on their documents page in the hub with [this bookmarklet](https://michaelaltmann.github.io/get-your-refund/bookmarklet.html)

### The code

For reference, this bookmarklet contains the code:

```
javascript: (function() {
    var gyr_msg_counter_js = document.createElement( 'script' );
    gyr_msg_counter_js.setAttribute( 'src', 'https://plocket.github.io/sms-counter/sms_counter.js' );
    document.body.appendChild( gyr_msg_counter_js );
})();
```

[See the code behind it on Github](https://github.com/plocket/sms-counter).

### Testing locally

If you make modifications to the javascript code and want to test them locally,
start an http server in this directory that will server up the javascript file
with the right content-type. For example, with python run

```
python3 -m http.server 9000
```

Once you have a local server running, create a bookmarklet whose content is

```
javascript: (function() {
    var gyr_msg_counter_js = document.createElement( 'script' );
    gyr_msg_counter_js.setAttribute( 'src', 'http://localhost:9000/sms_counter.js' );
    document.body.appendChild( gyr_msg_counter_js );
})();
```
