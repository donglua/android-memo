# LocationManager


```java
LocationListener mLocationListener = (LocationManager) activity.getSystemService(Context.LOCATION_SERVICE);

Criteria criteria = new Criteria();
criteria.setAccuracy(Criteria.ACCURACY_COARSE);
criteria.setPowerRequirement(Criteria.POWER_LOW);
criteria.setSpeedRequired(false);
criteria.setAltitudeRequired(false);
criteria.setBearingRequired(false);
criteria.setCostAllowed(false);

String bestProvider = mLocationManager.getBestProvider(criteria, false);
mLocationManager.requestLocationUpdates(bestProvider, 6000, 100, mLocationListener);



@Override protected void onDestroy() {
super.onDestroy();
mLocationManager.removeUpdates(mLocationListener);
}
```