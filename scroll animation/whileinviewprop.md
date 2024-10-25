- dekho ismien 2 props ki jrurat hai aur vo hai 
    -> whileinview prop . (ismien css aayegi jo element ko animate kregi after vo viewport mein dikh jaye).
    -> viewport prop.(iski bhi 2 properties hai ).
        -amount( kitne % of the element needs to be visible to trigger the animation, but you can adjust this value as needed.(iski value 0 se 1 hogi)).
        -once (agr true hai to hr baar viewport pr aane k baad animate hoga and jb viewport k bahr aayega to initial state mein aa jayega(initial prop wali css) , agr false hai to sirf ek baar hi animate hoga  ).

```jsx

'use client'
import React from 'react'
import { useRef ,useEffect} from 'react'
import { motion,useScroll,useTransform } from 'framer-motion'
function page() {
    const targetref=useRef()
    var {scrollYProgress}=useScroll(
        {
            target:targetref,
            offset: ["end center", " end start"],
        }
    )
    const val=useTransform(scrollYProgress,[0,1],[0,50])
    useEffect(() => {
        console.log(targetref.current); // Check if the ref is correctly targeting the element
      }, []);
  return (
    <>
  



Lorem ipsum dolor sit amet, consectetur adipisicing elit. Odit non necessitatibus reprehenderit, cumque, aliquid, dolorum nisi quos id unde in possimus dolor aperiam voluptatum aliquam iusto. Distinctio, inventore? Consequatur alias sapiente ipsam quae officia. Sint molestiae debitis molestias, suscipit qui numquam accusamus autem dicta facere, consectetur aut eum quidem nam dolore, alias aperiam sit. Inventore consequatur suscipit laborum, dignissimos, ratione quisquam id ad aliquid cupiditate neque consequuntur doloribus dolores quia fuga minus animi aut reprehenderit accusantium expedita asperiores dolore quam. Corrupti, iste! Ipsum facilis repellendus atque quam minima, tempora commodi sit accusamus numquam ipsa alias. Adipisci nam impedit nostrum nihil officiis beatae ab eligendi excepturi iusto facere distinctio nemo quidem sunt totam suscipit eveniet laudantium odit, sit praesentium fugiat nulla eaque saepe recusandae dignissimos! Dolorem repellat accusamus blanditiis facere, ad modi, ducimus quod iusto voluptas est ipsum suscipit voluptates aliquid provident ipsam nemo, quidem reprehenderit dicta? Quod corporis impedit laborum vero, sunt laboriosam tenetur autem ipsam quia officia saepe dicta et veritatis similique consequatur pariatur nam? Reiciendis voluptatum magni dicta debitis. Esse, nostrum aliquid illum omnis nemo dolorum quisquam explicabo eos culpa totam minima ad blanditiis facilis dicta saepe tempora voluptate similique a vero qui officiis quia aliquam? Iusto, sapiente. Eligendi asperiores omnis fugit hic non maxime mollitia, magni, delectus facere accusamus modi aspernatur veritatis. Distinctio rem sed ut nostrum. Ad hic quisquam debitis, harum deleniti pariatur dignissimos iste fugiat perspiciatis voluptatum eum? Nobis rem doloribus nihil necessitatibus tenetur odio natus voluptate sunt aliquid magnam repudiandae eos dolore veritatis totam voluptatem, expedita voluptates aut incidunt nam inventore delectus ipsum placeat. Ut aut natus accusantium nobis alias, veritatis iste voluptatibus? Blanditiis praesentium deleniti voluptatibus animi sint, nostrum harum. Dolorum sapiente praesentium placeat explicabo distinctio laudantium modi veniam temporibus eveniet, commodi esse enim delectus. Omnis quos, aperiam sunt, quaerat officia numquam cum repellendus optio labore natus voluptates quibusdam beatae architecto assumenda modi alias aspernatur nesciunt. Facilis fugit maiores accusantium, cumque perferendis placeat rerum vitae hic esse velit debitis, fuga distinctio nesciunt sit illo? Corrupti placeat facilis earum debitis dolore officiis qui accusamus corporis quam explicabo! Quia, dicta. Minus sapiente molestiae facere quisquam nemo quae sunt vitae reprehenderit, suscipit animi quidem doloribus hic recusandae. Soluta amet porro atque quae earum doloribus voluptates repellendus doloremque quas dicta, deleniti explicabo labore fugiat vitae recusandae delectus pariatur quisquam dolore libero perferendis praesentium nobis? Laborum illo quis dolorem sequi? Dolores accusantium illo vero itaque iusto possimus officia. Lorem ipsum dolor, sit amet consectetur adipisicing elit. Rerum at fugiat beatae. Nostrum, aliquid numquam, nobis facere non sequi ullam officia beatae ducimus autem possimus doloribus rem distinctio minus magnam cupiditate labore excepturi neque impedit maxime sunt eligendi laboriosam dolorum ea! Culpa, odit? Praesentium dolorum, cum officia repudiandae nulla, fugit corporis magni veritatis nostrum expedita odit, dolorem ipsum ea quae a similique! Possimus, dolore alias! Recusandae voluptatum quo saepe dolorum doloribus ad, dolores ipsum dolor hic beatae illo ratione veniam sint corporis cum accusantium vero maiores molestiae vel nisi nemo eaque quas? Vero suscipit odio sit doloribus soluta sapiente hic! Optio et dicta eaque accusantium temporibus rerum quas, necessitatibus vero fugit quae velit. Laudantium ad blanditiis eum molestiae, nostrum ratione incidunt facilis amet quas? Aspernatur ullam incidunt temporibus omnis porro ipsum, corporis facere perspiciatis praesentium laboriosam odio accusantium, autem dignissimos, qui quisquam delectus illum alias sed? Fuga quo non neque quis assumenda. Iusto assumenda voluptates repellat ducimus veniam facere laudantium accusantium neque iure suscipit vitae accusamus at, quis expedita, alias saepe. Praesentium odio alias, eum odit eius nobis animi repellendus mollitia expedita enim quam, aliquid ducimus sit fugit distinctio aperiam quaerat doloribus! Quibusdam unde, esse error deserunt doloremque quisquam nemo tenetur assumenda sequi, velit suscipit ad voluptatum at debitis natus maiores illum laudantium sed. Maiores nulla porro eos corporis tempora beatae velit sequi. Fugiat earum, voluptas possimus ipsam, quaerat adipisci illo numquam quae commodi laboriosam voluptate ratione aliquam porro fuga veniam. Ea possimus, laudantium recusandae, neque impedit quod rerum ipsum praesentium, dignissimos sunt ratione molestias modi voluptatibus cum pariatur doloribus doloremque officiis quasi alias excepturi! Quo eum consequuntur repudiandae possimus. Porro, odio est? Harum eveniet mollitia eligendi ad iste ratione numquam ex quaerat quis fuga non, adipisci est iure at facere nisi porro. Est nulla ex maiores at commodi maxime, aspernatur quam nisi dicta. Placeat laboriosam fugiat, a aperiam, amet at deleniti quas aliquam ut ad blanditiis molestiae quis quasi nihil esse ratione facilis mollitia non. Nemo consectetur sed recusandae enim quam eligendi, quisquam, similique neque voluptatibus deserunt cupiditate placeat, asperiores ipsa. Quas cumque aliquam ex consequuntur iusto placeat aliquid eligendi dolore. Quos nihil possimus aliquam, cupiditate iusto rem ea quasi enim optio temporibus. Dignissimos, necessitatibus excepturi sed reiciendis tempora eaque eos non ullam architecto itaque quas amet repellat sequi tenetur maiores harum iste ipsum dolore illo voluptate ex exercitationem facere molestias! Voluptatibus est quasi suscipit, ipsum dolorum sint nobis.



<div className='w-full h-[50vh] bg-blue-600 pt-64    overflow-hidden' ref={targetref}  >
    a
    </div>
    <motion.div className='bg-red-600 w-1/5 items-center  ' style={{x:val} } transition={{duration:4}} >hello</motion.div>

    Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quibusdam pariatur modi nisi omnis distinctio odio laudantium labore, itaque soluta dolores magni, aspernatur impedit a fugiat voluptatum nemo error praesentium veniam porro illo! Dolorum, dolore. Provident, aspernatur esse minus atque officiis harum enim accusantium itaque cum reprehenderit maiores commodi vitae facere sapiente dolorem. Recusandae laboriosam minima tempore iste saepe at voluptate error hic doloribus aliquam asperiores repellat quidem ad, distinctio fuga optio officiis mollitia sequi? Quibusdam itaque ipsam aut voluptas aliquid, dolor veritatis? Molestias deleniti qui ab vel architecto voluptates minima omnis nostrum magni voluptatem, totam quis facere. Tenetur debitis labore, eaque assumenda ad, atque ipsum exercitationem necessitatibus aperiam fuga explicabo? Natus perspiciatis animi necessitatibus. Tempora suscipit aliquam at modi et adipisci dolor mollitia sint nulla, repudiandae ad dolores voluptas. Eius blanditiis veniam nostrum molestiae id earum, hic minima eos porro consectetur quo corrupti quos modi, ipsam repellendus in error necessitatibus eveniet odit autem esse, eligendi ab. Doloremque ipsam accusamus corrupti rem esse mollitia dolorum aut placeat adipisci, voluptatibus architecto laudantium officia neque, nemo fugiat distinctio odit ipsa eveniet, id provident tenetur quibusdam cupiditate nulla reprehenderit. Veritatis fugit quibusdam laudantium quo fugiat voluptas illo et? Modi voluptatibus illo odio animi porro eveniet cumque commodi repudiandae delectus at consequatur deleniti cupiditate molestiae minus quis, molestias alias velit excepturi! Quibusdam labore quaerat expedita beatae excepturi deleniti minus dicta neque? Iure ad, facilis dignissimos fugiat, iste consequatur blanditiis rem asperiores eligendi totam minus maiores explicabo facere alias molestiae distinctio eum culpa aspernatur? Rem, voluptas placeat! Veritatis odit sequi eveniet quis dolorum amet quaerat veniam molestias perspiciatis velit dolor, perferendis rerum consequuntur nemo excepturi repellendus laborum aliquam eos? Excepturi, distinctio quas dolores sint tempora culpa repudiandae aut fugiat ad natus earum assumenda fuga ut facilis. Distinctio, rem, nam laudantium obcaecati deserunt cumque repudiandae explicabo nesciunt vero ratione reprehenderit adipisci maxime totam omnis impedit esse quia dolorem? Iure accusamus laudantium inventore aut vitae maiores magnam deserunt, modi a optio facere temporibus distinctio molestias odio necessitatibus perspiciatis expedita rerum earum. Ut sapiente pariatur in maxime nemo, dicta laboriosam, provident modi repellat aperiam nulla id ad eius dolor accusamus cum tempora porro quae velit repudiandae iste? Odio ex possimus nihil accusamus ipsa officia temporibus modi sunt exercitationem aperiam reprehenderit, natus necessitatibus doloribus corporis, aut amet consequuntur ratione ea molestias placeat? Delectus enim illum quod dolorem quia harum vel commodi voluptas, repellat maxime tempore doloremque est! Veritatis, eligendi! Dolorum?
    </>
  )
}

export default page
```

```jsx
offset: ["start end", "end end"]:

"start end": Yeh define karta hai ki scroll tracking(animation) tab shuru hoga jab target element ka start point viewport ke end (bottom) se match ho jaye.
"end end": Yeh define karta hai ki scroll tracking(animation) tab khatam hoga jab target element ka end point viewport ke end (bottom) se match ho jaye. 

use ev formula first element and then viewport 
```


Sure! Chalo, is code ko samajhte hain step by step. Yeh example Framer Motion ka istemal karta hai, jisse hum scrolling ke dauran animation create kar sakte hain.

### Code Explanation

1. **Imports**: 
   - `useRef` aur `useEffect` hooks ko React se import kiya gaya hai.
   - `motion`, `useScroll`, aur `useTransform` ko Framer Motion se import kiya gaya hai. Inka istemal animation aur scroll behavior ke liye hota hai.

2. **Component Definition**:
   ```jsx
   function page() {
       const targetref = useRef();
   ```

   - Yahan `page` naam ka functional component banaya gaya hai. `useRef` hook ka istemal karke `targetref` naam ka ek reference create kiya gaya hai. Yeh reference ek HTML element ko point karega.

3. **Scroll and Transform Setup**:
   ```jsx
   var { scrollYProgress } = useScroll({
       target: targetref,
       offset: ["end center", "end start"],
   });
   ```

   - `useScroll` hook ka istemal kiya gaya hai jo scroll position track karega. `target` mein humne `targetref` diya hai, iska matlab hai ki yeh scroll event tab hi trigger hoga jab yeh reference element viewport mein aaye.
   - `offset` property define karti hai ki animation kab shuru hoga. Yahan `"end center"` se `"end start"` tak ka range diya gaya hai.

4. **Transform Value Calculation**:
   ```jsx
   const val = useTransform(scrollYProgress, [0, 1], [0, 50]);
   ```

   - `useTransform` hook ka istemal scroll progress value ko transform karne ke liye hota hai. Yahan jab `scrollYProgress` 0 se 1 ke beech hoga, tab `val` 0 se 50 ke beech interpolate karega. Iska matlab hai ki animation ki position 0 se 50 pixels tak move karegi jaise jaise user scroll karega.

5. **Effect Hook**:
   ```jsx
   useEffect(() => {
       console.log(targetref.current); // Check if the ref is correctly targeting the element
   }, []);
   ```

   - `useEffect` ka istemal kiya gaya hai taaki ensure kiya ja sake ki reference sahi hai. Isme `console.log` use karke hum dekh sakte hain ki kya `targetref` sahi element ko target kar raha hai.

6. **Render JSX**:
   ```jsx
   return (
       <>
           <div className='w-full h-[50vh] bg-blue-600 pt-64 overflow-hidden' ref={targetref}>
               a
           </div>
           <motion.div className='bg-red-600 w-1/5 items-center' style={{ x: val }} transition={{ duration: 4 }}>
               hello
           </motion.div>
           <p>
               {/* Bahut saari content... */}
           </p>
       </>
   );
   ```

   - Yeh part JSX return karta hai. 
   - Pehle `div` ko `ref` diya gaya hai jisse scroll animation start hoga jab yeh viewport mein aaye.
   - Dusra `motion.div` hai jismein `style` prop ke zariye `x: val` diya gaya hai. Isse jab scroll hota hai, to yeh red box left ya right move karega.

### Flow of Animation

1. **Scrolling**: Jab user scroll karega, `scrollYProgress` update hoga.
2. **Transform**: `scrollYProgress` ki value ke according, `val` change hoga jo `motion.div` ke `x` property ko affect karega.
3. **Viewport Check**: Jab target reference viewport mein aayega, tab hi animation shuru hoga.

### Conclusion

Is tareeke se aap `useScroll` aur `useTransform` ka istemal karke scrolling animations create kar sakte hain. Yeh approach aapko control deta hai ki kab aur kaise animations trigger hongi, jo ki user experience ko enhance karne mein madadgar hai. Agar aapko is code ya concept mein koi specific part mein dikkat hai, to pooch sakte hain!
