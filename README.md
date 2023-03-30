# Unoffical Dynex Wallet flatpak

WARNING! Still under development.

## Build, Install and Run Flatpak (locally)

Assuming `flatpak`, `flatpak-builder`, and `git` are installed, then execute the following commands:

```shell
$ git clone https://github.com/smithcli/org.dynexcoin.dynex-wallet-app.git
$ cd org.dynexcoin.dynex-wallet-app/
$ flatpak remote-add --if-not-exists --user flathub https://flathub.org/repo/flathub.flatpakrepo
$ flatpak-builder build --force-clean --install-deps-from=flathub --install --user org.dynexcoin.dynex-wallet-app.yaml

# ...to uninstall the artifact
$ flatpak uninstall --delete-data --user org.dynexcoin.dynex-wallet-app

# ...and to clean-up everything
$ rm --force --recursive .flatpak-builder/ build/
$ flatpak uninstall --unused --user
$ flatpak remote-delete --user flathub
```

