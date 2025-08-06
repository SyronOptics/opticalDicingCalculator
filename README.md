# Optical Dicing Calculator

A web-based tool for calculating and visualizing optical filter dicing patterns on silicon wafers.

## Features

- Calculate the optimal layout for dicing optical filters on silicon wafers
- Support for both rectangular and round filter shapes
- Visualization of the dicing pattern with color-coded elements
- Customizable wafer size, filter size, blade width, and margin
- Real-time calculation and visualization

## How to Use

1. Select the wafer size from the dropdown (80mm, 60mm, or 100mm square wafers)
2. Choose the filter shape (Rectangle or Round)
3. Select a preset filter size or choose "Custom" to enter your own dimensions:
   - For rectangular filters, enter separate width and height values
   - For round filters, enter the diameter
4. Adjust the blade width (default 2mm) and margin (default 5mm) as needed
5. Click "Calculate" to see the results and visualization

## Understanding the Results

The results section shows:
- Wafer size and usable area after applying the margin
- Filter shape and size
- Blade width used for calculations
- Total number of filters that can be cut from the wafer

## Visualization Legend

- Green: Wafer area
- Blue: Filter positions
- Yellow (dashed border): Margin area
- Red lines: Blade cuts

## Technical Details

This tool uses JavaScript and D3.js for visualization. Calculations take into account:
- Wafer dimensions
- Filter dimensions (with added margin for round filters)
- Blade width between filters
- Safety margin around the wafer edge

The algorithm calculates how many filters fit in both X and Y directions, considering the space needed for blade cuts between filters.