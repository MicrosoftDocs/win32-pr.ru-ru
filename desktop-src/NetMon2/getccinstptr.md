---
description: Функция ЖеткЦинстптр возвращает указатель на данные экземпляра, добавленные в контекст записи.
ms.assetid: 6fb103d3-583b-4460-8b9a-ff921751b0eb
title: Функция ЖеткЦинстптр (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCCInstPtr
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2f078e91829b5324218b901e41e000d37b4cd6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808717"
---
# <a name="getccinstptr-function"></a>Функция ЖеткЦинстптр

Функция **жеткЦинстптр** возвращает указатель на данные экземпляра, добавленные в контекст записи.

## <a name="syntax"></a>Синтаксис


```C++
LPVOID WINAPI GetCCInstPtr(void);
```



## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращаемое значение является указателем на данные экземпляра определенной записи.

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

[кчеапаллок](ccheapalloc.md)
</dt> <dt>

[кчеапфри](ccheapfree.md)
</dt> <dt>

[кчеапреаллок](ccheaprealloc.md)
</dt> <dt>

[кчеапсизе](ccheapsize.md)
</dt> </dl>

 

 




