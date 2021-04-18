---
description: Типы данных эффектов. Данные содержатся в элементе pValue D3DXEFFECTDEFAULT.
ms.assetid: d698ad6e-2ce2-48d6-90be-49bc08f172a9
title: Перечисление D3DXEFFECTDEFAULTTYPE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECTDEFAULTTYPE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: ffd31167d712a8270011c061cd6328aa9214352e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694159"
---
# <a name="d3dxeffectdefaulttype-enumeration"></a>Перечисление D3DXEFFECTDEFAULTTYPE

Типы данных эффектов. Данные содержатся в элементе pValue [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md).

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DXEFFECTDEFAULTTYPE { 
  D3DXEDT_STRING      = 1,
  D3DXEDT_FLOATS      = 2,
  D3DXEDT_DWORD       = 3,
  D3DXEDT_FORCEDWORD  = 0x7fffffff
} D3DXEFFECTDEFAULTTYPE, *LPD3DXEFFECTDEFAULTTYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DXEDT_STRING"></span><span id="d3dxedt_string"></span>**\_Строка D3DXEDT**
</dt> <dd>

Тип данных является текстовой строкой ASCII, завершающейся НУЛЕМ.

</dd> <dt>

<span id="D3DXEDT_FLOATS"></span><span id="d3dxedt_floats"></span>**D3DXEDT с \_ плавающей запятой**
</dt> <dd>

Тип данных является массивом типа float. Число типов float в массиве задается параметром Нумбитес в [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md).

</dd> <dt>

<span id="D3DXEDT_DWORD"></span><span id="d3dxedt_dword"></span>**D3DXEDT \_ DWORD**
</dt> <dd>

Тип данных — DWORD.

</dd> <dt>

<span id="D3DXEDT_FORCEDWORD"></span><span id="d3dxedt_forcedword"></span>**D3DXEDT \_ форцедворд**
</dt> <dd>

Заставляет это перечисление компилироваться до 32 бит в размере. Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит. Это значение не используется.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




