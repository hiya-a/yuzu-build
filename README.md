# yuzu-build
Merge yuzu's 'early-access-merge' and 'mainline-merge' pr to master branch.

The build process is completely transparent, with source code from the official yuzu repo.

Download build from ['Action'](https://github.com/alexkiri/yuzu-build/actions) tab, in the "Artifacts" section of a finished action, or from the ['Releases'](https://github.com/alexkiri/yuzu-build/releases) section

# Additional functionality
The workflow includes logic that can make the build include various cmake flags, apply custom compilation flags as well as apply custom fixes in the form of `.patch` files. There are now 2 folders, 
`optionalPatches` and `defaultPatches`. The optional ones are applied based on the input flags of the workflow, the default ones are applied regardless. In this way, you can include your own patch file(s) in the `defaultPatches` folder, and they will be applied automatically without any changes to the workflow. The rest of the flags are configurable as inputs in the action workflow.
## Tips
- This workflow will release build files with 'release' tag. If you want to release files,please go to repo's setting → Action → General → Workflow permissions, choose 'Read and write permissions' and click 'save'. If you don't want to do this, just ignore the error about release failed.

