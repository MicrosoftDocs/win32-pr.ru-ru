---
description: Создает объект ID3DXTextureGutterHelper из входной сетки и данных текстуры.
ms.assetid: 1696fc3d-5b35-48cc-a79b-c0d4ed44e420
title: Функция D3DXCreateTextureGutterHelper (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureGutterHelper
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8957649f3cef6ea67932579918163613160ee993
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703797"
---
# <a name="d3dxcreatetexturegutterhelper-function"></a>Функция D3DXCreateTextureGutterHelper

Создает объект [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) из входной сетки и данных текстуры.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXCreateTextureGutterHelper(
  _In_    UINT                      Width,
  _In_    UINT                      Height,
  _In_    LPD3DXMESH                pMesh,
  _In_    FLOAT                     GutterSize,
  _Inout_ LPD3DXTEXTUREGUTTERHELPER *ppBuffer
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Ширина* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Ширина текстуры в пикселях.

</dd> <dt>

*Высота* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Высота текстуры (в пикселях).

</dd> <dt>

*пмеш* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**

Указатель на входной объект сетки [**ID3DXMesh**](id3dxmesh.md) .

</dd> <dt>

*Гуттерсизе* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Число пикселей текстуры, на которое будет перевышена текстура и создана область переплета. Должно быть не менее 1.

</dd> <dt>

*ппбуффер* \[ в, out\]
</dt> <dd>

Тип: **[ **LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)\***

Указатель на объект [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) , который необходимо создать.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение S \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Комментарии

Используйте [**D3DXConcatenateMeshes**](d3dxconcatenatemeshes.md) для преобразования сцены в новые координаты.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Предварительно вычисленные функции пересылки Радианце](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
