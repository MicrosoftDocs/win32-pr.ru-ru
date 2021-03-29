---
description: Функция Кчеапреаллок перераспределяет память, выделенную функцией Кчеапаллок.
ms.assetid: 82365ce2-3980-44ff-be0f-062a65f676fc
title: Функция Кчеапреаллок (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapReAlloc
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e1619e2e6e81e8a265600f8437a6633e18065f10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813625"
---
# <a name="ccheaprealloc-function"></a>Функция Кчеапреаллок

Функция **кчеапреаллок** перераспределяет память, выделенную функцией **кчеапаллок** .

## <a name="syntax"></a>Синтаксис


```C++
LPVOID WINAPI CCHeapReAlloc(
   LPVOID lpMem,
   DWORD  dwBytes,
   BOOL   bZeroInit
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лпмем* 
</dt> <dd>

Указатель на исходную выделенную память.

</dd> <dt>

*двбитес* 
</dt> <dd>

Размер перераспределенной памяти, измеряемый в байтах.

</dd> <dt>

*бзероинит* 
</dt> <dd>

Признак инициализации повторно выделяемой памяти. Если значение параметра равно **true**, то вновь выделенная память инициализируется нулем.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращаемое значение является указателем на перераспределенную память.

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

[кчеапсизе](ccheapsize.md)
</dt> </dl>

 

 




