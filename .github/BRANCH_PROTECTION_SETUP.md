# Branch Protection Setup Guide

This guide explains how to set up branch protection rules for this repository to ensure that only authorized personnel can commit changes.

## Quick Setup

To enable branch protection for this repository, follow these steps:

### 1. Navigate to Branch Protection Settings

1. Go to the repository on GitHub: https://github.com/BnB-GSorg/URFallTraining2025
2. Click on **Settings** (requires admin access)
3. In the left sidebar, click on **Branches**
4. Under "Branch protection rules", click **Add rule** or **Add classic branch protection rule**

### 2. Configure Protection for Main Branch

Enter the branch name pattern: `main` (or `master` if that's your default branch)

### 3. Recommended Protection Settings

Enable the following settings:

#### Required Settings for Permission Control:
- ✅ **Require a pull request before merging**
  - ✅ **Require approvals** (set to at least 1)
  - ✅ **Dismiss stale pull request approvals when new commits are pushed**
  - ✅ **Require review from Code Owners** (This uses the CODEOWNERS file)
  
- ✅ **Require status checks to pass before merging**
  - Select any CI/CD checks you want to run

- ✅ **Require conversation resolution before merging**
  - Ensures all comments are addressed

- ✅ **Require signed commits** (Optional but recommended for security)

- ✅ **Require linear history** (Optional - prevents merge commits)

- ✅ **Do not allow bypassing the above settings**
  - This prevents even administrators from bypassing the rules

#### Additional Restrictions:
- ✅ **Lock branch** - Makes the branch read-only (Only if you want to completely prevent direct commits)
- ✅ **Restrict who can push to matching branches**
  - Leave empty or add specific users/teams who can push directly
  - For maximum protection, leave this empty so nobody can push directly

### 4. Apply Protection to Other Branches (Optional)

You can also protect other branches:
- Pattern: `develop` - for development branch
- Pattern: `release/*` - for all release branches
- Pattern: `*` - for all branches (very restrictive)

## How It Works

### With CODEOWNERS File
The CODEOWNERS file in `.github/CODEOWNERS` specifies that all files (`*`) require approval from `@BnB-GSorg`.

When "Require review from Code Owners" is enabled:
- All pull requests must be reviewed and approved by the code owner
- Direct pushes to protected branches are blocked
- All changes must go through the pull request workflow

### Workflow for Contributors
1. Contributors create a new branch for their changes
2. They make commits to their branch
3. They open a pull request to merge into the protected branch
4. The repository owner (code owner) reviews and approves the changes
5. Only after approval can the changes be merged

## Testing the Setup

After enabling branch protection:

1. Try to push directly to the main branch - it should be rejected
2. Create a new branch, make changes, and open a pull request
3. Verify that the pull request requires your approval before merging

## Troubleshooting

### "I can't push to the main branch anymore"
This is expected! All changes must now go through pull requests.

### "The merge button is disabled"
Check that:
- All required approvals are provided
- All status checks have passed
- All conversations are resolved

### "I need to make an urgent fix"
If you need to bypass protection temporarily:
- Go to Settings > Branches
- Edit the branch protection rule
- Temporarily disable it or allow administrators to bypass
- Make your change
- Re-enable the protection

## Security Best Practices

1. **Never disable branch protection** except in emergencies
2. **Review all pull requests carefully** before approving
3. **Enable signed commits** to verify commit authenticity
4. **Keep the CODEOWNERS file updated** as team membership changes
5. **Use status checks** (CI/CD) to automatically verify code quality

## Additional Resources

- [GitHub Branch Protection Documentation](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/defining-the-mergeability-of-pull-requests/about-protected-branches)
- [GitHub Code Owners Documentation](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-code-owners)
- [Pull Request Reviews](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/reviewing-changes-in-pull-requests/about-pull-request-reviews)
