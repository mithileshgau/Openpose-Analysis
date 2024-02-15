# Openpose-Analysis
Openpose Analysis for Badminton Player Movement

## Problem Statement:
In sports analytics, obtaining real-time insights and conducting comprehensive analysis with static-camera setups poses a considerable challenge. The conventional approaches, often employing temporal CNNs, encounter processing speed issues, demanding substantial computational resources and time. Although effective, these methods fall short in delivering real-time analysis, a critical factor for augmenting player performance and making strategic decisions in sports.

OpenPose emerges as a solution, providing fast and accurate real-time multi-person 2D pose estimation. Its streamlined architecture, utilizing optimized neural network structures and parallel processing techniques, swiftly identifies key body points in images or videos. This efficiency enables simultaneous analysis of multiple individuals, making OpenPose a valuable tool in sports analytics for prompt performance evaluation and strategic decision-making. Our evaluation favors OpenPose over AlphaPose due to its well-maintained and extensively supported codebase.

## Architecture:


### Input Processing and Coordinate Extraction:
Analyze input videos using OpenPose to identify 25 key body points on each person in every frame.
Extract precise coordinates, laying the foundation for subsequent analysis.

### Player Filtering and Assignment:
Separate players from other entities by analyzing leg positions on the badminton court.
Label main players based on proximity to the top left corner, ensuring accurate analysis.

### Occlusion Handling:
Address instances of player occlusion by filling gaps in coordinates from nearby visible frames.
This approach ensures a complete dataset for accurate motion analysis and player performance assessment.

## Analysis:

### Total Distance Analysis:
Compute Euclidean distance between leg coordinates in adjacent frames to measure player movement.
Sum distances across all frames to determine the total distance traveled by each player.
Essential for understanding players' mobility patterns and aiding performance evaluation and strategic decision-making.

### Average Player Speed:
Calculate frame speed as the Euclidean distance between adjacent frames.
Obtain total average speed by summing individual frame speeds and dividing by the total number of frames.
Utilized for relative speed comparison between players.

### Heatmap:
Generate visual maps showing player movement on the badminton court using leg coordinates.
Combine individual player maps to provide a comprehensive view.
Intensity of colors indicates player movement in different areas, offering valuable insights for strategic decisions.

### Quadrant Dominance:
Evaluate player performance in specific court sections using leg coordinates.
Divide the court into customizable quadrants, creating a detailed map showcasing player dominance.
Enables players and coaches to optimize court coverage and strategize effectively.
