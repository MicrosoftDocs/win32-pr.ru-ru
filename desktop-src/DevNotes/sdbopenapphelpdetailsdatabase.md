---
description: Открывает указанную базу данных сведений о AppHelp.
ms.assetid: c3b07c00-a3c6-419c-94c6-34c573a04d6d
title: Функция Сдбопенапфелпдетаилсдатабасе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenApphelpDetailsDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 2810b0bbe1f10f013f39570aecda448a4ceeea6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104140734"
---
# <a name="sdbopenapphelpdetailsdatabase-function"></a>Функция Сдбопенапфелпдетаилсдатабасе

Открывает указанную базу данных сведений о AppHelp.

## <a name="syntax"></a>Синтаксис


```C++
PDB WINAPI SdbOpenApphelpDetailsDatabase(
  _In_opt_ LPCWSTR pwsDetailsDatabasePath
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвсдетаилсдатабасепас* \[ в необязательное\]
</dt> <dd>

Путь к базе данных. Если этот параметр имеет **значение NULL**, то открывается локальная системная база данных.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает Handle в базу данных AppHelp Details.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




