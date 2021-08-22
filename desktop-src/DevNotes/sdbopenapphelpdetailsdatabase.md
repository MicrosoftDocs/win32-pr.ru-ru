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
ms.openlocfilehash: d6bd0bc7cbd1404c3bcf5459254f53e62a777d0936b89a0f7a282dd8d0094227
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045164"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




