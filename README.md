# DEPRECATED

> Please use this instead: https://github.com/mlabs-haskell/mlabs-tooling.nix/blob/main/mk-hackage.nix

Add dependencies to haskell.nix project via `extra-hackages` and `extra-hackage-tarballs`.


```nix
let
  myHackages = mkHackagesFor system compiler-nix-name [ ./mydep ./mydepdep ];
in
cabalProject {
  inherit (myHackages) extra-hackages extra-hackage-tarballs modules;
  # ...
};
```
