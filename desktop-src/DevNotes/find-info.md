---
description: Содержит сведения о контексте поиска.
ms.assetid: 4b865563-98c2-459b-bb2b-75420d51d6a7
title: Структура FIND_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FIND_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 7d6b6dea42c008178c22f6e342a64b2f8d193ec5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655695"
---
# <a name="find_info-structure"></a>НАЙТИ \_ структуру сведений

Содержит сведения о контексте поиска.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _FIND_INFO {
  TAGID     tiIndex;
  TAGID     tiCurrent;
  TAGID     tiEndIndex;
  TAG       tName;
  DWORD     dwIndexRec;
  DWORD     dwFlags;
  ULONGLONG ullKey;
  union {
    LPCTSTR szName;
    DWORD   dwName;
    GUID    *pguidName;
  };
} FIND_INFO, *PFIND_INFO;
```



## <a name="members"></a>Члены

<dl> <dt>

**тииндекс**
</dt> <dd>

**TAGID** индекса для поиска.

</dd> <dt>

**тикуррент**
</dt> <dd>

**TAGID** для текущего найденного элемента.

</dd> <dt>

**тиендиндекс**
</dt> <dd>

**TAGID** для последней записи после FindFirst, если индекс уникален.

</dd> <dt>

**tName**
</dt> <dd>

Тип элемента, который необходимо найти. См. раздел [типы тегов](tag-types.md).

</dd> <dt>

**двиндексрек**
</dt> <dd>

Внутренний счетчик, используемый для наблюдения за тем, где в индексе должна начинаться следующая операция поиска.

</dd> <dt>

**dwFlags**
</dt> <dd>

Этот элемент может иметь **\_ \_ уникальный \_ ключ индекса** 0 или шимдб (0x00000001), что означает, что это индекс уникального ключа.

</dd> <dt>

**уллкэй**
</dt> <dd>

Ключ для текущей записи.

</dd> <dt>

**szName**
</dt> <dd>

Текущая строка (если тип тега — **тег \_ типа \_ стрингреф**).

</dd> <dt>

**двнаме**
</dt> <dd>

Текущее значение **DWORD** (если тип тега — **\_ тип \_ DWORD**).

</dd> <dt>

**пгуиднаме**
</dt> <dd>

Текущее значение идентификатора GUID (если тип тега является **\_ \_ двоичным типом ТЕГА** , а тег — **тегом \_ Database \_ ID**).

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сдбфиндфирстдвординдекседтаг**](sdbfindfirstdwordindexedtag.md)
</dt> </dl>

 

 




