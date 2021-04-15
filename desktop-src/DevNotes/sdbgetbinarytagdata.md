---
description: Извлекает двоичные данные для указанного TAGID.
ms.assetid: 18992406-67b4-4c48-9629-04d6bf1c5824
title: Функция Сдбжетбинаритагдата
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetBinaryTagData
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 028b073b149482b79b848216e44b8a425d6ffb56
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662079"
---
# <a name="sdbgetbinarytagdata-function"></a>Функция Сдбжетбинаритагдата

Извлекает двоичные данные для указанного **TAGID**.

## <a name="syntax"></a>Синтаксис


```C++
PVOID WINAPI SdbGetBinaryTagData(
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

**TAGID** , соответствующий получаемым данным.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает указатель на двоичные данные или **значение NULL** , если **TAGID** является недопустимым.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сдбжетстрингтагптр**](sdbgetstringtagptr.md)
</dt> <dt>

[**сдбреаддвордтаг**](sdbreaddwordtag.md)
</dt> <dt>

[**сдбреадквордтаг**](sdbreadqwordtag.md)
</dt> <dt>

[**сдбреадстрингтаг**](sdbreadstringtag.md)
</dt> </dl>

 

 




