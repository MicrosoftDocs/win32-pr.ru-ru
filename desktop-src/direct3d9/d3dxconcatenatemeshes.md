---
description: Объединяет группу сеток в одну общую сеть. Этот метод может при необходимости применить преобразование матрицы к каждой входной сетке и ее координатам текстуры.
ms.assetid: 0f2af63a-ece5-4c99-8cb8-045099eca3ea
title: Функция D3DXConcatenateMeshes (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXConcatenateMeshes
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b96fe47a3d818c382b35a93708ac51b60e891841
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694211"
---
# <a name="d3dxconcatenatemeshes-function"></a>Функция D3DXConcatenateMeshes

Объединяет группу сеток в одну общую сеть. Этот метод может при необходимости применить преобразование матрицы к каждой входной сетке и ее координатам текстуры.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXConcatenateMeshes(
  _In_        LPD3DXMESH        *ppMeshes,
  _In_        UINT              NumMeshes,
  _In_        DWORD             Options,
  _In_  const D3DXMATRIX        *pGeomXForms,
  _In_  const D3DXMATRIX        *pTextureXForms,
  _In_  const D3DVERTEXELEMENT9 *pDecl,
  _In_        LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_       LPD3DXMESH        *ppMeshOut
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппмешес* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Массив указателей входной сетки (см. [**ID3DXMesh**](id3dxmesh.md)). Число элементов в массиве — Нуммешес.

</dd> <dt>

*Нуммешес* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Количество входных сеток для сцепления.

</dd> <dt>

*Параметры* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Параметры создания сетки; Это сочетание одного или нескольких флагов [**D3DXMESH**](./d3dxmesh.md) . Параметры создания сетки эквивалентны параметрам Options, необходимым для [**D3DXCreateMesh**](d3dxcreatemesh.md).

</dd> <dt>

*пжеомксформс* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Необязательный массив преобразований Geometry. Число элементов в массиве — Нуммешес; Каждый элемент является матрицей преобразования (см. [**D3DXMATRIX**](d3dxmatrix.md)). Может иметь **значение NULL**.

</dd> <dt>

*птекстурексформс* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Необязательный массив преобразований текстур. Число элементов в массиве — Нуммешес; Каждый элемент является матрицей преобразования (см. [**D3DXMATRIX**](d3dxmatrix.md)). Этот параметр может иметь **значение NULL**.

</dd> <dt>

*пдекл* \[ окне\]
</dt> <dd>

Тип: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Необязательный указатель на объявление вершины (см. [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)). Этот параметр может иметь **значение NULL**.

</dd> <dt>

*pD3DDevice* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Указатель на устройство [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , которое используется для создания новой сетки.

</dd> <dt>

*ппмешаут* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Адрес указателя на созданную сетку (см. [**ID3DXMesh**](id3dxmesh.md)).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение S \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Комментарии

Если [объявление вершины](vertex-declaration.md) не указано в параметре создания сетки параметров, метод создаст объединение всех объявлений вершин подсетей, продвижение каналов и типов при необходимости. Метод создаст таблицу атрибутов из таблиц атрибутов входных сеток. Чтобы обеспечить создание таблицы атрибутов, вызовите [**optimize**](id3dxmesh--optimize.md) с флагами, установленными в D3DXMESHOPT \_ Compact и D3DXMESHOPT \_ Аттрсорт (см. [**D3DXMESHOPT**](./d3dxmeshopt.md)).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции сетки](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
