# String

任意の長さの文字列。長さは制限されていません。値には、ヌルバイトを含む任意のバイトセットを含めることができます。 String型は、VARCHAR、BLOB、CLOBなど、他のDBMSの型を置き換えます。

## Encodings

ClickHouse doesn't have the concept of encodings. Strings can contain an arbitrary set of bytes, which are stored and output as-is. If you need to store texts, we recommend using UTF-8 encoding. At the very least, if your terminal uses UTF-8 (as recommended), you can read and write your values without making conversions. Similarly, certain functions for working with strings have separate variations that work under the assumption that the string contains a set of bytes representing a UTF-8 encoded text. For example, the 'length' function calculates the string length in bytes, while the 'lengthUTF8' function calculates the string length in Unicode code points, assuming that the value is UTF-8 encoded.

[Original article](https://clickhouse.yandex/docs/en/data_types/string/) <!--hide-->
