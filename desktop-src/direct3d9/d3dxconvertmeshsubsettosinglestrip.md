---
description: Преобразует заданный поднабор сетки в одну ленту треугольника.
ms.assetid: 618c7bee-dd09-4379-bb8b-30505e809df9
title: Функция D3DXConvertMeshSubsetToSingleStrip (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXConvertMeshSubsetToSingleStrip
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 53d3ec4a0362ec923fdbeaa1d880188039e866292897d3fe5518ae34d4e2622d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857374"
---
# <a name="d3dxconvertmeshsubsettosinglestrip-function"></a>Функция D3DXConvertMeshSubsetToSingleStrip

Преобразует заданный поднабор сетки в одну ленту треугольника.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXConvertMeshSubsetToSingleStrip(
  _In_  LPD3DXBASEMESH         MeshIn,
  _In_  DWORD                  AttribId,
  _In_  DWORD                  IBOptions,
  _Out_ LPDIRECT3DINDEXBUFFER9 *ppIndexBuffer,
  _Out_ DWORD                  *pNumIndices
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Сетка* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**

Указатель на интерфейс [**ID3DXBaseMesh**](id3dxbasemesh.md) , представляющий сетку для преобразования в ленту.

</dd> <dt>

*Аттрибид* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Идентификатор атрибута подмножества сетки для преобразования в ленты.

</dd> <dt>

*Ибоптионс* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Сочетание одного или нескольких флагов из перечисления [**D3DXMESH**](./d3dxmesh.md) с указанием параметров для создания буфера индекса. Не может быть D3DXMESH \_ 32-разрядным. Буфер индекса будет создан с 32-разрядными или 16-битовыми индексами в зависимости от формата буфера индекса сетки, указанной параметром *сетки* .

</dd> <dt>

*ппиндексбуффер* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***

Указатель на интерфейс [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) , представляющий буфер индекса, содержащий полосу.

</dd> <dt>

*пнуминдицес* \[ заполняет\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***

Количество индексов в буфере, возвращенном в параметре *ппиндексбуффер* .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может иметь одно из следующих значений: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarks

Перед выполнением этой функции вызовите [**optimize**](id3dxmesh--optimize.md) или [**D3DXOptimizeFaces**](d3dxoptimizefaces.md)с \_ установленным флагом D3DXMESHOPT аттрсорт.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции сетки](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
