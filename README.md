# CNN Flattening Visualizer

A tiny, framework-free web app to demonstrate the flattening step in a convolutional neural network.

Students can watch:
- Feature maps unroll row-by-row (the second row glued to the first, then the third, etc.).
- The resulting vectors from each feature map get concatenated into one final flattened vector.

## How to use

1. Open `index.html` in a browser (no build or server required).
2. Use the controls at the top to set:
	- Number of feature maps
	- Rows and columns per map
	- Animation speed
3. Click Generate (optional), then either:
	- Play for an automated animation, or
	- Step to advance one action at a time (row unrolls, then concatenations).
4. Reset clears the stage.

All code is plain HTML/CSS/JS (no frameworks) and lives in `index.html`.

## Practice problems

Below the visualizer, there are practice questions that randomly generate:
- An RGB image size (H × W × 3)
- A number of kernels (K)

Assumptions are fixed: no padding, 3×3 convolution (stride 1), then 2×2 pooling (stride 2).

Students compute the flattened vector dimension after this pipeline. They can click “Reveal Answer” to check, which also shows intermediate shapes:
- Conv output: (H−2) × (W−2) × K
- Pooled output: floor((H−2)/2) × floor((W−2)/2) × K
- Flattened length: pooled_H × pooled_W × K

Use the “New Set” button to generate a fresh batch of problems.
