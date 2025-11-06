# GitHub Pages Setup Instructions

After merging this PR, follow these steps to enable GitHub Pages for this repository:

## Enable GitHub Pages

1. Go to your repository on GitHub: https://github.com/B-Wie/test_sphinx_documentation_deploy

2. Click on **Settings** (⚙️) in the top navigation bar

3. In the left sidebar, scroll down and click on **Pages** (under "Code and automation")

4. Under **Build and deployment**:
   - **Source**: Select "Deploy from a branch"
   - **Branch**: Select `gh-pages` and `/ (root)`
   - Click **Save**

5. Wait a few minutes for the initial deployment to complete

6. Your documentation will be available at:
   ```
   https://b-wie.github.io/test_sphinx_documentation_deploy/
   ```

## Verify Deployment

After the GitHub Actions workflow runs successfully:

1. Check the **Actions** tab to ensure the "Deploy Sphinx Documentation" workflow completed successfully

2. Visit your documentation URL: https://b-wie.github.io/test_sphinx_documentation_deploy/

3. You should see the Sphinx documentation homepage

## Automatic Updates

Once set up, the documentation will automatically rebuild and redeploy whenever you:
- Push changes to the `main` or `master` branch
- Manually trigger the workflow from the Actions tab

## Troubleshooting

### Documentation not updating
- Check the Actions tab for failed workflows
- Ensure the `gh-pages` branch exists and is set as the Pages source
- Check that GitHub Pages is enabled in repository settings

### 404 Error
- Wait a few minutes after the first deployment
- Verify the `gh-pages` branch has content
- Check that the Pages settings are configured correctly

### Build Failures
- Review the workflow logs in the Actions tab
- Ensure all dependencies in `requirements.txt` are correct
- Verify Sphinx configuration in `docs/source/conf.py` is valid

## Customization

To customize the documentation:
1. Edit files in `docs/source/`
2. Modify `docs/source/conf.py` to change theme, extensions, or settings
3. Push changes to trigger automatic rebuild and deployment
