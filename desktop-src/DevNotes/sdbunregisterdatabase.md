---
description: Отменяет регистрацию указанной базы данных и делает ее более недоступной.
ms.assetid: 7e6c50f4-85f6-4b33-b639-d8fda143e5e7
title: Функция Сдбунрегистердатабасе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbUnregisterDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 72171e1f9ae20ac2213a285046b2499093be4313
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496092"
---
# <a name="sdbunregisterdatabase-function"></a>Функция Сдбунрегистердатабасе

Отменяет регистрацию указанной базы данных и делает ее более недоступной.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI SdbUnregisterDatabase(
  _In_ GUID *pguidDB
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пгуиддб* \[ окне\]
</dt> <dd>

Идентификатор GUID базы данных. Этот параметр не может иметь **значение NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает **true** при успешном выполнении или **false** в случае сбоя.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сдбрегистердатабасикс**](sdbregisterdatabaseex.md)
</dt> </dl>

 

 




