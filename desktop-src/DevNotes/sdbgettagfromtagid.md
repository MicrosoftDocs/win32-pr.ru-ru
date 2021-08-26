---
description: Извлекает тег, связанный с указанным TAGID.
ms.assetid: 194d2035-fc2c-445d-a730-90db2ccea8af
title: Функция Сдбжеттагфромтагид
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetTagFromTagID
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: a7e58343cf9a863f6b3cecc7f9b6414414387e2f2b33859de1eb015d65f1a78b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058474"
---
# <a name="sdbgettagfromtagid-function"></a>Функция Сдбжеттагфромтагид

Извлекает тег, связанный с указанным **TAGID**.

## <a name="syntax"></a>Синтаксис


```C++
TAG WINAPI SdbGetTagFromTagID(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pdb* \[ -файл окне\]
</dt> <dd>

Маркер базы данных оболочек совместимости.

</dd> <dt>

*тивхич* \[ окне\]
</dt> <dd>

**TAGID** для тега.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает тег.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ТЕГАМИ**](tag.md)
</dt> <dt>

[**TAGID**](tagid.md)
</dt> </dl>

 

 




