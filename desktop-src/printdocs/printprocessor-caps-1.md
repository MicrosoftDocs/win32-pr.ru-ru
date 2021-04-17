---
description: Структура ПРИНТПРОЦЕССОР \_ Cap \_ 1 — это формат сведений о возможностях принтера, возвращаемых функцией жетпринтердата в буфере, заданном переменной pData.
ms.assetid: 43c568ff-ccc9-4873-b159-ede09b4a7e51
title: Структура PRINTPROCESSOR_CAPS_1 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTPROCESSOR_CAPS_1
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 131b5ecf874554c3642808570a53ee8b20ad0e68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693418"
---
# <a name="printprocessor_caps_1-structure"></a>\_Структура принтпроцессор Cap \_ 1

Структура **принтпроцессор \_ Cap \_ 1** — это формат сведений о возможностях принтера, возвращаемых функцией [**жетпринтердата**](getprinterdata.md) в буфере, заданном переменной *pData* .

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _PRINTPROCESSOR_CAPS_1 {
  DWORD dwLevel;
  DWORD dwNupOptions;
  DWORD dwPageOrderFlags;
  DWORD dwNumberOfCopies;
} PRINTPROCESSOR_CAPS_1, *PPRINTPROCESSOR_CAPS_1;
```



## <a name="members"></a>Члены

<dl> <dt>

**двлевел**
</dt> <dd>

Номер версии структуры. Это значение должно быть равно 1.

</dd> <dt>

**двнупоптионс**
</dt> <dd>

Битовая маска, представляющая различные числа страниц документа, которые принтер может печатать на физической странице. Младший значащий бит представляет 1 страницу документа на странице, следующий бит представляет две страницы документа на странице и т. д. Например, 0x0000810B указывает, что принтер поддерживает 1, 2, 4, 9 и 16 страниц документа на физическую страницу.

</dd> <dt>

**двпажеордерфлагс**
</dt> <dd>

Порядок, в котором будут печататься страницы. Это значение может иметь обычную \_ Печать, обратную \_ Печать или буклетную \_ Печать.

</dd> <dt>

**двнумберофкопиес**
</dt> <dd>

Максимальное число копий, которое может быть обработано принтером.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Значения всех членов структуры предоставляются функцией [**жетпринтпроцессоркапабилитиес**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) , которая описана в комплекте драйверов для Windows (WDK).

Диспетчер очереди вызовов вызывает функцию [**жетпринтпроцессоркапабилитиес**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) обработчика печати, когда приложение вызывает [**жетпринтердата**](getprinterdata.md), указывая имя значения с форматом типа данных принтпроккапс \_ , где *DataType* — это имя входного типа.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>Винспул. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Вывод на печать](printdocs-printing.md)
</dt> <dt>

[Структуры API диспетчера очереди печати](printing-and-print-spooler-structures.md)
</dt> <dt>

[**жетпринтердата**](getprinterdata.md)
</dt> </dl>

 

