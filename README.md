# Occluded-Object-Detection-and-Regeneration
A dual-branch pipeline for detecting and regenerating occluded vehicles. Integrates SAM 2 for modal masks and a fine-tuned Mask R-CNN for amodal segmentation, utilizing Generative Inpainting (DeepFill v2) and 6,000+ synthetic data samples for reconstruction.
## 📊 Qualitative Results
Here is a visual demonstration of the pipeline. The system detects the car, identifies the occluded (hidden) region, and regenerates the missing pixels.

| Original Occluded Image | Detected Occlusion (Mask) | Final Regenerated Output |
| :---: | :---: | :---: |
| ![Original](Images/Original%20Image.png) | ![Occluder Mask](Images/Occluder%20Mask.png) | ![Regenerated](Images/Final%20Regenerated%20Part.png) |
| *Input: Vehicle occluded by obstacle* | *The system calculates this "Occluder Mask" by subtracting the visible (SAM) mask from the full (Amodal) mask* | *Output: The hidden area is filled using DeepFill v2* |
