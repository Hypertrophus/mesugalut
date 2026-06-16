# Deploy Instructions (Netlify + GitHub)

Use this exact flow whenever you want your changes live.

## 1) Standard deploy flow

```powershell
# from project root
Set-Location "z:\Landing page - Autism 2026"

# optional: check what changed
git status --short

# commit your changes
git add -A
git commit -m "Describe your change"

# push to the branch Netlify watches
git push origin testing1.1
```

Netlify should auto-deploy after push.

## 2) If push is rejected (non-fast-forward)

Error looks like: `rejected (fetch first)`.

```powershell
Set-Location "z:\Landing page - Autism 2026"

# bring remote changes and replay your commit on top
git pull --rebase origin testing1.1
```

If there are conflicts:

1. Open conflicted files.
2. Remove conflict markers: `<<<<<<<`, `=======`, `>>>>>>>`.
3. Keep the correct final content.
4. Stage resolved files.

```powershell
# after conflict edits
git add -A
git rebase --continue

# if more conflicts appear, repeat edit + add + rebase --continue

# when rebase finishes, push again
git push origin testing1.1
```

## 3) Verify live deploy

1. Open Netlify dashboard -> Deploys.
2. Confirm latest deploy is from branch `testing1.1` and status is `Published`.
3. Hard refresh browser: `Ctrl+F5`.

Useful URLs:
- Home: `https://heroic-pothos-633a94.netlify.app/`
- Blog page: `https://heroic-pothos-633a94.netlify.app/blog/`
- Example article: `https://heroic-pothos-633a94.netlify.app/posts/article1/`

## 4) If Netlify did not deploy automatically

In Netlify:
1. Go to Deploys.
2. Click `Trigger deploy`.
3. Choose `Clear cache and deploy site`.

## 5) Optional local build check before push

```powershell
Set-Location "z:\Landing page - Autism 2026"
npx @11ty/eleventy
```

If build succeeds, `_site` is generated correctly.
