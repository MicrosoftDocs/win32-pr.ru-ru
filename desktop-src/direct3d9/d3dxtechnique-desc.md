---
description: Описывает методику, используемую в результате.
ms.assetid: 7ba2dbb3-8039-4d1c-ad9d-130d9bf3d80a
title: Структура D3DXTECHNIQUE_DESC (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTECHNIQUE_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: 7e835c0eac067825942568464df8d5d345a06b530b71b7eaf7f319eae5f5d366
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119630734"
---
# <a name="d3dxtechnique_desc-structure"></a>\_Структура D3DXTECHNIQUE DESC

Описывает методику, используемую в результате.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DXTECHNIQUE_DESC {
  LPCSTR Name;
  UINT   Passes;
  UINT   Annotations;
} D3DXTECHNIQUE_DESC, *LPD3DXTECHNIQUE_DESC;
```



## <a name="members"></a>Члены

<dl> <dt>

**Имя**
</dt> <dd>

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Строка, содержащая имя метода.

</dd> <dt>

**Соответствующий**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Количество проходов, выполненных методом подготовки к просмотру. См. заметки.

</dd> <dt>

**Заметки**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Число заметок. См. раздел [Добавление сведений, чтобы параметры вступили в действие с \_ заметками](using-an-effect.md).

</dd> </dl>

## <a name="remarks"></a>Remarks

Некоторые видеоадаптеры могут визуализировать две текстуры за один проход. Тем не менее, если у карточки нет этой возможности, часто можно визуализировать тот же результат в двух проходах, используя одну текстуру для каждого прохода.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx9effect. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры эффектов](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
