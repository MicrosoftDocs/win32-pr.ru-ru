---
description: В \_ структуре "сведения о принтере \_ 8" указаны глобальные параметры принтера по умолчанию.
ms.assetid: 98f26a45-5302-4358-bed6-691d9bc37554
title: Структура PRINTER_INFO_8 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_8
- _PRINTER_INFO_8A
- _PRINTER_INFO_8W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 0aa5d516dd099caeba5699a8328fa52add64f14ea970e6ccec28ea8bfbe87271
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119947674"
---
# <a name="printer_info_8-structure"></a>\_Сведения о принтере \_ 8 структура

В структуре " **\_ сведения о принтере \_ 8** " указаны глобальные параметры принтера по умолчанию.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _PRINTER_INFO_8 {
  LPDEVMODE pDevMode;
} PRINTER_INFO_8, *PPRINTER_INFO_8;
```



## <a name="members"></a>Члены

<dl> <dt>

**пдевмоде**
</dt> <dd>

Указатель на структуру [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) , определяющую глобальные данные принтера по умолчанию, такие как ориентация бумаги и разрешение.

</dd> </dl>

## <a name="remarks"></a>Remarks

Глобальные значения по умолчанию задаются администратором принтера, который может использоваться любым пользователем. В отличие от этого значения по умолчанию для каждого пользователя влияют на конкретного пользователя или других пользователей, использующих этот профиль. Для параметров по умолчанию для каждого пользователя [**Используйте \_ сведения \_ о принтере 9**](printer-info-9.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>винспул. h (включает Windows. h)</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **\_ \_ Сведения о \_ принтере 8W** (Юникод) и **\_ \_ \_ 8A info** (ANSI)<br/>                           |



## <a name="see-also"></a>См. также

<dl> <dt>

[Вывод на печать](printdocs-printing.md)
</dt> <dt>

[Структуры API диспетчера очереди печати](printing-and-print-spooler-structures.md)
</dt> <dt>

[**Наложение**](getprinter.md)
</dt> <dt>

[**сетпринтер**](setprinter.md)
</dt> <dt>

[**\_Сведения о принтере \_ 9**](printer-info-9.md)
</dt> </dl>

 

 




