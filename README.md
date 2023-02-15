# vite_fluentv9_issue
minimal reproduction required to report a bug/issue

# system info
```
* WSL2 *
  System:
    OS: Linux 5.10 Ubuntu 20.04.5 LTS (Focal Fossa)
    CPU: (2) x64 Intel(R) Core(TM) i5-8365U CPU @ 1.60GHz
    Memory: 15.56 GB / 19.54 GB
    Container: Yes
    Shell: 5.0.17 - /bin/bash
```

user@wsl2ubuntu:$ npm create vite@latest brand_new_project -- --template react-ts
```
Scaffolding project in /home/localnar/github/brand_new_project...

Done. Now run:

  cd brand_new_project
  npm install
  npm run dev
```
user@wsl2ubuntu:$ cd brand_new_project/
user@wsl2ubuntu:brand_new_project$ npm install
```
added 83 packages, and audited 84 packages in 23s

8 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities
```
user@wsl2ubuntu:brand_new_project$
user@wsl2ubuntu:brand_new_project$ npm install @fluentui/react-components
```
npm WARN ERESOLVE overriding peer dependency
npm WARN ERESOLVE overriding peer dependency
npm WARN ERESOLVE overriding peer dependency
npm WARN ERESOLVE overriding peer dependency

added 63 packages, changed 1 package, and audited 147 packages in 26s

8 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities
```
user@wsl2ubuntu:brand_new_project$


# logs:

```
npm WARN ERESOLVE overriding peer dependency
npm WARN While resolving: @fluentui/react-virtualizer@9.0.0-alpha.6
npm WARN Found: @types/react@18.0.28
npm WARN node_modules/@types/react
npm WARN   dev @types/react@"^18.0.28" from the root project
npm WARN   44 more (@fluentui/react-accordion, @fluentui/react-alert, ...)
npm WARN
npm WARN Could not resolve dependency:
npm WARN peer @types/react@">=16.8.0 <18.0.0" from @fluentui/react-virtualizer@9.0.0-alpha.6
npm WARN node_modules/@fluentui/react-components/node_modules/@fluentui/react-virtualizer
npm WARN   @fluentui/react-virtualizer@"9.0.0-alpha.6" from @fluentui/react-components@9.15.3
npm WARN   node_modules/@fluentui/react-components
npm WARN
npm WARN Conflicting peer dependency: @types/react@17.0.53
npm WARN node_modules/@types/react
npm WARN   peer @types/react@">=16.8.0 <18.0.0" from @fluentui/react-virtualizer@9.0.0-alpha.6
npm WARN   node_modules/@fluentui/react-components/node_modules/@fluentui/react-virtualizer
npm WARN     @fluentui/react-virtualizer@"9.0.0-alpha.6" from @fluentui/react-components@9.15.3
npm WARN     node_modules/@fluentui/react-components
npm WARN ERESOLVE overriding peer dependency
npm WARN While resolving: @fluentui/react-virtualizer@9.0.0-alpha.6
npm WARN Found: @types/react-dom@18.0.11
npm WARN node_modules/@types/react-dom
npm WARN   dev @types/react-dom@"^18.0.11" from the root project
npm WARN   41 more (@fluentui/react-accordion, @fluentui/react-alert, ...)
npm WARN
npm WARN Could not resolve dependency:
npm WARN peer @types/react-dom@">=16.8.0 <18.0.0" from @fluentui/react-virtualizer@9.0.0-alpha.6
npm WARN node_modules/@fluentui/react-components/node_modules/@fluentui/react-virtualizer
npm WARN   @fluentui/react-virtualizer@"9.0.0-alpha.6" from @fluentui/react-components@9.15.3
npm WARN   node_modules/@fluentui/react-components
npm WARN
npm WARN Conflicting peer dependency: @types/react-dom@17.0.19
npm WARN node_modules/@types/react-dom
npm WARN   peer @types/react-dom@">=16.8.0 <18.0.0" from @fluentui/react-virtualizer@9.0.0-alpha.6
npm WARN   node_modules/@fluentui/react-components/node_modules/@fluentui/react-virtualizer
npm WARN     @fluentui/react-virtualizer@"9.0.0-alpha.6" from @fluentui/react-components@9.15.3
npm WARN     node_modules/@fluentui/react-components
npm WARN ERESOLVE overriding peer dependency
npm WARN While resolving: @fluentui/react-virtualizer@9.0.0-alpha.6
npm WARN Found: react@18.2.0
npm WARN node_modules/react
npm WARN   react@"^18.2.0" from the root project
npm WARN   48 more (@fluentui/react-accordion, @fluentui/react-alert, ...)
npm WARN
npm WARN Could not resolve dependency:
npm WARN peer react@">=16.8.0 <18.0.0" from @fluentui/react-virtualizer@9.0.0-alpha.6
npm WARN node_modules/@fluentui/react-components/node_modules/@fluentui/react-virtualizer
npm WARN   @fluentui/react-virtualizer@"9.0.0-alpha.6" from @fluentui/react-components@9.15.3
npm WARN   node_modules/@fluentui/react-components
npm WARN
npm WARN Conflicting peer dependency: react@17.0.2
npm WARN node_modules/react
npm WARN   peer react@">=16.8.0 <18.0.0" from @fluentui/react-virtualizer@9.0.0-alpha.6
npm WARN   node_modules/@fluentui/react-components/node_modules/@fluentui/react-virtualizer
npm WARN     @fluentui/react-virtualizer@"9.0.0-alpha.6" from @fluentui/react-components@9.15.3
npm WARN     node_modules/@fluentui/react-components
npm WARN ERESOLVE overriding peer dependency
npm WARN While resolving: @fluentui/react-virtualizer@9.0.0-alpha.6
npm WARN Found: react-dom@18.2.0
npm WARN node_modules/react-dom
npm WARN   react-dom@"^18.2.0" from the root project
npm WARN   42 more (@fluentui/react-accordion, @fluentui/react-alert, ...)
npm WARN
npm WARN Could not resolve dependency:
npm WARN peer react-dom@">=16.8.0 <18.0.0" from @fluentui/react-virtualizer@9.0.0-alpha.6
npm WARN node_modules/@fluentui/react-components/node_modules/@fluentui/react-virtualizer
npm WARN   @fluentui/react-virtualizer@"9.0.0-alpha.6" from @fluentui/react-components@9.15.3
npm WARN   node_modules/@fluentui/react-components
npm WARN
npm WARN Conflicting peer dependency: react-dom@17.0.2
npm WARN node_modules/react-dom
npm WARN   peer react-dom@">=16.8.0 <18.0.0" from @fluentui/react-virtualizer@9.0.0-alpha.6
npm WARN   node_modules/@fluentui/react-components/node_modules/@fluentui/react-virtualizer
npm WARN     @fluentui/react-virtualizer@"9.0.0-alpha.6" from @fluentui/react-components@9.15.3
npm WARN     node_modules/@fluentui/react-components
```


package.json
```json
{
  "name": "brand_new_project",
  "private": true,
  "version": "0.0.0",
  "type": "module",
  "scripts": {
    "dev": "vite",
    "build": "tsc && vite build",
    "preview": "vite preview"
  },
  "dependencies": {
    "@fluentui/react-components": "^9.15.3",
    "react": "^18.2.0",
    "react-dom": "^18.2.0"
  },
  "devDependencies": {
    "@types/react": "^18.0.27",
    "@types/react-dom": "^18.0.10",
    "@vitejs/plugin-react": "^3.1.0",
    "typescript": "^4.9.3",
    "vite": "^4.1.0"
  }
}

```
