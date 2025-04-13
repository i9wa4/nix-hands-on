# nix-hands-on

## 1. 参考ページ

1. [Install Nix — nix.dev documentation](https://nix.dev/install-nix)
1. [NixOS と Nix Flakes の紹介](https://zenn.dev/kino_ma/articles/f2a4df384b91a4)
1. [Flakes｜Nix入門](https://zenn.dev/asa1984/books/nix-introduction/viewer/11-flakes)
1. [hercules-ci/gitignore.nix: Nix functions for filtering local git sources](https://github.com/hercules-ci/gitignore.nix)
1. [nix Flakesについて #NixOS - Qiita](https://qiita.com/Sumi-Sumi/items/bee2bba84fee668286e3)
1. [Zero to Nix](https://zero-to-nix.com/)

## 2. 実施した手順

1. このリポジトリをクローンする
1. Nix Flakes の有効化

    ```sh
    mkdir -p ~/.config/nix
    echo "experimental-features = nix-command flakes" >> ~/.config/nix/nix.conf
    ```

1. `nix flake init`
1. `nix run`

    ```sh
    $ nix run
    warning: Git tree '/home/i9wa4/src/github.com/i9wa4/nix-handson' is dirty
    warning: creating lock file '/home/i9wa4/src/github.com/i9wa4/nix-handson/flake.lock':
    • Added input 'nixpkgs':
        'github:nixos/nixpkgs/xxxxxxxxxxxxxxx' (2024-07-08)
    warning: Git tree '/home/i9wa4/src/github.com/i9wa4/nix-handson' is dirty
    Hello, world!
    ```

## 3. 雑多なメモ

```sh
# 使い捨てシェル環境を作り Vim をインストールしてくれる
nix-shell -p vim
```
