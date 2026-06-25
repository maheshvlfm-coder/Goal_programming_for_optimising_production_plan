## 📝 Project README

### Production Optimization Tool - Google Colab

This interactive tool facilitates production planning using a variety of optimization methods directly within Google Colab. It allows users to upload their Bill of Materials (BOM), inventory, demand, and priority data, or use sample data, to determine optimal production quantities based on selected objectives (e.g., maximize profit, maximize quantity, minimize cost).

### ✨ Features

-   **Data Management**: Load sample data for quick demonstrations or upload your own CSV files.
-   **Multiple Optimization Methods**: Choose from:
    -   Linear Programming (LP) using PuLP and CVXPY
    -   Mixed Integer Programming (MIP)
    -   Integer Programming (IP)
    -   Goal Programming
    -   Genetic Algorithm (Heuristic)
    -   OR-Tools Linear Solver
-   **Configurable Objectives**: Optimize for maximizing profit, maximizing total production quantity, minimizing cost, or a balanced approach combining profit and priority.
-   **Interactive Interface**: User-friendly widgets for method and objective selection.
-   **Comprehensive Results Analysis**: Detailed production plans, profit calculations, demand fulfillment rates, and material utilization analysis.
-   **Visualizations**: Graphs to quickly understand production vs. demand, profit by product, demand fulfillment, and material usage.
-   **Bottleneck Identification**: Pinpoint materials with high utilization to identify potential bottlenecks.

### 🚀 Setup

The notebook automatically installs all necessary Python libraries, including `pulp`, `cvxpy`, `ortools`, and `deap`. No manual setup is required beyond running the notebook cells in order.

### 💡 Usage

1.  **Run all cells** in the notebook.
2.  At the bottom, you will see two main buttons:
    -   **`📝 Load Sample Data`**: Use this to quickly see the tool in action with pre-defined example datasets.
    -   **`📁 Upload Files`**: Click this to upload your own production data in CSV format.
3.  **Process Data**: After loading sample data or uploading your files, the data preview will be displayed. If you uploaded files, click the `🔄 Process Files` button.
4.  **Select Optimization Parameters**: An interface will appear allowing you to choose:
    -   **Method**: Select your desired optimization algorithm.
    -   **Objective**: Choose what you want to optimize for.
5.  **Run Optimization**: Click `🚀 Run Optimization` to execute the selected method with the chosen objective.
6.  **Review Results**: The tool will display the solution status, optimal value, and a detailed production plan with tables and visualizations, including material utilization analysis.

### 📊 Data Formats

Ensure your CSV files have the following headers and columns:

-   **BOM (Bill of Materials)**:
    -   `Product`: Name of the finished product.
    -   `Material`: Name of the raw material.
    -   `Quantity_Required`: Amount of the material needed per unit of product.

-   **Inventory**:
    -   `Material`: Name of the raw material.
    -   `On_Hand_Quantity`: Current available quantity of the material.
    -   `Unit_Cost`: Cost per unit of the material.

-   **Demand**:
    -   `Product`: Name of the finished product.
    -   `Demand_Quantity`: Total demand for the product.
    -   `Selling_Price`: Selling price per unit of the product.

-   **Priorities**:
    -   `Product`: Name of the finished product.
    -   `Priority_Weight`: A numerical weight indicating the importance or priority of producing this product (higher value = higher priority).
    -   `Profit_Margin`: Expected profit margin for the product (e.g., 0.25 for 25%).
