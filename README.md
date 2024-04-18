# DismantletheComputer

## Scope of the Project

This project attempts to make the artefact model of computer science education more accessible. This model encourages students to think about computing objects within their context. This pedagogy aims to keep students away from thinking of computing as some magical abstraction; students must perceive computing objects within their contextual reality rather than as immaterial entities. It is far too easy to spend a life staring at a screen, and never question where our creations, stored on the cloud, truly exist on the ground. Artefact thinking proposes breaking down computational objects, such as theories, concepts, and practices, and examining them not unlike art history examines artworks; there must be an understanding of how an artefact has come to be and how it stands in conversation with other artefacts. For example, when learning a new theory, students could be taught what previous theories influenced it, who came up with it and why, in what context it was established, and how it interacts with other theories. Artefact thinking requires establishing computer science as a human artefact and human creation, thus centering it within human activity.

This project focuses on the issue of materiality in the artefact model. The application of a material-centered education could prove beneficial in computer science education. This would contextualise computer science in the physical, and frame computing knowledge through a larger network of media. Teaching computer science as grounded in materiality would equally facilitate the understanding of relationships between companies and industries, as many of them are tied through channels of production. Furthermore, this could encourage students to consider environmentally aware practices when computing. An extremely prominent example of computing that doesn’t consider materiality is the mining of bitcoin. These programs require immense amounts of space and energy. Perhaps if computer scientists were trained to be more aware of their consumption of physical resources, they would have more consideration for the impacts of their products.
To investigate this framework, this project aims to make an investigation of computer objects more accessible. Through this website, people are able to explore the different components of computers.

## Process:

This website runs through Github pages.

The biggest component of this project is the 3D model. The model parts were taken from blendart on cgtrader, then compiled together in Unity. The main challenge was then scripting interactivity. I started with working on camera movement, and set up a script, `CameraMovement`, that would allow for panning, zoom, and rotation. Then, I created a canvas on which I would display buttons and created the menu. The `NavButton` script serves to toggle the menu navigation, `CaseVisibility` toggles the case when the button is clicked.

I then worked on the highlighting effect for the computer components. To do this, I created a new material “Glow”, and installed the `PostProcessing Rendering` package to create a glow effect. The `InfoButtons` script then implements the interactivity. When a button is hovered over, the related component’s current material is stored, and replaced with the glow material. A challenge here was that each computer component is composed of several sub-components. Because of this, I created a 2-dimensional array that could store the different materials for each section and that could grow or shrink to allow for different numbers of sub-parts per component.

The last script is `InformationText`, which handles displaying the information text for each component. Similar to an artist statement, this text describes the part, its materials, and dimensions. The intention of these plaques is to draw a comparison between learning computer science objects as artworks, thus applying an art history lens to how we learn.

## Future Improvements

A further improvement for this project is to be able to toggle between a dark mode (as it is right now), and a colorful mode (in which each component would be color coded to its respective button). I started implementing this, but it is technically more complicated than the other scripts so far. The reason for this is that every component is made of many different materials. In order to change all of these materials, I would need to create several new data structures that could hold all of the information about old materials and new materials. This data structure would then have to be shared among different scripts so that the new materials work with the previous code.

To do this, my preliminary idea is to create a linked-list of tuples that hold the appropriate colors, then select which part of the list to use when changing mode.

Another improvement would be to make the website responsive on small devices such as phones. This will require adapting both the website using media queries, and re-scripting UI elements in Unity so that they are compatible.

## Ressources:

- https://github.com/skills/github-pages?tab=readme-ov-file
- https://www.youtube.com/watch?v=K52l9P19_2o&ab_channel=HarrisonMcGuire
- https://docs.unity3d.com/Manual/mesh-compression.html#:~:text=By%20default%2C%20Vertex%20Compression%20is,Tangent
- https://forum.unity.com/threads/unable-to-parse-build-html5-framework-js-gz-need-help.1083602/
- https://www.cgtrader.com/3d-models/electronics/computer/computer-parts
- https://medium.com/nerd-for-tech/making-a-glass-material-in-unity-eda50c616463
- https://www.youtube.com/watch?v=iuygipAigew&ab_channel=LMHPOLY
- https://github.com/EmmaPrats/Camera-Rotation-Tutorial
- https://www.youtube.com/watch?v=mx__ZPw4fzg&ab_channel=TheGameDevCave
- https://github.com/DA-LAB-Tutorials/YouTube-Unity-Tutorials/blob/main/PanZoomOrbitCenter.cs
- https://www.youtube.com/watch?v=-RBwPD6NNms&ab_channel=RigorMortisTortoise 
- https://www.engineering.com/story/what-raw-materials-are-used-to-make-hardware-in-computing-devices
- https://www.diskmfr.com/the-process-of-how-we-make-ssd-from-a-start-to-finish-for-only-learning/
- https://typeset.io/questions/what-are-the-materials-used-to-build-a-cpu-4xnnbp7chl
- https://designlife-cycle.com/nvidia-gpu#:~:text=%E2%80%9CGPUs%20are%20silicon%20layered%20with,engineering.com%2C%202021.)
- https://www.designlife-cycle.com/harddrives#:~:text=Hard%20drives%20are%20made%20of,thorium%2C%20which%20produces%20radioactive%20wastes.
- https://www.quora.com/What-are-the-various-materials-that-motherboards-are-made-of
- https://www.crucial.com/articles/about-memory/how-is-memory-made
- https://www.designlife-cycle.com/cpu#:~:text=The%20basic%20raw%20materials%20used,environmental%20impacts%20of%20raw%20materials.
- https://www.coolermaster.com/what-is-an-sfx-psu/#:~:text=A%20standard%20ATX%20PSU%20is,even%20a%20micro%20ATX%20PSU.
- https://www.snia.org/forums/cmsi/knowledge/formfactors
- https://www.techpowerup.com/gpu-specs/geforce-rtx-4070.c3924
- https://www.seagate.com/www-content/datasheets/pdfs/3-5-barracudaDS1900-11-1806US-en_US.pdf
- https://premioinc.com/blogs/blog/motherboard-form-factors
- https://www.idc-online.com/technical_references/pdfs/data_communications/Random_access_memory_Ram_or_Pc_memory.pdf
