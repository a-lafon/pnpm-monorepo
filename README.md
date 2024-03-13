This repository serves as a demonstration and testbed for utilizing a monorepo structure with PNPM as the package manager. The aim is to explore the benefits of managing multiple related projects within a single repository and leveraging PNPM's features for efficient dependency management.

## Features
- Monorepo Structure: All related projects are organized within a single repository.
- PNPM Integration: Utilizing PNPM for package management to optimize dependency resolution and disk space usage.
- Demo Projects: Includes sample projects to demonstrate interdependency and shared packages within the monorepo.

## Getting Started

Install PNPM:
```bash
npm install -g pnpm
```

Navigate to the root directory of the cloned repository and install dependencies for all projects using PNPM:
```bash
pnpm install
```

## Commands

```bash
pnpm --filter <package-name> <command>
```

Install package example:
```bash
pnpm add --filter shared-ui react
```

Add local dependency to workspace:
```bash
pnpm add shared-ui --filter my-remix-app --workspace
```

Start remix:
```bash
pnpm --filter my-remix-app dev
```

Run command recursively using the -r flag
```bash
pnpm run -r build
```

Parallelize the run by using --parallel
```bash
pnpm run --parallel -r build
```
