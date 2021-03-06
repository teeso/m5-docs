# スピーカー

## tone()

**機能:**

指定した音と長さでスピーカーを鳴らします。

**構文:**

<mark>tone(uint16_t freq, [uint32_t duration]);</mark>

| 引数 | 説明 | 型 |
| --- | --- | -- |
| freq | 音の高さ（周波数Hz） | uint16_t |
| duration | 鳴動時間 (ms)、 省略可能。 | uint16_t |

**使用例:**

```arduino
#include <M5Stack.h>

void setup() {
  M5.begin();
  M5.Speaker.tone(900, 1000);
}
```

<!--
### <mark>tone</mark>
> M5.Speaker.tone(uint32_t freq);

Set the pitch of speaker.

| Param | Type | Description |
| --- | --- | --- |
| freq | <code>uint32_t</code> | frequency |

**Example**
```arduino
M5.Speaker.tone(100);
``` -->