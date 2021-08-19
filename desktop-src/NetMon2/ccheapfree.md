---
description: Функция Кчеапфри освобождает память, выделенную функцией Кчеапаллок.
ms.assetid: 4e1f3332-b0cb-4c21-8c36-59e14c9686cd
title: Функция Кчеапфри (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapFree
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b29d57c3d56136103fb1948340472343f56727c2df0268a5036dc148fdd0493a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796344"
---
# <a name="ccheapfree-function"></a>Функция Кчеапфри

Функция **кчеапфри** освобождает память, выделенную функцией **кчеапаллок** .

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI CCHeapFree(
   LPVOID lpMem
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лпмем* 
</dt> <dd>

Указатель на память, которую выпустит эта функция.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция **кчеапфри** выполнена успешно, возвращается значение **true**.

Если функция завершается неудачно, возвращается значение **false**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Библиотека<br/>                  | <dl> <dt>Нмапи. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[сеткЦинстптр](setccinstptr.md)
</dt> <dt>

[жеткЦинстптр](getccinstptr.md)
</dt> <dt>

[кчеапаллок](ccheapalloc.md)
</dt> <dt>

[кчеапреаллок](ccheaprealloc.md)
</dt> <dt>

[кчеапсизе](ccheapsize.md)
</dt> </dl>

 

 




