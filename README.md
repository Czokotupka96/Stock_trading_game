# RetroTrade - Stock Market Simulator

A browser-based stock market simulation game built with HTML, Tailwind CSS, jQuery, and Chart.js. This project demonstrates dynamic state management, real-time charting, and algorithmic data generation within a single-file architecture.

## Features

* **Simulated Market Engine:** Generates 10 years (3,650 days) of mock market data on load.
* **Time Dilation:** Adjustable simulation speed, allowing players to pause, step through days normally, or fast-forward through months.
* **Real-Time Charting:** Visualizes market trends using a 100-day sliding window to ensure high performance.
* **Portfolio Tracking:** Calculates and tracks average cost basis, total portfolio value, and individual asset profit/loss dynamically.

## How It Works

The simulation does not rely on a live API. Instead, it uses a custom "Random Walk" algorithm. When the page initializes, it assigns a starting price to three assets (AAPL, TSLA, AMZN). It then runs a loop to calculate the next 3,650 days of prices by applying randomized daily volatility with a slight underlying upward drift. 

The game state (cash, owned shares, cost basis) is managed entirely in the client's browser using JavaScript. 

## How to Play

1. **Start the Game:** Click the "Start Simulation" button to begin the flow of time.
2. **Control Speed:** Use the slider below the start button to adjust the tick speed from Normal (1 second per day) to Ultra Fast. 
3. **Execute Trades:** In the Trade Desk panel, select an asset, enter a share quantity, and click Buy or Sell. 
4. **Monitor Holdings:** Watch the "Your Holdings" table at the bottom of the screen to track your active positions, average cost, and overall profit or loss.
5. **Objective:** Maximize your initial $10,000 cash balance before the 10-year simulation runs out.

## Setup and Installation

This project requires no server, build tools, or package managers. 

1. Save the code as an `index.html` file.
2. Ensure you have an active internet connection (required to fetch the Tailwind, jQuery, and Chart.js libraries via CDN).
3. Double-click the file to open it in any modern web browser.