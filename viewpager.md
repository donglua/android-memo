### 给ViewPager加上切换的动画效果

```java
mViewPager.setPageTransformer(true, (page, position) -> {
  if (position > 1 || position < -1) return;
  View view = page.findViewById(R.id.fragment_root);
  view.setAlpha(1 - Math.abs(position) * 0.8f);
});
```