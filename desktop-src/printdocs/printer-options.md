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
ms.openlocfilehash: d7eb7be8443c6a49c670e0573a79831a7aacfd88087f6ab19de632223b8588c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091754"
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
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                            |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>винспул. h (включает Windows. h)</dt> </dl> |



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

 

 




