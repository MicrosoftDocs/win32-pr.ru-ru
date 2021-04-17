---
description: Создает точную копию сетки, используя код гибкого формата вершин (ФВФ).
ms.assetid: b7d23ea9-1a2f-46e3-bcb5-82040d2a1e12
title: 'Метод ID3DXBaseMesh:: Клонемешфвф (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.CloneMeshFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4cb3b0ad33e54e79464949f441842173fb48a180
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703759"
---
# <a name="id3dxbasemeshclonemeshfvf-method"></a>Метод ID3DXBaseMesh:: Клонемешфвф

Создает точную копию сетки, используя код гибкого формата вершин (ФВФ).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CloneMeshFVF(
  [in]          DWORD             Options,
  [in]          DWORD             FVF,
  [in]          LPDIRECT3DDEVICE9 pDevice,
  [out, retval] LPD3DXMESH        *ppCloneMesh
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Параметры* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Сочетание одного или нескольких флагов [**D3DXMESH**](./d3dxmesh.md) , задающее параметры создания для сетки.

</dd> <dt>

*Фвф* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Сочетание кодов ФВФ, определяющих формат вершины для вершин в выходной сетке. Значения кодов см. в разделе [D3DFVF](d3dfvf.md).

</dd> <dt>

*пдевице* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий объект устройства, связанный с сеткой.

</dd> <dt>

*ппклонемеш* \[ out, retval\]
</dt> <dd>

Тип: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Адрес указателя на интерфейс [**ID3DXMesh**](id3dxmesh.md) , представляющий клонированную сетку.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Комментарии

**ID3DXBaseMesh:: клонемешфвф** используется для переформатирования и изменения макета данных вершин. Это делается путем создания нового объекта сетки. Например, используйте его для добавления пространства для нормалей, текстурных координат, цветов, весов и т. д., которые отсутствовали ранее.

[**ID3DXBaseMesh:: упдатесемантикс**](id3dxbasemesh--updatesemantics.md) обновляет объявление вершины с другой семантической информацией без изменения макета буфера вершин. Этот метод не изменяет содержимое буфера вершин. Например, используйте его, чтобы переметить координату трехмерной текстуры как бинормал или тангенс или наоборот.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> <dt>

[**D3DXFVFFromDeclarator**](d3dxfvffromdeclarator.md)
</dt> </dl>

 

 
