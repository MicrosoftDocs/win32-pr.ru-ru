---
description: Структура ПРОВИДОР \_ info \_ 2 добавляет поставщик печати в список порядка поставщиков печати.
ms.assetid: 840523ca-22d0-460f-81fb-e0a9e2d4f5d6
title: Структура PROVIDOR_INFO_2 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROVIDOR_INFO_2
- _PROVIDOR_INFO_2A
- _PROVIDOR_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 969af36fe0a64bb586fbf62912ca27c6ebba9ba0a627701e4bc57f6202bfe1b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091684"
---
# <a name="providor_info_2-structure"></a>\_Структура провидор info \_ 2

Структура **провидор \_ info \_ 2** добавляет поставщик печати в список порядка поставщиков печати.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _PROVIDOR_INFO_2 {
  LPTSTR pOrder;
} PROVIDOR_INFO_2, *PPROVIDOR_INFO_2;
```



## <a name="members"></a>Члены

<dl> <dt>

**пордер**
</dt> <dd>

Указатель на строку, завершающуюся нулем, которая указывает имя поставщика печати.

</dd> </dl>

## <a name="remarks"></a>Remarks

Эта структура используется при вызове [**аддпринтпровидор**](addprintprovidor.md), уровень 2 для добавления указанного поставщика печати в конец списка порядка поставщиков печати. Поставщик будет немедленно использоваться для маршрутизации, если вызов будет выполнен.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>винспул. h (включает Windows. h)</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **\_ Провидор \_ info \_ 2W** (Юникод) и **\_ провидор \_ сведения \_ 2A** (ANSI)<br/>                         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Вывод на печать](printdocs-printing.md)
</dt> <dt>

[Структуры API диспетчера очереди печати](printing-and-print-spooler-structures.md)
</dt> <dt>

[**аддпринтпровидор**](addprintprovidor.md)
</dt> </dl>

 

 




