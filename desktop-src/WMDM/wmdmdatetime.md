---
title: Структура ВМДМДАТЕТИМЕ
description: Структура ВМДМДАТЕТИМЕ содержит дату и время суток.
ms.assetid: 47f3994d-66c6-47e4-803d-0c98c70eccc8
keywords:
- Структура ВМДМДАТЕТИМЕ Windows Media диспетчер устройств
- Указатель структуры ПВМДМДАТЕТИМЕ Windows Media диспетчер устройств
topic_type:
- apiref
api_name:
- WMDMDATETIME
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07acf706aa63a21edd27fb2ac206db3039249055
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694464"
---
# <a name="wmdmdatetime-structure"></a>Структура ВМДМДАТЕТИМЕ

Структура **вмдмдатетиме** содержит дату и время суток.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _WMDMDATETIME {
  WORD wYear;
  WORD wMonth;
  WORD wDay;
  WORD wHour;
  WORD wMinute;
  WORD wSecond;
} WMDMDATETIME, *PWMDMDATETIME;
```



## <a name="members"></a>Члены

<dl> <dt>

**веар**
</dt> <dd>

Слово, содержащее год из четырех цифр.

</dd> <dt>

**вмонс**
</dt> <dd>

Слово, содержащее месяц (1-12).

</dd> <dt>

**вдай**
</dt> <dd>

Слово, содержащее день месяца (1-31).

</dd> <dt>

**вхаур**
</dt> <dd>

Слово, содержащее час (0-23).

</dd> <dt>

**вминуте**
</dt> <dd>

Слово, содержащее минуту (0-59).

</dd> <dt>

**всеконд**
</dt> <dd>

Слово, содержащее второе (0-59).

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Вмдм. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Имдспстораже:: GETDATE**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getdate)
</dt> <dt>

[**Ивмдмстораже:: GETDATE**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getdate)
</dt> <dt>

[**вмдмригхтс**](wmdmrights.md)
</dt> <dt>

[**Структуры**](structures.md)
</dt> </dl>

 

 





