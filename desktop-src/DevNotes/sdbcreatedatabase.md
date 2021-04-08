---
description: Создает новую базу данных оболочек совместимости.
ms.assetid: 91fb180d-1a21-4011-821d-ea0fc999dc76
title: Функция Сдбкреатедатабасе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCreateDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 1ab8b8071cc210f6129545985d2d2e089680f0f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990551"
---
# <a name="sdbcreatedatabase-function"></a>Функция Сдбкреатедатабасе

Создает новую базу данных оболочек совместимости.

## <a name="syntax"></a>Синтаксис


```C++
PDB WINAPI SdbCreateDatabase(
  _In_ LPCWSTR   pwszPath,
  _In_ PATH_TYPE eType
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвсзпас* \[ окне\]
</dt> <dd>

Путь, по которому должна быть сохранена база данных. Этот параметр не может иметь **значение NULL**.

</dd> <dt>

*eType* \[ окне\]
</dt> <dd>

Тип пути. Список значений см. в разделе [**\_ тип пути**](path-type.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает маркер в базу данных оболочек совместимости или **значение NULL** при сбое.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сдбопендатабасе**](sdbopendatabase.md)
</dt> </dl>

 

 




