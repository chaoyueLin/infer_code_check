# infer_code_check
infer是facebook出品的代码检查工具，但是只能在mac或linux上安装使用
# 安装
需要有安装python2.7以上,推荐使用brew安装

```
brew install infer
```
配置环境变量,可以通过brew list infer 查看位置
# 使用 
进入android project目录

```
cd /Users/zbtu/Documents/Develope/infer/examples/android_hello
./gradlew clean（重新编译）
infer -- ./gradlew build（执行）
```
推荐：/.gradlew可以换成 gradle

```
infer --keep-going -- gradle assembleDebug
./gradlew clean then infer run -- ./gradlew assembleDebug
 ./gradlew clean then infer run -- ./gradlew assembleRelease
./gradlew clean then infer run -- ./gradlew build
```
等待执行完毕，就可以查看到输出结果了,inferTraceBugs（更详细的报告),工程下面的infer-out文件夹可以找到

...too many issues to display (limit=10 exceeded), please see /Users/charles/Documents/Android/workplace/wky_android/OneCloud/infer-out/bugs.txt or run `infer-explore` for the remaining issues.