<template>
  <!-- GetButton.io widget -->
  <script type="text/javascript">
    (function () {
    var options = {
    whatsapp: "+62 812-2455-7760", // WhatsApp number
    instagram: "arntonius", // Instagram username
    call_to_action: "", // Call to action
    button_color: "#129BF4", // Color of button
    position: "right", // Position may be 'right' or 'left'
    order: "whatsapp,instagram", // Order of buttons
    pre_filled_message: "Hello Reza, I just want to buy some product", // WhatsApp pre-filled message
    };
    var proto = document.location.protocol, host = "getbutton.io", url = proto + "//static." + host;
    var s = document.createElement('script'); s.type = 'text/javascript'; s.async = true; s.src = url + '/widget-send-button/js/init.js';
    s.onload = function () { WhWidgetSendButton.init(host, proto, options); };
    var x = document.getElementsByTagName('script')[0]; x.parentNode.insertBefore(s, x);
    })();
  </script>
  <!-- /GetButton.io widget -->
</template>
