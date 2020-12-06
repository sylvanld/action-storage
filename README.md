# action-storage
Store files on an orphan branch of a repo dedicated for static storage

```yaml
      # Generate an asset in your job. E.G: Download a badge image from shields.io
      - name: Download a badge file
        run: wget https://img.shields.io/badge/license-MIT-red
      
      # Store this asset in 'gh-storage' branch.
      - name: Save file in a new orphan storage branch
        uses: sylvanld/action-storage@v1
        with:
          src: license-MIT-blue
          dst: legal/LICENSE
```
