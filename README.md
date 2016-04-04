#yandex-translator-java-api
* * *

Provides a Java wrapper around the Yandex machine translation web service API. 

Currently, only the services for translating a single string and detecting the language of a single string are implemented in this API. The translate/detect services are not implemented for an array of strings, and the getLangs service is not implemented.

This project was adapted from the microsoft-translator-java-api project by Jonathan Griggs.

## Requires

* A Yandex API Key - [Sign Up Here](http://api.yandex.com/translate/)

Quickstart
==========

```xml
<repositories>
	<repository>
		<id>jitpack.io</id>
		<url>https://jitpack.io</url>
	</repository>
</repositories>
<dependencies>
	<dependency>
		<groupId>com.github.matushd</groupId>
		<artifactId>yandex-translator-java-api</artifactId>
		<version>1.0.7</version>
	</dependency>
</dependencies>
```

```java
import com.rmtheis.yandtran.language.Language;
import com.rmtheis.yandtran.translate.Translate;

public class test {
    public static void main(String[] args) throws Exception {
        Translate translate = new Translate("[Put your API Key here]");

        String translatedText = translate.execute("Hola, mundo!", Language.SPANISH, Language.ENGLISH);

        System.out.println(translatedText);
    }
}

```

License
=======

This project is licensed under the [Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0.html)
