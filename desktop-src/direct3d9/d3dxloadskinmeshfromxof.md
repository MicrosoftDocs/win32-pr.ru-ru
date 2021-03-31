---
description: Загружает сетку обложки из объекта данных файла DirectX. x.
ms.assetid: db284061-2996-4a5f-972d-24577dd1a6d7
title: Функция D3DXLoadSkinMeshFromXof (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSkinMeshFromXof
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b87e97e0bde7be37497f68c276a09163ea68ee71
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103820956"
---
# <a name="d3dxloadskinmeshfromxof-function"></a>Функция D3DXLoadSkinMeshFromXof

Загружает сетку обложки из объекта данных файла DirectX. x.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXLoadSkinMeshFromXof(
  _In_  LPD3DXFILEDATA    pxofMesh,
  _In_  DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppAdjacency,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ DWORD             *pMatOut,
  _Out_ LPD3DXSKININFO    *ppSkinInfo,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пксофмеш* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**

Указатель на интерфейс [**ID3DXFileData**](id3dxfiledata.md) , представляющий файл данных файла для загрузки.

</dd> <dt>

*Параметры* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Сочетание одного или нескольких флагов из перечисления [**D3DXMESH**](./d3dxmesh.md) , в котором указываются параметры создания сетки.

</dd> <dt>

*pD3DDevice* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , объект устройства, связанный с сеткой.

</dd> <dt>

*ппаджаценци* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Адрес указателя на интерфейс [**ID3DXBuffer**](id3dxbuffer.md) . При возврате из этого метода этот параметр заполняется массивом из трех DWORD на грань, которые указывают три соседа для каждой грани в сети.

</dd> <dt>

*ппматериалс* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Адрес указателя на интерфейс [**ID3DXBuffer**](id3dxbuffer.md) . Когда метод возвращает значение, этот параметр заполняется массивом структур [**D3DXMATERIAL**](d3dxmaterial.md) .

</dd> <dt>

*ппеффектинстанцес* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Указатель на буфер, содержащий массив экземпляров эффектов, по одному на группу атрибутов в возвращенной сетке. Экземпляр Effect — это конкретный экземпляр сведений о состоянии, используемый для инициализации результата. См. [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md). Дополнительные сведения о доступе к буферу см. в разделе [**ID3DXBuffer**](id3dxbuffer.md).

</dd> <dt>

*пматаут* \[ заполняет\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***

Указатель на число структур [**D3DXMATERIAL**](d3dxmaterial.md) в массиве *ппматериалс* , когда метод возвращает значение.

</dd> <dt>

*ппскининфо* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***

Адрес указателя на интерфейс [**ID3DXSkinInfo**](id3dxskininfo.md) , представляющий сведения о обложках.

</dd> <dt>

*ппмеш* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Адрес указателя на интерфейс [**ID3DXMesh**](id3dxmesh.md) , который представляет загруженную сетку.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY

## <a name="remarks"></a>Комментарии

Этот метод принимает указатель на внутренний объект в файле x, позволяя загрузить иерархию рамок.

Для файлов сетки, не содержащих сведений об экземпляре влияния, экземпляры эффектов по умолчанию будут сформированы на основе сведений о материалах в файле. x. Экземпляр действия по умолчанию будет иметь значения по умолчанию, соответствующие элементам структуры [**D3DMATERIAL9**](d3dmaterial9.md) .

Имя текстуры по умолчанию также заполняется, но обрабатывается по-другому. Имя будет иметь значение Texture0@Name , соответствующее переменной Effect с именем "Texture0" с заметкой "имя". Он будет содержать строковое имя файла для текстуры.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции сетки](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md)
</dt> <dt>

[**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)
</dt> </dl>

 

 
