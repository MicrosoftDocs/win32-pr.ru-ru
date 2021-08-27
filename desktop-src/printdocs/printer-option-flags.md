---
description: Задает кэширование маркера для принтера, открытого с помощью OpenPrinter2.
ms.assetid: e5a62322-723c-490d-8de1-f74dcac9e22d
title: Перечисление PRINTER_OPTION_FLAGS (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_OPTION_FLAGS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: b8541ec00f0d53bf58a826ceb7d8b8a821008fb6a66c0fe3917ebc12822e0e5f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091804"
---
# <a name="printer_option_flags-enumeration"></a>\_ \_ Перечисление флагов параметров принтера

Задает кэширование маркера для принтера, открытого с помощью [**OpenPrinter2**](openprinter2.md).

## <a name="syntax"></a>Синтаксис


```C++
typedef enum tagPRINTER_OPTION_FLAGS { 
  PRINTER_OPTION_NO_CACHE,
  PRINTER_OPTION_CACHE,
  PRINTER_OPTION_CLIENT_CHANGE
} PRINTER_OPTION_FLAGS;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="PRINTER_OPTION_NO_CACHE"></span><span id="printer_option_no_cache"></span>**\_вариант принтера \_ без \_ кэша**
</dt> <dd>

Этот маркер не кэшируется. Все функции, применяемые к маркеру, возвращенному [**OpenPrinter2**](openprinter2.md) , будут отправлены на удаленный компьютер.

</dd> <dt>

<span id="PRINTER_OPTION_CACHE"></span><span id="printer_option_cache"></span>**\_кэш параметров \_ принтера**
</dt> <dd>

Этот маркер кэшируется. Все функции, применяемые к маркеру, возвращаемому функцией [**OpenPrinter2**](openprinter2.md) , переходят в локальный кэш.

</dd> <dt>

<span id="PRINTER_OPTION_CLIENT_CHANGE"></span><span id="printer_option_client_change"></span>**\_параметр принтера \_ \_ изменение клиента**
</dt> <dd>

Маркер, возвращенный [**OpenPrinter2**](openprinter2.md) , может использоваться [**сетпринтер**](setprinter.md) для переименования подключения к принтеру.

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

[**сетпринтер**](setprinter.md)
</dt> </dl>

 

 




