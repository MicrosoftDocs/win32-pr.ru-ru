---
description: Функция Жетпротоколфромнаме возвращает маркер для протокола с заданным именем.
ms.assetid: 18f5a9a7-4245-479d-a0da-2ede362a60b8
title: Функция Жетпротоколфромнаме (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolFromName
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e104c066be2a5465083c7983aaefebd46f548b7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808705"
---
# <a name="getprotocolfromname-function"></a>Функция Жетпротоколфромнаме

Функция **жетпротоколфромнаме** возвращает маркер для протокола с заданным именем.

## <a name="syntax"></a>Синтаксис


```C++
HPROTOCOL WINAPI GetProtocolFromName(
  _In_ LPSTR ProtocolName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ProtocolName* \[ окне\]
</dt> <dd>

Имя протокола (например, IP).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращаемое значение является маркером протокола.

Если функция завершилась неудачно, возвращается значение **null**.

## <a name="remarks"></a>Комментарии

[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **жетпротоколфромнаме** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Библиотека<br/>                  | <dl> <dt>Нмапи. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




