### Cubism
---
https://github.com/square/cubism

https://square.github.io/cubism/

https://github.com/square/cubism/wiki/Tutorials

```
var context = cubism.context();

var context = cubism.context()
  .serverDelay(30 * 1000)
  .step(5 * 60 * 1000)
  .size(1920);
  
context.on("change", function(start, stop){
  d3.select("#update-time").text("Last updated at " + stop + ".");
});

context.on("focus", function(i){
  d3.selectAll(".value").style("right", i == null ? null : context.size() - i + "px");
});

context.metric(function(start, stop, step, callback){
  var values = [];
  start = +start;
  stop = +stop;
  while(start < stop){
    start += step;
    value.push(Math.random());
  }
  callback(null, values);
});

var context = cubism.contet(),
  cube = context.cube("http://cube.example.com");

var requests = cube.metric("sum(request)");

var context = cubism.contet(),
  graphite = context.graphite("http://graphite.example.com");

var foo = graphite.metric("sumSeries(nonNegativeDerivative(exclude(hosts.foo.cpu.*.*, 'idle')))");

var foo = graphite.metric("foo").summarize("avg");

graphite.find("hosts.*.cpu.0", function(error, results){
  console.log(results);
});

var context = cubism.context(),
  horizon = context.horizon();
  
var cube = context.cube("http://cube.example.com");

var metrics = [
  cube.metric("sum(request.eq(language, 'en'))"),
  cube.metric("sum(request.eq(language, 'es'))"),
  cube.metric("sum(request.eq(language, 'de'))"),
  cube.metric("sum(request.eq(language, 'fr'))")
];

var horizon = context.horizon()
  .metric(cube.metric);
var metrics = [
  "sum(request.eq(language, 'en'))",
  "sum(request.eq(language, 'es'))",
  "sum(request.eq(language, 'de'))",
  "sum(request.eq(language, 'fr'))"
];

var horizon = context.horizon()
  .metric(function(d) { return cube.metric("sum(request.eq(language, '" + d + "'))"); });
var metrics = [
  "en",
  "es",
  "de",
  "fr"
];

d3.select().selectAll()
    .data(metrics)
  .enter().append("div")
    .attr("class", "hotizon")
    .call(horizon);

d3.select(".horizon")
  .call(horizon.remove)
  .remove();
  
var context = cubism.context(),
  rule = context.rule();
  
d3.select("body").append("div")
  .attr("class", "rule")
  .call(rule);
  
d4.select(".rule")
  .call(rule.remove)
  .remove();
  
var context = cubism.context(),
  cube = context.cube("http://cube.example.com"),
  requests = cube.metric("sum(request)");
  
var requestsPerSecond = cube.metric("sum(request)").divide(5 * 60);
var requestsPerSecond = cube.metric("sum(request)").divide(context.step() / 1000);

var requestsThisWeek = cube.metric("sum(request)"),
  requestsLastWeek = requestThisWeek.sihft(-7 * 24 * 60 * 60 * 1000),
  changeInRequests = requestsThisWeek.subtract(requestslasWeek);
```

```
```

```
```

