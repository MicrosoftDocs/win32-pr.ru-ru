---
description: Параметры, применяемые по умолчанию.
ms.assetid: a8a24cf2-0ecd-4429-97d3-086ff49540a1
title: Структура D3DXEFFECTDEFAULT (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECTDEFAULT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 41beda43807ace6b0f335dc1937f8843cbc11544e4842f86af98eb0e0bb0802a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117731883"
---
# <a name="d3dxeffectdefault-structure"></a>Структура D3DXEFFECTDEFAULT

Параметры, применяемые по умолчанию.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DXEFFECTDEFAULT {
  LPSTR                 pParamName;
  D3DXEFFECTDEFAULTTYPE Type;
  DWORD                 NumBytes;
  LPVOID                pValue;
} D3DXEFFECTDEFAULT, *LPD3DXEFFECTDEFAULT;
```



## <a name="members"></a>Члены

<dl> <dt>

**ппарамнаме**
</dt> <dd>

Тип: **LPSTR**

</dd> <dd>

Имя параметра.

</dd> <dt>

**Тип**
</dt> <dd>

Тип: **[ **D3DXEFFECTDEFAULTTYPE**](./d3dxeffectdefaulttype.md)**

</dd> <dd>

Тип данных в pValue. Дополнительные сведения см. в разделе [ **D3DXEFFECTDEFAULTTYPE**](./d3dxeffectdefaulttype.md)

</dd> <dt>

**нумбитес**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Размер (в байтах) данных, на которые указывает pValue.

</dd> <dt>

**pValue**
</dt> <dd>

Тип: **[ **лпвоид**](../winprog/windows-data-types.md)**

</dd> <dd>

Указатель на место в памяти, содержащее данные.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры эффектов](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
