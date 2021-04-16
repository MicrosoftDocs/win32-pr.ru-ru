---
description: '\_Структура значений перечислений принтера \_ задает имя, тип и данные для значения конфигурации принтера, возвращаемого функцией енумпринтердатаекс.'
ms.assetid: 87eb1452-0d9d-46bd-8af8-0542a11a929b
title: Структура PRINTER_ENUM_VALUES (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_ENUM_VALUES
- _PRINTER_ENUM_VALUESA
- _PRINTER_ENUM_VALUESW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: ea73318db7a91fa4d422624b1c3c0c6f09d97cb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712242"
---
# <a name="printer_enum_values-structure"></a>\_Структура значений перечислений принтера \_

Структура **\_ \_ значений перечислений принтера** задает имя, тип и данные для значения конфигурации принтера, возвращаемого функцией [**енумпринтердатаекс**](enumprinterdataex.md) .

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _PRINTER_ENUM_VALUES {
  LPTSTR pValueName;
  DWORD  cbValueName;
  DWORD  dwType;
  LPBYTE pData;
  DWORD  cbData;
} PRINTER_ENUM_VALUES, *PPRINTER_ENUM_VALUES;
```



## <a name="members"></a>Члены

<dl> <dt>

**пвалуенаме**
</dt> <dd>

Указатель на строку, завершающуюся нулем, которая указывает имя извлеченного значения.

</dd> <dt>

**кбвалуенаме**
</dt> <dd>

Число байтов в **пвалуенаме** члене, включая завершающий нуль символа.

</dd> <dt>

**двтипе**
</dt> <dd>

Код, указывающий тип данных, на который указывает элемент **pData** . Список возможных кодов типов см. в разделе [типы значений реестра](/windows/desktop/SysInfo/registry-value-types).

</dd> <dt>

**pData**
</dt> <dd>

Указатель на буфер, содержащий данные для извлеченного значения.

</dd> <dt>

**cbData**
</dt> <dd>

Число байтов, полученных в буфере **pData** .

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>Винспул. h (включение Windows. h)</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **\_ \_ Перечисление \_ валуесв** (Юникод) и **\_ \_ Перечисление \_ значений принтера** (ANSI)<br/>                 |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Вывод на печать](printdocs-printing.md)
</dt> <dt>

[Структуры API диспетчера очереди печати](printing-and-print-spooler-structures.md)
</dt> <dt>

[**енумпринтердатаекс**](enumprinterdataex.md)
</dt> </dl>

 

