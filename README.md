# BlueRov2 - Unified NMPC &amp; CBF
Videos of BlueRov2 Simulation, with Nonlinear Model Predictive Control for 6DOF Trajectory Tracking &amp; Control Barrier Functions for Collision Avoidance.
This is a companion of the Paper '*A Unified NMPC-CBF Approach to Kino-Dynamic,
Collision-Avoidant Trajectory Tracking of Autonomous Underwater
Vehicles*' authored by J. Close<sup>a</sup>, M. Van<sup>a</sup>, N. Nguyen<sup>a</sup>, S. McIlvanna<sup>a</sup>, Y. Sun<sup>a</sup>, K. Olayemi<sup>a</sup> and C. Wei<sup>b</sup><br/>
<sup>a</sup>School of Electronics, Electrical Engineering &amp; Computer Science, Queen's University Belfast, Northern Ireland <br/>
<sup>b</sup>School of Mechanical &amp; Aerospace Engineering, Queen's University Belfast, Northern Ireland

***

# Point Stabilisation Tasks (MPC *only*)
## 1 Axis Reference
In the following examples showcasing Model Predictive Control for Point Stabilisation, the target point is only defined in 1 Axis.
Due to the gravitational component, Z has Upwards &amp; Downwards versions for comparison. <br/>
#### Reference in X
<p float="left">
<img src="Media/2.png" width="300" height="300">
<img src="Media/1axis_x.gif" width="446" height="300">
</p>

#### Reference in Y
<p float="left">
<img src="Media/1.png" width="300" height="300">
<img src="Media/1axis_y.gif" width="446" height="300">
</p>

#### Reference in Z (Upwards)
<p float="left">
<img src="Media/4.png" width="300" height="300">
<img src="Media/1axis_z_up.gif" width="446" height="300">
</p>

#### Reference in Z (Downwards)
<p float="left">
<img src="Media/3.png" width="300" height="300">
<img src="Media/1axis_z_down.gif" width="446" height="300">
</p>

## 2 Axis Reference
In the following examples showcasing Model Predictive Control for Point Stabilisation, the target point is defined in 2 Axis. 
This shows how the controller adapts when handling targets in multiple different DOF. Directly below is a good test for maintainining
depth during a horizontal translation, and the latter two examples in this section allow comparison between working with and against
gravity. <br/>
#### Reference in (X,Y)
<p float="left">
<img src="Media/5.png" width="300" height="300">
<img src="Media/2axis_xy.gif" width="446" height="300">
</p>

#### Reference in (X,Z) (Upwards)
<p float="left">
<img src="Media/6.png" width="300" height="300">
<img src="Media/2axis_xz_up.gif" width="446" height="300">
</p>

#### Reference in (Y,Z) (Downwards)
<p float="left">
<img src="Media/7.png" width="300" height="300">
<img src="Media/2axis_yz_down.gif" width="446" height="300">
</p>

## 3 Axis Reference
In the following examples showcasing Model Predictive Control for Point Stabilisation, the target point is defined in 3 Axis. 
This shows how the controller adapts when handling targets in multiple different DOF. In the first example below, the Reference Angles 
are consistent and it is only moving in 3DOF (X,Y,Z). In the second example, all 6DOF are changed, giving it a rigorous test with multiple 
simultaneous variables. <br/>
#### Reference in (X,Y,Z) (Upwards)
<p float="left">
<img src="Media/8.png" width="300" height="300">
<img src="Media/3axis_up.gif" width="446" height="300">
</p>

#### Reference in 6DOF (Flip)
<p float="left">
<img src="Media/9.png" width="300" height="300">
<img src="Media/6DOF_Ref_BR2.gif" width="446" height="300">
</p>

***

# Trajectory (Circle) Tracking Tasks (MPC *only*)
## Reference Circle Aligned
#### The BlueRov2 is lined up with the circular path that acts as a reference before the controller starts. <br/>
<p float="left">
<img src="Media/10.png" width="300" height="300">
<img src="Media/6DOF_BR2_Circle_Aligned.gif" width="446" height="300">
</p>

## Reference Circle Aligned (Above/Below)
The BlueRov2 is only lined up with the circular path, that acts as a reference, in (X,Y) before the controller starts. The circle
is then placed either Above or Below for comparison of gravitational effects. <br/>
#### Reference Circle placed Above
<p float="left">
<img src="Media/12.png" width="300" height="300">
<img src="Media/6DOF_BR2_Circle_Lift.gif" width="446" height="300">
</p>

#### Reference Circle placed Below
<p float="left">
<img src="Media/11.png" width="300" height="300">
<img src="Media/6DOF_BR2_Circle_Drop.gif" width="446" height="300">
</p>

## Reference Circle Offset (Above/Below)
The BlueRov2 is not lined up with the circular path that acts as a reference before the controller starts. The starting point of the
circle is offset in (X,Y) and then placed either Above or Below for comparison of gravitational effects. <br/>
#### Reference Circle Offset and placed Above
<p float="left">
<img src="Media/14.png" width="300" height="300">
<img src="Media/6DOF_BR2_Circle_Offset_Lift_Github.gif" width="446" height="300">
</p>

#### Reference Circle Offset and placed Below
<p float="left">
<img src="Media/13.png" width="300" height="300">
<img src="Media/6DOF_BR2_Circle_Offset_Drop_Github.gif" width="446" height="300">
</p>

***

# Point Stabilisation & Collision Avoidance Tasks (MPC *and* CBF)
## Static Obstacle Avoidance
Introducing a single static obstacle demonstrates how the CBF acts as a safety factor to avoid collision. The CBF
ensures that a radius of safety around both the BlueRov2 and the Obstacle never cross, which can be observed. <br/>
<p float="left">
<img src="Media/CBF1.png" width="300" height="300">
<img src="Media/PS_StOb_GIF.gif" width="446" height="300">
</p>

## Moving Obstacle Avoidance
Since the controller is contstantly provided live data on the location and size of an obstacle, it can adapt and respond to obstacles
that aren't in a fixed location and are moving around the environment. <br/>
<p float="left">
<img src="Media/CBF2.png" width="300" height="300">
<img src="Media/PS_MoOb_GIF.gif" width="446" height="300">
</p>

## Static &amp; Moving Obstacle Avoidance
Assuming that the BlueRov2 can detect and track any obstacles within range using SONAR or HD Camera footage, the CBF can enable multiple obstacles - 
both static and moving - to be avoided during the task. An advantageous feature for dynamic ocean envrironments. <br/>
<p float="left">
<img src="Media/CBF3.png" width="300" height="300">
<img src="Media/PS_StMoOb_GIF.gif" width="446" height="300">
</p>

***

# Trajectory (Circle) Tracking & Collision Avoidance Tasks (MPC *and* CBF)
## Static &amp; Moving Obstacle Avoidance

Carrying on from the previous example with multiple static and moving obstacles, it is observed below that the same functionality
is available for path tracking tasks. <br/>
<p float="left">
<img src="Media/CBF4.png" width="300" height="300">
<img src="Media/CT_Offset_StMoOb_GIF.gif" width="550" height="300">
</p>
