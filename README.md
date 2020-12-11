# Your Experience is My Mine
## Visualizing an Installation for Group Interaction

In this project, students are asked to develop their Project 2 prototypes into a conceptualized application of their sensors and physical computing systems. As they proceeded in each process of Project 1 and 2, the next step is to visualize how their prototypes may be used, how they should function and what new ideas can be created in their design research.

Students will have the opportunity to continue their prototype exploration and/or apply design research to add validity, robustness and feasibility of their prototype's design, technology, idea and concepts. Students will gain more advanced skills in their design process to sell prototypes in the industry or pitch.

This case study will explore the application, technicality and conceptualization in practice of a two-way communication button developed by Michael Brzuchalski and William Luk. Due to COVID-19 safety measures, in person development of physical group ideation and prototyping did not happen. Efforts to communicate ideation strategies and activities in text will be used.

<br/>
## Where does this work?
### FINDING THE APPLICATION OF THE PHYSICAL PROTOTYPE

In the previous project, Michael and William developed a two way communication device using Adafruit IO, ESP8266 Feather HUZZAH and p5js to trigger a simple change on the button press to a p5 sketch, [shown here](https://www.youtube.com/watch?v=kvUjG0uZmqE). The technical features of the controller were thoroughly established as the team believed it to be beneficial to start design research and "theory-crafting" potential solutions and applications of their controller.

Working through the Design Matrix, the team produced several project ideas of how their system can be used. A design matrix is a guideline for generation design concepts and discovering meaningful areas of exploration for physical computing projects. Using a design matrix provided to students, 3 categories named "Design Taxonomy", "Area of Focus" and "Sensory Environment" with relevant sub-categories helped to direct the potential nature and use of prototype controller. Using the matrix, the team established:

**Design Taxonomy**
* Crowd Participation
  - Increased number of users enhance or instigate increased physical/ emotional/ media/computational response
  
**Area of Focus**
* Media Architecture
  - Computational display systems incorporated into the physical landscape including screens, lights, and projections.
  
**Sensory Environment**
* Visual: Graphic
  - 2D physical imaging technologies that use pigment or found objects, including printing, painting, and mixed media.
  
* Visual: Distorion
  - Intentionally or randomly affecting the pattern of a series or sequence of light/pixels/images.
  
* Sound: Distortion/Generation
  - Intentionally or randomly affecting the pattern of, or creating of, an audio wave or series.
  
* Sound: Sonification
  - Using non-speech audio to perceptualize data.

In addition to the Design Matrix, the team also described how Bodystorming would have worked if were possible. Bodystorming is a form of ideation like brainstorming, but performed physically. This provides necessary testing on the real application and how an idea should be executed. For some, it may be difficult to completely visualize a concept in their mind, so these bodystorming activities provide physical and tangible examples of what should happen.

In our best efforts, we will provide a detailed description to help with visualization. We would have participants walking around in a hallway or a path with propped up walls that are white. As they are walking, participants hold the controllers in hand and arrive in a specific location. When they gather in the specific location with the right amount of people and with a coordinated button press, a production team would flash RGB lights onto the walls, turn on sounds and change images on the wall.

With the framework and Bodystorming, the team created a general conceptual vision for the controller. A walkaround installation that focuses on group interactivity.

<br/>
## Prototype 1.0
### PITCHING AND REFINING THE IDEA

![Prototype 1-A](/images/TDMovieOut.0.jpg) ![Prototype 1-B](/images/TDMovieOut.1.jpg) ![Prototype 1-C](/images/TDMovieOut.2.jpg) ![Prototype 1-D](/images/TDMovieOut.3.jpg)


>"If we had the ability to create a bodystorming process video, we would have multiple participants holding our controller as they travel through a room with blank white walls. The ambient light would be darkened to help heighten the experience and atmosphere. While they walk, participants can trigger the button on their controllers to activate changes when they are near an “image” produced by a projector. If there are more than 1 participants near a projection, multiple changes are made to the “image.” 
A combination of our previous Adafruit IO two way communication, geolocation to track location of each participant and now TouchDesigner will be used to imagine this interactive installation."

In this first prototype, the team provided a live demonstration to show the validity of the interaction between the Feather controller and TouchDesigner. Michael's button changed the colour of the texture while William's button changed the number of textures. This was done by using the Adafruit IO server JSON data and parsing the information into TouchDesigner. The 3D mockup helped to visualize a room with a projection onto the ground, where it would track an individual. With the button press, participants would change the visualization of the projection.

After showing the prototype pitch for critique, there were interesting developments to extend the technicality and sophistication of the installation. The rudimentary button press is sufficient on its own to trigger a response, but a discussion of human interaction was sparked. Expanding outward from a simple button press, the team discovered an important affordance to achieve in support for stronger user experience:

**Autonomous Interaction + Forced Group Interaction**

Autonomous Interaction is the code and the sensors that drive subconscious freeplay. By just being around the projection and tracking passive human interaction like location, body count or walking, the installation establishes an invitation for users to play. As soon as users notice their basic actions or behaviour are having a direct, but minor change to the projection, curiosity will develop into active human interaction. This is when users exaggerate their limb movements and start to ask “What can I do to get a reaction?” At this point we hope to develop a Forced Group Interaction, a series of reactions that only occur and only continue when people are engaged in collaborative action.

Additional interactions can include microphones for auditory sensory. Noise gates would be used to filter a minimal amount of participant sound. When the number of participants increase, the ambient sound increases and triggers a change. Cameras for limb and facial tracking can be used for more complex features. From this important discussion, the team asked "What interactions can inform new physical computing from TouchDesigner and controller prototype?"

<br/>
## More than Magic
### EXPLORING OPTIONS FOR INTERACTION

Currently, the Feather HUZZAH still seems to be the best option for to use. Other microcontrollers with integrated microphones, camera and sensors under Adafruit distribution will work. This is necessary as Adafruit IO comes free with the server storage for reading sensor inputs and outputs. The majority of parsed data that works in this project and the previous comes from the JSON provided by Adafruit IO's service. Adafruit IO's only issue is the free subscription limitations to data rates when sending information to their servers. Increasingly more powerful physical components would be important to mention as with more participants, the greater the chance for error.

Other Adafruit computing components are available for use such as the [Adafruit Feather RFM69HCW](https://www.adafruit.com/product/3176). This Radio transceiver can be used to [communicate with other RFM69 radios](https://learn.adafruit.com/adafruit-feather-m0-radio-with-rfm69-packet-radio/using-the-rfm69-radio), to drive the effect of Forced Group Interaction.

While it would be beneficial to integrate devices particpants already have such as their phones, multiple steps would be needed for complete integration. App development is paramount, with enabled features to collect data with the built in geolocation, accelerometers, cameras and microphones. A major issue to address are the privacy concerns due to the nature of the interactions the installation. There must be willful consent for the collection of participant's information. Some will not agree to the notion, being perceived as a form of surveillance. Should this be applicable, next would be to store the information to a server.
>Additionally, this would require mobile app development which is out of the realm of current IXD curriculum and an external team.


[Dweet.io](http://dweet.io/) is an open source platform that allows publishing of IoT information to a public dashboard. Simple alert functions outline an easy way to integrate conditional statements to trigger a response when specific conditions are met. Public “dweets” are available for public viewing, but a paid subscription service at a minimal fee can provide extra features and private security of push notifications and alerts. From those Dweets, JSON data can be parsed and used in whatever capacity.
[Example project here](https://subscription.packtpub.com/book/hardware_and_creative/9781785286582/1/ch01lvl1sec15/sending-data-to-the-cloud).

With student access to myPHP and mySQL, it is entirely possible to store information in a database from scratch. Students are learning more advanced physical computing functionality and affordances, and very basic SQL and PHP development. The tricky part would be to understand the required PHP code and connections for this to work. It would be a more involved process but entirely free.
[Example project here](https://theiotprojects.com/insert-data-into-mysql-database-with-esp8266/).
