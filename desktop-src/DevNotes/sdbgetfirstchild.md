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
ms.openlocfilehash: 58e63b3c1c8b3e56c9610ec795c1706fe58990e4611c36886ee4a3061d0816fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075978"
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
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сдбфиндфирсттаг**](sdbfindfirsttag.md)
</dt> <dt>

[**сдбфинднексттаг**](sdbfindnexttag.md)
</dt> <dt>

[**сдбжетнекстчилд**](sdbgetnextchild.md)
</dt> </dl>

 

 




