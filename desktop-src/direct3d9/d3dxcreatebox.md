---
description: Использует левую систему координат для создания сетки, содержащей прямоугольник с выровняйтем по осям.
ms.assetid: 396ef0f7-65d5-46f9-9b97-e6471f2fb5fe
title: Функция D3DXCreateBox (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateBox
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 66afc489611936a122e05e8a797997d11e5073429834f8f1b534b03b02c2de4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118526548"
---
# <a name="d3dxcreatebox-function"></a>Функция D3DXCreateBox

Использует левую систему координат для создания сетки, содержащей прямоугольник с выровняйтем по осям.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXCreateBox(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             Width,
  _In_  FLOAT             Height,
  _In_  FLOAT             Depth,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдевице* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, связанное с сеткой созданных Box.

</dd> <dt>

*Ширина* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Ширина прямоугольника вдоль оси x.

</dd> <dt>

*Высота* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Высота поля вдоль оси y.

</dd> <dt>

*Глубина* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Глубина бокса вдоль оси z.

</dd> <dt>

*ппмеш* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Адрес указателя на выходную форму, интерфейс [**ID3DXMesh**](id3dxmesh.md) .

</dd> <dt>

*ппаджаценци* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Адрес указателя на интерфейс [**ID3DXBuffer**](id3dxbuffer.md) . Когда метод возвращает значение, этот параметр заполняется массивом из трех DWORD на грань, которые указывают три соседа для каждой грани в сети. Можно указать **значение NULL** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarks

Созданное поле выравнивается по центру источника.

Эта функция создает сетку с \_ параметром управляемого создания D3DXMESH и [D3DFVF \_ XYZ D3DFVF с \| \_ нормальным](d3dfvf.md) гибким форматом вершин (фвф).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9shape. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>    |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции рисования фигур](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
