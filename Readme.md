# 🎨 URP Shader Workshop

## 📘 Chapter 1 — The Basics

### 🧩 Step 1  
Download this project, add it to Unity Hub, and open it.

### 🧱 Step 2  
Open the **Sample Scene** and add any 3D objects you want to work with.

### 🎛️ Step 3  
Go to the **Shaders** folder and choose one of the two example shaders.  
Expand it using the arrow and drag the shader onto a 3D object in the scene.

1. create in the map Shaders a new shader via
Create -> Shader Graph -> URP -> Unlit Shader Graph

---

## 🎨 Chapter 2 — Adding Color  
Learn how to apply and adjust colors inside your shader to give your object a unique look.

1. Create an unlit shader and name it Color
2. In the shader graph, add 2 colors of your choosing to the editor on the left side of your screen.
3. Drag those in the shader graph.
4. Create an 'Add' node and combine these colors.
5. Drag the output of the end node to the fragment of the shader graph.
6. Add this material to an object in your scene. You will see that the colors have been combined.  

## 🖼️ Chapter 3 — Adding Textures  
Add textures to create detail, patterns, and more realistic surfaces.

1. Work in the same shader graph as in chapter 2.
2. Find in the Cartoon_Texture_Pack a texture you want to use. And copy the texture in Assets -> Textures

3. Open your new made shader and add in the blackboard left of your screen a new variable Texture2D

4. Click on the new variable and go in the Graph Inspector. There you can add by default value your own texture. 

5. Drag your Texture2D variable into the workspace. And right click to add a new node Sample Texture 2D. 
6. Dot the Texture2D to the Sample Texture 2D variable Texture T2.
7. If you want you can dot the Sample Texture 2D directly to the fragment. Or if you want to add a color you can create a new node called Multiply.
8. Use the colors you used from chapter 2. And dot the color to A and the Sample Texture 2D to B. Now you can dot Multiply to the fragment. 

---

## 🔄 Chapter 4 — Adding Movement  
Animate your shader by modifying parameters over time to create motion and dynamic effects.

---

# 🚀 Create Your Own Shader(s)  
Experiment, tweak, break things, and build something awesome!
