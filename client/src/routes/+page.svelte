<script>
  import {
    Navbar,
    NavBrand,
    NavHamburger,
    NavUl,
    NavLi,
    Button,
    Card,
    Footer,
  } from "flowbite-svelte";
  import { FireSolid } from "flowbite-svelte-icons";
  import Problem from "../components/Problem.svelte";
</script>

<Navbar let:hidden let:toggle color="primary">
  <NavBrand href="/">
    <!-- <img src="/static/logo.png" class="me-3 h-6 sm:h-9" alt="Flowbite Logo" /> -->
    <span
      class="self-center whitespace-nowrap text-xl font-semibold dark:text-red-800"
      >LeetCode Pattern Detector</span
    >
  </NavBrand>
  <NavHamburger on:click={toggle} />
  <NavUl {hidden}>
    <NavLi href="/" active={true}>Home</NavLi>
    <NavLi href="/about">About</NavLi>
    <NavLi href="/patterns">Patterns</NavLi>
    <NavLi href="/contact">Contact</NavLi>
  </NavUl>
</Navbar>

<main class="flex-grow">
  <section class="hero bg-cover bg-center">
    <div class="container mx-auto text-center py-20">
      <h1 class="text-5xl font-bold mb-4">
        Welcome to LeetCode Pattern Detector
      </h1>
      <p class="text-xl mb-8">
        Solve LeetCode challenges more efficiently by detecting patterns.
      </p>
      <!-- <Button color="primary" href="/patterns">Get Started</Button> -->
    </div>
  </section>

  <section class="flex flex-grow justify-center">
    <Problem
      title="Two Sum"
      difficulty="Easy"
      description="Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target."
      likes={11779}
      link="https://leetcode.com/problems/two-sum/"
    />
  </section>
</main>

<!-- <Footer class="footer p-4 bg-gray-800 text-white text-center">
  <p>&copy; 2024. Developed by nhkhang</p>
</Footer> -->

<style>
  html,
  body {
    height: 100%;
    margin: 0;
  }
  body {
    display: flex;
    flex-direction: column;
    min-height: 100%;
  }
  main {
    flex-grow: 1;
  }

  footer {
    clear: both;
    position: relative;
    height: 200px;
    margin-top: -200px;
  }
</style>
