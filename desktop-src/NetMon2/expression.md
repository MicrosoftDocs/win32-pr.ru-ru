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
ms.openlocfilehash: b6565c294c0d8e0a7a277769404cb8b1b206380e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662199"
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

## <a name="remarks"></a>Комментарии

Дополнительные сведения о реализации этой структуры в составе фильтра записи см. в разделе [фильтры записи](capture-filters.md).

## <a name="requirements"></a>Требования



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

 

 




