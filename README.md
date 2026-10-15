A notebook that uses the Grey Wolf Optimizer (GWO) to pick several thresholds for grayscale image segmentation. Exhaustively searching multiple thresholds is expensive, so GWO searches for them instead.

How it works
Objective: Otsu’s between-class variance, computed from the image histogram. A larger value means better-separated classes, so GWO maximizes it.
Optimizer: 25 agents × 80 iterations, searching 3 integer thresholds in [0, 255]. The alpha, beta and delta wolves guide the pack.
Segmentation: The 3 thresholds split the image into 4 classes. Each class is painted with the midpoint of its gray range.
Output: Original vs. segmented image side by side, plus the best thresholds.
