# Matrix Build with Artifacts - DevOps Challenge

## Overview
This repository demonstrates a GitHub Actions matrix build strategy with artifact management for multi-platform CI/CD pipelines.

## Contact
**Email:** 23f3000704@ds.study.iitm.ac.in

## Workflow Features

### Matrix Configuration
- **Operating Systems:** Ubuntu, macOS, Windows
- **Node.js Versions:** 18, 20
- **Total Matrix Jobs:** 6 parallel builds (3 OS × 2 Node versions)

### Artifacts Generated
Each matrix job generates a unique artifact with the naming pattern:
- `build-badb1f2-linux-node18`
- `build-badb1f2-linux-node20`
- `build-badb1f2-macos-node18`
- `build-badb1f2-macos-node20`
- `build-badb1f2-windows-node18`
- `build-badb1f2-windows-node20`

### Artifact Contents
Each artifact contains:
- `build-info.txt` - Build metadata and configuration
- `manifest.json` - Machine-readable build information

## Workflow Triggers
- Push to `main` or `master` branch
- Pull requests to `main` or `master` branch
- Manual workflow dispatch

## Setup Instructions

1. **Create Repository:**
   ```bash
   mkdir matrix-build-demo
   cd matrix-build-demo
   git init
   ```

2. **Add Workflow File:**
   ```bash
   mkdir -p .github/workflows
   # Copy the workflow YAML to .github/workflows/matrix-build.yml
   ```

3. **Update README:**
   - Replace `your.email@example.com` with your actual email address

4. **Commit and Push:**
   ```bash
   git add .
   git commit -m "Add matrix build workflow"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
   git push -u origin main
   ```

## Validation Checklist
- ✅ At least 3 successful matrix jobs
- ✅ At least 6 artifacts uploaded with prefix `build-badb1f2`
- ✅ All artifacts contain actual content (non-empty)
- ✅ Step identifier `matrix-badb1f2` included
- ✅ README.md contains email address

## Viewing Results
1. Go to your repository on GitHub
2. Click the **Actions** tab
3. Select the latest workflow run
4. View the matrix jobs and their artifacts
5. Download artifacts from the workflow run page

## License
MIT License
