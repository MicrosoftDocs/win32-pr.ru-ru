---
description: Определяет кэш метрик шрифтов Uniscribe.
ms.assetid: 56a98529-6ae9-4b71-bd7d-cf056a1e3683
title: SCRIPT_CACHE (usp10. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ece29fe0ed610b4576263c36c50311ef57317579
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651114"
---
# <a name="script_cache"></a>\_кэш скриптов

Определяет кэш метрик шрифтов Uniscribe.


```C++
typedef void* SCRIPT_CACHE;
```



## <a name="remarks"></a>Комментарии

Это непрозрачная структура. Приложение должно выделить и хранить одну \_ переменную кэша скрипта для каждого используемого стиля символов. Переменная должна быть инициализирована **значением NULL**.

Многие функции скрипта используют сочетание дескриптора контекста аппаратного устройства и \_ переменной кэша скрипта. Uniscribe сначала пытается получить доступ к данным шрифта с помощью \_ переменной кэша скрипта. Он проверяет контекст устройства оборудования только в том случае, если необходимые данные еще не кэшированы.

Маркер контекста аппаратного устройства может быть передан Uniscribe как **null**. Если данные, необходимые для Uniscribe, уже кэшированы, контекст устройства недоступен, и операция продолжится нормально.

Если контекст устройства передается как **значение NULL** , а Uniscribe — по любой причине, Uniscribe возвращает код ошибки E \_ Pending. Этот код быстро возвращается, позволяя приложению избежать требующих много времени вызовов [**SelectObject**](/windows/win32/api/wingdi/nf-wingdi-selectobject) .

## <a name="examples"></a>Примеры

Следующий пример применяется ко всем функциям, которые принимают \_ переменную кэша скрипта и дополнительный дескриптор контекста аппаратного устройства.


```C++
hr = ScriptShape(NULL, &sc,
                 pwcChars, cChars, cMaxGlyphs, psa, pwOutGlyphs, pwLogClust, psva, pcGlyphs);
if (hr == E_PENDING)
{
    // ... select font into hdc ...
    hr = ScriptShape(hdc, &sc,
                 pwcChars, cChars, cMaxGlyphs, psa, pwOutGlyphs, pwLogClust, psva, pcGlyphs);
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Usp10. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Uniscribe](uniscribe.md)
</dt> <dt>

[Структуры Uniscribe](uniscribe-structures.md)
</dt> <dt>

[Кэширование](caching.md)
</dt> </dl>

 

 
