# Foreign Packages

Install and update foreign package dependencies (NPM, Yarn, PIP, etc) when a composer project is installed or updated.

## Getting Started

Add the following script commands to your `composer.json`

```json
"scripts": {
    "post-install-cmd": "Proximify\\ForeignPackages::auto",
    "post-update-cmd": "Proximify\\ForeignPackages::auto",
    "post-create-project-cmd": "Proximify\\ForeignPackages::auto"
}
```

Create the file `ForeignPackages.json` under the `settings` folder of your project and define the paths to each type of foreign package. For example,

```json
{
    "src/nodejs": "npm"
}
```

defines the directory `src/nodejs` as an NPM package. When your project is installed, the command `npm install` will be run within this directory. Similarly, when you project is updated, the command `npm update` will be run in that directory.

---

## Contributing

This project welcomes contributions and suggestions. Most contributions require you to agree to a Contributor License Agreement (CLA) declaring that you have the right to and actually do, grant us the rights to use your contribution. For details, visit our [Contributor License Agreement](https://github.com/Proximify/community/blob/master/docs/proximify-contribution-license-agreement.pdf).

When you submit a pull request, we will determine whether you need to provide a CLA and decorate the PR appropriately (e.g., label, comment). Simply follow the instructions provided. You will only need to do this once across all repositories using our CLA.

This project has adopted the [Proximify Open Source Code of Conduct](https://github.com/Proximify/community/blob/master/docs/code_of_conduct.md). For more information see the Code of Conduct FAQ or contact support@proximify.com with any additional questions or comments.

## License

Copyright (c) Proximify Inc. All rights reserved.

Licensed under the [MIT](https://opensource.org/licenses/MIT) license.

**Software component** is made by [Proximify](https://proximify.com). We invite the community to participate.
