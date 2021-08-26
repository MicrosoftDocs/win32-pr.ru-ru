---
description: Вспомогательная структура для управления таблицей констант шейдера. Это также можно сделать с помощью ID3DXConstantTable.
ms.assetid: cc6d66e4-c600-420b-b7b5-1bd10ecb22f9
title: Структура D3DXSHADER_CONSTANTTABLE (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_CONSTANTTABLE
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: f423eba3187c6bbc5c17d4ba9284e4e1b2048a016b8a11744b83b46e4d8522af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027294"
---
# <a name="d3dxshader_constanttable-structure"></a>\_Структура КОНСТАНТТАБЛЕ D3DXSHADER

Вспомогательная структура для управления таблицей констант шейдера. Это также можно сделать с помощью [**ID3DXConstantTable**](id3dxconstanttable.md).

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DXSHADER_CONSTANTTABLE {
  DWORD Size;
  DWORD Creator;
  DWORD Version;
  DWORD Constants;
  DWORD ConstantInfo;
  DWORD Flags;
  DWORD Target;
} D3DXSHADER_CONSTANTTABLE, *LPD3DXSHADER_CONSTANTTABLE;
```



## <a name="members"></a>Члены

<dl> <dt>

**Размер**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Размер структуры. См. заметки.

</dd> <dt>

**Автор**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Смещение от начала этой структуры (в байтах) к строке, содержащей имя создателя.

</dd> <dt>

**Version**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Версия шейдера.

</dd> <dt>

**Константы**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Число констант.

</dd> <dt>

**константинфо**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Массив константных данных, \_ \[ *константы* D3DXSHADER константинфо \] . См. раздел [**D3DXSHADER \_ константинфо**](d3dxshader-constantinfo.md).

</dd> <dt>

**Флаги**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Флаги [флагов D3DXSHADER](d3dxshader-flags.md) , используемые для компиляции шейдера.

</dd> <dt>

**Целевой объект**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Смещение в строке, содержащей целевой объект.

</dd> </dl>

## <a name="remarks"></a>Remarks

Сведения о константах шейдера включаются в таблицу комментариев, разделенных табуляцией. Все смещения измеряются в байтах от начала структуры. Записи в таблице констант сортируются по автору в возрастающем порядке.

С помощью интерфейсов [**ID3DXConstantTable**](id3dxconstanttable.md) можно управлять таблицей констант шейдера. Кроме того, можно управлять таблицей констант с помощью **D3DXSHADER \_ константтабле**.

Этот элемент размера часто инициализируется с помощью следующего:


```
D3DXSHADER_CONSTANTTABLE constantTable;
constantTable.Size = sizeof(D3DXSHADER_CONSTANTTABLE)
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Структуры D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXGetShaderConstantTable**](d3dxgetshaderconstanttable.md)
</dt> </dl>

 

 
