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
ms.openlocfilehash: 92d63182273c96707bb155071164a6b6838378615f603d8ef6d332d6c65be460
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911574"
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
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                   |
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

 

 




