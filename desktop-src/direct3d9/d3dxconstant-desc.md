---
description: Описание константы в таблице констант.
ms.assetid: d1970536-7195-4270-a1b9-b082ebe4f17f
title: Структура D3DXCONSTANT_DESC (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCONSTANT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: d737fa1d95a119668602aeb056e15bc4248200aa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713926"
---
# <a name="d3dxconstant_desc-structure"></a>\_Структура D3DXCONSTANT DESC

Описание константы в таблице констант.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DXCONSTANT_DESC {
  LPCSTR              Name;
  D3DXREGISTER_SET    RegisterSet;
  UINT                RegisterIndex;
  UINT                RegisterCount;
  D3DXPARAMETER_CLASS Class;
  D3DXPARAMETER_TYPE  Type;
  UINT                Rows;
  UINT                Columns;
  UINT                Elements;
  UINT                StructMembers;
  UINT                Bytes;
  LPCVOID             DefaultValue;
} D3DXCONSTANT_DESC, *LPD3DXCONSTANT_DESC;
```



## <a name="members"></a>Члены

<dl> <dt>

**Name**
</dt> <dd>

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Имя константы.

</dd> <dt>

**Register**
</dt> <dd>

Тип: **[ **D3DXREGISTER \_ Set** .](./d3dxregister-set.md)**

</dd> <dd>

Постоянный тип данных. См. раздел [**D3DXREGISTER \_ Set**](./d3dxregister-set.md).

</dd> <dt>

**регистериндекс**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Отсчитываемый от нуля индекс константы в таблице.

</dd> <dt>

**регистеркаунт**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Количество регистров, содержащих данные.

</dd> <dt>

**Класс**
</dt> <dd>

Тип: **[ **\_ класс D3DXPARAMETER**](./d3dxparameter-class.md)**

</dd> <dd>

Класс параметра. См. раздел [**\_ класс D3DXPARAMETER**](./d3dxparameter-class.md).

</dd> <dt>

**Тип**
</dt> <dd>

Тип: **[ **D3DXPARAMETER \_ тип**](./d3dxparameter-type.md)**

</dd> <dd>

Тип параметра. См. раздел [**\_ тип D3DXPARAMETER**](./d3dxparameter-type.md).

</dd> <dt>

**Строки**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Число строк.

</dd> <dt>

**Столбцы**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Число столбцов.

</dd> <dt>

**Elements (XElement Dynamic Property)** (Elements (Динамическое свойство XElement))
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Число элементов в массиве.

</dd> <dt>

**структмемберс**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Число подпараметров элемента структуры.

</dd> <dt>

**Байт**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Размер данных в байтах.

</dd> <dt>

**DefaultValue**
</dt> <dd>

Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**

</dd> <dd>

Указатель на значение по умолчанию.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXCONSTANTTABLE \_ DESC**](d3dxconstanttable-desc.md)
</dt> </dl>

 

 
