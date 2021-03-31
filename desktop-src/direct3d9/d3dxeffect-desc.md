---
description: Описывает объект Effect.
ms.assetid: 161d3e7a-213a-4a83-a1b5-837b0aab96bf
title: Структура D3DXEFFECT_DESC (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: c8e7a3a2adf19514e2e4d1c6f61dbea888ce033d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821093"
---
# <a name="d3dxeffect_desc-structure"></a>\_Структура D3DXEFFECT DESC

Описывает объект Effect.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DXEFFECT_DESC {
  LPCSTR Creator;
  UINT   Parameters;
  UINT   Techniques;
  UINT   Functions;
} D3DXEFFECT_DESC, *LPD3DXEFFECT_DESC;
```



## <a name="members"></a>Члены

<dl> <dt>

**Автор**
</dt> <dd>

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Строка, содержащая имя создателя эффектов.

</dd> <dt>

**Параметры**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Количество параметров, используемых для вступления в действие.

</dd> <dt>

**Технологий**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Количество методов, которые могут визуализировать результат.

</dd> <dt>

**Функции**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Число функций, которые могут визуализировать результат.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Объект Effect может содержать несколько методов отрисовки и параметров для одного и того же результата.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9effect. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры эффектов](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
