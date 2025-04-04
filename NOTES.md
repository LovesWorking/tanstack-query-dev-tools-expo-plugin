# Terminal 1

cd react-query-clone/packages/query-devtools
pnpm build:dev & (while true; do yalc push --changed; sleep 2; done)

# Terminal 2

cd react-query-clone/packages/react-query-devtools
pnpm build:dev & (while true; do yalc push --changed; sleep 2; done)

# Web Tools

yalc add @tanstack/query-devtools --watch
yalc add @tanstack/react-query-devtools --watch

# Make sure to modify html src after build to include all js files.

@dist/index.html - Add js scripts from @dist/\_expo/static/js

# Build

cd packages/react-query-devtools
pnpm build

# pack

pnpm pack
