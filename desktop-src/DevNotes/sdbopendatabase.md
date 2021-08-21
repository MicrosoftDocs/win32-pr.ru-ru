---
description: Открывает указанную базу данных оболочек.
ms.assetid: 148181d7-a20a-467c-984b-e32013960783
title: Функция Сдбопендатабасе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: df0081d7373bf67d3df1723be7d5beb272ef7ee4c77c54da8a6985dfe250d7c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161197"
---
# <a name="sdbopendatabase-function"></a>Функция Сдбопендатабасе

Открывает указанную базу данных оболочек.

## <a name="syntax"></a>Синтаксис


```C++
PDB WINAPI SdbOpenDatabase(
  _In_ LPCTSTR   pwszPath,
  _In_ PATH_TYPE eType
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвсзпас* \[ окне\]
</dt> <dd>

Путь к базе данных. Этот параметр не может иметь **значение NULL**.

</dd> <dt>

*eType* \[ окне\]
</dt> <dd>

Тип пути. Список значений см. в разделе [**\_ тип пути**](path-type.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает маркер в базу данных оболочек совместимости.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**сдбкреатедатабасе**](sdbcreatedatabase.md)
</dt> </dl>

 

 




