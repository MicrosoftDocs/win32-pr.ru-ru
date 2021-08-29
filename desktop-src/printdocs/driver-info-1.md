---
description: Структура драйвера \_ \_ 1 определяет драйвер принтера.
ms.assetid: 9435192b-3eba-4937-8cd3-bff4e9eb84d3
title: Структура DRIVER_INFO_1 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_1
- _DRIVER_INFO_1A
- _DRIVER_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 57fd1fe4eea1585dce36d3d5bd03d2039ad345adbabcfdf1ab4b301f3fc15a69
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092084"
---
# <a name="driver_info_1-structure"></a>\_Структура сведений о драйвере \_ 1

Структура **драйвера \_ \_ 1** определяет драйвер принтера.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _DRIVER_INFO_1 {
  LPTSTR pName;
} DRIVER_INFO_1, *PDRIVER_INFO_1;
```



## <a name="members"></a>Члены

<dl> <dt>

**pName**
</dt> <dd>

Указатель на строку, завершающуюся нулем, которая указывает имя драйвера принтера.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>винспул. h (включает Windows. h)</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **\_ \_ Сведения о \_ драйвере 1W** (Юникод) и **\_ драйвер \_ \_ 1A** (ANSI)<br/>                             |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Вывод на печать](printdocs-printing.md)
</dt> <dt>

[Структуры API диспетчера очереди печати](printing-and-print-spooler-structures.md)
</dt> <dt>

[**енумпринтердриверс**](enumprinterdrivers.md)
</dt> </dl>

 

 




