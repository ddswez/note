#### bean类解析json为map

json：

```
{result : {"1":[{"allowTrade":1,"coinSymbol":"USDT","nameZh":"泰达币","weight":0,"nameEn":"USDT"}],"2":[{"allowTrade":1,"coinSymbol":"USDT","nameZh":"泰达币","weight":2,"nameEn":"USDT"},{"allowTrade":1,"coinSymbol":"BTC","nameZh":"比特币","weight":1,"nameEn":"Bitcoin"},{"allowTrade":1,"coinSymbol":"ETH","nameZh":"以太坊","weight":0,"nameEn":"Ethereum"}]}
}
```

后台有可能还会动态添加数据， 解析为map

```
class A {
  LinkedHashMap<String, List<B>> result;

  static A fromMap(Map<String, dynamic> map) {
    if (map == null) return null;
    A a = A();

    a.result =
        new LinkedHashMap<String, List<B>>.from(
            map['result'].map((key, value) {
      List<B> values =
          List.from(value.map((it) => B.fromMap(it)));
      return MapEntry(
          key.toString(),
          values);
    }));

    return a;
  }

  Map toJson() => {
        "result": result,
      };
}


class B {
  int allowTrade;
  String coinSymbol;
  String nameZh;
  int weight;
  String nameEn;

  static B fromMap(Map<String, dynamic> map) {
    if (map == null) return null;
    B b = B();
    b.allowTrade = map['allowTrade'];
    b.coinSymbol = map['coinSymbol'];
    b.nameZh = map['nameZh'];
    b.weight = map['weight'];
    b.nameEn = map['nameEn'];
    return b;
  }

  Map toJson() => {
        "allowTrade": allowTrade,
        "coinSymbol": coinSymbol,
        "nameZh": nameZh,
        "weight": weight,
        "nameEn": nameEn,
      };
}

```

