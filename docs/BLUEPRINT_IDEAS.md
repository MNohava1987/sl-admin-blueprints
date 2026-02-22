# Blueprint Ideas Backlog

Use this file as a lightweight backlog for blueprint candidates.

## Blueprint Template

- `name`: short blueprint id.
- `problem`: what manual or risky step it removes.
- `inputs`: required user inputs.
- `actions`: what resources it creates/updates.
- `outputs`: what IDs/URLs/paths it returns.
- `guardrails`: validations, naming constraints, policy requirements.
- `status`: draft, approved, in-progress, implemented.

## Candidate Ideas

### `admin-tool-onboarding`

- `problem`: onboarding new admin tooling is repetitive and can drift from standards.
- `inputs`: tool name, repository name, environment target, assurance tier, default branch, owner team.
- `actions`: creates or initializes tool repo, seeds baseline Terraform/docs, creates stack, attaches repo, sets labels, applies RBAC, injects required context vars.
- `outputs`: created repo URL, stack ID/slug, PR link for manifest registration.
- `guardrails`: enforce naming convention, required labels, required branch strategy, deletion protection defaults.
- `status`: draft

### `customer-tenant-bootstrap`

- `problem`: customer stack setup across dev/test/prod is manual and inconsistent.
- `inputs`: customer slug, repo name, branch mapping, assurance tier, parent space.
- `actions`: creates customer space tree, creates dev/test/prod stacks, applies labels and policies, attaches repo/branches.
- `outputs`: space IDs, stack IDs, onboarding checklist.
- `guardrails`: case-insensitive uniqueness and label policy compliance.
- `status`: draft

### `policy-pack-rollout`

- `problem`: policy distribution across existing stacks is hard to standardize.
- `inputs`: policy pack name, target selector labels, enforcement mode.
- `actions`: creates/updates policy artifacts and attaches them to matching stacks or spaces.
- `outputs`: attachment summary and exceptions.
- `guardrails`: deny unknown enforcement modes and require rollback plan.
- `status`: draft
