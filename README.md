# cs7638---project--particle-filter---solved
**TO GET THIS SOLUTION VISIT:** [CS7638 – Project -Particle Filter – Solved](https://mantutor.com/product/cs7638-artificial-intelligence-for-robotics-solar-system-particle-filter-project-solved/)


---

**For Custom/Order Solutions:** **Email:** mantutorcodes@gmail.com  

*We deliver quick, professional, and affordable assignment help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;91533&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;4&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (4 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS7638 - Project -Particle Filter - Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (4 votes)    </div>
    </div>
The goal of this project is to give you practice implementing a particle filter used to localize a man-made satellite in a solar system. After completing an intergalactic mission, it’s time for you to return home. Your satellite is warped through a wormhole and released into your home solar system in perfect circular orbit around the sun. The satellite receives measurements of the magnitude of the collective gravitation pull of the planets in the solar system. Note that this measurement does NOT include the gravitational effects of the sun. Although the gravitation forces of other planets can be measured, curiously in your home solar system, the satellite and the planets follow their orbit around the sun and their motion is not affected by other planets.

Your satellite has an on-board model of the solar system that it is being dropped into.

You’ll be riding in the satellite which will exit the wormhole somewhere within the solar system, possibly as far off as +/- 4 AU in both X and Y, and it will be ejected into circular counter-clockwise orbit around the sun, which is located at (0,0).

The planets in the solar system are also orbiting counter-clockwise around the sun in circular or elliptical orbits.

You also have at most 300 days to locate yourself and the satellite before food and resources run out.

Note that your software solution is limited to 15 seconds of “real” CPU time, which is different from the simulated “satellite time”. Unless your localization and control algorithm is VERY efficient, you will probably not hit the 300-day limit before you run into the CPU timeout. If it takes your localization system more than 100-200 days to determine the satellite location, you may need to improve your localization algorithm.

The gravimeter sensor [sense function] gives you a (noisy) magnitude of the sum across each planet of the gravitational force on the satellite by that planet, +/- some Gaussian noise.

<em>v </em>= X<em>n G∗</em>2<em>M</em><em>p</em>,

<em>p</em>=1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <em>r</em><em>p&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </em>

where <em><sub>v </sub></em>is the gravity magnitude, <em><sub>n </sub></em>is the number of planets, <em><sub>G </sub></em>is the gravitational constant, <em>M<sub>p </sub></em>is the mass of planet <em><sub>p</sub></em>, and <em><sub>r </sub></em>is the vector from the satellite to the planet.

The body.py file (which you should not modify, but may examine or import) implements the simulated satellite and planets.

The solar_system.py file contains the model for the sun and planets, helper functions to initialize planets in orbit, move them in orbit, or sense the gravimeter measurement from a certain location in the solar system.

&nbsp;

<h1>Part A</h1>
After warping back to your home solar system, you must localize where you are. The first function is called <sub>estimate_next_pos</sub>, and must determine the next location of the satellite given its gravimeter measurement. If your estimate is less than 0.1 AU from the target satellite’s actual (x,y) position, you will succeed and the test case will end.

Note that your function is called once per day (time step), and each time your function is called, you will receive one additional data point. It is likely you will need to integrate the information from multiple calls to this function before you will be able to correctly estimate your satellite’s position. The “OTHER” variable is passed into your function and can be used to store data which you would like to have returned back to your function the next time it is called (the next day).

A particle filter may include the following steps and you may want to consider the following questions:

<ul>
<li>Initialization
<ul>
<li>How many particles do you need such that some cover the target satellite?</li>
</ul>
</li>
<li>Importance Weights
<ul>
<li>How does the sigma parameter affect the probability density function of a gaussian distribution and the weights of the particles?</li>
<li>Considering the gravimeter measurement has an inverse r-squared relationship to distance, how might using a fixed sigma vs a sigma relative to the gravimeter measurement affect your results?</li>
</ul>
</li>
<li>Resample
<ul>
<li>How many particles should you keep at each timestep and what are the pros/cons to having more/less particles?</li>
</ul>
</li>
<li>Fuzz
<ul>
<li>How much positional fuzzing should you have?</li>
<li>What percentage of your particles should you fuzz?</li>
</ul>
</li>
<li>Mimic the motion of the target satellite</li>
<li>Estimate</li>
</ul>
<h1>Part B</h1>
Now that you’re back in your home solar system you must send SOS messages back to your home planet, the last planet in the solar system, so that they know to come pick you up. The second function is called <sub>next_angle</sub>. The goal of this function is to set the angle to send a radio message from the satellite to your home planet. Each message you send contains part of your location and trajectory. It takes 10 messages to fully transmit this data. When your home planet receives your messages they will send a team out to retrieve you and your satellite. The test will end once your home planet has received 10 messages.

Your two functions will have the same input (gravimeter), but the next_angle function will return an absolute angle from the satellite to the home planet in radians in addition to the predicted location.
