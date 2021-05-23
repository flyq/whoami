# sha224test

Welcome to your new sha224test project and to the internet computer development community. By default, creating a new project adds this README and some template files to your project directory. You can edit these template files to customize your project and to include your own code to speed up the development cycle.

To get started, you might want to explore the project directory structure and the default configuration file. Working with this project in your development environment will not affect any production deployment or identity tokens.

To learn more before you start working with sha224test, see the following documentation available online:

- [Quick Start](https://sdk.dfinity.org/docs/quickstart/quickstart-intro.html)
- [SDK Developer Tools](https://sdk.dfinity.org/docs/developers-guide/sdk-guide.html)
- [Motoko Programming Language Guide](https://sdk.dfinity.org/docs/language-guide/motoko.html)
- [Motoko Language Quick Reference](https://sdk.dfinity.org/docs/language-guide/language-manual.html)

If you want to start working on your project right away, you might want to try the following commands:

安装 keysmith， https://github.com/dfinity/keysmith，并生成账号。
```sh
keysmith generate # Generate your mnemonic seed.
keysmith private-key # Derive your private key.
echo {} > dfx.json # Create an empty project.
dfx identity import test identity.pem # Import your private key.
dfx identity use test # Use your private key to sign messages.

keysmith account # 输出 64 位 Hex 字符串，即 account identifier
```

terminal 1:
```sh
cd whoami/

sudo dfx start --clean
```

terminal 2:
```sh

sudo dfx deploy --no-wallet

dfx canister --no-wallet call whoami whoami # 得到的 account identifier 和 keysmith 的一致
```

注意：需要使用一致的账号，可以通过 `dfx identity whoami` 查看是否使用 keysmith 生成并导入的那个账号。