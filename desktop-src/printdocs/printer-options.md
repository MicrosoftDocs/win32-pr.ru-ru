---
description: Представляет параметры принтера.
ms.assetid: 7cc3d10c-8bc2-4899-b083-63d802ee16e7
title: Структура PRINTER_OPTIONS (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_OPTIONS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 37c45277f0a7e30bc94b2d23ffa27de0092a7164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693179"
---
# <a name="printer_options-structure"></a>\_Структура параметров принтера

Представляет параметры принтера.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _PRINTER_OPTIONS {
  UINT  cbSize;
  DWORD dwFlags;
} PRINTER_OPTIONS, *PPRINTER_OPTIONS;
```



## <a name="members"></a>Члены

<dl> <dt>

**кбсизе**
</dt> <dd>

Размер структуры **\_ параметров принтера** .

</dd> <dt>

**dwFlags**
</dt> <dd>

Набор [**\_ \_ флагов параметров принтера**](printer-option-flags.md) , указывающих, как маркер принтера, возвращаемого [**OpenPrinter2**](openprinter2.md) , будет использоваться другими функциями.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Винспул. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Вывод на печать](printdocs-printing.md)
</dt> <dt>

[Структуры API диспетчера очереди печати](printing-and-print-spooler-structures.md)
</dt> <dt>

[**OpenPrinter2**](openprinter2.md)
</dt> <dt>

[**\_ \_ флаги параметров принтера**](printer-option-flags.md)
</dt> </dl>

 

 




