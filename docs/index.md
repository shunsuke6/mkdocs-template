
# mkdocs-template

This repository is my template for the use of mkdocs.

When you do a `git push` against the remote repository, the GitHub Pages will be updated.

## Usage

Using this repository as a template, create a new repository.

Edit `mkdocs.yml`

```bash
site_name: {Arbitrary name}
.
.
theme:
  name: material
  language: "{Your local language}" 
.
plugins:
  search:
    lang: "{Your local language}"
```

Add markdown files to docs.
Then change nav in medocs.yml.

Then you can git push and go to the `https://{github id}.github.io/{repository name}/`

exsample -> [https://shunsuke6.github.io/mkdocs-template/](https://shunsuke6.github.io/mkdocs-template/)

## locally

If you want to run it locally.

### Depend on

- [asdf](https://github.com/asdf-vm/asdf)
  - python
    - mkdocs
  - nodejs
    - markdownlint
    - markdownlint-cli

If your editor is VSCode, Sublime or ccc-Vim(NeoVim) and you are using markdown lint, you can remove the following.

`.tool-versions`> `nodejs 19.0.1`

```bash
rm -f package-lock.json package.json
```

Your remote repository settings.
action>general > Workflow poermission >

- [x] Read and write poermission

Save.

![ ](https://user-images.githubusercontent.com/84017923/215385554-5d43bb8a-18cf-461e-bc59-829036c184d2.png)

### Usage

1. Add asdf plugins.

   ```bash
   asdf plugin-add python
   asdf plugin-add nodejs
   # If need to nodejs
   ```

2. Install asdf plugins.

   ```bash
   asdf install
   ```

3. Install mkdocs using pip.

   ```bash
   pip install --requirement requirements.txt
   ```

4. If you need to markdown lint

   ```bash
   npm install
   ```

5. Local boot with mkdocs.

   ```bash
   mkdocs serve
   ```

   Accessed at [http://127.0.0.1:8000/](http://127.0.0.1:8000/)

6. For manual deployment, run the command

   ```bash
   mkdos gh-deploy
   ```
