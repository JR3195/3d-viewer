# 3D Model Viewer

Client-facing 3D viewer. Clients open a link (WhatsApp, any browser), no sign-in. They can rotate and zoom the model.

## Add a model for a client

1. On GitHub, open the `models` folder and choose **Add file → Upload files**.
2. Drag in a folder named after the model, for example `foundation-day-backdrop`, containing:
   - `model.glb` (recommended, export from Blender as glTF 2.0 → .glb), **or**
   - `model.fbx` plus its texture images, with the same file names the FBX uses
   - optional `info.json` (see below)
3. Commit. After about a minute the link works:

   `https://<your-username>.github.io/<repo-name>/?m=foundation-day-backdrop`

Folder names: letters, numbers, `-` and `_` only. No spaces.

## info.json (optional)

```json
{
  "title": "Foundation Day backdrop",
  "background": "grey",
  "twinmotion": "https://... your Twinmotion Cloud link ..."
}
```

- `background`: `grey` (default) or `studio`
- `twinmotion`: adds a **View in Twinmotion** button. If Twinmotion gives you an embed link, use `twinmotion_embed` instead so it plays inside the page.
- `file`: only needed if the model file isn't called `model.glb` / `model.fbx`

## Notes

- This repo is public (GitHub Pages on a free account needs that), so anyone with a link can view the model files. Don't put confidential client work here.
- GitHub warns at 50 MB and blocks files over 100 MB. Keep models small (under ~20 MB loads well on phones).
- Opening the site without `?m=` shows a sample scene and lets you preview any FBX/GLB locally. Nothing is uploaded from that preview.
