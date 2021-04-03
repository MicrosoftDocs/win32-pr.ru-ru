---
description: Выполняет поиск следующего дочернего ТЕГА в указанном родителе и возвращает TAGID следующего дочернего элемента.
ms.assetid: c7311f20-15ca-4b2d-a08d-8bb992a3a0cd
title: Функция Сдбжетнекстчилд
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetNextChild
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 4f2943eaf0baec84a9473b679743b9eafad3b7fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895817"
---
# <a name="sdbgetnextchild-function"></a>Функция Сдбжетнекстчилд

Выполняет поиск следующего дочернего ТЕГА в указанном родителе и возвращает **TAGID** следующего дочернего элемента.

## <a name="syntax"></a>Синтаксис


```C++
TAGID WINAPI SdbGetNextChild(
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

**TAGID** предыдущего дочернего элемента.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

**TAGID** дочернего элемента или **TAGID \_ null** , если дочерний элемент не найден.

## <a name="remarks"></a>Комментарии

Перед вызовом этой функции вызовите функцию [**сдбжетфирстчилд**](sdbgetfirstchild.md) .

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

[**сдбжетфирстчилд**](sdbgetfirstchild.md)
</dt> </dl>

 

 




