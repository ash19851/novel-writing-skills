# Chapter Length Lessons

## Core Finding: Write One Chapter Per Call

Each write call must contain exactly ONE chapter. Merging multiple chapters into one call yields N insufficient chapters.

## Expansion Protocol (when a chapter comes in short)

Use `terminal` with `sed` + `cat >>` instead of `patch` for Chinese text (special characters cause patch matching to fail).

Steps:
1. Remove end marker: `sed -i 's/【本章完】//g' "8-正文-第N章.txt"`
2. Append content via heredoc
3. Re-add end marker: `echo '【本章完】' >> file`
4. Verify: `grep -v '【本章完】' file | tr -d '[:space:]' | wc -m`

## Word Count Verification

```bash
chars=$(grep -v '【本章完】' "8-正文-第{ch}章.txt" | tr -d '[:space:]' | wc -m)
```

## Anti-Drift Rules (Summary)

1. 大纲锁定: cover ALL outline key plot points
2. 风格锁定: follow 2-核心设定.txt style
3. 口癖禁止: No 不是……而是……, No 不禁想到, No 只见 abuse
4. 2500+ characters
5. No characters/plot not in outline
