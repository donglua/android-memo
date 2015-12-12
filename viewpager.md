### 给ViewPager加上切换的动画效果

```java
mViewPager.setPageTransformer(true, (page, position) -> {
  if (position > 1 || position < -1) return;
  page.setAlpha(1 - Math.abs(position));
});
```