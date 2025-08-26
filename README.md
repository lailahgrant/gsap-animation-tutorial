## Web Animations Full Course 2025 _ Build an Awwwards Website _ Master GSAP in Two Hours by Adrian (JavaScript Mastery)

> Web Animations enable web developers build `experiences`.

<div align="center">
    <a href="https://gsap-crash-course.vercel.app" target="_blank">
      <img src="public/preview.png" alt="Project Banner">
    </a>
  <h3 align="center">GSAP Workshop (Starter)</h3>
</div>

##  <br /> 📋 <a name="table">Table of Contents</a>

- ✨ [Introduction](#introduction)
- ⚙️ [Tech Stack](#tech-stack)
-    [Why GSAP](#why-gsap)
- 🔋  [Features](#features)
- 🚀 [Quick Start](#quick-start)
- ⚙️ [How to Animate using GSAP](#animate-using-gsap)

##  <br /> <a name="introduction">✨ Introduction</a>

Simple GSAP workshop showcasing various primary animations. GSAP (GreenSock Animation Platform) is a framework-agnostic JavaScript animation library used to create fluid and engaging animations.


##  <br /> <a name="tech-stack">⚙️ Tech Stack</a>

#### To Use
- [x] GSAP
- [x] React
- [x] Vite

- [**React**](https://react.dev/reference/react) is a popular JavaScript library for building user interfaces, particularly single-page applications where data changes over time. React's component-based architecture allows developers to create reusable UI components, making development more efficient and the codebase easier to maintain. 

- [**GSAP**](https://gsap.com/resources/) (GreenSock Animation Platform) is a powerful JavaScript library for creating high-performance animations. It excels in animating HTML elements with smoothness and precision, making it ideal for enhancing user interfaces and web experiences. GSAP's robust API allows developers to create complex animations easily, leveraging timelines and plugins for advanced control and customization. Its efficient rendering engine ensures animations run smoothly across different browsers and devices, providing a seamless user experience.

- [**Vite**](https://vitejs.dev/guide/) is a modern frontend build tool known for fast ES Module imports, efficient bundling, and quick development server startup times. It supports frameworks like Vue.js and React, optimizing workflow and performance compared to traditional bundlers.


## <br /> <a name="why-gsap">✨ Why GSAP?</a>
- [x] What is GSAP?
- [x] Why is it so powerful?
- [x] Pro tips, tricks
- [x] Common mistakes
- [x] How to integrate GSAP with Reactjs, Vuejs, Nextjs or any other frontend framework

[Ultimate GSAP Animations Course](https://www.jsmastery.pro)


### GSAP Basics
- [x] How to animate elements using `from()` `to()` `fromTo()` methods
- [x] How to control animations with `ScrollTrigger() `
- [x] How to **stagger animations** for maximum visual impact
- [x] How to animate text using `SplitText` plugin
- [x] How to sequence animations one after another with `gsap.timeline()`


## <br /> <a name="features">🔋 Features</a>
👉 **SplitText Animations**: Create impactful text reveals using GSAP’s SplitText for dynamic intros and section highlights.

👉 **ScrollTrigger Effects**: Power scroll-based animations and timeline control with GSAP’s ScrollTrigger.

👉 **Parallax Scrolling**: Add immersive depth with smooth parallax effects that respond to user scroll.

👉 **Pinned Sections**: Lock sections in view while animating content for engaging scroll experiences.

👉 **Scroll-Synced Video Playback**: Sync video progress with scroll position for cinematic storytelling.

👉 **Image Masking Effects**: Use scroll-triggered pins and masks for visually striking image transitions.

👉 **Custom Carousel**: Build a fully customized carousel with multiple navigation options and animated slides.

👉 **Seamless Timeline Animations**: Craft smooth animation timelines that span across multiple sections.

👉 **Responsive Design**: Ensure fluid UI and adaptive GSAP animations across all screen sizes.

And many more, including enhanced security and optimized video performance!


## <br /> <a name="quick-start">🚀 Quick Start</a>


Follow these steps to set up the project locally on your machine.


<br/>**Prerequisites**


Make sure you have the following installed on your machine:


- [Git](https://git-scm.com/)
- [Node.js](https://nodejs.org/en)
- [npm](https://www.npmjs.com/) (Node Package Manager)

<br/>**Installation**

Let's install the project dependencies, from your terminal, run:

```bash
npm install
```

<br/>**Running the Project**

Installation will take a minute or two, but once that's done, you should be able to run the following command:

```bash
npm run dev
```

Open [`http://localhost:5173`](http://localhost:5173) in your browser to view the project.


<br/>**Install GSAP**

Use the following command to start adding the **GSAP animations**:

```bash
npm install gsap @gsap/react
```

##  <br /> <a name="animate-using-gsap">⚙️ How to Animate using GSAP</a>

**Navigate to** `src` `pages` `GsapTo.jsx`
- Import the `useGSAP` hook.
- Import the `useGSAP` from `"@gsap/react"`
- import `gsap` from `"gsap"`;
- Define a callback function of `useGSAP` and pass the dependence array `[]`.
- Use `useGSAP` to animate any element we want.

```jsx
import { useGSAP } from "@gsap/react";
import gsap from "gsap";
const GsapTo = () => {
  // TODO: Implement the gsap.to() method

  useGSAP(() => {
    // gsap.to("#blue-box", { x: 300, duration: 2 });
    gsap.to('#blue-box', { x: 250, repeat: -1, yoyo: true, rotation: 360, duration: 2, ease: 'elastic' });
  }, []);

```


**Gsapfrom**

```jsx
import { useGSAP } from "@gsap/react";
import gsap from "gsap";

const GsapFrom = () => {
  // TODO: Implement the gsap.from() method
  useGSAP(() => {
    gsap.from('#green-box', {
      x: 250,
      repeat: -1,
      yoyo: true,
      rotation: 360,
      duration: 2,
      ease: 'power1.inOut'
    })
  }, []);
```

**GsapFromTo**

```jsx
import { useGSAP } from "@gsap/react";
import gsap from "gsap";

const GsapFromTo = () => {
  // TODO: Implement the gsap.fromTo() method
  useGSAP(() => {
    gsap.fromTo('#red-box', {
      x: 0,
      rotation: 0,
      borderRadius: '0%'
    },
      {
        x: 250,
        repeat: -1,
        yoyo: true,
        borderRadius: '100%',
        rotation: 360,
        duration: 2,
        ease: 'bounce.out'
      }
    )
  }, []);
```

> The 3 base GSAP animations are `GsapTo` *`to()`*  `GsapFrom` *`from()`* and `GsapFromTo` *`fromTo()`*


**GSAP Timeline**
`timeline()`

```jsx
import { useGSAP } from "@gsap/react";
import gsap from "gsap";
const GsapTimeline = () => {
  // TODO: Implement the gsap timeline
  const timeline = gsap.timeline({
    repeat: -1,
    repeatDelay: 1,
    yoyo: true
  });

  useGSAP(() => {
    timeline.to('#yellow-box', {
      x: 250,
      rotation: 360,
      borderRadius: '100%',
      duration: 2,
      ease: 'back.inOut'
    })

    timeline.to('#yellow-box', {
      y: 250,
      scale: 2,
      rotation: 360,
      borderRadius: '100%',
      duration: 2,
      ease: 'back.inOut'
    })

    timeline.to('#yellow-box', {
      x: 500,
      y: 0,
      scale: 1,
      rotation: 360,
      borderRadius: '8px',
      duration: 2,
      ease: 'back.inOut'
    })

  }, []);

  return (
    <main>
      <h1>GsapTimeline</h1>

      <p className="mt-5 text-gray-500">
        The <code>gsap.timeline()</code> method is used to create a timeline
        instance that can be used to manage multiple animations.
      </p>

      <div className="mt-20 space-y-10">
        <button onClick={() => {
          if (timeline.paused()) {
            timeline.play();
          } else {
            timeline.pause();
          }
        }}>Play/Pause</button>

        <div id="yellow-box" className="w-20 h-20 bg-yellow-500 rounded-lg" />
      </div>
    </main>
  );
};

export default GsapTimeline;
```

**GSAPStagger**
- [x] Stagger is a `property` you can apply to any animation.
- Use `gsap.to()` to apply animation
- [x] apply a stagger property to animate one object at a time. `stagger: 0.5`
- [x] apply *more stagger properties* by defining stagger as an **`object`**. 
- [ ] You can pass the following properties to the stagger object:-
  - [x] `amount` : amount of time to stagger the animation between each element. `amount: 1.5`
  - [x] `grid` : selects the number of rows and columns in a grid, `grid: [2, 1]`
  - [x] `axis` : choose the axis along the stagger animation, `axis: 'y'`
  - [x] `ease` : type of animation, `ease: 'circ.inOut'`
  - [x] `from`: starting position of the staggered animation. `from: 'center'` - the centered elements stagger first

```jsx
import { useGSAP } from "@gsap/react";
import gsap from "gsap";
const GsapStagger = () => {
  // TODO: Implement the gsap.stagger() method

  useGSAP(() => {
    //stagger is a property used in anuy animation
    // use .to()
    gsap.to('.stagger-box', {
      y: 250,
      rotation: 350,
      borderRadius: '100%',
      repeat: -1,
      yoyo: true,
      /*apply a stagger property to animate one object at a time
      stagger: 0.5*/

      //apply more stagger properties by defining stagger as an object
      stagger: {
        amount: 1.5,
        grid: [2, 1],
        axis: 'y',
        ease: 'circ.inOut',
        from: 'center'
      }
    })
  }, []);



  return (
    <main>
      <h1>GsapStagger</h1>

      <div className="mt-20">
        <div className="flex gap-5">
          <div className="w-20 h-20 bg-indigo-200 rounded-lg stagger-box" />
          <div className="w-20 h-20 bg-indigo-300 rounded-lg stagger-box" />
          <div className="w-20 h-20 bg-indigo-400 rounded-lg stagger-box" />
          <div className="w-20 h-20 bg-indigo-500 rounded-lg stagger-box" />
          <div className="w-20 h-20 bg-indigo-600 rounded-lg stagger-box" />
          <div className="w-20 h-20 bg-indigo-700 rounded-lg stagger-box" />
          <div className="w-20 h-20 bg-indigo-800 rounded-lg stagger-box" />
        </div>
      </div>
    </main>
  );
};

export default GsapStagger;

```

**GSAPScrollTrigger**

> - Gsap Scroll Trigger is a plugin that allows you to create animations that are triggered by the scroll position of the page.

- Need to import it from gsap. `import {ScrollTrigger} from "gsap/all"`
- Register the plugin to make it work. `gsap.registerPlugin(ScrollTrigger)`
- With `triggers`, you also have to define a **`reference`**. 
  - `const scrollRef = useRef();` -  This is **Reactjs** related and *NOT* **Gsap**. `import { useRef } from "react";`
- Attach the `scrollRef` to the _div_ with the 2 boxes.
  - `<div className="mt-20 w-full h-screen" ref={scrollRef}>`
- Apply `scrollTrigger` properties to the `.to()`
- `start` : defines the start of the animation. `start: 'position  viewport'`
- `scrub` : makes animation smooth. `scrub: true`

```jsx
import { useGSAP } from "@gsap/react";
import gsap from "gsap";
import { ScrollTrigger } from "gsap/all";
import { useRef } from "react";

gsap.registerPlugin(ScrollTrigger)

const GsapScrollTrigger = () => {
  const scrollRef = useRef();
  // TODO: Implement the gsap scroll trigger

  useGSAP(() => {
    //get access to the boxes
    //get the children using a react route
    const boxes = gsap.utils.toArray(scrollRef.current.children);

    //apply a property for each box
    boxes.forEach((box) => {
      gsap.to(box, {
        //x: 150,
        //since we are mapping over the boxes, can apply math to each box
        x: 150 * (boxes.indexOf(box) + 5),
        rotation: 360,
        borderRadius: '100%',
        scale: 1.5,
        scrollTrigger: {
          trigger: box,
          start: 'bottom bottom',
          end: 'top 10%',
          scrub: true,
          ease: 'power1.inOut'
        }
      })
    })

  }, { scope: scrollRef });

  return (
    <main>
      <h1>GsapScrollTrigger</h1>

      <p className="mt-5 text-gray-500">
        Gsap Scroll Trigger is a plugin that allows you to create animations
        that are triggered by the scroll position of the page.
      </p>

      <p className="mt-5 text-gray-500">
        With ScrollTrigger, you can define various actions to be triggered at
        specific scroll points, such as starting or ending an animation,
        scrubbing through animations as the user scrolls, pinning elements to
        the screen, and more.{" "}
      </p>

      <p className="mt-5 text-gray-500">
        Read more about the{" "}
        <a
          href="https://gsap.com/docs/v3/Plugins/ScrollTrigger/"
          target="_blank"
          rel="noreferrer noopener nofollow"
        >
          gsap scroll trigger
        </a>{" "}
        method.
      </p>

      <div className="w-full h-[70vh] flex justify-center items-center flex-col">
        <p className="text-center text-gray-500">
          Scroll down to see the animation
        </p>

        <svg
          className="animate-bounce mt-5"
          xmlns="http://www.w3.org/2000/svg"
          width="24"
          height="24"
          viewBox="0 0 24 24"
          fill="none"
          stroke="blue"
          strokeWidth="2"
          strokeLinecap="round"
          strokeLinejoin="round"
        >
          <path d="M12 19V5" />
          <path d="M5 12l7 7 7-7" />
        </svg>
      </div>

      <div className="mt-20 w-full h-screen" ref={scrollRef}>
        <div
          id="scroll-pink"
          className="scroll-box w-20 h-20 rounded-lg bg-pink-500"
        />
        <div
          id="scroll-orange"
          className="scroll-box w-20 h-20 rounded-lg bg-orange-500"
        />
      </div>
    </main>
  );
};

export default GsapScrollTrigger;
```