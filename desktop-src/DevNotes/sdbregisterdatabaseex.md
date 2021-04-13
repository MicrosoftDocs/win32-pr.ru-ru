---
description: Регистрирует указанную базу данных.
ms.assetid: 65eceb1a-9ce1-4b97-98d7-731932797794
title: Функция Сдбрегистердатабасикс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbRegisterDatabaseEx
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 74872f8895032abe02b024396fda12c43dc1611d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538660"
---
# <a name="sdbregisterdatabaseex-function"></a>Функция Сдбрегистердатабасикс

Регистрирует указанную базу данных.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI SdbRegisterDatabaseEx(
  _In_     LPCTSTR    pszDatabasePath,
  _In_     DWORD      dwDatabaseType,
  _In_opt_ PULONGLONG pTimeStamp
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псздатабасепас* \[ окне\]
</dt> <dd>

Путь к базе данных. Этот параметр не может иметь **значение NULL**.

</dd> <dt>

*двдатабасетипе* \[ окне\]
</dt> <dd>

Тип базы данных. Список значений см. в разделе [типы базы данных оболочек](shim-database-types.md) .

</dd> <dt>

*птиместамп* \[ в необязательное\]
</dt> <dd>

Метка времени для базы данных. Если этот параметр имеет **значение NULL**, используется системное время.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает **true** при успешном выполнении или **false** в случае сбоя.

## <a name="remarks"></a>Комментарии

База данных должна быть зарегистрирована, прежде чем можно будет использовать любые другие SDB-функции.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сдбунрегистердатабасе**](sdbunregisterdatabase.md)
</dt> </dl>

 

 




