# CMakeの検証

## メモ
### *target\_include\_directories*コマンド
### *PRIVATE*の場合
*<target>*のコンパイル時のみ*-I*オプション付加
### *INTERFACE*の場合
*<target>*の**依存元**のコンパイル時のみ*-I*オプション付加
### *PRIVATE*の場合
*<target>*とその**依存元**のコンパイル時に*-I*オプション付加
