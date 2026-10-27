# Security policy

This policy covers every repository in the [dbt-labs](https://github.com/dbt-labs) organization that does not publish its own `SECURITY.md`.

**Do not report security vulnerabilities through public GitHub issues, pull requests, or discussions.**

## Report a vulnerability

- **Code in this organization:** use GitHub private vulnerability reporting on the affected repository. Open its **Security and quality** tab (under **⋯** if hidden) and click **Report a vulnerability**, or go to `https://github.com/dbt-labs/<REPO_NAME>/security/advisories/new`. If no repository fits, use `https://github.com/dbt-labs/.github/security/advisories/new`.
- **dbt platform and dbt Labs websites** (`*.getdbt.com`, `*.dbt.com`, `*.dbtlabs.com`): report through the [Fivetran Bugcrowd program](https://bugcrowd.com/engagements/fivetran-mbb-og), which covers dbt Labs. Its program brief governs those reports, including testing rules, disclosure, and safe harbor.

If a code vulnerability also affects the dbt platform, report the code issue on GitHub and any platform-only impact, such as access to other customers' data, through Bugcrowd.

### What to include

- The affected repository or package, and the version or commit.
- A description of the vulnerability and its impact.
- Steps to reproduce, with a proof of concept if you have one.
- Your suggested severity, if any.
- How you would like to be credited.

## What to expect

For reports made through GitHub private vulnerability reporting:

- **Acknowledgment:** within **10 business days**. If you have not heard from us by then, comment on your advisory.
- **Updates:** at least every **30 business days** until the report is resolved.
- **Disclosure:** we coordinate a disclosure date with you, by default 90 days from the report, adjusted for severity and fix complexity.
- **Advisory and credit:** for confirmed vulnerabilities in released versions, we publish a GitHub Security Advisory and request a CVE where appropriate, crediting you unless you prefer to stay anonymous.

## Scope

In scope: code, CI workflows, and other content in this organization's public repositories, on the default branch and in every release that still receives security fixes (see [dbt version support](https://docs.getdbt.com/docs/dbt-versions/core)).

This includes untrusted input, including files from dependencies, that makes dbt do more than the invoked command is designed to do, such as running a command, writing outside the project, or exposing a credential.

Generally out of scope:

- Models, macros, hooks, and other code from a dbt project or its installed packages doing what dbt is designed to let them do, including reading environment variables with `env_var`, when you run a command that executes that code.
- Vulnerabilities in third-party dependencies without a demonstrated exploit path through our code. Report those upstream.
- Automated scanner or AI-generated output without a verified reproduction and demonstrated impact.
- Example, workshop, and demo repositories, except exposed credentials, CI workflow flaws, and issues that affect anyone beyond the example.
- Denial-of-service testing against our services or others' systems, social engineering, physical attacks, and spam.

## Guidelines and safe harbor

These guidelines and this safe harbor cover research on the code above. The Bugcrowd program brief governs testing of our services.

We ask that you:

- Test only against your own systems, accounts, and data. Stop and report if you access data that is not yours, and do not keep it.
- Do not publish proof-of-concept packages to the dbt package hub or another public registry. Use a local or private package.
- Keep the report confidential until we publish an advisory or the agreed or default disclosure date passes.

We consider security research conducted in good faith under this policy to be authorized, and we will not pursue legal action against you for it. If a third party brings legal action against you for activity that complied with this policy, we will make this authorization known.
