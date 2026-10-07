# EO/IR Capstone — Visible–Infrared Fusion for Low-Light Pedestrian Detection

Code, configs, split manifests, and results for our ML capstone using the LLVIP paired visible/infrared dataset.

**Shared Drive folder:** <paste Drive folder link here>

---

## One-time setup (each team member)

1. **Accept the GitHub invite** sent to your email (or at github.com/notifications).
2. **Add the Drive shortcut**
   - Open Google Drive → **Shared with me** → right-click `EO_IR_Capstone` → **Organize → Add shortcut → My Drive**.
   - The shortcut must be named exactly `EO_IR_Capstone` (underscores, no hyphens).
3. **Create a GitHub token** (needed because this repo is private)
   - GitHub → profile picture → **Settings → Developer settings → Personal access tokens → Tokens (classic) → Generate new token (classic)**.
   - Tick the **`repo`** scope, set expiration past the end of the semester, and copy the token.
4. **Add the token to Colab**
   - Open any Colab notebook → click the **key icon** (Secrets) in the left sidebar → **Add new secret**.
   - Name: `GITHUB_TOKEN` — Value: your token — turn on **Notebook access**.
   - Never paste the token into a notebook cell.
5. **Let Colab see private repos**
   - In Colab: **File → Open notebook → GitHub** tab → tick **Include private repos** → authorize.

## Each work session

1. In Colab: **File → Open notebook → GitHub** tab → select `<your-github-username>/<repo-name>` → open `notebooks/00_setup.ipynb`.
2. **Runtime → Change runtime type → T4 GPU** → Save.
3. Run the cells **top to bottom**. Approve the Google Drive popup when asked.
4. If the notebook asks for secret access, allow `GITHUB_TOKEN`.

The Colab runtime is temporary — anything left only in `/content` is erased when the session ends. Save checkpoints and results to Drive, and code/docs to GitHub.

## Where things live

| Location | Contents |
|---|---|
| **GitHub (this repo)** | Code, notebooks, configs, split manifests, metrics tables, a small set of example images, environment/version records, documentation |
| **Google Drive (`EO_IR_Capstone`)** | Dataset archives (`data/raw`, `data/prepared`), model checkpoints and full training logs (`runs/`), full overlays and prediction examples (`evidence/`), poster files (`poster/`) |

Do **not** commit the dataset, archives, or model weights to GitHub.

## Tested environment

See [`requirements/versions.txt`](requirements/versions.txt) for the Python, PyTorch, GPU, and pinned YOLOv5 commit used in testing.
`requirements/pinned.txt` lists exact torch/torchvision versions if Colab's defaults change.
