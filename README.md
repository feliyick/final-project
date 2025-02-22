# Final Project!

This is it! The culmination of your procedural graphics experience this semester. For your final project, we'd like to give you the time and space to explore a topic of your choosing. You may choose any topic you please, so long as you vet the topic and scope with an instructor or TA. We've provided some suggestions below. The scope of your project should be roughly 1.5 homework assignments). To help structure your time, we're breaking down the project into 4 milestones:

### Design Doc

#### Introduction
I have a lot of experience in interior environment modelling, however, not so much exterior. I have once attempted to model a street-view environment piece, however found it time consuming and difficult to get right. I also do love Japanese architecture and Japan itself. Thus, combining those two interests, and drawing some inspiration from this poster in my bedroom wall, I want to create a tool that can procedurally generate traditional 'minka' to be placed in a courtyard scene. I was really inspired after the Houdini-environment assignment. I had never used Houdini before, and since it is such an industry standard tool, I figured this would be a good opportunity to experiment more with it. 


#### Goal
As a minimum viable product, I hope to create an art tool that procedurally creates a traditional japanese minka. Users can customise number of stories, width and height, number of sections, roof slant, whether it sits on top of an elevated platform with staris etc. Colours can be customised too. As a stretch goal, I want to put these houses in a courtyard layout. Placement of the minka would be procedural too. 

#### Inspiration/reference:
I was inspired from this poster in my bedroom wall, and this series of youtube videos:
![image](https://user-images.githubusercontent.com/59979404/141842228-30ea29e6-5119-4356-adaa-fb21b245b9fb.png)
https://www.youtube.com/watch?v=TwCthsWsI7Y&ab_channel=RaduCius
https://www.youtube.com/watch?v=dpqsePcSRkk&ab_channel=Houdini

I found this tutorial on how to procedural create a european style house, which I can adapt for my purposes: https://www.youtube.com/watch?v=WuNTFrDLABY&ab_channel=SimonHoudini

There are also a handful tutorials on creating procedural cities. I can reduce the scale of the city to a smaller courtyard. 
https://www.youtube.com/watch?v=n3m9E4-NkqE&t=522s&ab_channel=%D0%94%D0%B5%D0%BD%D0%B8%D1%81VFX

#### Specification:
- Create a HDA in houdini that generates a traditional japanese Minka procedrally
- Add sliders to adjust various parts of the model including colour
- If I don't get to placing the houses in a procedurally generated courtyard map, I will just use my tool to populate a fixed scene. 
- Aim to get a really nice render!

Create a basic tool that generates a single flower procedurally
Import a petal with a texture and rotate around center n number of times
Add blooming animation that follows pattern from visual reference
Fine tune tool to add more variance and input controls
Focus on getting a really nice render of one flower - will have to learn how to light a scene
Use flower tool to fill a bouquet of flowers or populate some organic scene

#### Techniques:
- What are the main technical/algorithmic tools you’ll be using? Give an overview, citing specific papers/articles.
- I came into this class with little to no experience with Houdini, so I look forward to experimenting and learning how to use this piece of software as my technical challenge. I don't want to over complicate this project too much, so just focusing on the basics of understanding how to use the graph editor, and vex expressions to achieve the exterior of the Japanese house.
- https://www.youtube.com/watch?v=Ri9AAF_hB6Q&ab_channel=IlliaStatkevych
- https://www.artstation.com/marketplace/p/y3DV/houdini-tutorial-procedural-japanese-castle-in-unreal-engine-4

#### Design:
- I don't think my project suits a free-body diagram. In words, however, my minka house tool will be controlled by various inputs/sliders as a Houdini Digital Asset. This tool can be used for populating scenes quickly and with lot of variety.

#### Timeline:
- WEEK 1: Work through some houdini procedural house examples, and adapt what I have learned to create a basic Japanese house tool. Focus on breaking down a Japanese house into distinct features (roof, floors, windows and doors, shape)
- WEEK 2: Add more polish to the generator tool as well as texture the house. Give users ability to change the colours of the house. Look into courtyard layout and proceduralism if I have time.
- WEEK 3: Use my tool to create a cool scene in a static/generated courtyard. Render multiple scenes. Add a sky, some trees, etc. to mimic reference images.

## Milestone 2: 

### Images

![ms_2_example](https://user-images.githubusercontent.com/59979404/142963979-001d21b8-8c74-468a-9cae-eaf9351b54de.PNG)

![ms_3_example](https://user-images.githubusercontent.com/59979404/142964543-53526590-0bb7-47cf-81ff-f4c569303c97.PNG)

![ms_1_example](https://user-images.githubusercontent.com/59979404/142964615-c00c0edc-cea7-43ad-af4a-c0610a54dd8b.PNG)

![ms_5_example](https://user-images.githubusercontent.com/59979404/143037730-60164ee0-e580-407f-b408-9b2c0a4cf2a0.PNG)

### Progress Report 1!

#### Implemented the following: 

- Main generator is almost done! The tool is able of generating a traditional Japanese minka-esque looking structure. The house is currently limited to two floors. The minka sits on an elevated platform with a railing, which is reachable via stairs. The house also has windows and doors.
- The following aspects can be procedurally generated: width and height of the main structure. number of extrusions/divets on the first floor, roof is automatically calculated, number of doors, stairs, windows, dimensions and number of steps of stairs. 

#### To dos: 
- I need to add more variation to the second floor. Currently to achieve the iconic tapered roof, the second floor's shape is pretty much fixed. I'll have to figure out how to add overhangs to the second floor.

- Next week I'll add colour/materials, and maybe add more logic so that steps spawn near doors, and windows spawn only on walls that face the outside.


## Milestone 2: 

### Images

![ms2_example](https://user-images.githubusercontent.com/59979404/143985218-20257670-92e8-40d1-bad2-9cf41fd4efb0.PNG)
![ms2_example_3](https://user-images.githubusercontent.com/59979404/143985219-6cf46255-e6ee-405a-b76c-760093cf38c7.PNG)
![ms2_example_2](https://user-images.githubusercontent.com/59979404/143985221-88da0d74-a5ef-4047-b53d-dce3664cedd6.PNG)

### Progress Report 2!

#### Implemented the following: 

- Added a courtyard functionality. So far, you can add a singular courtyard in the center of the structure and adjust the size. If there is a courtyard, there will be no second floor, however. I decided to go with this feature instead of window overhangs as I thought this courtyard cutout had the biggest visual impact.
- Added some materials to everything except the windows and doors. The windows and doors are an fbx I created in maya that I have not textured. I am thinking of replacing it with a procedurally modelled ones so I can easily texture them and adjust their look
- Didn't manage to fix the second floor or add overhangs due to time constraints

#### To dos: 
- Texture the windows
- Create a scene with multiple houses. Add grass, trees, a background and render a nice scene
- My tool runs really slowly (due to the number of computations and nodes). I want to find a way to simplify it a little to improve run time
- Add more sliders for maximum variability


## Milestone 3:

Please look at minka_tool.hdanc, and final-project-scene.hipnc as my final submissions! Sorry there are a lot of texture files, and a few fbxes.

### Images
![test_render_04](https://user-images.githubusercontent.com/59979404/144917022-de85d0f1-7dd3-4e08-9c8c-359438dc6c6e.png)
![test_render_02](https://user-images.githubusercontent.com/59979404/144917024-6bd69639-13a0-4b60-b6b8-0f6d44c7314d.png)
![test_render_03](https://user-images.githubusercontent.com/59979404/144917027-6f8507d3-4684-4129-a5d7-36bd1a55b8e1.png)

### Progress Report 3!

I think my project went really well! I started off with little to no exerperience in procedural modelling, but after milestone 1 I felt as if I had greatly developed my understanding of Houdini. My traditional Japanese house generator is capable of creating 1-2 story high houses, with an optional courtyard (which sacrifices the second floor). The following aspects can be edited/changed through the HDA UI:
- House base shape, base height, number of wall extrusions
- Size of courtyard in the center(can be 0 for no courtyard)
- Number of doors, windows, stairs
- Railing, platform depth and height
- Colours of all elements
- Most features have seeds to allow users to adjust variation with the same count

The features are best visualised in the renders above. I tried to create a small scene with multiple minkas of varying heights, shapes, etc. I will continue to work on creating better renders, since there is some visible material issues/stretching. 

I think I checked off all of my original minimum viable product goals. The only stretch goal I did not achieve was that the houses themselves were going to be procedurally placed. The houses we're placed manually in the scene above. However, the the trees were procedurally placed so that it would spawn on the outer perimeter of the houses.

There are a few remaining bugs or issues. Stairs warp a little bit when the height of the platform is too high. Due to the scale of the generator, the tool runs a little slow at times. 
