## How to use canvas =>

1. const canvas = document.querySelector("canvas");
2. const ctx = canvas.getContext("2d");
// getContext("2d") function canvas element ke liye 2D rendering context ko retrieve karta hai. Iss context ka istemal phir 2D shapes draw karne ke liye kiya jata hai, jaise rectangles, lines, circles, text, etc.
// "2D rendering context" ek tarah ka object hai jo <canvas> element ke sath associated hota hai aur usmein 2D shapes aur graphics ko draw karne ke liye methods aur properties provide karta hai.
// Jab aap getContext("2d") ka istemal karte hain, toh aap ek 2D rendering context ko retrieve karte hain, jise aap phir use karke various shapes, lines, colors, text, images, aur aur bhi bahut kuch canvas par draw kar sakte hain.

3. canvas.width = window.innerWidth;
// canvas ki width window ke innerWidth ke barabar krne ke liye.

4. canvas.height = window.innerHeight;
// canvas ki height window ke innerHeigth ke barabar krne ke liye.

5. window.addEventListener("resize", () => {
    canvas.width = window.innerWidth;
    canvas.height = window.innerHeight;

    render();
})
// jab bhi hum window ko resize karenge toh canvas ki width aur height window ke innerWidth aur innerHeight ke barabar ho jayenge. aur sath hi me render() function ko bhi chala do, yaha render function me hum phir se canvas ke liye 2D rendering context ko retrieve karenge aur phir se 2D shapes draw karenge. saral tareeke se kahe to render function image ko window ke chata ya bada hone pr load krta hai, jitni baar window chota ya bada hota hai utni baar ye function call hoga.
render koi inbuilt function nhi hai ise banaya gya hai jise hum aage dekhege.

6. function files(index) {
  var data = `
       ./img/0001.png
       ./img/0002.png
       ./img/0003.png
       ./img/0004.png
       ./img/0005.png
       ./img/0006.png
       ./img/0007.png
       ./img/0008.png
       ./img/0009.png
       ./img/0010.png
       ./img/0011.png
       ./img/0012.png
       ./img/0013.png
       ./img/0014.png
       ./img/0015.png
       ./img/0016.png
       ./img/0017.png
       ./img/0018.png
       ./img/0019.png
       ./img/0020.png
       ./img/0021.png
       ./img/0022.png
       ./img/0023.png
       ./img/0024.png
       ./img/0025.png
       ./img/0026.png
       ./img/0027.png
       ./img/0028.png
       ./img/0029.png
       ./img/0030.png
       ./img/0031.png
       ./img/0032.png
       ./img/0033.png
       ./img/0034.png
       ./img/0035.png
       ./img/0036.png
       ./img/0037.png
       ./img/0038.png
       ./img/0039.png
       ./img/0040.png
       ./img/0041.png
       ./img/0042.png
       ./img/0043.png
       ./img/0044.png
       ./img/0045.png
       ./img/0046.png
       ./img/0047.png
       ./img/0048.png
       ./img/0049.png
       ./img/0050.png
       ./img/0051.png
       ./img/0052.png
       ./img/0053.png
       ./img/0054.png
       ./img/0055.png
       ./img/0056.png
       ./img/0057.png
       ./img/0058.png
       ./img/0059.png
       ./img/0060.png
       ./img/0061.png
       ./img/0062.png
       ./img/0063.png
       ./img/0064.png
       ./img/0065.png
       ./img/0066.png
       ./img/0067.png
       ./img/0068.png
       ./img/0069.png
       ./img/0070.png
       ./img/0071.png
       ./img/0072.png
       ./img/0073.png
       ./img/0074.png
       ./img/0075.png
       ./img/0076.png
       ./img/0077.png
       ./img/0078.png
       ./img/0079.png
       ./img/0080.png
       ./img/0081.png
       ./img/0082.png
       ./img/0083.png
       ./img/0084.png
       ./img/0085.png
       ./img/0086.png
       ./img/0087.png
       ./img/0088.png
       ./img/0089.png
       ./img/0090.png
       ./img/0091.png
       ./img/0092.png
       ./img/0093.png
       ./img/0094.png
       ./img/0095.png
       ./img/0096.png
       ./img/0097.png
       ./img/0098.png
       ./img/0099.png
       ./img/0100.png
       ./img/0101.png
       ./img/0102.png
       ./img/0103.png
       ./img/0104.png
       ./img/0105.png
       ./img/0106.png
       ./img/0107.png
       ./img/0108.png
       ./img/0109.png
       ./img/0110.png
       ./img/0111.png
       ./img/0112.png
       ./img/0113.png
       ./img/0114.png
       ./img/0115.png
       ./img/0116.png
       ./img/0117.png
       ./img/0118.png
       ./img/0119.png
       ./img/0120.png
       ./img/0121.png
       ./img/0122.png
       ./img/0123.png
       ./img/0124.png
       ./img/0125.png
       ./img/0126.png
       ./img/0127.png
       ./img/0128.png
       ./img/0129.png
       ./img/0130.png
       ./img/0131.png
       ./img/0132.png
       ./img/0133.png
       ./img/0134.png
       ./img/0135.png
       ./img/0136.png
       ./img/0137.png
       ./img/0138.png
       ./img/0139.png
       ./img/0140.png
       ./img/0141.png
       ./img/0142.png
       ./img/0143.png
       ./img/0144.png
       ./img/0145.png
       ./img/0146.png
       ./img/0147.png
       ./img/0148.png
       ./img/0149.png
       ./img/0150.png
       ./img/0151.png
       ./img/0152.png
       ./img/0153.png
       ./img/0154.png
       ./img/0155.png
       ./img/0156.png
       ./img/0157.png
       ./img/0158.png
       ./img/0159.png
       ./img/0160.png
       ./img/0161.png
       ./img/0162.png
       ./img/0163.png
       ./img/0164.png
       ./img/0165.png
       ./img/0166.png
       ./img/0167.png
       ./img/0168.png
       ./img/0169.png
       ./img/0170.png
       ./img/0171.png
       ./img/0172.png
       ./img/0173.png
       ./img/0174.png
       ./img/0175.png
       ./img/0176.png
       ./img/0177.png
       ./img/0178.png
       ./img/0179.png
       ./img/0180.png
       ./img/0181.png
       ./img/0182.png
       ./img/0183.png
       ./img/0184.png
       ./img/0185.png
       ./img/0186.png
       ./img/0187.png
       ./img/0188.png
       ./img/0189.png
       ./img/0190.png
       ./img/0191.png
       ./img/0192.png
       ./img/0193.png
       ./img/0194.png
       ./img/0195.png
       ./img/0196.png
       ./img/0197.png
       ./img/0198.png
       ./img/0199.png
       ./img/0200.png
       ./img/0201.png
       ./img/0202.png
       ./img/0203.png
       ./img/0204.png
       ./img/0205.png
       ./img/0206.png
       ./img/0207.png
       ./img/0208.png
       ./img/0209.png
       ./img/0210.png
       ./img/0211.png
       ./img/0212.png
       ./img/0213.png
       ./img/0214.png
       ./img/0215.png
       ./img/0216.png
       ./img/0217.png
       ./img/0218.png
       ./img/0219.png
       ./img/0220.png
       ./img/0221.png
       ./img/0222.png
       ./img/0223.png
       ./img/0224.png
       ./img/0225.png
       ./img/0226.png
       ./img/0227.png
       ./img/0228.png
       ./img/0229.png
       ./img/0230.png
       ./img/0231.png
       ./img/0232.png
       ./img/0233.png
       ./img/0234.png
       ./img/0235.png
       ./img/0236.png
       ./img/0237.png
       ./img/0238.png
       ./img/0239.png
       ./img/0240.png
       ./img/0241.png
       ./img/0242.png
       ./img/0243.png
       ./img/0244.png
       ./img/0245.png
       ./img/0246.png
       ./img/0247.png
       ./img/0248.png
       ./img/0249.png
       ./img/0250.png
       ./img/0251.png
       ./img/0252.png
       ./img/0253.png
       ./img/0254.png
       ./img/0255.png
       ./img/0256.png
       ./img/0257.png
       ./img/0258.png
       ./img/0259.png
       ./img/0260.png
       ./img/0261.png
       ./img/0262.png
       ./img/0263.png
       ./img/0264.png
       ./img/0265.png
       ./img/0266.png
       ./img/0267.png
       ./img/0268.png
       ./img/0269.png
       ./img/0270.png
       ./img/0271.png
       ./img/0272.png
       ./img/0273.png
       ./img/0274.png
       ./img/0275.png
       ./img/0276.png
       ./img/0277.png
       ./img/0278.png
       ./img/0279.png
       ./img/0280.png
       ./img/0281.png
       ./img/0282.png
       ./img/0283.png
       ./img/0284.png
       ./img/0285.png
       ./img/0286.png
       ./img/0287.png
       ./img/0288.png
       ./img/0289.png
       ./img/0290.png
       ./img/0291.png
       ./img/0292.png
       ./img/0293.png
       ./img/0294.png
       ./img/0295.png
       ./img/0296.png
       ./img/0297.png
       ./img/0298.png
       ./img/0299.png
       ./img/0300.png
   `;

   
  return data.split("\n")[index];
}

7. const frameCount = 469;
// total no. of images.
// agar yaha hum 300 kr dete hai to 300 images ke chalne ke baad canvas band ho jayega, isiliye hum images ko 1 se 469 tak hi show krne ke liye 469 likhege.

8. const images = [];
// aage hum for loop chalayege aur uss for loop ki madad se image ke src ko ek-ek krke images array me store kr denge.

9. const imageseq = {
    frame: 1
};
// images ko kaha se start krna hai.

10. for(let i = 0; i < frameCount; i++){
        const img = new Image();
        img.src = files(i);
        images.push(img);
    };
// for(let i = 0; i < frameCount; i++): Yeh loop frameCount tak chalega, jiska value 469 hai.
// const img = new Image();: Har loop iteration mein, ek nayi <img> HTML element create hoti hai. Isse nayi img object banaya jata hai.
// img.src = files(i);: files() ek function hai jo i ko input ke roop mein lete hue frame ke URL ko return karta hai. Yeh URL img.src property mein set kiya jata hai, jisse image load ho sake.
// images.push(img);: Har image ko images array mein store kiya jata hai, jisse baad mein unhe access kiya ja sake.

11. gsap.to(imageSeq, {
    frame: frameCount - 1,
    snap: "frame",
    ease: "none",
    scrollTrigger: {
        scrub: 0.15,
        trigger: "canvas",
        start: "top top",
        end: "600% top",
        scroller: "main"
    },
    onUpdate: render,
});
// frame: frameCount - 1, => ek ke baad ek image pr gsap lagega.
// snap: "frame" =>  iska mtlb hai ki ek time me sirf ek hi image/frame ko dikhao.
// ease: "none", => Transition ke liye koi ease nahi hai, matlab ki image ka transition linear hoga.
// scrub: 0.15, => Scroll karne par animation ka speed set kiya jata hai.
// trigger: "canvas", => ScrollTrigger ka trigger element set kiya jata hai, yahaan canvas element.
// start: "top top", => Animation start hoga jab canvas ka top screen ke top par aayega.
// end: "600% top", => Animation end hoga jab canvas 600% scroll kiya jaayega.
// scroller: "main" => Scroll karne ke liye scroller element set kiya jata hai, yahaan main element.
// onUpdate: render, => Animation update hone par render function ko call kiya jata hai.

12. images[1].onload = render;
// jab bhi browser load ho to render function ko call kiya jata hai aur 1st image ko show kr deta render function.

13. function render(){
        scaleImage(images[imageSeq.frame], context);
    };
// images[imageSeq.frame] se images array se current frame ki image select ki jati hai. imageSeq.frame variable, jo animation ka frame count represent karta hai, uski madad se current frame ki image select ki jati hai.
// Phir scaleImage() function ko call kiya jata hai currentFrameImage (current frame ki image) aur context (canvas ke context) ke saath. Isse selected image ko canvas ke context ke saath scale kiya jata hai.

14. function scaleImage(img, ctx) {
        var canvas = ctx.canvas;
        var hRatio = canvas.width / img.width;
        var vRatio = canvas.height / img.height;
        var ratio = Math.max(hRatio, vRatio);
        var centerShift_x = (canvas.width - img.width * ratio) / 2;
        var centerShift_y = (canvas.height - img.height * ratio) / 2;
        ctx.clearRect(0, 0, canvas.width, canvas.height);
        ctx.drawImage(
            img,
            0,
            0,
            img.width,
            img.height,
            centerShift_x,
            centerShift_y,
            img.width * ratio,
            img.height * ratio
        );
    };
`// Canvas aur image ka aspect ratio ko calculate kiya jata hai =>`
    var canvas = ctx.canvas;   => Canvas ka reference liya jata hai
    var hRatio = canvas.width / img.width;   => Horizontal scaling ratio calculate kiya jata hai
    var vRatio = canvas.height / img.height;   => Vertical scaling ratio calculate kiya jata hai
    var ratio = Math.max(hRatio, vRatio);   => Final scaling ratio, jo horizontal aur vertical scaling ratio mein se maximum ka chuna hua hai

`var hRatio = canvas.width / img.width;` => 
hRatio variable canvas ki width ko image ki width se divide karke horizontal scaling ratio ko represent karta hai.
Jab hum canvas.width / img.width ko calculate karte hain, toh hum essentially image ko canvas ke width ke hisaab se kitna stretch karna chahte hain wo dekh rahe hain.
Agar hRatio ki value 1 se zyada hai, toh image horizontally stretch hogi, aur agar 1 se choti hai, toh image horizontally shrink hogi.

`var ratio = Math.max(hRatio, vRatio);` =>
Math.max(hRatio, vRatio) expression se hume hRatio aur vRatio mein se maximum value milta hai. Yani, yeh expression hume width aur height ke scaling ratios mein se jo bhi bada hai wo provide karta hai.
Jaise agar hRatio 2 hai aur vRatio 1 hai, to Math.max(hRatio, vRatio) ka result 2 hoga. Iska matlab hai ki hume image ko horizontal direction mein 2 guna stretch karna chahiye.
Aur agar hRatio 1 hai aur vRatio 2 hai, to Math.max(hRatio, vRatio) ka result phir bhi 2 hoga, matlab hume image ko vertical direction mein 2 guna stretch karna chahiye.

`// Image ko canvas ke center mein shift karne ke liye x aur y coordinates ka shift calculate kiya jata hai`
var centerShift_x = (canvas.width - img.width * ratio) / 2;    =>  X coordinate ka shift calculate kiya jata hai
var centerShift_y = (canvas.height - img.height * ratio) / 2;    =>  Y coordinate ka shift calculate kiya jata hai

`ctx.clearRect(0, 0, canvas.width, canvas.height); =>`
ctx.clearRect() function canvas ko clear karne ke liye istemal hota hai. Yeh function canvas ke specified area ko clear karta hai, jisse koi bhi previously draw ki gayi content clear ho jata hai.
Yahan, clearRect() function ke arguments canvas ke x aur y coordinates (0, 0) se lekar canvas ke width aur height tak ka area specify karte hain. Isse canvas ka pura area clear ho jata hai.

`// Image ko canvas par draw kiya jata hai, scaled size ke saath aur center shift ke saath =>`
ctx.drawImage(
  img,      // Draw karne wali image ka reference
  0,        // Source image ka x coordinate
  0,        // Source image ka y coordinate
  img.width,        // Source image ka width
  img.height,       // Source image ka height
  centerShift_x,  // Canvas par image draw karne ka x coordinate
  centerShift_y,  // Canvas par image draw karne ka y coordinate
  img.width * ratio,        // Canvas par image ka final width
  img.height * ratio        // Canvas par image ka final height
);