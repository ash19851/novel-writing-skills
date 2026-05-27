# Heredoc 定界符冲突陷阱

## 问题

使用 `cat >> file << 'DELIMITER'` 扩充时，如果追加文本中包含 DELIMITER 这个单词，bash 会提前终止。

## 修复方案

### 方案A：使用极不可能出现的定界符
```bash
cat >> file << 'ENDOFFILE_9a7b3c'
```

### 方案B：用 write_file 直接覆盖（最可靠）
当文本复杂时，直接重新 write_file 整个文件。

### 方案C：逐行追加
```bash
echo "第一句" >> file
echo "第二句" >> file
```

## 经验法则

- 不要用 'EXPAND'、'END'、'EOF'、'FIX' 等可能在正文中出现的单词做定界符
- 最安全的做法：用随机后缀，如 `'ENDOFFILE_9a7b3c'`
- 真正最可靠的：写 write_file 全量写，避开 heredoc
