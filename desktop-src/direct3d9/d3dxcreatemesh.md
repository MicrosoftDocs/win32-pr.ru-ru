---
description: Создает объект сетки с помощью декларатора.
ms.assetid: ff977517-0a46-4c32-8d5e-f5fc3c1718c1
title: Функция D3DXCreateMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cfb56fe5c52d2726dff0877522b6f72f70437552
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694252"
---
# <a name="d3dxcreatemesh-function"></a>Функция D3DXCreateMesh

Создает объект сетки с помощью декларатора.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXCreateMesh(
  _In_        DWORD               NumFaces,
  _In_        DWORD               NumVertices,
  _In_        DWORD               Options,
  _In_  const LPD3DVERTEXELEMENT9 *pDeclaration,
  _In_        LPDIRECT3DDEVICE9   pD3DDevice,
  _Out_       LPD3DXMESH          *ppMesh
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Нумфацес* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Число граней для сетки. Допустимый диапазон для этого числа больше 0 и один меньше максимального значения DWORD (обычно 65534), так как последний индекс зарезервирован.

</dd> <dt>

*Нумвертицес* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Число вершин для сетки. Этот параметр должен быть больше 0.

</dd> <dt>

*Параметры* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Сочетание одного или нескольких флагов из перечисления [**D3DXMESH**](./d3dxmesh.md) с указанием параметров для сетки.

</dd> <dt>

*пдекларатион* \[ окне\]
</dt> <dd>

Тип: **const [**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Массив элементов [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , описывающих формат вершины для возвращенной сетки. Этот параметр должен быть напрямую сопоставлен с гибким форматом вершин (ФВФ).

</dd> <dt>

*pD3DDevice* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , объект устройства, связываемый с сеткой.

</dd> <dt>

*ппмеш* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Адрес указателя на интерфейс [**ID3DXMesh**](id3dxmesh.md) , представляющий созданный объект сетки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции сетки](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXDeclaratorFromFVF**](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
