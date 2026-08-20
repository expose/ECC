# Private expose Cursor fork patch

This directory holds **private** customizations for the expose ECC fork.
They are **not** intended as PRs to `affaan-m/ECC`.

## Files

- `expose-cursor-fork.patch` ÔÇö single cumulative diff vs `affaan-m/ECC` `main`
- Mirror (recommended for apply/sync): `D:\job\git\expose-cursor-fork.patch`

## Sync workflow (pull upstream, keep private changes, no PR)

```powershell
cd D:\job\git\ECC
git fetch upstream main
git reset --hard upstream/main
git apply --index D:\job\git\expose-cursor-fork.patch
Copy-Item D:\job\git\expose-cursor-fork.patch patches\expose-cursor-fork.patch -Force
git add patches
git commit -m "chore(expose): apply private Cursor fork customizations"
git push --force-with-lease origin main
```

## Apply on any clean ECC clone

```powershell
git apply --check path\to\expose-cursor-fork.patch
git apply --index path\to\expose-cursor-fork.patch
git commit -m "chore(expose): apply private Cursor fork customizations"
```
