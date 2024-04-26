## how to download images like this ./images/almost500Images =>

(1.) go to website jisse img ko download krna hai.
(2.) network -> img -> select any image then right click -> copy -> copy all as HAR
(3.) console -> write here ->
                var har = paste here copied HAR,  iske baad
                har(),    then enter
                paste this code -> 

                    var imageUrls = [];
                    har.log.entries.forEach(function (entry) {
                      if (entry.response.content.mimeType.indexOf("image/") !== 0) return;
                      imageUrls.push(entry.request.url);
                    });
                    console.log(imageUrls.join('\n'));  
                    
ab aapko sabhi img ke links mil gaye hoge.

(4.) now follow these files =>
     (a.) downloadImg.js
     (b.) package.json  =>   isme "type": "module" khud se likhna padega.
          aur isme node-fetch ko npm i node-fetch se install krna padega.

(5.) now run this command =>
     node downloadImg.js

(6.) ab aapko sabhi img download ho jayegi.




## imp =>  agar aapko iss tarike se img nhi milti hai to iska mtlb hai ki aap jis url ko iss tarah se download kr rhe ho wo encripted hai.                                 *recommended
`second method => url nikalne ka same tareeka hai ab uss url se img ko ek sath download krne ke liye follow these steps =>`
1. use chrome extension => Bulk image downloader from url list
2. paste your all url line by line in the extension
3. then select the folder where you want to download images
4. click on download button
5. now you will get all images in your selected folder/downloads.