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
ms.openlocfilehash: 512e180549c246a5504bc14675d61082c68904aa767d98deca5111d9a275dc60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984104"
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

## <a name="remarks"></a>Remarks

База данных должна быть зарегистрирована, прежде чем можно будет использовать любые другие SDB-функции.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**сдбунрегистердатабасе**](sdbunregisterdatabase.md)
</dt> </dl>

 

 




