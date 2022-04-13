# cra-script-nomod
This package is monorepo of react-scripts@5.0.0
##### It will create react app using given template without copying over `node_modules`, `package.json`, `package-lock.json`, `yarn.lock`, `.env.development` and `.env` from template folder.
#
#
##### `.env` and `.env.development` entries can be dynamically added in `template.json` of custom cra template 
This way developers can work on custom cra templates without worrying about deleting installed packages in template folder for development purposes

#### Useage with create-react-app
```sh
yarn create react-app myapp --scripts-version cra-script-nomod 
```
##### _OR_
#
#
```sh
npx create-react-app myapp --scripts-version cra-script-nomod 
```

#### Adding .env and .env.development
Customize cra-template `template.json`
```sh
{
    "package": {
        "dependencies":{
            ...
        },
        "devDependencies":{
            ...
        }
    },
    "env":{
        "REACT_APP_API_URL" : "https://example.com/api"
    },
    "envDevelopment":{
        "REACT_APP_DEVELOPMENT_API_URL" : "https://example.com/api"
    },
}
```

This package includes scripts and configuration used by [Create React App](https://github.com/facebook/create-react-app).<br>     
Please refer to its documentation:

- [Getting Started](https://facebook.github.io/create-react-app/docs/getting-started) – How to create a new app.
- [User Guide](https://facebook.github.io/create-react-app/) – How to develop apps bootstrapped with Create React App.

#
#

`Monorepo created by cloning create-react-app and using`
```sh
git filter-branch –prune-empty –subdirectory-filter packages/react-scripts main
```

## License

MIT
