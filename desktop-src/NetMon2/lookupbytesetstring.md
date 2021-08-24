---
description: Функция Лукупбитесетстринг возвращает строку, соответствующую указанному значению набора с меткой.
ms.assetid: 295891f9-dc8d-4dbe-aac9-7d0a96993cfa
title: Функция Лукупбитесетстринг (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LookupByteSetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 208f7cef1a658ae321d7ce03aaee763e5387b5a45985d59134418a4d136e0b56
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742504"
---
# <a name="lookupbytesetstring-function"></a>Функция Лукупбитесетстринг

Функция **лукупбитесетстринг** возвращает строку, соответствующую указанному значению набора с меткой.

## <a name="syntax"></a>Синтаксис


```C++
LPBYTE WINAPI LookupByteSetString(
   LPSET lpSet,
   BYTE  Value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лпсет* 
</dt> <dd>

Указатель на набор с меткой, из которого можно извлечь метку значения.

</dd> <dt>

*Значение* 
</dt> <dd>

Значение набора с меткой.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращаемое значение является строкой, соответствующей предоставленному значению.

Если функция завершилась неудачно, возвращается значение **null**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                            |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Библиотека<br/>                  | <dl> <dt>Parser. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




