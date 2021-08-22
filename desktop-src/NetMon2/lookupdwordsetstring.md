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
ms.openlocfilehash: b72f21d47001e2060c3b27daa80a584dcad77b55fd1df289a5bdb5476549cf38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677234"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                            |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Библиотека<br/>                  | <dl> <dt>Parser. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




