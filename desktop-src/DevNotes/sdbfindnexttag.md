---
description: Выполняет поиск следующего ТЕГА в указанном родителе и возвращает TAGID совпадения.
ms.assetid: c96aa1c1-b0e6-49f5-9f74-7d0e050bee3b
title: Функция Сдбфинднексттаг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFindNextTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 7a5baf728a75e4c02c20ed4207b7d6b9a968af1e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895661"
---
# <a name="sdbfindnexttag-function"></a>Функция Сдбфинднексттаг

Выполняет поиск следующего ТЕГА в указанном родителе и возвращает **TAGID** совпадения.

## <a name="syntax"></a>Синтаксис


```C++
TAGID WINAPI SdbFindNextTag(
  _In_ PDB   pdb,
  _In_ TAGID tiParent,
  _In_ TAGID tiPrev
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pdb* \[ -файл окне\]
</dt> <dd>

Маркер базы данных оболочек совместимости.

</dd> <dt>

*типарент* \[ окне\]
</dt> <dd>

**TAGID** начала поиска. Этот параметр может иметь **тип TAGID \_ root** или **Tag \_ \_**.

</dd> <dt>

*типрев* \[ окне\]
</dt> <dd>

**TAGID** предыдущего совпадения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

**TAGID** совпадения.

## <a name="remarks"></a>Комментарии

Перед вызовом этой функции вызовите функцию [**сдбфиндфирсттаг**](sdbfindfirsttag.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сдбфиндфирсттаг**](sdbfindfirsttag.md)
</dt> <dt>

[**сдбтагрефтотагид**](sdbtagreftotagid.md)
</dt> </dl>

 

 




