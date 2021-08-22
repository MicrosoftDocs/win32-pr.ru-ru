---
description: Функция Кчеапсизе возвращает размер памяти, выделенной функцией Кчеапаллок.
ms.assetid: 45d0fd89-bcd1-4298-8cc3-834d86301f93
title: Функция Кчеапсизе (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapSize
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b086777b571af417662bd60a582fbc53a07c49300d21d2c59b6a36d2247b9d14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012319"
---
# <a name="ccheapsize-function"></a>Функция Кчеапсизе

Функция **кчеапсизе** возвращает размер памяти, выделенной функцией **кчеапаллок** .

## <a name="syntax"></a>Синтаксис


```C++
SIZE_T WINAPI CCHeapSize(
   LPVOID lpMem
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лпмем* 
</dt> <dd>

Указатель на выделенную область памяти.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращаемое значение равно размеру запрошенного блока памяти, измеряемого в байтах.

Если функция завершилась неудачно, возвращается значение **null**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Библиотека<br/>                  | <dl> <dt>Нмапи. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[сеткЦинстптр](setccinstptr.md)
</dt> <dt>

[жеткЦинстптр](getccinstptr.md)
</dt> <dt>

[кчеапаллок](ccheapalloc.md)
</dt> <dt>

[кчеапфри](ccheapfree.md)
</dt> <dt>

[кчеапреаллок](ccheaprealloc.md)
</dt> </dl>

 

 




