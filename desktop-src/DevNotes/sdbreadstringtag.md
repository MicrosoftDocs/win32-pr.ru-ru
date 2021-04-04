---
Description: Извлекает строку для указанного TAGID.
ms.assetid: d67d386d-a2c5-46e2-8887-9ee20ea427f9
title: Функция Сдбреадстрингтаг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadStringTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 3f368d66e0fbc144a46683a04655cd7f650c3bce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989276"
---
# <a name="sdbreadstringtag-function"></a>Функция Сдбреадстрингтаг

Извлекает строку для указанного **TAGID**.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI SdbReadStringTag(
  _In_  PDB    pdb,
  _In_  TAGID  tiWhich,
  _Out_ LPTSTR pwszBuffer,
  _In_  DWORD  cchBufferSize
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

*пвсзбуффер* \[ заполняет\]
</dt> <dd>

Буфер, который получает строку. Этот параметр не может иметь **значение NULL**.

</dd> <dt>

*кчбуфферсизе* \[ окне\]
</dt> <dd>

Размер буфера *пвсзбуффер* в символах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает **true** при успешном выполнении или **false** в случае сбоя.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сдбжетбинаритагдата**](sdbgetbinarytagdata.md)
</dt> <dt>

[**сдбжетстрингтагптр**](sdbgetstringtagptr.md)
</dt> <dt>

[**сдбреадбинаритаг**](sdbreadbinarytag.md)
</dt> <dt>

[**сдбреаддвордтаг**](sdbreaddwordtag.md)
</dt> </dl>

 

 




