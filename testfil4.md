# Getting Started

Security is added to your code repositories in 3 easy steps:

1. Install the Github Apps.
2. Enable the Scanners.
3. Update the Policies.

![3 Steps to Security](assets/first-steps.png)



## Install the GitHub Apps

Installing the GitHub App on your organization enables the `BoostSecurity` service 

* Access the GitHub API
* Insert comments on pull requests 
* Install and update check statuses 
* Enable the CI/CD and Dependabot security checks

In order to install the GitHub App on your GitHub organization, follow these steps:

* Navigate to the Integration view, i.e., in <a href="https://app.boostsecurity.io/settings" target="_blank">`Settings > Integrations`</a>. Select the GitHub integration from the `Available` section
* Select Install: You will be directed to GitHub apps to install the `BoostSecurity` GitHub app.
* Select the appropriate GitHub organization for which you want to install the `BoostSecurity` GitHub app.
* Select whether to install the GitHub App on All `repositories` or `Only select repositories`. It is recommended to install it for all repositories so that it makes it simpler to add the security scanner to new repositories.
* Select `Install and Authorize`.

Once the installation is completed, the `BoostSecurity` GitHub card is added to the `Settings > Integrations > Installed` section. At this point, the `BoostSecurity` GitHub App is installed on your GitHub organization. You might want to enable the CI/CD pipeline configuration security checks and Dependabot security checks. To do so, 

* Go to the installed integration in <a href="https://app.boostsecurity.io/settings" target="_blank">`Settings > Integrations > Installed`</a>.
* Select the GitHub App card.
* Then the Configuration tab. On the configuration line item for your GitHub organization, select the Dependabot and/or CI/CD toggles to turn on security checks

## Enable the Scanners

Once the GitHub App is installed, scanner modules can be configured to run in your organization's repositories. This can be achieved by configuring the `BoostSecurity` scanner modules leveraging the supported continuous Integration (CI) plugins for each repository.

Follow the steps described in [Configure Boost Security](/user-guide/boost-ci.html) continuous Integration (CI) to configure the scanners in your code repositories.

## Update the Policies

Once the required scanners are configured on your code repositories, you can then update or create policies for processing the security events triggered by the scanners with the policy rules required. A **BoostSecurity Policy** you granular control of which security findings are important and how they should be automatically routed to the proper recipients. On the Policy [page](https://app.boostsecurity.io/policy), you can configure what should cause a finding to be a **violation**. Violations are tracked separately in `BoostSecurity` so you can easily see where repositories violate your policy.

The policy also lets you enable actions when violations occur. These actions can alert a developer by

* Adding a comment in a pull request.
* Blocking a pull request from merging. 
* Sending a Slack message to a specific channel - just to name a few.

Refer to the section for how to create or update policies.


## Reviewing the findings

Once `BoostSecurity` data feeds, you can explore the results on the **Findings** [page](https://app.boostsecurity.io/findings).

You can filter and drill down through the [Findings](https://app.boostsecurity.io/findings) using the filters, allowing you to focus on findings from one or more project(s) (i.e., GitHub repositories) or that were triggered by a specific scanner rule, for example.

For each finding on this page, you can see 
* The rule that detected the [Findings](https://app.boostsecurity.io/findings).
* The file path.
* Source code lines where it was found.
* A description , and a link to the documentation explaining why this is an issue and how to address it, and more.

