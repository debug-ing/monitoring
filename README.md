## monitoring
monitoring event


## type alerting
انواع الرت ها prometheus
info
warning
critical

## type data prometheus
# Counter
برای ذخیره تعداد با میره مثلا ذخیره تعداد درخواست ورودی یک API یا اکشن
# Gauge 
برای سنجس یک مقدار در اون لحظه استفاده میشه مثل ذخیره میزان مصرف cpu یا ram
# Histogram
میاد لیست از اطلاعات داخل خودش ذخیره میکنه مثل چی؟ میشه دقیقا همه API ها کال شده متناسب با زمان رسپانسش داخل گذاشت و اونو به باکت مختلف تقسیم کرد
```js
const httpRequestDuration = new client.Histogram({
  name: 'http_request_duration_seconds',
  help: 'Duration of HTTP requests in seconds',
  labelNames: ['method', 'route', 'status_code'],
  buckets: [0.05, 0.1, 0.2, 0.3, 0.4, 0.5, 0.6, 1, Infinity]
});
```
# Summary 
دقیقا شبیه Histogram هستش فقط با این فرق تقسیم بندی نوع کوانتیل‌ها هستش یعنی چی؟ حالا
```js
const httpRequestDuration = new client.Histogram({
  name: 'http_request_duration_seconds',
  help: 'Duration of HTTP requests in seconds',
  labelNames: ['method', 'route', 'status_code'],
  buckets: [0.5, 0.9, 0.99]
});
```

## Docker prometheus
you can show all docker prometheus

## ToDo
- [x] prometheus + nginx (docker)
- [x] grafana (docker)
- [x] sample node js
- [ ] alert manager send 