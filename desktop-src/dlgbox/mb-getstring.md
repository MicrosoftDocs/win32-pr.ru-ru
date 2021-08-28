---
title: Функция MB_GetString (User. h)
description: Возвращает строки для стандартных кнопок окна сообщения.
ms.assetid: D2AF238D-F5A8-477D-BF47-0F5D4D68B27E
keywords:
- Диалоговые окна MB_GetString функции
topic_type:
- apiref
api_name:
- MB_GetString
api_location:
- user32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bdd984a2f65ab8c2eed8a77fffa56af1d94633c828196428a674c9eee78c3ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985364"
---
# <a name="mb_getstring-function"></a>MB, \_ функция GetString

Возвращает строки для стандартных кнопок окна сообщения.

## <a name="syntax"></a>Синтаксис


```C++
LPCWSTR WINAPI MB_GetString(
   UINT wBtn
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*вбтн* 
</dt> <dd>

Идентификатор возвращаемой строки. Они определяются значениями ИДЕНТИФИКАТОРов команд диалогового окна, указанными в файле WinUser. h.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Строка или значение NULL, если объект не найден.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>User. h</dt> </dl>     |
| Библиотека<br/> | <dl> <dt>User32. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>User32.dll</dt> </dl> |



 

 





