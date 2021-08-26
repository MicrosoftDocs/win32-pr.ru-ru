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
ms.openlocfilehash: f534031da1c8f8f50309d4a2db0bfa39fe272ac34f59d1b490c24026d8fee261
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950004"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>винспул. h (включает Windows. h)</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **\_ \_ Сведения о \_ документации: 1W** (Юникод) и **\_ doc \_ info \_ 1A** (ANSI)<br/>                                   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Вывод на печать](printdocs-printing.md)
</dt> <dt>

[Структуры API диспетчера очереди печати](printing-and-print-spooler-structures.md)
</dt> <dt>

[**стартдокпринтер**](startdocprinter.md)
</dt> </dl>

 

 




