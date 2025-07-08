# Player Re-Identification in Sports Footage (YOLOv5 + ResNet)

This project identifies the same players across two video feeds (e.g., broadcast and tacticam) using:
- YOLOv5 (for player detection)
- ResNet18 (for feature embedding)
- Cosine similarity (for matching players)

## 📂 Files
- `Player_ReID_YOLOv5.ipynb` — Main Jupyter Notebook
- `broadcast.mp4`, `tacticam.mp4` — Input videos
- `best.pt` — YOLOv5 model for player detection
- `requirements.txt` — Python dependencies
- `player_id_mapping.txt` — Output file with matched player IDs

## 🚀 How to Run

```bash
pip install -r requirements.txt
jupyter notebook Player_ReID_YOLOv5.ipynb
```

## ✅ Output

After running the notebook, the mapping of players between the two videos will be saved in:
```
player_id_mapping.txt
```

## ⚠ Assumptions

- YOLOv5 model is trained to detect players as class `0`.
- Only the first frame from each video is processed for simplicity.
