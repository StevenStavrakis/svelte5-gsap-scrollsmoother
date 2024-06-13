<script lang="ts">
  import "../app.css";
  import { navigating } from "$app/stores";
  import { ScrollSmoother } from "gsap/ScrollSmoother";
  import {ScrollTrigger} from "gsap/ScrollTrigger";
  import gsap from "gsap";

  let { children } = $props();

  gsap.registerPlugin(ScrollSmoother, ScrollTrigger);

  $effect(() => {
    // on first load, we need to create the smoother
      ScrollSmoother.create({
        wrapper: "#smooth-wrapper",
        content: "#smooth-content",
      });
  })

  $effect(() => {
    const smoother = ScrollSmoother.get();
    if ($navigating === null) {
      // When navigating is null, that means we are no longer navigating; the page has been loaded
      ScrollSmoother.refresh();
    } else {
      // when we start navigating, we scroll to the top otherwise we get some weird behavior
      if (!!smoother) {
      smoother.scrollTo(0)
      }
    }
  });
</script>

<div class="flex" id="smooth-wrapper">
  <div class="h-screen w-[200px] bg-slate-600 text-white p-8">
    <h2 class="text-xl font-bold">Menu</h2>
    <a class="block" href="/">Home</a>
    <a class="block" href="/second-page">Second page</a>
  </div>
  <div class="w-full" >
    <div id="smooth-content">
      {@render children()}
    </div>
  </div>
</div>
