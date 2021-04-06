---
description: Выполняет поиск совпадения ТЕГА в указанном родительском элементе и возвращает TAGID первого совпадения.
ms.assetid: ecbe216c-1e46-4472-b1d1-e2ac7ace82ab
title: Функция Сдбфиндфирсттаг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFindFirstTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: dc8b752d536be83d90ded55474166d14521f0f7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990308"
---
# <a name="sdbfindfirsttag-function"></a>Функция Сдбфиндфирсттаг

Выполняет поиск совпадения ТЕГА в указанном родительском элементе и возвращает **TAGID** первого совпадения.

## <a name="syntax"></a>Синтаксис


```C++
TAGID WINAPI SdbFindFirstTag(
  _In_ PDB   pdb,
  _In_ TAGID tiParent,
  _In_ TAG   tTag
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

*ттаг* \[ окне\]
</dt> <dd>

ТЕГ для сопоставления. Список возможных значений см. в разделе [тег](tag.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

**TAGID** первого совпадения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сдбфинднексттаг**](sdbfindnexttag.md)
</dt> <dt>

[**сдбтагрефтотагид**](sdbtagreftotagid.md)
</dt> </dl>

 

 




