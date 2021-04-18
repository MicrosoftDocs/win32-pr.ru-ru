---
description: Возвращает таблицу-константу шейдера, внедренную в шейдер.
ms.assetid: eb965074-819f-44d2-889b-6c6eada4f062
title: Функция D3DXGetShaderConstantTable (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderConstantTable
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 876802023601c14b4cceed0ef0e2db431d7339e0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713667"
---
# <a name="d3dxgetshaderconstanttable-function"></a>Функция D3DXGetShaderConstantTable

Возвращает таблицу-константу шейдера, внедренную в шейдер.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXGetShaderConstantTable(
  _In_  const DWORD               *pFunction,
  _Out_       LPD3DXCONSTANTTABLE * ppConstantTable
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфунктион* \[ окне\]
</dt> <dd>

Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***

Указатель на поток функции DWORD.

</dd> <dt>

 *ппконстанттабле* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***

Возвращает интерфейс таблицы констант (см. [**ID3DXConstantTable**](id3dxconstanttable.md)), который управляет таблицей констант.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Комментарии

Таблица констант создается [**D3DXCompileShader**](d3dxcompileshader.md) и внедряется в текст шейдера. Если требуется дополнительное виртуальное адресное пространство, см. раздел [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции шейдера](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
