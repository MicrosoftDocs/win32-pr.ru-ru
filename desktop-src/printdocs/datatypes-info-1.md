---
description: '\_ \_ Структура Data info 1 содержит сведения о типе данных, который используется для записи задания печати.'
ms.assetid: 6169006c-12d4-4608-865c-732f04107f9f
title: Структура DATATYPES_INFO_1 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DATATYPES_INFO_1
- _DATATYPES_INFO_1A
- _DATATYPES_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: e7259f6559220697538774fef8d2460318df84c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264460"
---
# <a name="datatypes_info_1-structure"></a>Структура данных с \_ информацией \_ 1

Структура Data **\_ info \_ 1** содержит сведения о типе данных, который используется для записи задания печати.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _DATATYPES_INFO_1 {
  LPTSTR pName;
} DATATYPES_INFO_1, *PDATATYPES_INFO_1;
```



## <a name="members"></a>Члены

<dl> <dt>

**pName**
</dt> <dd>

Указатель на строку, завершающуюся нулем, которая определяет тип данных, используемый для записи задания печати.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>Винспул. h (включение Windows. h)</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | Сведения о **\_ типах \_ данных \_ 1W** (Юникод) и **\_ типы данных \_ \_ 1A** (ANSI)<br/>                       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Вывод на печать](printdocs-printing.md)
</dt> <dt>

[Структуры API диспетчера очереди печати](printing-and-print-spooler-structures.md)
</dt> <dt>

[**енумпринтпроцессордататипес**](enumprintprocessordatatypes.md)
</dt> </dl>

 

 




