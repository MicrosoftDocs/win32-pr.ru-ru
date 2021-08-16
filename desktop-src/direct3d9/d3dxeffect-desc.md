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
ms.openlocfilehash: 0b30ad0348a5c799690d668e036724d30808c2998eee9d762fa2ad3fc8106c91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118298597"
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

## <a name="remarks"></a>Remarks

Объект Effect может содержать несколько методов отрисовки и параметров для одного и того же результата.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx9effect. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры эффектов](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
