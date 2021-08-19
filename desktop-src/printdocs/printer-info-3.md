---
description: В структуре "сведения о ПРИНТЕРе \_ \_ 3" указаны сведения о безопасности принтера.
ms.assetid: 527d635d-2d75-4b56-bab7-e95c9919a8fb
title: Структура PRINTER_INFO_3 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_3
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: c6b9bc249921b3247f5df898c2810d735dc1a75c8e643e965b3fd249d9496f78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117867929"
---
# <a name="printer_info_3-structure"></a>\_Сведения о принтере \_ 3 структура

В структуре " **сведения о принтере \_ \_ 3** " указаны сведения о безопасности принтера.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _PRINTER_INFO_3 {
  PSECURITY_DESCRIPTOR pSecurityDescriptor;
} PRINTER_INFO_3, *PPRINTER_INFO_3;
```



## <a name="members"></a>Члены

<dl> <dt>

**псекуритидескриптор**
</dt> <dd>

Указатель на структуру [**\_ дескриптора безопасности**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) , указывающую сведения о безопасности принтера.

</dd> </dl>

## <a name="remarks"></a>Remarks

Структура **принтера \_ info \_ 3** позволяет приложению получить и установить дескриптор безопасности принтера. Вызывающий объект может сделать это, даже если у него отсутствуют определенные разрешения принтера, если у него есть стандартные права, описанные в [**сетпринтер**](setprinter.md) и в средстве [**печати**](getprinter.md). Таким образом, приложение может временно запретить доступ к принтеру, одновременно позволяя владельцу принтера получить доступ к списку управления доступом принтера.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>винспул. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Вывод на печать](printdocs-printing.md)
</dt> <dt>

[Структуры API диспетчера очереди печати](printing-and-print-spooler-structures.md)
</dt> <dt>

[**сетпринтер**](setprinter.md)
</dt> <dt>

[**Наложение**](getprinter.md)
</dt> <dt>

[**\_Сведения о принтере \_ 1**](printer-info-1.md)
</dt> <dt>

[**\_Сведения о принтере \_ 2**](printer-info-2.md)
</dt> <dt>

[**\_Сведения о принтере \_ 4**](printer-info-4.md)
</dt> <dt>

[**\_дескриптор безопасности**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

