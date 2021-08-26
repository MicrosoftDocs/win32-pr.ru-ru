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
ms.openlocfilehash: 210e0aab8cb5e43bfc649e8abb72cf565c4d4f892f651708286f7a3f87d11ce2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045320"
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

## <a name="remarks"></a>Remarks

Перед вызовом этой функции вызовите функцию [**сдбжетфирстчилд**](sdbgetfirstchild.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**сдбфиндфирсттаг**](sdbfindfirsttag.md)
</dt> <dt>

[**сдбфинднексттаг**](sdbfindnexttag.md)
</dt> <dt>

[**сдбжетфирстчилд**](sdbgetfirstchild.md)
</dt> </dl>

 

 




