---
description: Представляет драйвер принтера, от которого зависят другие драйверы принтеров.
ms.assetid: b03f9ac1-7ad2-4aee-b496-e1ee15ba7d38
title: Структура CORE_PRINTER_DRIVER (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CORE_PRINTER_DRIVER
- _CORE_PRINTER_DRIVERA
- _CORE_PRINTER_DRIVERW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 18ac3dba88d9cf781393b01b6594777426b7195e6f68afa0fd00a5bddb01f129
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950404"
---
# <a name="core_printer_driver-structure"></a>Основная \_ \_ Структура драйвера принтера

Представляет драйвер принтера, от которого зависят другие драйверы принтеров.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _CORE_PRINTER_DRIVER {
  GUID      CoreDriverGUID;
  FILETIME  ftDriverDate;
  DWORDLONG dwlDriverVersion;
  TCHAR     szPackageID[MAX_PATH];
} CORE_PRINTER_DRIVER, *PCORE_PRINTER_DRIVER;
```



## <a name="members"></a>Члены

<dl> <dt>

**коредривергуид**
</dt> <dd>

Идентификатор GUID основного драйвера принтера.

</dd> <dt>

**фтдривердате**
</dt> <dd>

Дата и время последней версии драйвера основного принтера.

</dd> <dt>

**двлдриверверсион**
</dt> <dd>

Идентификатор версии последней версии драйвера основного принтера.

</dd> <dt>

**Сзпаккажеид \[ максимальный \_ путь\]**
</dt> <dd>

Путь к пакету драйверов, который содержит основной драйвер принтера.

</dd> </dl>

## <a name="remarks"></a>Remarks

Эта структура может представлять базовый драйвер производителя, от которого зависят драйверы различных моделей принтеров.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                            |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>винспул. h (включает Windows. h)</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **\_ Основной \_ принтер \_ дриверв** (Юникод) и **\_ основной \_ \_ драйвер принтера** a (ANSI)<br/>                 |



## <a name="see-also"></a>См. также

<dl> <dt>

[Вывод на печать](printdocs-printing.md)
</dt> <dt>

[Структуры API диспетчера очереди печати](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




