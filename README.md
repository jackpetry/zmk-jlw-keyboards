## Instructions
Add this repository to your existing `config/west.yml` as shown below. (No idea what that means? [Make a new repo from this template first](https://github.com/zmkfirmware/unified-zmk-config-template), and [go read the docs](https://zmk.dev/docs/customization#building-additional-keyboards)!)
```yaml
manifest:
  remotes:
    - name: zmkfirmware
      url-base: https://github.com/zmkfirmware
    # Add the base GitHub URL as a remote.
    - name: jlw # You can name this whatever you like; just make sure the "remote" below matches.
      url-base: https://github.com/josh-l-wang
  projects:
    - name: zmk
      remote: zmkfirmware
      revision: main
      import: app/west.yml
    # Add the name of the repository as a project.
    - name: zmk-jlw-keyboards
      remote: jlw
      revision: main # This is the name of the branch you want to use.
  self:
    path: config
```
After making this change, copy any keymaps you may need out of the appropriate board and/or shield folders and paste them into your `config` folder for later modification. Don't forget to [edit your `build.yaml` to include them](https://zmk.dev/docs/customization#building-additional-keyboards), too.

## Further Troubleshooting Resources
- [ZMK's troubleshooting page](https://zmk.dev/docs/troubleshooting)
- Ask the ZMK experts in [ZMK's Discord](https://zmk.dev/community/discord/invite)
