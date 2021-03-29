---
description: Функция Лукупдвордсетстринг возвращает строку, соответствующую указанному значению набора с меткой.
ms.assetid: ee2b1b7a-6b64-4c8c-a71d-de970b66d46e
title: Функция Лукупдвордсетстринг (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LookupDwordSetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 57688edab7421f939e03322b8b244219b00d31fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810289"
---
# <a name="lookupdwordsetstring-function"></a>Функция Лукупдвордсетстринг

Функция **лукупдвордсетстринг** возвращает строку, соответствующую указанному значению набора с меткой.

## <a name="syntax"></a>Синтаксис


```C++
LPBYTE WINAPI LookupDwordSetString(
   LPSET lpSet,
   DWORD Value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лпсет* 
</dt> <dd>

Набор с метками, из которого можно извлечь метку значения.

</dd> <dt>

*Значение* 
</dt> <dd>

Значение набора с меткой.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращаемое значение является строкой, соответствующей указанному значению.

Если функция завершилась неудачно, указанное значение отсутствует в наборе, возвращаемое значение равно **null**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                            |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Библиотека<br/>                  | <dl> <dt>Parser. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




