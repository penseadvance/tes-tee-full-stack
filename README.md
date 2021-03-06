<p align="center">
    <img src="/assets/logo/logo.png" alt="Tes-tee logo">
</p>

# Tes-tee Full Stack
An internationally acclaimed (fake) shirt brand for developers. A collection of beautiful shirts
 designed by (fake) artists around the world. Also a (real) test for full stack developers aiming
  for a position at Advance Comunicação, a super real full-service agency based in Fortaleza, Ceará.

## What's this test about?
We created a fake brand of shirts called Tes-tee, and we need you (yes, you!) to create a simple
 product listing page for our diverse collection of designs. You can take a look at said designs
  at the `assets` folder. They are absolutely lovely and totally not color swaps of the same shirt.

### I was told to take this test, what now?
Then you may proceed to the next section to learn what to do. Good luck!

### I just found this test around the internet, and it seems weird and kinda funny?
Not sure this is a question, but if you're still reading this, you're probably an awesome developer
 with great sense of humor, and at Advance we value those of you a lot. You can check us out at 
  [advance.com.br](https://advance.com.br). We have a job board on our home page, but you can
   always send us your resume over [Starhunters](https://starhunters.advance.com.br), even if an
    open developer position isn't listed on our website.

Not looking for a job right now, but you still want to learn something new? We encourage you to
 take this test. It was tailored to test your knowledge in various aspects of CSS and JavaScript
  programming, from basic logic to advanced coding patterns. If you do, please send us a link to
   your finished project, we'll be more than happy to give you feedback :)
   
## The task
![Tes-tee screenshot](/assets/screenshot.png)

You need to create a ~~complete ecommerce solution~~ simple responsive product listing page to our
 new in-house brand, Tes-tee. Tes-tee is known for selling awesome shirts that cost $19 each. 
  The test consists of:
 
 - [ ] A single page where our shirts will be listed
 - [ ] A super simple menu that slides from the side of the user's screen
 - [ ] A cart view that slides from the other side of the screen and show which products the user
  picked from the listing
 - [ ] A simple backend service made in **PHP** that manages the user's cart
  
You won't create any code related to checkout or payment, which means that the "Proceed to checkout" 
button on the frontend shouldn't do anything.
 
You can use an interactive prototype of the frontend on Figma
 [clicking here](https://www.figma.com/proto/wFzq47HoFPSWSq8tdebaNY/Tes-tee). There's a link at the 
  bottom of the side menu that switches between desktop and mobile prototypes.
  
You can view the complete user interface and assets on Figma
 [clicking here](https://www.figma.com/file/wFzq47HoFPSWSq8tdebaNY/Tes-tee). It's the actual file
  that powers the prototype above. You don't need a Figma account to view it, but we highly
   recommend that you do create one. By doing so, you can make a copy of this file and interact
    with it, which makes it easier to analyze fonts, colors and spacing between elements. Figma
     is free for personal projects, and super easy to use.
     
Although you can easily export assets from the Figma file above, we already did this for you. All
 shirt images and SVG icons that you'll need can be found on the `assets` folder on this repository.
   
The interface uses a single font family, Cabin. We used the Regular and Bold variants. You can
 fetch it from [Google Fonts](https://fonts.google.com/specimen/Cabin).
 
All interface parts must be responsive. It doesn't matter if your CSS is mobile or desktop-first, 
 pick whatever feels right to you.
  
### The listing page
This is the only page you need to create. It shows a simple listing of our shirts, and provides a
 way for users to find the shirt they want and add it to their cart. Here's what it needs to do:
 
- [ ] It should list shirts
    - You don't need to fetch products from any API or service. Just create an array/object
     containing all shirts. Shirts have only two properties: color and available sizes. You can
      create any number of shirts you want, with any combination of colors and available sizes.
- [ ] It should let users search for shirts
    - Use the search bar at the top of the screen to filter shirts by name. On mobile, the search
     bar is initially hidden, but should appear when the users click on the search icon.
- [ ] It should let users filter shirts by color
    - The first button (the one with a rainbow) should show all colors. The others should filter
     shirts by its respective color.
- [ ] It should let users filter shirts by available sizes
    - If, for instance, the user click on the XL button, show only shirts which have XL as an
     available size.
- [ ] It should let users add a shirt to their cart
    - When clicked, a modal window should open and let users pick a size and a quantity. The user
     should see a live preview of the price based on the quantity they picked. All shirts cost
      $19 each. After adding, the cart window should open.
- [ ] It should allow the user to open the side menu, and the cart window
    - Check the Figma prototype to see how they work.

### The menu
This part is super simple. It's simply a menu that slides from the left of the user's screen and
 shows a list of links. There's no real functionality here, this menu is only decorative.
 
 > NOTE: the Figma prototype has a link that switches between Desktop and Mobile designs. You
> **should not** implement this. This is simply a way to navigate between Figma prototypes
> seamlessly.

### The cart
The cart is a window that slides from the right side of the user's screen, just like the menu. It
 lists shirts that the user picked. It lets the user update quantities and shows them the grand
  total in real time. Here's what it needs to do:
  
- [ ] It should start empty
    - This can be seen on Figma by clicking on the "Empty cart" button.
- [ ] It should list shirts the user picked from the listing
    - If the user picked the same shirt with the same size more than once, it should only update the
     shirt's quantity. Each shirt size shows as a separate shirt.
- [ ] It should let users update quantities by clicking on the + and - icons
    - If the quantity reaches zero, the shirt should be removed from the cart.
- [ ] It should let users empty their cart
    - Simply remove all shirts when clicked.
- [ ] It should show the grand total
    - This should update in real time. Shipping is a fixed $12. Remember: all shirts cost $19 each.

Also, remember that the Checkout button shouldn't do anything. It's simply decorative.

### The backend
The backend should manage the user's cart by exposing a restful API that the frontend can use.
The API should manage the following:
- [ ] It should list all items in the user's cart
    - **Super important note**: you don't need to create a new cart for each visitor. We want this 
    test to be simple, after all. There must be a single cart on your system, and all visitors will
    share it.
- [ ] It should let the user add shirts to their cart
- [ ] It should let the user remove shirts from their cart
- [ ] It should let the user update the quantity of each shirt on the cart individually
    - Remember: If the quantity reaches zero, the shirt should be removed from the cart.
- [ ] It should differentiate shirts with different properties as separate items
    - For instance, a blue XL shirt and a blue M shirt should be considered two different products.
    This means that the user can update their quantities independently of each other.
- [ ] It should let the user empty their cart when clicking "Empty cart" on the frontend

However, we want this API to as simple as possible. This means that you **shouldn't** do the following:
- [ ] You **should not** implement an authentication system
    - Since all visitors will see and share the same cart, there's no need to worry about who is using
    your store. This also makes this test way simpler.
- [ ] You **should not** implement a checkout process
- [ ] You **should not** implement a payment system
- [ ] You **should not** implement an account management system
  
## What we expect
On the frontend, you are free to use whatever technologies you want, as long as you create a website. 
However, we recommend frameworks like React, Vue, Svelte, etc. As of April 2020, we use React a lot at
Advance, particularly the Next.js framework, which is built on top of React. Since this test
doesn't need routing, if you're in doubt about which technology to use, we recommend using
React with [Create React App](https://github.com/facebook/create-react-app).

On the backend, we expect you to use PHP. However, you are also free to use whatever framework you want,
or not use one, if you're comfortable with this. Internally, when we feel the need to have an API, we
generally use Laravel. It's easy, highly customizable, and it provides a myriad of tools that help us
when developing new services. We recommend Laravel, but feel free to use any tools that you want, as
long as you use PHP.

Even if you don't want to use Laravel, we still recommend you to use Laravel's Homestead, which is a
pre-configured Vagrant image that streamlines the process of creating a complete Linux VM to develop on.
You can read more on [Homestead's documentation](https://laravel.com/docs/homestead).
    
We expect you to create concise and optimized code, with as few dependencies as possible, and
 respecting the design we created on Figma. We also expect this website to be responsive.
 
We'll analyze the following aspects of your test:
- General logic and problem solving abilities
- Code formatting and conciseness
- Use of recommended code patterns
- Use of current and new CSS, JavaScript and PHP technologies
- Use of native PHP and JS APIs instead of third-party packages when viable
- Use of currently supported PHP versions
- Performance optimizations
- Code and asset size optimizations
- Quantity of fatal, disrupting bugs
- Quality of both mobile and desktop design implementations
- Attention to details of the provided design
- Use of version control (in other words, use of git)

After finishing your test, create a README file like this one telling us how to build and/or run
 your website, commit your code to git and create a public repository with it here on GitHub.
 
If you received an invitation to take this test, respond our invitational email with the link to
 your repository.
  
If you're taking this test on your own, you can 
[create an issue](https://github.com/penseadvance/tes-tee-full-stack/issues/new) on this repository with a link
to your test repository. We'll gladly give feedback to you as soon as we can :)
 
 ## Any questions?
 Feel free to [create an issue](https://github.com/penseadvance/tes-tee-full-stack/issues/new) if you have
  any questions related to this test. Questions related your invitation should be made responding
   the email we sent you. Questions related to job openings should be made using our contact form at
    [advance.com.br](https://advance.com.br).
