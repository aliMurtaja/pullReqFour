# pullReqFour
pullReqFour



<html>
   <body>
      <button id="rzp-button">Authenticate</button>
      <script src="https://checkout.razorpay.com/v1/checkout.js"></script>
      <script>
         var options = {
           "key": "rzp_test_X1T10XJvRiK2n6",
           "subscription_id": "sub_OVKcHUUol7XWVP",
          //  "image": "https://leafletjs.com/docs/images/logo-ua.png",
          //  "recurring": true,
          //  "name": "My Billing Label",
          //  "description": "Auth txn for sub_00000000000001",
          //  "handler": function (response){
          //    alert(response.razorpay_payment_id);
          //  }
         };
         var rzp1 = new Razorpay(options);
         document.getElementById('rzp-button').onclick = function(e){
           rzp1.open();
         }

         rzp1.on('payment.failed', function (response){
            console.log(response.error.code);
        });
      </script>
   </body>
</html>
