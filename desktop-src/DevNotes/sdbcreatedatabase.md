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
ms.openlocfilehash: 6c7ac5d30c9c5a0154d770266410d278c5c3f31a65166515078a5384b1b8b55d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161564"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**сдбопендатабасе**](sdbopendatabase.md)
</dt> </dl>

 

 




