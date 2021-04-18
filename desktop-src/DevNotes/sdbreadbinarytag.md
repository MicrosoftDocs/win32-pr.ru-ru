---
Description: Извлекает двоичные данные для указанного TAGID.
ms.assetid: b349f2af-2505-4efc-bd59-203f7666ce61
title: Функция Сдбреадбинаритаг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadBinaryTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 024b432c3210b98721a0cf3058bad0f765287fde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654487"
---
# <a name="sdbreadbinarytag-function"></a>Функция Сдбреадбинаритаг

Извлекает двоичные данные для указанного **TAGID**.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI SdbReadBinaryTag(
  _In_  PDB   pdb,
  _In_  TAGID tiWhich,
  _Out_ PBYTE pBuffer,
  _In_  DWORD dwBufferSize
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

*pBuffer* \[ заполняет\]
</dt> <dd>

Буфер, который получает двоичные данные. Этот параметр не может иметь **значение NULL**.

</dd> <dt>

*двбуфферсизе* \[ окне\]
</dt> <dd>

Размер буфера *pBuffer* в байтах.

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

[**сдбреаддвордтаг**](sdbreaddwordtag.md)
</dt> <dt>

[**сдбреадстрингтаг**](sdbreadstringtag.md)
</dt> </dl>

 

 




