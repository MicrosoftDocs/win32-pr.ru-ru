---
description: Структура АНДЕКСП содержит массив совпадений шаблонов, используемых для вычисления данных кадра.
ms.assetid: e5f4c030-eb2b-4cc9-9032-9ad4701b6503
title: Структура АНДЕКСП (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ANDEXP
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 1d27d5bdd51a45b31f518271053f44b45917cdeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346835"
---
# <a name="andexp-structure"></a>Структура АНДЕКСП

Структура **андексп** содержит массив совпадений шаблонов, используемых для вычисления данных кадра.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _ANDEXP {
  DWORD        nPatternMatches;
  PATTERNMATCH PatternMatch[MAX_PATTERNS];
} ANDEXP, *LPANDEXP;
```



## <a name="members"></a>Члены

<dl> <dt>

**нпаттернматчес**
</dt> <dd>

Число совпадений шаблонов.

</dd> <dt>

**паттернматч**
</dt> <dd>

Массив элементов сопоставления шаблона. Обратите внимание, что каждая структура **андексп** может содержать до четырех элементов соответствия шаблону. Дополнительные сведения об этом элементе см. в разделе [фильтры записи](capture-filters.md).

</dd> </dl>

## <a name="remarks"></a>Комментарии

Шаблоны в массиве **паттернматч** \[ Max \_ Patterns \] соединяются как одноранговые в операторах логического или в формате

(Шаблон 1 \| \| Шаблон 2 \| \| шаблон 3).

Дополнительные сведения о реализации этой структуры см. в разделе [фильтры записи](capture-filters.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[паттернматч](patternmatch.md)
</dt> </dl>

 

 




