# 🏗️ Character Plot Generator (MVC Pattern)  

## 📜 Overview  
This project implements a **plot generator** using the **Model-View-Controller (MVC)** design pattern. The generator allows users to create plots by either selecting story elements interactively or generating them randomly.  

## 🎯 Problem Explanation  
A **plot generator** helps in crafting narratives by selecting key story elements such as **hero names, professions, villains, and conflicts**. The project consists of three types of generators:  

1. **SimplePlotGenerator**  
   - Returns a basic plot:  
     ```python
     pg = SimplePlotGenerator()
     pg.generate()
     ```
     **Output:**  
     ```
     Something happens
     ```

2. **RandomPlotGenerator**  
   - Generates a random plot using elements from **seven predefined text files**.  
   - Constructs sentences in the format:  
     ```
     <plot_name>, a <plot_adjective> <plot_profession>, must <plot_verb> the <plot_adjective_evil> <plot_villain_job>, <plot_villain>.
     ```
     **Example Output:**  
     ```
     Aaliyah Mosley, an abiding alabasterer, must acknowledge the assuming assassin, Acheron Redwood.
     ```

3. **InteractivePlotGenerator**  
   - Allows users to **select** elements for their story interactively.  
   - The system presents **five random options** for each category and asks the user to **choose one**.
   - Ensures user-friendly interaction **without direct I/O handling** in the generator classes.  

## 🛠️ Implementation Details  
- **Model:** Handles plot generation logic and stores narrative elements.  
- **View & Controller:** Managed by the `PlotViewer` class, which interacts with the user and displays results.  
- **Separation of Concerns:** The model (plot generator) does **not** handle direct user input/output. Instead, it **registers with PlotViewer**, which manages interaction.  
