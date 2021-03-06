# cryptoCompareAPI
Fork of [Josh-McFarlins CryptoCompare API](https://github.com/Josh-McFarlin/CryptoCompareAPI) to make it usable with gradle.

## Integration

### Gradle Dependency

Add this in your `build.gradle` file:
```gradle
repositories {
    maven { url 'https://jitpack.io' }
}
...
dependencies {
    compile 'com.github.atz3n:cryptoCompareAPI:v0.3'
}
```


## Usage
```java
double dayAverage = Market.getDayAverage("BTC", "USD");
System.out.println("Bitcoin day average:");
System.out.println(dayAverage);

Market.ExchangeAverage exchangeAverage = Market.getExchangeAverage("BTC", "USD", "Coinbase", "Kraken", "Bitstamp");
System.out.println("Bitcoin average from Coinbase, Kraken, and Bitstamp:");
System.out.println(exchangeAverage.high24Hour);

Map<String, Double> btcPrice = Market.getPrice("BTC", "USD", "EUR");
System.out.println("Bitcoin price in USD and EUR:");
System.out.println(btcPrice);
```

An example is provided in the test sources.


## License
This project is developed under the MIT license. This license can be found at [LICENSE](LICENSE).
