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
ms.openlocfilehash: ae0bca035f203593c43bb36e70119fbaf3024059
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807042"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сдбкреатедатабасе**](sdbcreatedatabase.md)
</dt> </dl>

 

 




