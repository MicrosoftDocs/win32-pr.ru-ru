---
description: '\_ \_ Структура документа с информацией 1 описывает документ, который будет напечатан.'
ms.assetid: 142d988b-dd74-4312-8b27-331a7ec70344
title: Структура DOC_INFO_1 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOC_INFO_1
- _DOC_INFO_1A
- _DOC_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 6f905a89163b46743a92c8616ee0fa3d0564590c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264339"
---
# <a name="doc_info_1-structure"></a>\_Структура сведений о документе \_ 1

Структура документа с **\_ информацией \_ 1** описывает документ, который будет напечатан.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _DOC_INFO_1 {
  LPTSTR pDocName;
  LPTSTR pOutputFile;
  LPTSTR pDatatype;
} DOC_INFO_1;
```



## <a name="members"></a>Члены

<dl> <dt>

**пдокнаме**
</dt> <dd>

Указатель на строку, завершающуюся нулем, которая указывает имя документа.

</dd> <dt>

**паутпутфиле**
</dt> <dd>

Указатель на строку, завершающуюся нулем, которая указывает имя выходного файла. Для печати на принтере установите значение **null**.

</dd> <dt>

**пдататипе**
</dt> <dd>

Указатель на строку, завершающуюся нулем, которая определяет тип данных, используемых для записи документа.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>Винспул. h (включение Windows. h)</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **\_ \_ Сведения о \_ документации: 1W** (Юникод) и **\_ doc \_ info \_ 1A** (ANSI)<br/>                                   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Вывод на печать](printdocs-printing.md)
</dt> <dt>

[Структуры API диспетчера очереди печати](printing-and-print-spooler-structures.md)
</dt> <dt>

[**стартдокпринтер**](startdocprinter.md)
</dt> </dl>

 

 




