---
description: Структура ADDJOB \_ info \_ 1 определяет задание печати, а также каталог и файл, в котором приложение может сохранить это задание.
ms.assetid: de915932-11a7-47e8-9be9-edab76d94189
title: Структура ADDJOB_INFO_1 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDJOB_INFO_1
- _ADDJOB_INFO_1A
- _ADDJOB_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 08197a6a72da7e38a349014e08d2d2c2c946f6e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272492"
---
# <a name="addjob_info_1-structure"></a>\_Структура ADDJOB info \_ 1

Структура **ADDJOB \_ info \_ 1** определяет задание печати, а также каталог и файл, в котором приложение может сохранить это задание.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _ADDJOB_INFO_1 {
  LPTSTR Path;
  DWORD  JobId;
} ADDJOB_INFO_1, *PADDJOB_INFO_1;
```



## <a name="members"></a>Члены

<dl> <dt>

**Путь**
</dt> <dd>

Указатель на строку, завершающуюся нулем, которая содержит путь и имя файла, которые приложение может использовать для хранения задания печати.

</dd> <dt>

**JobId**
</dt> <dd>

Маркер задания печати.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>Винспул. h (включение Windows. h)</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **\_ \_ Сведения о ADDJOB \_ 1W** (Юникод) и **\_ ADDJOB \_ info \_ 1A** (ANSI)<br/>                             |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Вывод на печать](printdocs-printing.md)
</dt> <dt>

[Структуры API диспетчера очереди печати](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddJob**](addjob.md)
</dt> </dl>

 

 




