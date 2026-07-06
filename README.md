# Gaussian Splatting Colab

Train and view 3D Gaussian Splats from your own images or videos, entirely in Google Colab.

## Notebooks

| Notebook | Description |
| --- | --- |
| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Dyl777/gaussian-splatting-colab/blob/main/gaussian_splatting_colab.ipynb) | **gaussian_splatting_colab** — mount Google Drive, extract video frames, run COLMAP, train Gaussian Splatting, render output video |
| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Dyl777/gaussian-splatting-colab/blob/main/gaussian_splatting_viewer_colab.ipynb) | **gaussian_splatting_viewer_colab** — serve your trained `point_cloud.ply` in an interactive WebGL viewer via a public Cloudflare tunnel |

## Workflow

1. Put your images or videos in a Google Drive folder
2. Run `gaussian_splatting_colab.ipynb` step by step — it handles frame extraction, COLMAP, and training
3. Once training is done, run `gaussian_splatting_viewer_colab.ipynb` to view your scene in 3D in the browser

## Input

- Images: `.jpg`, `.jpeg`, `.png`
- Videos: `.mp4`, `.mov`, `.avi`, `.mkv`, `.webm`

Update `DATASET_PATH` in Step 1 of the training notebook to point to your Drive folder.

## Output

- Trained model: `/content/my_scene/output/point_cloud/iteration_30000/point_cloud.ply`
- Rendered video: `/content/warehouse_render.mp4`
- Optionally copied back to Google Drive in Step 7

## References

- Main repo: https://github.com/graphdeco-inria/gaussian-splatting
- Paper: https://arxiv.org/abs/2308.04079
- WebGL viewer: https://github.com/antimatter15/splat (thanks to [@antimatter15](https://twitter.com/antimatter15))
