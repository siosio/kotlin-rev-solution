

# Kotlinでtry-with-resourcesが使いたい 



useを使います。

    val inputStream = Thread.currentThread().contextClassLoader.getResourceAsStream("hogehoge")
    inputStream.use {
        // `it`がInputStreamのインスタンス
        val b = it.read()
    }


useはClosableインターフェースを実装しているクラスの拡張関数として提供されています。
したがってcloseが実装されているクラスには同じように適用できます。

https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.io/use.html
