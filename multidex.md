### 快速统计dex方法数

    unzip -p build/outputs/apk/app-debug.apk classes.dex | head -c 92 | tail -c 4 | hexdump -e '1/4 "%d\n"'