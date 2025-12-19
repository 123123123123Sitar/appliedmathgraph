# 3D Matchup Graph Visualization

A 3D force-directed graph visualization showing the connectivity between different sports based on shared participants.

## Live Demo
[View Live Graph](https://123123123123Sitar.github.io/appliedmathgraph/)

## Project Overview

This visualization models the relationships between 7 sports: **Soccer, Hockey, Cricket, Basketball, XC (Cross Country), Ping Pong, and Chess Boxing**.

### Logic
- **Nodes**: Represent individual sports.
- **Edges**: Exist if at least one person rated both sports.
- **Weights**: The number of people who rated both sports (shared raters).

## Data and Analysis

### Matchup Data Table

| Matchup | Shared Raters (Weight) | Key Participants |
|:---|:---:|:---|
| **Cricket – Chess Boxing** | **6** | Theo, Bridger, Idan, Varenya, Sitar, Kai |
| Soccer – Cricket | 5 | Theo, Bridger, Varenya, Sitar, Kai |
| Soccer – Chess Boxing | 5 | Theo, Bridger, Varenya, Sitar, Kai |
| Hockey – Cricket | 5 | Theo, Idan, Varenya, Sitar, Kai |
| Hockey – Chess Boxing | 5 | Theo, Idan, Varenya, Sitar, Kai |
| Soccer – Hockey | 4 | Theo, Varenya, Sitar, Kai |
| Ping Pong – Chess Boxing | 4 | Bridger, Idan, Varenya, Sitar |
| Basketball – Chess Boxing | 4 | Theo, Bridger, Varenya, Kai |
| Soccer – Basketball | 3 | Theo, Bridger, Varenya |
| Soccer – Ping Pong | 3 | Bridger, Varenya, Sitar |
| Hockey – Basketball | 3 | Theo, Varenya, Kai |
| Hockey – Ping Pong | 3 | Theo, Varenya, Sitar |
| Cricket – Basketball | 3 | Theo, Bridger, Varenya |
| Cricket – Ping Pong | 3 | Bridger, Varenya, Sitar |
| Soccer – XC | 2 | Bridger, Varenya |
| Hockey – XC | 2 | Bridger, Varenya |
| Cricket – XC | 2 | Bridger, Varenya |
| Basketball – Ping Pong | 2 | Varenya, Sitar |
| XC – Ping Pong | 2 | Bridger, Varenya |
| XC – Chess Boxing | 2 | Bridger, Varenya |
| **Basketball – XC** | **1** | Varenya |

### Report Summary

> "Each edge represents a head-to-head matchup defined by at least one participant rating both sports, with edge weights equal to the number of shared raters; although all sport pairs appear, matchup strength varies significantly across pairs."

This graph is a complete weighted graph ($K_7$), meaning every sport is connected to every other sport, but the strength of these connections varies from 1 to 6 shared raters. This structure is ideal for dominance modeling methods like Colley Matrix ranking, where strength of schedule is weighted by these variable edge weights.

## Interactive Features

- **Draggable Nodes**: Click and drag spheres to rearrange the layout. They will stay where you drop them.
- **Hover Effects**: Hovering over a node or link highlights it in **red**.
- **Zoom/Pan**: Scroll to zoom, drag background to rotate/pan.

## Running Locally

1. Clone the repository:
   ```bash
   git clone https://github.com/123123123123Sitar/appliedmathgraph.git
   cd appliedmathgraph
   ```

2. Start a local server:
   ```bash
   python3 -m http.server 8080
   ```

3. Open your browser to `http://localhost:8080`.
