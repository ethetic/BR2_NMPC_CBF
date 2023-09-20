# BlueRov2 - Unified MPC &amp; CBF
Videos of BlueRov2 Simulation, with Model Predictive Control for 6DOF Trajectory Tracking &amp; Control Barrier Functions for Collision Avoidance.
This is a companion of the Paper '[*PAPER NAME*]' authored by J. Close<sup>a</sup>, M. Van<sup>a</sup>, N. Nguyen<sup>a</sup>, S. McIlvanna<sup>a</sup>, Y. Sun<sup>a</sup>, K. Olayemi<sup>a</sup> and C. Wei<sup>b</sup><br/>
<sup>a</sup>School of Electronics, Electrical Engineering &amp; Computer Science, Queen's University Belfast, Northern Ireland <br/>
<sup>b</sup>School of Mechanical &amp; Aerospace Engineering, Queen's University Belfast, Northern Ireland

***

# Point Stabilisation Tasks (MPC *only*)
## 1 Axis Reference
In the following examples showcasing Model Predictive Control for Point Stabilisation, the target point is only defined in 1 Axis.
Due to the gravitational component, Z has Upwards &amp; Downwards versions for comparison. <br/>
#### Reference in X
<img src="https://github.com/ethetic/BR2_MPC_CBF/assets/119050148/09febfe9-a39d-4e02-8a5b-d15589123094" width="300" height="300">
<img src="https://github.com/ethetic/BR2_MPC_CBF/assets/119050148/11873f2d-bd5b-4835-91ad-c4f8bd7ade84" width="446" height="300">

#### Reference in Y
<img src="https://github.com/ethetic/BR2_MPC_CBF/assets/119050148/c7d066d7-5537-4270-8d4b-09c4927828d4" width="300" height="300">
<img src="https://github.com/ethetic/BR2_MPC_CBF/assets/119050148/e4235a9f-bb91-4ea6-9c3e-d67c327df342" width="446" height="300">

#### Reference in Z (Upwards)
<img src="https://github.com/ethetic/BR2_MPC_CBF/assets/119050148/cdf93839-e8c9-4b71-83d9-62d684605cc6" width="300" height="300">
<img src="https://github.com/ethetic/BR2_MPC_CBF/assets/119050148/0d4c67b7-cef3-4aeb-a282-273cfc4ec98c" width="446" height="300">

#### Reference in Z (Downwards)
<img src="https://github.com/ethetic/BR2_MPC_CBF/assets/119050148/a0d29b12-82b7-4ef8-8f72-7f06ff8b3fb0" width="300" height="300">
<img src="https://github.com/ethetic/BR2_MPC_CBF/assets/119050148/ab200926-a877-43b5-9a36-a72db6c2c01a" width="446" height="300">

## 2 Axis Reference
In the following examples showcasing Model Predictive Control for Point Stabilisation, the target point is defined in 2 Axis. 
This shows how the controller adapts when handling targets in multiple different DOF. Directly below is a good test for maintainining
depth during a horizontal translation, and the latter two examples in this section allow comparison between working with and against
gravity. <br/>
#### Reference in (X,Y)
<img src="https://github.com/ethetic/BR2_MPC_CBF/assets/119050148/f8c0d57f-b080-40d9-88d3-d348c323d2c0" width="300" height="300">
<img src="https://github.com/ethetic/BR2_MPC_CBF/assets/119050148/d4ebcd9a-2264-4f50-afb8-860b1920d983" width="446" height="300">

#### Reference in (X,Z) (Upwards)
<img src="https://github.com/ethetic/BR2_MPC_CBF/assets/119050148/d20205b7-fc1c-4aba-ab5c-88c7b3b4f73a" width="300" height="300">
<img src="https://github.com/ethetic/BR2_MPC_CBF/assets/119050148/7fbdf5b3-36b1-41d5-9813-6557fec7fe6d" width="446" height="300">

#### Reference in (Y,Z) (Downwards)
<img src="https://github.com/ethetic/BR2_MPC_CBF/assets/119050148/d46d2b37-d3d1-4c8d-96a1-ce337bed815c" width="300" height="300">
<img src="https://github.com/ethetic/BR2_MPC_CBF/assets/119050148/2869a5f1-5406-413b-929d-2720c8212fe1" width="446" height="300">

## 3 Axis Reference
In the following examples showcasing Model Predictive Control for Point Stabilisation, the target point is defined in 3 Axis. 
This shows how the controller adapts when handling targets in multiple different DOF. In the first example below, the Reference Angles 
are consistent and it is only moving in 3DOF (X,Y,Z). In the second example, all 6DOF are changed, giving it a rigorous test with multiple 
simultaneous variables. <br/>
#### Reference in (X,Y,Z) (Upwards)
<img src="https://github.com/ethetic/BR2_MPC_CBF/assets/119050148/3dddb427-4238-41f1-8ea0-3a83e28cfea8" width="300" height="300">
<img src="https://github.com/ethetic/BR2_MPC_CBF/assets/119050148/fb70a725-cb58-4459-b8c5-be81cc0bdd78" width="446" height="300">

#### Reference in 6DOF (Flip)
<img src="https://github.com/ethetic/BR2_MPC_CBF/assets/119050148/87b8f1ee-49d6-44bb-a577-d26ffb1eee77" width="300" height="300">
<img src="https://github.com/ethetic/BR2_MPC_CBF/assets/119050148/e177c86b-c56d-44c5-bc39-f812740ec8f5" width="446" height="300">

***

# Trajectory (Circle) Tracking Tasks (MPC *only*)
## Reference Circle Aligned
#### The BlueRov2 is lined up with the circular path that acts as a reference before the controller starts. <br/>
<img src="https://github.com/ethetic/BR2_MPC_CBF/assets/119050148/72cd1448-f88b-4a79-aab5-03885c5672e0" width="300" height="300">
<img src="https://github.com/ethetic/BR2_MPC_CBF/assets/119050148/ebd74132-6206-49c5-a078-7bf64b0321c6" width="446" height="300">

## Reference Circle Aligned (Above/Below)
The BlueRov2 is only lined up with the circular path, that acts as a reference, in (X,Y) before the controller starts. The circle
is then placed either Above or Below for comparison of gravitational effects. <br/>
#### Reference Circle placed Above
<img src="https://github.com/ethetic/BR2_MPC_CBF/assets/119050148/bc9191d4-342b-4f3f-b086-f5fe3187af6c" width="300" height="300">
<img src="https://github.com/ethetic/BR2_MPC_CBF/assets/119050148/61a6ec20-518f-475c-99e3-a2ec7efdae73" width="446" height="300">

#### Reference Circle placed Below
<img src="https://github.com/ethetic/BR2_MPC_CBF/assets/119050148/46e18050-77c5-4773-aafb-581d3052435e" width="300" height="300">
<img src="https://github.com/ethetic/BR2_MPC_CBF/assets/119050148/bcc25ac3-34ec-48c4-834b-9c42a78c6d18" width="446" height="300">

## Reference Circle Offset (Above/Below)
The BlueRov2 is not lined up with the circular path that acts as a reference before the controller starts. The starting point of the
circle is offset in (X,Y) and then placed either Above or Below for comparison of gravitational effects. <br/>
#### Reference Circle Offset and placed Above
<img src="https://github.com/ethetic/BR2_MPC_CBF/assets/119050148/6499da0d-c2e8-4d4b-8b3d-cc7111a6ef44" width="300" height="300">
<img src="https://github.com/ethetic/BR2_MPC_CBF/assets/119050148/a4d037a7-229d-4546-8b1b-8e1348318d15" width="446" height="300">

#### Reference Circle Offset and placed Below
<img src="https://github.com/ethetic/BR2_MPC_CBF/assets/119050148/6220948b-ff1d-4f3a-8b73-5ec45c831b4d" width="300" height="300">
<img src="https://github.com/ethetic/BR2_MPC_CBF/assets/119050148/acd99da1-2a61-4f72-8001-439d06f65b76" width="446" height="300">

***

# Point Stabilisation & Collision Avoidance Tasks (MPC *and* CBF)
## Static Obstacle Avoidance
Introducing a single static obstacle demonstrates how the CBF acts as a safety factor to avoid collision. The CBF
ensures that a radius of safety around both the BlueRov2 and the Obstacle never cross, which can be observed. <br/>
<img src="https://github.com/ethetic/BR2_MPC_CBF/assets/119050148/fb013107-e2c2-4306-8a03-a84241b7f5b0" width="300" height="300">
<img src="https://github.com/ethetic/BR2_MPC_CBF/assets/119050148/90ab5527-5456-48c3-95df-90e1825d4681" width="446" height="300">

## Moving Obstacle Avoidance
Since the controller is contstantly provided live data on the location and size of an obstacle, it can adapt and respond to obstacles
that aren't in a fixed location and are moving around the environment. <br/>
<img src="https://github.com/ethetic/BR2_MPC_CBF/assets/119050148/d417fbac-4757-4342-b989-3cb711a37131" width="300" height="300">
<img src="https://github.com/ethetic/BR2_MPC_CBF/assets/119050148/2974d408-a740-44ba-b7fd-792413d04ea3" width="446" height="300">

## Static &amp; Moving Obstacle Avoidance
Assuming that the BlueRov2 can detect and track any obstacles within range using SONAR or HD Camera footage, the CBF can enable multiple obstacles - 
both static and moving - to be avoided during the task. An advantageous feature for dynamic ocean envrironments. <br/>
<img src="https://github.com/ethetic/BR2_MPC_CBF/assets/119050148/2f21eba5-3790-4371-9728-7e448c7de055" width="300" height="300">
<img src="https://github.com/ethetic/BR2_MPC_CBF/assets/119050148/e441624b-8d86-4825-b421-ae7b76276e6b" width="446" height="300">

***

# Trajectory (Circle) Tracking & Collision Avoidance Tasks (MPC *and* CBF)
## Static &amp; Moving Obstacle Avoidance

Carrying on from the previous example with multiple static and moving obstacles, it is observed below that the same functionality
is available for path tracking tasks. <br/>
<img src="https://github.com/ethetic/BR2_MPC_CBF/assets/119050148/0c3aa58d-eaca-408e-a38b-fd23031f9020" width="300" height="300">
<img src="https://github.com/ethetic/BR2_MPC_CBF/assets/119050148/8d2c9d9d-0120-4cf3-b6d9-3a03256ed053" width="550" height="300">
