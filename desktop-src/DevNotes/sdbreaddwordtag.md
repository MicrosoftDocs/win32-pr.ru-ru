---
Description: Возвращает значение DWORD для указанного TAGID.
ms.assetid: 6610e101-9068-4812-b0ca-528658b62535
title: Функция Сдбреаддвордтаг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadDWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 4ce168aab7755dcd11f145caf44678a489bca152753ea010edbd7387b3e730f5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044954"
---
# <a name="sdbreaddwordtag-function"></a>Функция Сдбреаддвордтаг

Возвращает значение **DWORD** для указанного **TAGID**.

## <a name="syntax"></a>Синтаксис


```C++
DWORD WINAPI SdbReadDWORDTag(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich,
  _In_ DWORD dwDefault
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

*двдефаулт* \[ окне\]
</dt> <dd>

Значение по умолчанию, возвращаемое при сбое.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает значение в случае успеха или *двдефаулт* при сбое.

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

[**сдбреадквордтаг**](sdbreadqwordtag.md)
</dt> <dt>

[**сдбреадстрингтаг**](sdbreadstringtag.md)
</dt> </dl>

 

 




