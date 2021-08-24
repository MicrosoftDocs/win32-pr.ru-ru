---
description: Описывает параметр, используемый для объекта Effect.
ms.assetid: 60d19b52-67ef-4903-bbde-922a8fac1ad8
title: Структура D3DXPARAMETER_DESC (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPARAMETER_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: a12541e9bfb33979b11f8198e218a3eb474f948aeb8c74982a5369eed782eaa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631154"
---
# <a name="d3dxparameter_desc-structure"></a>\_Структура D3DXPARAMETER DESC

Описывает параметр, используемый для объекта Effect.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DXPARAMETER_DESC {
  LPCSTR              Name;
  LPCSTR              Semantic;
  D3DXPARAMETER_CLASS Class;
  D3DXPARAMETER_TYPE  Type;
  UINT                Rows;
  UINT                Columns;
  UINT                Elements;
  UINT                Annotations;
  UINT                StructMembers;
  DWORD               Flags;
  UINT                Bytes;
} D3DXPARAMETER_DESC, *LPD3DXPARAMETER_DESC;
```



## <a name="members"></a>Члены

<dl> <dt>

**Имя**
</dt> <dd>

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Имя параметра.

</dd> <dt>

**Семантическ**
</dt> <dd>

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Семантическое значение, также называемое использованием.

</dd> <dt>

**Класс**
</dt> <dd>

Тип: **[ **\_ класс D3DXPARAMETER**](./d3dxparameter-class.md)**

</dd> <dd>

Класс параметра. Задайте для этого параметра одно из значений в [**\_ классе D3DXPARAMETER**](./d3dxparameter-class.md).

</dd> <dt>

**Тип**
</dt> <dd>

Тип: **[ **D3DXPARAMETER \_ тип**](./d3dxparameter-type.md)**

</dd> <dd>

Тип параметра. Задайте для него одно из значений [**\_ типа D3DXPARAMETER**](./d3dxparameter-type.md).

</dd> <dt>

**Строки**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Количество строк в массиве.

</dd> <dt>

**Столбцы**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Число столбцов в массиве.

</dd> <dt>

**Elements (XElement Dynamic Property)** (Elements (Динамическое свойство XElement))
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Число элементов в массиве.

</dd> <dt>

**Заметки**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Число заметок.

</dd> <dt>

**структмемберс**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Число элементов структуры.

</dd> <dt>

**Флаги**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Атрибуты параметра. См. раздел [константы эффектов](dx9-graphics-reference-effects-constants.md).

</dd> <dt>

**Байт**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Размер параметра в байтах.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx9effect. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры эффектов](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
