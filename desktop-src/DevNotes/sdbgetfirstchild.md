---
description: Выполняет поиск дочернего ТЕГА в указанном родительском элементе и возвращает TAGID первого дочернего элемента.
ms.assetid: 67538c7e-6360-40fa-b50f-dcbc7a6a147d
title: Функция Сдбжетфирстчилд
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetFirstChild
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: abc06ae0e4b5d842a968d0f3fbeb7a15702660b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538255"
---
# <a name="sdbgetfirstchild-function"></a>Функция Сдбжетфирстчилд

Выполняет поиск дочернего ТЕГА в указанном родительском элементе и возвращает **TAGID** первого дочернего элемента.

## <a name="syntax"></a>Синтаксис


```C++
TAGID WINAPI SdbGetFirstChild(
  _In_ PDB   pdb,
  _In_ TAGID tiParent
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

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

**TAGID** первого дочернего элемента или **TAGID \_ null** не найден дочерний элемент.

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

[**сдбфинднексттаг**](sdbfindnexttag.md)
</dt> <dt>

[**сдбжетнекстчилд**](sdbgetnextchild.md)
</dt> </dl>

 

 




