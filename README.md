<header>

<!--
  <<< Author notes: Course header >>>
  Include a 1280×640 image, course title in sentence case, and a concise description in emphasis.
  In your repository settings: enable template repository, add your 1280×640 social image, auto delete head branches.
  Add your open source license, GitHub uses MIT license.
-->

# Secure your repository's supply chain

_Secure your supply chain, understand dependencies in your environment, know about vulnerabilities in those dependencies and patch them._

</header>

## Step 1: Review and add dependencies using dependency graph

_Welcome to "Secure your repository's supply chain"! :wave:_

**What's the big deal about securing your repository's supply chain?**: With the accelerated use of open source, most projects depend on hundreds of open-source dependencies. This poses a security problem: what if the dependencies you're using are vulnerable? You could be putting your users at risk of a supply chain attack. One of the most important things you can do to protect your supply chain is to patch your vulnerable dependencies and replace any malware.

GitHub offers a range of features to help you understand the dependencies in your environment, know about vulnerabilities in those dependencies, and patch them. The supply chain features on GitHub are:

- Dependency graph
- Dependency review
- Dependabot alerts
- Dependabot updates
  - Dependabot security updates
  - Dependabot version updates

**What is a dependency graph**: The dependency graph is a summary of the manifest and lock files stored in a repository and any dependencies that are submitted for the repository using the dependency submission API (beta). For each repository, it shows:

- Dependencies, the ecosystems and packages it depends on
- Dependents, the repositories and packages that depend on it

### :keyboard: Activity 1.1: Verify that dependency graph is enabled

**We recommend opening another browser tab to work through the following activities so you can keep these instructions open for reference.**

Dependency graph is enabled by default for all new public repositories. If you're working in a public repository, you can go straight to "Activity 1.2: Add a new dependency and view your dependency graph." For private or internal repositories, you'll need to enable Dependency graph.

1. Navigate to the **Settings** tab.
1. Click **Code security and analysis**.
1. **Enable** "Dependency graph." 

### :keyboard: Activity 1.2: Add a new dependency and view your dependency graph

1. Navigate to the **Code** tab and locate the `code/src/AttendeeSite` folder.
1. Add the following content to the `package-lock.json` file after the third to last bracket `}` and before the last two brackets.
   ```
   ,
    "follow-redirects": {
      "version": "1.14.1",
      "resolved": "https://registry.npmjs.org/follow-redirects/-/follow-redirects-1.14.1.tgz",
      "integrity": "sha512-HWqDgT7ZEkqRzBvc2s64vSZ/hfOceEol3ac/7tKwzuvEyWx3/4UegXh5oBOIotkGsObyk3xznnSRVADBgWSQVg=="
    }
   ```
1. Navigate to the **Insights** tab.
1. Select **Dependency graph** from the side navigation bar.
1. Review all the dependencies on the **Dependencies** tab.
1. Search for `follow-redirects` and review the new dependency you just added.
   ![Screen Shot showing the "follow-redirects" dependency.](https://user-images.githubusercontent.com/6351798/196288729-734e3319-c5d7-4f35-a19c-676c12f0e27d.png)

Wait about 20 seconds then refresh this page (the one you're following instructions from). [GitHub Actions](https://docs.github.com/en/actions) will automatically update to display the next step.

<footer>

<!--
  <<< Author notes: Footer >>>
  Add a link to get support, GitHub status page, code of conduct, license link.
-->

---

Get help: [Post in our discussion board](https://github.com/skills/.github/discussions) &bull; [Review the GitHub status page](https://www.githubstatus.com/)

&copy; 2024 GitHub &bull; [Code of Conduct](https://www.contributor-covenant.org/version/2/1/code_of_conduct/code_of_conduct.md) &bull; [MIT License](https://gh.io/mit)

</footer>
