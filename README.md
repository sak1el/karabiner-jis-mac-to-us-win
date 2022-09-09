# Karabiner-jis-mac-to-us-win

JIS配列M1 MacBook AirをUS配列のWindowsっぽく操作するためのkarabiner設定ファイル

## やりたいこと

- `Command`キーをWindowsで言う`Ctrl`キーっぽく使うため左下に持っていきたい
- JIS配列M1 MacBook Airは[`1`]の横にキーがなく[`~`]が入力できないので余っている[`_`]の位置に退避したい
- `Shift+CapsLock`でIMEのON/OFFを制御したい
- `CapsLock`でCapsLockのON/OFFを制御したい
- ターミナルエミュレータ使用時は`Command`キーを`Ctrl`キーに変換したい
- Windows用の外部キーボード接続時もできるだけ違和感なく操作したい

## Simple Modifications

### MacBook内蔵キーボード

| 物理キー         | 割り当て                | メモ                    |
| ---------------- | ----------------------- | ----------------------- |
| `caps_lock`      | `left_command`          | CommandをCtrlっぽく使う |
| `international1` | `rave_accent_and_tilde` | [`~`]対策               |
| `left_command`   | `left_control`          | 消去法                  |
| `left_control`   | `caps_lock`             | Winに合わせたい         |

### 外部キーボード（Keychronk3）

| 物理キー        | 割り当て        | メモ                       |
| --------------- | --------------- | -------------------------- |
| `left_command`  | `left_control`  | commandとcontrolを入れ替え |
| `left_control`  | `left_command`  |                            |
| `right_command` | `right_control` |                            |
| `right_control` | `right_command` |                            |

## complex_modifications

以下４つの内容を設定

- IMEのON/OFFを`CapsLock`単体ではなく`Shift+CapsLock`に割り当てる
- `CapsLock`のON/OFFを`CapsLock`キー単体に割り当てる
- ターミナルエミュレータ上では一番左下に割り当てた`Command`キーを`Ctrl`として認識させる
- ターミナルエミュレータ上では一番左下に割り当てた`Control`キーを`Command`キーとして認識させる

※ターミナルエミュレータは純正ターミナル,iTerm2,Hyperを想定
