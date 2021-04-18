---
description: Структура порта \_ info \_ 1 определяет поддерживаемый порт принтера.
ms.assetid: e474fe9c-e554-406a-a5bf-de07f9a72b32
title: Структура PORT_INFO_1 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PORT_INFO_1
- _PORT_INFO_1A
- _PORT_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d64e7dfa29cbe6b3f7efd3aaa0076851aea0311b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702208"
---
# <a name="port_info_1-structure"></a>\_Сведения о порте \_ 1 структура

Структура **порта \_ info \_ 1** определяет поддерживаемый порт принтера.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _PORT_INFO_1 {
  LPTSTR pName;
} PORT_INFO_1, *PPORT_INFO_1;
```



## <a name="members"></a>Члены

<dl> <dt>

**pName**
</dt> <dd>

Указатель на строку, завершающуюся нулем, которая определяет поддерживаемый порт принтера (например, "LPT1:").

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>Винспул. h (включение Windows. h)</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **\_ \_ Сведения о \_ порте 1W** (Юникод) и **\_ \_ сведения о порте \_ 1A** (ANSI)<br/>                                 |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Вывод на печать](printdocs-printing.md)
</dt> <dt>

[Структуры API диспетчера очереди печати](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPorts**](enumports.md)
</dt> </dl>

 

 




