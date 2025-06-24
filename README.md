
# 🧭 Travel Planner - Route Optimization Tool

A C++ console application that helps users find the most **cost-effective** or **fastest** travel route between cities using **Dijkstra’s algorithm**. The project dynamically builds a graph from city and route data files and outputs the optimal path in a user-friendly HTML file.

---

## 🚀 Features

- 🗺️ **Dynamic Graph Construction** from input files
- ⚡ **Fastest or Cheapest Path Calculation** using Dijkstra’s Algorithm
- 📂 **User Input Support** for custom files, origin/destination, and preference
- 📄 **HTML Output Generation** with full route breakdown
- 🧩 **Modular Design** using object-oriented principles

---

## 📂 File Structure

```
.
├── Main.cpp                   # Program entry point
├── GraphFunctions.h          # Graph class and Dijkstra's algorithm
├── FileOperations.h          # HTML output generation
├── Location.h                # Location (City) class
├── Route.h                   # Route (Edge) class
├── Parser.h                  # Parsers for cities and routes
├── cities.txt                # Sample city data (tab-separated)
├── routes.txt                # Sample route data (CSV)
├── output.html               # Generated route visualization
```

---

## 📥 Input Format

### 🔹 `cities.txt` (Tab-separated)
```
Country    Capital    Latitude    Longitude
India      New Delhi  28.6167     77.2167
...
```

### 🔹 `routes.txt` (CSV)
```
Origin,Destination,Transport,Time,Cost,Note
New Delhi,Mumbai,train,15,200,Scenic route
...
```

---

## 🧠 How It Works

1. **Parse** the input files using `locationParser` and `routeParser`
2. **Construct** a graph with cities as nodes and routes as edges
3. **Run Dijkstra’s algorithm** based on user preference (fastest or cheapest)
4. **Backtrack** using stacks to record the optimal path
5. **Generate an HTML file** visualizing the route step-by-step

---

## 🛠️ How to Run

### 🔧 Requirements
- C++17 or later
- g++ or any C++ compiler

### ▶️ Compile and Run

```bash
g++ Main.cpp -o travel_planner
./travel_planner
```

You’ll be prompted to enter:
- Cities file (e.g., `cities.txt`)
- Routes file (e.g., `routes.txt`)
- Output filename (e.g., `output.html`)
- Origin city
- Destination city
- Preference (`fastest` or `cheapest`)

---

## 📤 Output

A styled `output.html` file that lists:
- Cities visited in order
- Routes taken with mode, time, and cost
- Total travel time/cost based on preference

---

## 🧩 Algorithms & Concepts

- **Graph Representation** (Adjacency via city-linked routes)
- **Dijkstra’s Algorithm** with a min-heap (priority queue)
- **Dynamic Data Binding** using pointers and parsers
- **Stack-based Backtracking** to reconstruct paths
- **File I/O & HTML Generation**

---

## 📈 Future Improvements

- 🌍 Map visualization using latitude/longitude (e.g., Leaflet.js or Google Maps)
- 📱 GUI frontend using Qt or web-based technologies
- 🚌 Multi-modal transportation optimization
- 📊 Analytics dashboard for travel data

---

## 🙋‍♂️ Author

**Swagat Suman Mishra**  
B.Tech IT Student | IIIT Bhubaneswar

---

## 📄 License

This project is licensed under the MIT License. Feel free to use, modify, and distribute it for educational or commercial use.
