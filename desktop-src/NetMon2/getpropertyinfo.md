---
description: Функция GetPropertyInfo возвращает указатель на сведения о свойстве данного протокола.
ms.assetid: f65166ba-1d94-4d65-b9d7-edb84ada0826
title: Функция GetPropertyInfo (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPropertyInfo
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 007332a85f170f865604526199681cad6d68cdcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896774"
---
# <a name="getpropertyinfo-function"></a>Функция GetPropertyInfo

Функция **GetPropertyInfo** возвращает указатель на сведения о свойстве данного протокола.

## <a name="syntax"></a>Синтаксис


```C++
LPPROPERTYINFO WINAPI GetPropertyInfo(
  _In_ HPROPERTY hProperty
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хпроперти* \[ окне\]
</dt> <dd>

Обработчик для свойства.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращаемое значение является указателем на свойство.

Если функция завершилась неудачно, возвращается значение **null**.

## <a name="remarks"></a>Комментарии

[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **GetPropertyInfo** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Библиотека<br/>                  | <dl> <dt>Нмапи. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




