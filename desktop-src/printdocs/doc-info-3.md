---
description: '\_ \_ Структура документа info 3 описывает документ, который будет напечатан.'
ms.assetid: 6e7b6727-da04-4f67-af77-6b51c68a4eb3
title: Структура DOC_INFO_3 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOC_INFO_3
- _DOC_INFO_3A
- _DOC_INFO_3W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 85d1d0f6af2eece8f9bd58112347478ec384642a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711938"
---
# <a name="doc_info_3-structure"></a>\_Структура документа info \_ 3

Структура **документа \_ info \_ 3** описывает документ, который будет напечатан.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _DOC_INFO_3 {
  LPTSTR pDocName;
  LPTSTR pOutputFile;
  LPTSTR pDatatype;
  DWORD  dwFlags;
} DOC_INFO_3, *PDOC_INFO_3;
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

**dwFlags**
</dt> <dd>

Метки. В настоящее время он может иметь **значение NULL** или быть следующим.



| Flag                 | Значение                                                                                                                                          |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| DI \_ меморимап \_ запись | Приводит к тому, что [**стартдокпринтер**](startdocprinter.md) не использует [**AddJob**](addjob.md) и [**ScheduleJob**](schedulejob.md) для локальной печати. |



 

</dd> </dl>

## <a name="remarks"></a>Комментарии

Параметр "DI \_ меморимап \_ Write" в **документе \_ info \_ 3** является оптимизацией. Это позволяет GDI сопоставлять файлы очереди в приложении и ускорить запись.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>Винспул. h (включение Windows. h)</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **\_ Doc \_ info \_ «кто** (Юникод) и **\_ \_ сведения о документе \_ 3a** (ANSI)<br/>                                   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Вывод на печать](printdocs-printing.md)
</dt> <dt>

[Структуры API диспетчера очереди печати](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddJob**](addjob.md)
</dt> <dt>

[**ScheduleJob**](schedulejob.md)
</dt> <dt>

[**стартдокпринтер**](startdocprinter.md)
</dt> </dl>

 

 




