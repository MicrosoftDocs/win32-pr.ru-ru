---
Description: Извлекает значение QWORD для указанного TAGID.
ms.assetid: 5fa94a95-c7f3-477b-ab7c-931e8d62d501
title: Функция Сдбреадквордтаг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadQWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 4280c21983fa86312229930b7496625c594f0caac384f0dc6d130f673ce68509
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815284"
---
# <a name="sdbreadqwordtag-function"></a>Функция Сдбреадквордтаг

Извлекает значение **QWORD** для указанного **TAGID**.

## <a name="syntax"></a>Синтаксис


```C++
ULONGLONG WINAPI SdbReadQWORDTag(
  _In_ PDB       pdb,
  _In_ TAGID     tiWhich,
  _In_ ULONGLONG qwDefault
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

**TAGID** , соответствующий получаемым данным.

</dd> <dt>

*квдефаулт* \[ окне\]
</dt> <dd>

Значение по умолчанию, возвращаемое при сбое.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает значение в случае успеха или *квдефаулт* при сбое.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**сдбжетбинаритагдата**](sdbgetbinarytagdata.md)
</dt> <dt>

[**сдбжетстрингтагптр**](sdbgetstringtagptr.md)
</dt> <dt>

[**сдбреаддвордтаг**](sdbreaddwordtag.md)
</dt> <dt>

[**сдбреадстрингтаг**](sdbreadstringtag.md)
</dt> </dl>

 

 




