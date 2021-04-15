---
description: Создает объект ID3DXPRTEngine, который может эффективно создавать предварительно вычисленные имитации радианце перемещения (PRT) трехмерной сцены.
ms.assetid: fdfe02b5-03fb-4bee-a53b-012ae3572644
title: Функция D3DXCreatePRTEngine (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTEngine
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7b76b58953de81041922659c3315bba9cdf7788b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547930"
---
# <a name="d3dxcreateprtengine-function"></a>Функция D3DXCreatePRTEngine

Создает объект [**ID3DXPRTEngine**](id3dxprtengine.md) , который может эффективно создавать предварительно вычисленные имитации радианце перемещения (PRT) трехмерной сцены.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXCreatePRTEngine(
  _In_    LPD3DXMESH      pMesh,
  _In_    DWORD           *pAdjacency,
  _In_    BOOL            ExtractUVs,
  _In_    LPD3DXMESH      pBlockerMesh,
  _Inout_ LPD3DXPRTENGINE ppEngine
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пмеш* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**

Указатель на входной объект сетки [**ID3DXMesh**](id3dxmesh.md) , моделирующий трехмерную сцену. Эта сеть должна иметь таблицу атрибутов, в которой вершины находятся в уникальном атрибуте.

</dd> <dt>

*паджаценци* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***

Необязательный указатель на массив из трех DWORD на лицо, заполняемый смежными индексами граней. Число байтов в этом массиве должно быть не меньше ((3 \* [**жетнумфацес**](id3dxbasemesh--getnumfaces.md)) \* sizeof (DWORD)). Может иметь **значение NULL**.

</dd> <dt>

*Екстрактувс* \[ окне\]
</dt> <dd>

Тип: **[ **bool** .](../winprog/windows-data-types.md)**

Если **значение — true**, текстуры будут использоваться для хранения векторов АЛБЕДОС или PRT.

</dd> <dt>

*пблоккермеш* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**

Указатель на необязательный объект сетки [**ID3DXMesh**](id3dxmesh.md) , который блокирует трехмерную сцену. Может иметь **значение NULL**.

</dd> <dt>

*ппенгине* \[ в, out\]
</dt> <dd>

Тип: **[ **LPD3DXPRTENGINE**](id3dxprtengine.md)**

Указатель на выходной объект [**ID3DXPRTEngine**](id3dxprtengine.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Комментарии

Используйте [**D3DXConcatenateMeshes**](d3dxconcatenatemeshes.md) для объединения нескольких сеток в один интерфейс сетки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Предварительно вычисленные функции пересылки Радианце](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
