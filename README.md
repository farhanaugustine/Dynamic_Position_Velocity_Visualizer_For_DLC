# Dynamic_Position_Velocity_Visualizer_For_DLC

## Motion Analysis and Visualization
------
Video Tutorial and Walkthrough: [Link](https://youtu.be/ydrdTd5-YJU)

------

![Tumbnail](https://github.com/farhanaugustine/Dynamic_Position_Velocity_Visualizer_For_DLC/assets/54376988/e10d8e14-d057-42bf-b7ee-001b04879e5b)


# **Overview**
This Jupyter script is designed for motion analysis of tracked body parts in DeepLabCut CSV files. I created this notebook to help me with behavioral neuroscience experiments. It calculates the average positions and velocities of two body parts (for better accuracy). It creates visualizations such as GIFs and streamline plots to represent the motion and flow of movement. Although there are tools like Simba, DLCAnalyzer, and Bonsai, none are as easy as running a Python script. 

### Installation
To run this script, you will need Python installed on your system along with the following libraries:

`pandas`
`numpy`
`matplotlib`
`imageio`
`scipy`
`IPython`

You can install these libraries using pip:
For example pip install pandas numpy matplotlib imageio scipy IPython
###
### Usage
To use this script, you will need a CSV file containing the tracked body part data generated from DLC analyses. The script reads this data, performs calculations and generates visualizations.
1. Load your CSV data into a DataFrame.
2. Create a dictionary mapping body part names to their coordinate columns.
3. Define functions to calculate average positions and velocities.
4. Generate GIFs to visualize the movement of body parts.
5. Create optical flow diagrams and streamline plots to visualize the flow of movement.
###
### Functions
`calculate_average_position` - Calculates the average position of two body parts.
`create_position_gif` - Creates and displays a GIF from the average positions of two body parts.
### Example of Averaged Head and Thorax Movements of Mouse in T-maze
![average_position_Head_Thorax](https://github.com/farhanaugustine/Dynamic_Position_Velocity_Visualizer_For_DLC/assets/54376988/bab06b35-c0b8-4472-a833-c8f4defd0055)
###
`calculate_average_velocity` - Calculates the average velocity of two body parts.
###
`create_optical_flow_gif` - Creates and displays a GIF from the average positions and velocities of two body parts.
### Example of Averaged Head and Thorax Velocities of Mouse in T-maze
#### Arrow length represent the magnitude of the velocity at each point
![optical_flow_Nose_Head](https://github.com/farhanaugustine/Dynamic_Position_Velocity_Visualizer_For_DLC/assets/54376988/0444e9a1-5b62-442e-91bc-8a49644e3174)
###
`Optical Flow Diagram for Individual Body Part` - This Section creates quivers to generate optical flow diagrams.
### Example of T-maze Flow Diagram
![image](https://github.com/farhanaugustine/Dynamic_Position_Velocity_Visualizer_For_DLC/assets/54376988/5af2ee01-2d5e-4cdf-9568-6ea0b8b0628f)
###
`Streamline Plot` - This Section of the code creates a streamlined plot where the red color represents the higher average speed.
###
![image](https://github.com/farhanaugustine/Dynamic_Position_Velocity_Visualizer_For_DLC/assets/54376988/80665711-33ee-4c5a-aa9a-7ec9dc3e1928)


Other Notes:
1. Ensure that the CSV file path is correct and accessible on your system.
2. Replace placeholder comments with actual values like frame rates and body part names based on your experimental data.
3. The calculate_average_velocity function uses np.diff, which reduces the array size by one. Ensure that the positions array is adjusted accordingly when used with velocities.
4. When creating streamline plots, ensure that the grid interpolation is performed correctly.

