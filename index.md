---
title: 'DescribeWorld: One-Shot Learning of Complex Tasks with Hierarchical Latent Language' layout: default
---

<style>thead { display: none; }</style>

<p class="cover" align="center"> <img src="assets/front_cartoon.jpg" width="90%" /> </p>

## DescribeWorld

Humans have the capability, aided by the expressive, compositional nature of language, to learn quickly by
demonstration. Given very few examples, they can generalize known concepts in order to infer novel goals then accomplish
them in novel settings. Here we introduce DescribeWorld, a task environment designed to test this sort of generalization
skill in grounded autonomous agents. We task agents first with inferring an unseen goal from a single demonstration in a
2D Minecraft-style grid world, then with accomplishing the goal in a new setting without access to ground truth task
descriptions. Goals are linguistically and procedurally composed of learnt concepts.

Inspired by how humans leverage language as a powerful tool for generalization, we propose a neural agent infused with
hierarchical latent language--both at the level of goal inference and subgoal planning-- that learns to perform
grounded, one-shot demonstration following. We find that agents that thus reparametrize the task into a policy search
through text space are better equipped to perform the challenge, particularly when faced with tests of systematic
generalization.

## DescribeWorld: A Demonstration/Description-Following Environment for Tasks with Complex Subdependencies

This work tests whether artificial agents can learn new complex tasks just from a single demonstration. For example, we
show a bot a demonstration of agent completing the task `build a house then go to the lumbershop`, then test whether the
bot can accomplish the same task in a new gridworld environment.

<table>
<tr> 
<td><img src="assets/task_demos/house_lumber_agent.gif" /></td>
<td><img src="assets/task_demos/house_lumber_bot.gif"  /></td>
</tr>
</table>

In order to test this, we construct a gridworld environment containing many subtasks with interrelated task
dependencies.

<p class="cover" align="center"> <img src="assets/example_unroll.gif"  /> </p>

That way, we can create an inventory of many high-level tasks whose subdependencies overlap with each other.

### Task Categories

<table>
  <tr>
    <td>Navigation to Locations</td>
    <td>Crafting Items</td>
  </tr>
<tr>
<td><img src="assets/task_demos/tree_then_diamond.gif"  /></td>
<td><img src="assets/task_demos/build_fence.gif" /></td>
</tr>
  <tr> <td>Building Structures</td> <td>Placing Terrains</td></tr>
<tr>
<td>Covering Terrains</td>
<td>Clearing Items</td>
</tr>
</table>


<!-- ![example_unroll](https://user-images.githubusercontent.com/93727661/140437262-908cd450-9d06-4126-a2ca-263b55063c79.gif) -->

<!-- ![task_categories.pdf](https://github.com/describeworld/describeworld.github.io/files/7479511/task_categories.pdf) -->

## Hierarchical Latent Language Policy Agent

<!-- ![HLLP_diagram.pdf](https://github.com/describeworld/describeworld.github.io/files/7479494/HLLP_diagram.pdf) -->

## Testing for Language-Aided Systematic Generalization

<!-- ![generalization_splits.pdf](https://github.com/describeworld/describeworld.github.io/files/7479497/generalization_splits.pdf) -->
