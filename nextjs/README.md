# Next.js Dockerfile

This Dockerfile is intended for a standalone Next.js project, not for a monorepo setup (e.g., with Turborepo).

## Docker Usage

This dockerfile include a multi-stage Dockerfile for building and running the Next.js application in production. The resulting image is optimized for size and typically weighs around 350-400MB for a basic Next.js project.

### Prerequisites
- Docker installed on your system
- The project must be configured to run in standalone mode

### Next.js Standalone Configuration

To use this Dockerfile, ensure your `next.config.mjs` includes the standalone output:
```mjs
/** @type {import('next').NextConfig} */
const nextConfig = {
  mode: "standalone"
};

export default nextConfig;
```
