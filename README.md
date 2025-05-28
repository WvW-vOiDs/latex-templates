## 说明

个人使用的 LaTeX 模板, 包括 beamer, lecture note 等. 大部分内容都是基于已有项目修改而来, 具体见 Acknowledgement 部分.


## Usage

### 注意事项

- 使用 `xelatex` 编译.
- 使用 `\sym...` 代替 `\math...`. (如 `\symbb{R}` 代替 `\mathbb{R}`. 详见 [unicode-math 宏包文档](http://mirrors.ctan.org/macros/unicodetex/latex/unicode-math/unicode-math.pdf))


## 其他

### 资源下载

如果你想从各个项目中下载原资源, 可以按照下面的步骤操作.

1. shared/fonts/FiraMath

```bash
wget -q https://github.com/firamath/firamath/releases/download/v0.3.4/FiraMath-Regular.otf # 本项目使用的版本

mkdir -p ./shared/fonts/FiraMath && mv FiraMath-Regular.otf shared/fonts/FiraMath/
```

2. shared/fonts/LXGWBright

```bash
# wget -q https://github.com/lxgw/LxgwBright/raw/v5.517/LXGWBright/LXGWBright-Regular.ttf https://github.com/lxgw/LxgwBright/raw/v5.517/LXGWBright/LXGWBright-MediumItalic.ttf https://github.com/lxgw/LxgwBright/raw/v5.517/LXGWBright/LXGWBright-Medium.ttf https://github.com/lxgw/LxgwBright/raw/v5.517/LXGWBright/LXGWBright-Italic.ttf # 本项目使用的版本
wget -q https://github.com/lxgw/LxgwBright/raw/main/LXGWBright/LXGWBright-Regular.ttf https://github.com/lxgw/LxgwBright/raw/main/LXGWBright/LXGWBright-MediumItalic.ttf https://github.com/lxgw/LxgwBright/raw/main/LXGWBright/LXGWBright-Medium.ttf https://github.com/lxgw/LxgwBright/raw/main/LXGWBright/LXGWBright-Italic.ttf

mkdir -p shared/fonts/LXGWBright && mv LXGWBright-*.ttf shared/fonts/LXGWBright/
```

3. shared/fonts/SarasaTermSCNerd

```bash
# wget -q https://github.com/laishulu/Sarasa-Term-SC-Nerd/releases/download/v2.3.1/SarasaTermSCNerd.ttf.tar.gz # 本项目使用的版本
wget -q https://github.com/laishulu/Sarasa-Term-SC-Nerd/releases/latest/download/SarasaTermSCNerd.ttf.tar.gz

tar -xzvf SarasaTermSCNerd.ttf.tar.gz \
    --wildcards \
    "SarasaTermSCNerd-Bold.ttf" \
    "SarasaTermSCNerd-BoldItalic.ttf" \
    "SarasaTermSCNerd-Italic.ttf" \
    "SarasaTermSCNerd-Regular.ttf"

mkdir -p shared/fonts/SarasaTermSCNerd && mv SarasaTermSCNerd-Bold.ttf SarasaTermSCNerd-BoldItalic.ttf SarasaTermSCNerd-Italic.ttf SarasaTermSCNerd-Regular.ttf shared/fonts/SarasaTermSCNerd/

rm -f SarasaTermSCNerd.ttf.tar.gz
```

4. shared/themes/Catppuccin

```bash
git clone --depth 1 https://github.com/atticus-sullivan/beamercolortheme.git

cd beamercolortheme && l3build unpack && cd ..

mkdir -p shared/themes/Catppuccin && mv beamercolortheme/build/unpacked/beamercolorthemecatppuccin.sty shared/themes/Catppuccin/

rm -rf beamercolortheme
```
