# 🎨✨ URP Shader Workshop

Welcome to the URP Shader Workshop!  
In this workshop, you’ll learn how to build shaders step‑by‑step using Unity’s Shader Graph.

---

## 📘 Chapter 1 — The Basics

### 🧩 Step 1 — Start the Project  
Download this project, add it to Unity Hub, and open it.

### 🧱 Step 2 — Add Objects  
Open the **Sample Scene** and add any 3D objects you want to experiment with.

### 🎛️ Step 3 — Apply an Example Shader  
Go to the **Shaders** folder and choose one of the two example shaders.  
Expand it using the arrow and drag the shader onto a 3D object.

### 🆕 Step 4 — Create Your Own Shader  
In the **Shaders** folder, create a new shader:  
**Create → Shader Graph → URP → Unlit Shader Graph**

---

# 🎨 Chapter 2 — Adding Color  
In this chapter, you’ll create your first custom shader by blending colors.

### 🌈 Goal  
Combine two colors and output them to the object.

### 🪄 Steps  
1. Create a new **Unlit Shader Graph** and name it **Color**.  
2. In the **Blackboard**, add **two Color properties**.  
3. Drag both Color properties into the graph.  
4. Add an **Add** node and connect both colors to it.  
5. Connect the output of the Add node to the **Fragment → Base Color**.  
6. Save the shader and apply the material to an object.  
   → Your object now displays the combined colors.

This forms the foundation for the next chapters.

---

# 🖼️ Chapter 3 — Adding Textures  
Now you’ll extend your color shader by adding a texture and optionally blending it with color.

### 🎯 Goal  
Sample a texture and optionally tint it with your color.

### 🪄 Steps  
1. Continue working in the same shader graph from Chapter 2.  
2. Choose a texture from the **Cartoon_Texture_Pack** and copy it into **Assets → Textures**.  
3. In the Blackboard, add a **Texture2D** property.  
4. Select the property and assign your chosen texture as the **Default** value in the Graph Inspector.  
5. Drag the Texture2D property into the graph and create a **Sample Texture 2D** node.  
6. Connect the Texture2D property → **Texture** input of the Sample node.  
7. Choose your output method:  
   - **Option A (simple):** Sample Texture 2D → Fragment  
   - **Option B (tinted):**  
     - Add a **Multiply** node  
     - Color (from Chapter 2) → A  
     - Sample Texture 2D → B  
     - Multiply → Fragment  

Your shader now supports both color and texture.

---

# 🔄 Chapter 4 — Adding Movement  
Time to animate your texture by scrolling it across the surface.

### 🎯 Goal  
Use UV manipulation + Time to create movement.

### 🪄 Steps  
1. In the Blackboard, add:  
   - **Texture2D** (your texture)  
   - **Vector2 (Velocity)** → e.g. `(0.5, 0)` for horizontal scrolling  
2. Add a **Time** node  
   - Use the **Time (top output)** → this gives a steadily increasing value  
3. Add a **Multiply** node  
   - Time → A  
   - Velocity → B  
   → This calculates how far the texture should move  
4. Add a **UV** node  
5. Add a **Tiling And Offset** node  
   - UV → UV  
   - Multiply → Offset  
6. Add a **Sample Texture 2D** node  
   - Texture2D → Texture  
   - Tiling And Offset → UV  
7. Connect Sample Texture 2D → Fragment  

Your texture now scrolls smoothly across the object.

---

# 🏠🚀 Final Assignment — Decorate Your Own House

**Who:** Your research team  
**What:** Build a house using primitive 3D objects and decorate it using your own shaders.  
- Make **transparent glass** (tip: use *Alpha*).  
- Make **light reflections** or shiny surfaces.  
- Use color, texture, and movement creatively.

**Goal:** Build the most creative house and beat the other teams.  
**Reward:** Eternal glory… and a real prize.

---
