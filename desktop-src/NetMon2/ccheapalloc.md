---
description: Функция Кчеапаллок выделяет память для каждого образа.
ms.assetid: 6403c35f-d78f-48dc-90cc-0b76260bbab7
title: Функция Кчеапаллок (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapAlloc
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 14fce9f56103803e575d295799a5c5971ed1c459
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909416"
---
# <a name="ccheapalloc-function"></a>Функция Кчеапаллок

Функция **кчеапаллок** выделяет память для каждого образа.

## <a name="syntax"></a>Синтаксис


```C++
LPVOID WINAPI CCHeapAlloc(
   DWORD dwBytes,
   BOOL  bZeroInit
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*двбитес* 
</dt> <dd>

Запрошенная Длина выделенной памяти.

</dd> <dt>

*бзероинит* 
</dt> <dd>

Индикатор того, была ли инициализирована выделенная память. Если значение параметра равно **true**, то выделенная память инициализируется нулем.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращаемое значение является указателем на выделенную память. По завершении использования выделенной памяти освободите память, вызвав функцию [**кчеапфри**](ccheapfree.md) .

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

[**сеткЦинстптр**](setccinstptr.md)
</dt> <dt>

[**жеткЦинстптр**](getccinstptr.md)
</dt> <dt>

[**кчеапфри**](ccheapfree.md)
</dt> <dt>

[**кчеапреаллок**](ccheaprealloc.md)
</dt> <dt>

[**кчеапсизе**](ccheapsize.md)
</dt> </dl>

 

 




