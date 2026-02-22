Awesome Yuescript!
===

Anything and everything related to [Yue](https://github.com/IppClub/Yuescript).

Yuescript started as a [Moonscript](https://github.com/leafo/moonscript) compiler
and has turned into a much better alternative to Lua than Moonscript.

If you haven't checked out Yuescript, check the docs on [yuescript.org](https://yuescript.org)!

Sample from the website:

```moonscript
-- import syntax
import p, to_lua from "yue"

-- object literals
inventory =
  equipment:
    - "sword"
    - "shield"
  items:
    - name: "potion"
      count: 10
    - name: "bread"
      count: 3

-- list comprehension
map = (arr, action) -> [action item for item in *arr]
filter = (arr, cond) -> [item for item in *arr when cond item]
reduce = (arr, init, action): init -> init = action init, item for item in *arr

-- pipe operator
[1, 2, 3]
  |> map (x) -> x * 2
  |> filter (x) -> x > 4
  |> reduce 0, (a, b) -> a + b
  |> print

-- metatable manipulation
apple =
  size: 15
  <index>:
    color: 0x00ffff

with apple
  p .size, .color, .<index> if .<>?

-- js-like export syntax
export 🌛 = "Script of Moon"
```


## ToC

- [Editor Tools](#editor-tools)
- [WASM](#wasm)
- [Tools](#tools)
- [Libraries](#libraries)
- [Game Engines](#game-engines)
- [Love2D](#love2d)
- [Configs](#configs) - software configs written in Yue (yue->lua)
- [Projects](#projects) - projects that use Yue
- [Miscellaneous](#miscellaneous) - miscellaneous things written in yue


## Editor Tools


### vim/neovim

- [yuescript-vim](https://github.com/IppClub/yuescript-vim) - yue support for vim
- [yuecheck-vim](https://github.com/Shados/yuecheck-vim) - ALE integration for yue


### VSCode

- [yuescript-vscode](https://github.com/IppClub/yuescript-vscode) - yue support for VSCode
- [YueRunner](https://github.com/MTadder/YueRunner) - provides YueScript compilation support


### micro

- [yuescript-micro-syntax](https://github.com/SkyyySi/yuescript-micro-syntax) - yue support for [micro](https://github.com/zyedidia/micro)


### emacs

- [yuescript-mode](https://github.com/bkudria/yuescript-mode)


## WASM

- [yuescript.org's wasm](https://github.com/leodev-xyz/yuescript-wasm) copied to GH by @leodev-xyz


## Tools

- [yuepack](https://github.com/Le0Developer/yuepack) - tool for packing YueScript projects into a single file
- [yuecheck](https://github.com/chrsm/yuecheck) - linter and formatter for YueScript


## Libraries

- [leadoc](https://github.com/Le0Developer/leadoc) - write documentation for anything in YueScript
- [moonclass](https://github.com/HTV04/moonclass) - function wrapper for class system
- [pretty](https://github.com/SkyyySi/yuescript-pretty) - pretty printer, written in yue (for yue+lua)
- [yuescript-tokenizer](https://github.com/SkyyySi/yuescript-tokenizer) - simple tokenizer/lexer for yuescript
- ? [libsunshine](https://github.com/SkyyySi/libsunshine) - general purpose/standard library
- [fractional-lua](https://github.com/pmarreck/fractional-lua) - bignum/fraction math library
- [lj4lj](https://github.com/chrsm/lj4lj) - luajit ffi for luajit


## Game Engines

- (archived) [Yuema](https://github.com/megagrump/yuema) - raylib + luajit + yuescript
- [YueCat](https://github.com/RobinsAviary/YueCat) - software development framework, focused on games
- [YASDK](https://github.com/amanitasolanaceae/YASDK) - "Yet Another Stupid Development Kit"


## Love2D

Libraries or projects using Yue and Love2D.

- [weave](https://github.com/chrsm/weave) - wrapper around Love2D's threading
- [behave](https://github.com/chrsm/behave) - behavior tree written for Love2D (doesn't seem love specific)


## Project Templates

- [Playdate](https://github.com/ChildishGiant/playdate-yuescript-template) - Yuescript template for Playdate
- [Tsuki](https://github.com/Kaleidosium/Tsuki) - project template for Love2D
- [yuelove2d](https://github.com/mathisto/yuelove2d) - barebones starter template


## Configs

Configurations for things that use Lua, but in Yuescript

- [@ekickx's neovim config](https://github.com/ekickx/nvim)
- [@LooserName404's neovim config](https://github.com/LooserName404/nvim-config-yue)
- [@dharmx's awesome config](https://github.com/dharmx/awesome)
- [@thyvini's neovim config](https://github.com/thyvini/nvim-config-yue)
- [@SkyyySi's awesomewm config](https://github.com/SkyyySi/awesome-yuescript)
- [@chrsm's neovim config](https://github.com/chrsm/dotfiles/tree/master/neovim/.config/nvim)


## Projects

Projects that use Yue.

- [Dorothy SSR](https://github.com/IppClub/Dora-SSR) - platformer by by Yuescript's creator
- [Yuescript-GTKTests](https://github.com/JeysonFlores/YuescriptGTKTests) - GTK test snippets in Yue
- [yuescript-src-rs](https://github.com/Tarik02/yuescript-src-rs) mLua+yuescript (rust)
- [yuescript-mlua](https://github.com/khvzak/yuescript-mlua) - mLua+yuescript (rust)
- [fir](https://github.com/daelvn/fir) - language-agnostic documentation generator
- [gm_moonloader](https://github.com/Pika-Software/gm_moonloader) - integration of Yuescript + MoonScript into Garry's
  Mod
- [YueLovePlatformer](https://github.com/mathisto/YueLovePlatformer)
- [luapack](https://github.com/Le0Developer/luapack) - tool for packing multiple Lua files into one


## Miscellaneous

- [@bartek-bartlomiej's advent-of-code](https://github.com/bartek-bartlomiej/advent-of-code-in-moonscript)
- [100-languages-speedrun](https://github.com/taw/100-languages-speedrun/tree/master/episode-90-yuescript) - examples of
  yue
- [impulse.nvim](https://github.com/chrsm/impulse.nvim) - Neovim notion.so plugin built in yue
- [YuescriptMemo](https://github.com/muu2007/YuescriptMemo) - Japanese notes on YueScript
- [net-transfer](https://github.com/unknown-gd/net-transfer) - send/receive large data/files (Garry's Mod?)
