---
description: В \_ структуре doc info \_ описывается документ, который будет напечатан.
ms.assetid: d62333f3-cc39-4c9b-8fb3-02a2d24bbbad
title: Структура DOC_INFO_2 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOC_INFO_2
- _DOC_INFO_2A
- _DOC_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 27d7753fa16abcfbc30b28bcc4343b2e1ef7996cad408b54fefb850feac9b17e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846264"
---
# <a name="doc_info_2-structure"></a>\_Структура сведений о документе \_ 2

В **структуре \_ doc \_ info** описывается документ, который будет напечатан.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _DOC_INFO_2 {
  LPTSTR pDocName;
  LPTSTR pOutputFile;
  LPTSTR pDatatype;
  DWORD  dwMode;
  DWORD  JobId;
} DOC_INFO_2, *PDOC_INFO_2;
```



## <a name="members"></a>Члены

<dl> <dt>

**пдокнаме**
</dt> <dd>

Указатель на строку, завершающуюся нулем, которая указывает имя документа.

</dd> <dt>

**паутпутфиле**
</dt> <dd>

Указатель на строку, завершающуюся нулем, которая указывает имя выходного файла.

</dd> <dt>

**пдататипе**
</dt> <dd>

Указатель на строку, завершающуюся нулем, которая определяет тип данных, используемых для записи документа.

</dd> <dt>

**двмоде**
</dt> <dd>

Информирует диспетчер очереди печати о характере данных, которые следует отслеживать. Если это значение равно нулю, диспетчер очереди печати рассматривает данные, отправленные последующими вызовами [**вритепринтер**](writeprinter.md) , как обычные задания печати (независимо от того, зависит ли оно от свойства принтера). Если это значение — \_ канал di, то открывается только канал связи. В этом случае данные, передаваемые в последующие вызовы **вритепринтер** , отправляются на принтер или последующие вызовы [**реадпринтер**](readprinter.md) получать данные с принтера. Этот режим действует до тех пор, пока не будет вызван [**енддок**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) .

</dd> <dt>

**JobId**
</dt> <dd>

Зарезервировано для внутреннего использования; должно быть равно нулю.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>винспул. h (включает Windows. h)</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **\_ Doc \_ info \_ 2W** (Юникод) и **\_ doc \_ info \_ 2A** (ANSI)<br/>                                   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Вывод на печать](printdocs-printing.md)
</dt> <dt>

[Структуры API диспетчера очереди печати](printing-and-print-spooler-structures.md)
</dt> <dt>

[**енддок**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)
</dt> <dt>

[**реадпринтер**](readprinter.md)
</dt> <dt>

[**стартдокпринтер**](startdocprinter.md)
</dt> <dt>

[**вритепринтер**](writeprinter.md)
</dt> </dl>

 

 




