---
description: В \_ структуре "сведения о принтере \_ 9" указаны параметры принтера по умолчанию для каждого пользователя.
ms.assetid: 8bafb995-f31c-46e3-a950-45e240c678aa
title: Структура PRINTER_INFO_9 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_9
- _PRINTER_INFO_9A
- _PRINTER_INFO_9W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 684ffc6ccfc4f94c036bde42faec9458c8bb60911fc8c9398006f58631baa791
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118234239"
---
# <a name="printer_info_9-structure"></a>\_Структура сведений о принтере \_ 9

В структуре " **\_ сведения о принтере \_ 9** " указаны параметры принтера по умолчанию для каждого пользователя.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _PRINTER_INFO_9 {
  LPDEVMODE pDevMode;
} PRINTER_INFO_9, *PPRINTER_INFO_9;
```



## <a name="members"></a>Члены

<dl> <dt>

**пдевмоде**
</dt> <dd>

Указатель на структуру [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) , определяющую данные принтера по умолчанию для каждого пользователя, такие как ориентация бумаги и разрешение. **DEVMODE** хранится в реестре пользователя.

</dd> </dl>

## <a name="remarks"></a>Remarks

Значения по умолчанию для каждого пользователя влияют только на конкретного пользователя или всех, кто использует этот профиль. В отличие от них глобальные значения по умолчанию устанавливаются администратором принтера, который может использоваться любым пользователем. Для глобальных значений по умолчанию [**Используйте \_ сведения \_ о принтере 8**](printer-info-8.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>винспул. h (включает Windows. h)</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **\_ \_ Сведения о \_ принтере 9W** (Юникод) и **\_ \_ \_ 9a info** (ANSI)<br/>                           |



## <a name="see-also"></a>См. также статью

<dl> <dt>

[Вывод на печать](printdocs-printing.md)
</dt> <dt>

[Структуры API диспетчера очереди печати](printing-and-print-spooler-structures.md)
</dt> <dt>

[**Наложение**](getprinter.md)
</dt> <dt>

[**сетпринтер**](setprinter.md)
</dt> <dt>

[**\_Сведения о принтере \_ 8**](printer-info-8.md)
</dt> </dl>

 

 




