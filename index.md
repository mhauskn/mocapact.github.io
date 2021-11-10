---
title: 'DescribeWorld: One-Shot Learning of Complex Tasks with Hierarchical Latent Language' layout: default
---

<style>thead { display: none; }</style>


<p class="cover" align="center"> <img src="assets/front_cartoon.jpg" width="90%" /> </p>

## Abstract

> Humans have the capability, aided by the expressive, compositional nature of language, to learn quickly by
demonstration. Given very few examples, they can generalize known concepts in order to infer novel goals then accomplish
them in novel settings. Here we introduce DescribeWorld, a task environment designed to test this sort of generalization
skill in grounded autonomous agents. We task agents first with inferring an unseen goal from a single demonstration in a
2D Minecraft-style grid world, then with accomplishing the goal in a new setting without access to ground truth task
descriptions. Goals are linguistically and procedurally composed of learnt concepts.

> Inspired by how humans leverage language as a powerful tool for generalization, we propose a neural agent infused with
hierarchical latent language--both at the level of goal inference and subgoal planning-- that learns to perform
grounded, one-shot demonstration following. We find that agents that thus reparametrize the task into a policy search
through text space are better equipped to perform the challenge, particularly when faced with tests of systematic
generalization.

## DescribeWorld: A Demonstration/Description-Following Environment for Tasks with Complex Subdependencies

This work tests whether artificial agents can learn new complex tasks just from a single demonstration.
This task is difficult for an agent because this task involves many subtasks that require interacting with various domain objects in order to acquire tools and ingredients in the right order. Moreover, the agent _can't see the text description of the task_, so it must learn what the goal is from demonstration state transitions alone.


For example, we
show a bot a demonstration of agent completing the task `build a house then go to the lumbershop`, then test whether the
bot can accomplish the same task in a new gridworld environment:

<table>
<tr> 
<td><img src="assets/task_demos/house_lumber_agent.png" alt="house_lumber_agent" data-alt="assets/task_demos/house_lumber_agent.gif" /></td>
<td><img src="assets/task_demos/house_lumber_bot.png" alt="house_lumber_bot" data-alt="assets/task_demos/house_lumber_bot.gif"  /></td>
</tr>
</table>




In order to test this, we construct a gridworld environment containing many subtasks with interrelated task dependencies.
That way, an agent can learn to reuse subtasks in order to accomplish unseen tasks within realistic expectations.

<p class="cover" align="center"> <img src="assets/example_unroll.png" alt="example_unroll" data-alt="assets/example_unroll.gif"  /> </p>


### Task Categories

<table>
  <tr>
    <td>Navigating to Landmarks</td>
    <td>Crafting Items</td>
  </tr>
<tr>
<td><img src="assets/task_demos/tree_then_diamond.png" alt="tree_then_diamond" data-alt="assets/task_demos/tree_then_diamond.gif"  /></td>
<td><img src="assets/task_demos/craft_necklace.png" alt="craft_necklace" data-alt="assets/task_demos/craft_necklace.gif" /></td>
</tr>
  <tr> <td>Building Structures</td> <td>Placing Terrains</td></tr>
<tr>
<td><img src="assets/task_demos/build_fence.png" alt="build_fence" data-alt="assets/task_demos/build_fence.gif" /></td>
<td><img src="assets/task_demos/dirt_water.png" alt="dirt_water" data-alt="assets/task_demos/dirt_water.gif"  /></td>
</tr>
<tr>
<td>Covering Terrains</td>
<td>Clearing Items</td>
</tr>
<tr>
<td><img src="assets/task_demos/silver_cover_lava.png" alt="silver_cover_lava" data-alt="assets/task_demos/silver_cover_lava.gif" /></td>
<td><img src="assets/task_demos/clear_grass_chicken.png" alt="clear_grass_chicken" data-alt="assets/task_demos/clear_grass_chicken.gif" /></td>
</tr>
<tr>
<th colspan="2">
We also add environmental constraints, like penalties for walking on a terrain or rewards for walking on another.
</th>
</tr>
<tr>
<td><img src="assets/task_demos/stone_then_furnace.png" alt="stone_then_furnace" data-alt="assets/task_demos/stone_then_furnace.gif" /></td>
<td><img src="assets/task_demos/iron_cover_lava_pig_road.png" alt="iron_cover_lava_pig_road" data-alt="assets/task_demos/iron_cover_lava_pig_road.gif"  /></td>
</tr>
</table>

<script src="js/script.js"></script>


<!-- ![example_unroll](https://user-images.githubusercontent.com/93727661/140437262-908cd450-9d06-4126-a2ca-263b55063c79.gif) -->

<!-- ![task_categories.pdf](https://github.com/describeworld/describeworld.github.io/files/7479511/task_categories.pdf) -->

## Hierarchical Latent Language Policy Agent

<!-- ![HLLP_diagram.pdf](https://github.com/describeworld/describeworld.github.io/files/7479494/HLLP_diagram.pdf) -->

## Testing for Language-Aided Systematic Generalization

<!-- ![generalization_splits.pdf](https://github.com/describeworld/describeworld.github.io/files/7479497/generalization_splits.pdf) -->
