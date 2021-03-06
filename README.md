# File-storage action

> Store files on an orphan branch of a repo dedicated for static storage

## ⭐ Features

- Save files on a separate branch
- Specify a custom commit message on save
- Customize `storage-branch` name

## 🚀 Quickstart

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

Badge generated in this action can then be referenced from your README or anywhere else...


## 📗 Parameters

|Name|Function|
|-|-|
|src|Relative or absolute path to the file that must be saved in storage-branch|
|dst|Path relative to storage branch root where the file (or folder) will be stored. If destination folder doesn't exists it is automatically created.|
|storage-branch|Name of the branch used as storage branch (defaults to 'gh-storage', you can have multiple in differents jobs).|
|comment|Message that will be used to document commit associated with this change.|

## 🔥 Roadmap

- Automated tests
