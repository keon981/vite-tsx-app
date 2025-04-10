# keon-starter  ()

Example project to showcase how to build your own `create-keon-app` npx starter template.

> [React + TS + Vite + Shadcn/ui Template](./template/README.md)


## Getting Started

1. Clone this repository:
   ```bash
   git clone git@github.com:keon981/vite-tsx-app.git
   ```

2. Install and start a local Verdaccio server (if you haven't already):
   ```bash
   pnpm add -g verdaccio
   verdaccio
   ```

3. In a separate terminal, publish the CLI package to your local Verdaccio:
   ```bash
   cd vite-react-starter &&\
   pnpm run publish:local
   ```

4. Now you can scaffold a new project using:
   ```bash
   pnpm dlx vite-starter new-app
   ```

## License

No License. You can use this starter as you wish.
