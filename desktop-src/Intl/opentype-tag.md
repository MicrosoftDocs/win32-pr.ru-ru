---
description: Определяет 4-байтовый массив, который содержит 4 8-разрядные значения ASCII для пробелов, A – Z или a – z для определения тегов в скриптах, языках и шрифтах OpenType.
ms.assetid: 188ad9a1-e0eb-411f-b6df-8c394d122d6f
title: OPENTYPE_TAG (usp10. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7c784fa7f6243e7e5444dcbc64c690ce7184d6ace469759c19be9de87854732
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040784"
---
# <a name="opentype_tag"></a>\_тег OPENTYPE

Определяет 4-байтовый массив, который содержит 4 8-разрядные значения ASCII для пробелов, A – Z или a – z для определения тегов в скриптах, языках и шрифтах OpenType.


```C++
typedef ULONG OPENTYPE_TAG;
```



## <a name="remarks"></a>Remarks

В следующих примерах определяются представления тегов функций OpenType.

-   Тег функции для функции лигатуры — "Лига".
-   Теги языка для румынского, урду и фарси имеют «ROM», «УРД» и «FAR» соответственно. Обратите внимание, что каждый из этих тегов заканчивается пробелом.
-   Теги script для латиницы и арабского алфавита — это «ЛАТН» и «Арабская» соответственно.

Дополнительные сведения о тегах функций OpenType и спецификации OpenType см. в разделе <https://www.microsoft.com/typography/otspec/featuretags.htm> .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                               |
| Распространяемые компоненты<br/>          | Usp10.dll версии 1,600 или более поздней в Windows.<br/>                |
| Заголовок<br/>                   | <dl> <dt>Usp10. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Uniscribe](uniscribe.md)
</dt> <dt>

[Структуры Uniscribe](uniscribe-structures.md)
</dt> <dt>

[**скриптжетфонталтернатеглифс**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontalternateglyphs)
</dt> <dt>

[**скриптжетфонтфеатуретагс**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontfeaturetags)
</dt> <dt>

[**скриптжетфонтлангуажетагс**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontlanguagetags)
</dt> <dt>

[**скриптжетфонтскрипттагс**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontscripttags)
</dt> <dt>

[**скриптитемизеопентипе**](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype)
</dt> <dt>

[**скриптплацеопентипе**](/windows/desktop/api/Usp10/nf-usp10-scriptplaceopentype)
</dt> <dt>

[**скриптпоситионсинглеглиф**](/windows/desktop/api/Usp10/nf-usp10-scriptpositionsingleglyph)
</dt> <dt>

[**скриптшапеопентипе**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype)
</dt> <dt>

[**скриптсубститутесинглеглиф**](/windows/desktop/api/Usp10/nf-usp10-scriptsubstitutesingleglyph)
</dt> </dl>

 

 




