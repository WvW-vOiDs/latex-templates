## Usage

### assets download

如果你想从各个原项目中得到资源, 你可以按照下面的步骤操作.

1. assets/fonts/FiraMath

```bash
wget -q https://github.com/firamath/firamath/releases/download/v0.3.4/FiraMath-Regular.otf # 本项目使用的版本

mkdir -p ./assets/fonts/FiraMath && mv FiraMath-Regular.otf assets/fonts/FiraMath/
```

2. assets/fonts/LXGWBright

```bash
# wget -q https://github.com/lxgw/LxgwBright/raw/v5.517/LXGWBright/LXGWBright-Regular.ttf https://github.com/lxgw/LxgwBright/raw/v5.517/LXGWBright/LXGWBright-MediumItalic.ttf https://github.com/lxgw/LxgwBright/raw/v5.517/LXGWBright/LXGWBright-Medium.ttf https://github.com/lxgw/LxgwBright/raw/v5.517/LXGWBright/LXGWBright-Italic.ttf # 本项目使用的版本
wget -q https://github.com/lxgw/LxgwBright/raw/main/LXGWBright/LXGWBright-Regular.ttf https://github.com/lxgw/LxgwBright/raw/main/LXGWBright/LXGWBright-MediumItalic.ttf https://github.com/lxgw/LxgwBright/raw/main/LXGWBright/LXGWBright-Medium.ttf https://github.com/lxgw/LxgwBright/raw/main/LXGWBright/LXGWBright-Italic.ttf

mkdir -p assets/fonts/LXGWBright && mv LXGWBright-*.ttf assets/fonts/LXGWBright/
```

3. assets/fonts/SarasaTermSCNerd

```bash
# wget -q https://github.com/laishulu/Sarasa-Term-SC-Nerd/releases/download/v2.3.1/SarasaTermSCNerd.ttf.tar.gz # 本项目使用的版本
wget -q https://github.com/laishulu/Sarasa-Term-SC-Nerd/releases/latest/download/SarasaTermSCNerd.ttf.tar.gz

tar -xvf SarasaTermSCNerd.ttf.tar.gz

mkdir -p assets/fonts/SarasaTermSCNerd && mv SarasaTermSCNerd-Bold.ttf SarasaTermSCNerd-BoldItalic.ttf SarasaTermSCNerd-Italic.ttf SarasaTermSCNerd-Regular.ttf assets/fonts/SarasaTermSCNerd/

rm -f SarasaTermSCNerd*
```

4. assets/themes/Catppuccin

```bash
git clone --depth 1 https://github.com/atticus-sullivan/beamercolortheme.git

cd beamercolortheme && l3build unpack && cd ..

mkdir -p assets/themes/Catppuccin && mv beamercolortheme/build/unpacked/beamercolorthemecatppuccin.sty assets/themes/Catppuccin/

rm -rf beamercolortheme
```

### 注意事项

- 你需要使用 `xelatex` 或 `lualatex` 来编译这个模板.
- 你应该使用 `\sym...` 来代替 `\math...` 来使用数学符号. (如 `\symbb{R}` 代替 `\mathbb{R}`. 详见 [unicode-math 宏包文档](http://mirrors.ctan.org/macros/unicodetex/latex/unicode-math/unicode-math.pdf))