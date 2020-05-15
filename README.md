# erlvm

Erlvm is a erlang version manager tool.It helps to install any version of erlang from source code and switch version conveniently.

## Usage

1. cp `erlvm` script to `$PATH`.
2. exec `erlvm init` in command line to initialize erlvm path, default in `$HOME/.erlvm/`.
   It can be changed by `export erlvm_root_path=OTHER_PATH` in ~/.bashrc.
3. exec `erlvm install 23.0` to download and install otp_23.0 to `$HOME/.erlvm/ver/`.
4. exec `erlvm use 23.0` to set the 23.0 as current version.
5. write `export PATH=$HOME/.erlvm/bin:$PATH` to ~/.bashrc.

## Directory Struct

```bash
$HOME/.erlvm/
├── bin -> $HOME/.erlvm/ver/otp_21.1/bin
├── pkg
│   ├── otp_src_21.1/
│   ├── otp_src_21.1.tar.gz
│   ├── otp_src_22.3/
│   └── otp_src_22.3.tar.gz
└── ver
    ├── otp_21.1/
    └── otp_22.3/
```

`ver/` maintain all installed otp version.
`pkg/` cache downloaded source code packet.
`bin/` is a link point to one version path in `ver/*/bin`, switch version actually change this link pointer.

## Other

More information can be got from `erlvm help` commond.
