---
description: Функция Лукупвордсетстринг возвращает строку, соответствующую запрошенному значению из набора с меткой.
ms.assetid: e8d158a1-8544-4c10-b8e8-46888c1097e4
title: Функция Лукупвордсетстринг (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LookupWordSetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7487becb195571e1eb88044195293b2c0b226e8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542375"
---
# <a name="lookupwordsetstring-function"></a>Функция Лукупвордсетстринг

Функция **лукупвордсетстринг** возвращает строку, соответствующую запрошенному значению из набора с меткой.

## <a name="syntax"></a>Синтаксис


```C++
LPBYTE WINAPI LookupWordSetString(
   LPSET lpSet,
   WORD  Value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лпсет* 
</dt> <dd>

Набор с меткой, из которого извлекается метка значения.

</dd> <dt>

*Значение* 
</dt> <dd>

Значение набора с меткой.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращаемое значение является строкой, соответствующей запрошенному значению.

Если функция завершилась неудачно, указанное значение отсутствует в наборе, возвращаемое значение равно **null**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                            |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Библиотека<br/>                  | <dl> <dt>Parser. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




