---
description: Содержит группу массивов АНДЕКСП, оцененных как одноранговые.
ms.assetid: 14fa568c-9535-4415-923d-7e93ba4d2e80
title: Структура выражения (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPRESSION
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4efa1f79477e3dcc13bedfddb2cdca7fd660f5430b7d7f2b87dbd9d4b4425098
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366842"
---
# <a name="expression-structure"></a>Структура выражения

Структура **выражения** содержит группу массивов **андексп** , вычисленную как одноранговые в логических выражениях и, имеющих формат

(АНДЕКСП 1 && АНДЕКСП 2 && АНДЕКСП 3).

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _EXPRESSION {
  DWORD  nAndExps;
  ANDEXP AndExp[MAX_PATTERNS];
} EXPRESSION, *LPEXPRESSION;
```



## <a name="members"></a>Члены

<dl> <dt>

**нандекспс**
</dt> <dd>

Количество шаблонов **андексп** .

</dd> <dt>

**андексп**
</dt> <dd>

Массив шаблонов **андексп** . Фильтр записи упорядочивает все строки этого массива как логические операторы и. Имейте в виду, что каждая структура выражения может содержать не более четырех шаблонов **андексп** .

</dd> </dl>

## <a name="remarks"></a>Remarks

Дополнительные сведения о реализации этой структуры в составе фильтра записи см. в разделе [фильтры записи](capture-filters.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[андексп](andexp.md)
</dt> <dt>

[каптурефилтер](capturefilter.md)
</dt> </dl>

 

 




