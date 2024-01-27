
```java

根据id去重
Set<CustomerValue> customerSet = new TreeSet<>((o1, o2) -> o1.getId().compareTo(o2.getId()));

java 跨域 (可以在filter里设置全局)：   
response().setHeader("Access-Control-Allow-Origin", "http://localhost:8000");
response.setHeader("Access-Control-Allow-Origin", "*");
response.setHeader("Access-Control-Allow-Methods", "POST, GET, OPTIONS, DELETE");
response.setHeader("Access-Control-Max-Age", "3600");
response.setHeader("Access-Control-Allow-Headers", "x-requested-with,Authorization,content-type");
response.setHeader("Access-Control-Allow-Credentials","true");

json  数字转字符串
@JsonSerialize(using = ToStringSerializer.class)
json  时间格式化
@JsonFormat(pattern = "yyyy-MM-dd HH:mm:ss", timezone = "GMT+8")

double金额格式化
DecimalFormat df = new DecimalFormat("0.00");
df.setRoundingMode(RoundingMode.HALF_UP);
Double amount;
df.format(amount);

fastjson转对象
CustomerRefsSeller c2 = JSON.parseObject(JSON.toJSONString(customerRefs), CustomerRefsSeller.class);

jackson json转换
JsonNode json = request().body().asJson();
JsonNode orderJson = json.get("orderIds");
List<String> orderIds = CommonUtils.objectMapper.convertValue(orderJson, new TypeReference<List<String>>() {});

Profile pf = objectMapper.readValue(xxxxx.toString(), new TypeReference<Profile>() {});

```