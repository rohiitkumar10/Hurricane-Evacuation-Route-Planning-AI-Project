# Hurricane Evacuation Route Planning
A project for the Intro to Artificial Intelligence course at the University of New Haven  
Created by: Rohit and Ben

---

## 📌 Project Overview
This project applies artificial intelligence search algorithms to plan optimal evacuation routes during hurricanes. Using storm data from the National Oceanic and Atmospheric Administration (NOAA), we implemented and compared **Uniform Cost Search (UCS)** and **A\* Search** to determine which algorithm provides a safer and more efficient evacuation path in the state of Louisiana.

The goal of this documentation is to help students and researchers understand the project structure, models used, and how to run and use the system.

---

## 🧠 Background and Motivation
Hurricane evacuation route planning is critical for minimizing casualties and ensuring safe travel during severe weather events. Different search methods can greatly impact how quickly and safely a route is identified.

We selected UCS and A\* Search because:

### Why UCS?
- Expands nodes in order of lowest cumulative cost  
- Does not require a heuristic  
- Guarantees an optimal path when step costs are positive  

### Why A\* Search?
- Uses **cost so far + heuristic**  
- Employs Euclidean distance as a guidance heuristic toward safe zones  
- Much faster in practice because the search is directed  
- Often optimal and more efficient in real-world scenarios  

---

## 📂 Project Structure

```
project/
│── data/                         # NOAA storm data
│── src/
│   ├── ucs.py                    # Uniform Cost Search implementation
│   ├── astar.py                  # A* Search implementation
│   ├── heuristics.py             # Euclidean heuristic definition
│   ├── grid_builder.py           # Creates hazard grid from NOAA data
│   ├── visualizations.py         # Graphs, heatmaps, route plots
│── main.py                       # Main execution file
│── comparison_table.csv          # Performance results (UCS vs A*)
│── README.md                     # User documentation manual
```

---

## ⚙️ Installation and Setup

### **Requirements**
- Python 3.8+
- Required libraries:
  - numpy  
  - pandas  
  - matplotlib  
  - seaborn  
  - scipy  
  - scikit-learn (if used in preprocessing)

### **Install Dependencies**

If using `requirements.txt`:

```bash
pip install -r requirements.txt
```

Otherwise:

```bash
pip install numpy pandas matplotlib seaborn scipy scikit-learn
```

---

## ▶️ How to Run the Model

### **Run Uniform Cost Search**
```bash
python main.py --method ucs
```

### **Run A\* Search**
```bash
python main.py --method astar
```

### **Outputs Include**
- Optimal evacuation route  
- Total path cost  
- Nodes expanded  
- Path length  
- Total runtime  
- Visual graphs and heatmaps saved to `/outputs`  

---

## 📊 Visualizations Produced
The system automatically generates:

- **Comparison table** (UCS vs A\*)  
- **Heatmap of storm density**  
- **Storm event distribution**  
- **3D surface plot of hazard grid**  
- **Evacuation route plot (UCS vs A\*)**  
- **Cost path evolution graph**  
- **Top 15 regions with highest storm frequency**  

These help students understand how hurricanes impact Louisiana and how search algorithms navigate hazardous areas.

---

## 📝 Key Findings from the Analysis

### **Path Cost**
- UCS Path Cost: **170.53**  
- A\* Path Cost: **170.53**  
➡️ Both algorithms produced **optimal and identical cost paths**.

### **Nodes Expanded**
- UCS: **171 nodes**  
- A\*: **171 nodes**  
➡️ Both explored the same number of nodes.

### **Runtime**
- UCS Runtime: **75.42 ms**  
- A\* Runtime: **52.72 ms**  

➡️ **A\*** was significantly faster due to its heuristic.

### **Conclusion**
A\* search was the more efficient algorithm and is the safer and preferred approach for real-world evacuation route planning.

---

## 🧭 Real-World Application
This framework can be extended to:

- Real-time hurricane tracking systems  
- Emergency management software  
- Disaster response simulations  
- Routing for ambulances, fire rescue, and evacuation coordination  

The approach demonstrates how AI search strategies can be directly applied to public safety.

---

## 👥 Contributors
- **Ben** — Data processing, model design, visualizations  
- **Rohit** — Route planning model, search implementations, analysis

---

## 📞 Contact
For questions or further research collaboration, feel free to reach out.
