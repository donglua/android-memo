

# 引用本地aar文件
```
dependencies {
  compile(name:'nameOfYourAARFileWithoutExtension', ext:'aar')
}
repositories {
  flatDir{
    dirs 'libs'
  }
}
```