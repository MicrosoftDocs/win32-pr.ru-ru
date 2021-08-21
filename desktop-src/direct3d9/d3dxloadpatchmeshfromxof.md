---
description: Загружает сетку исправлений из объекта ID3DXFileData.
ms.assetid: 8054e33e-6bf8-4a56-9f66-30600732c84f
title: Функция D3DXLoadPatchMeshFromXof (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadPatchMeshFromXof
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8bfdf0faf0a9a8d8d32d38899cdd666d7c4a5d3910119ac36cbca2bf8bb33430
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564834"
---
# <a name="d3dxloadpatchmeshfromxof-function"></a>Функция D3DXLoadPatchMeshFromXof

Загружает сетку исправлений из объекта [**ID3DXFileData**](id3dxfiledata.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXLoadPatchMeshFromXof(
  _In_  LPD3DXFILEDATA    pxofMesh,
  _In_  DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ PDWORD            pNumMaterials,
  _Out_ LPD3DXPATCHMESH   *ppMesh
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

Сочетание одного или нескольких флагов [**D3DXMESH**](./d3dxmesh.md) , задающее параметры создания для сетки.

</dd> <dt>

*pD3DDevice* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Указатель на устройство, из которого создается сетка.

</dd> <dt>

*ппматериалс* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Массив материалов, содержащихся в сетке. Каждый материал индексируется с помощью интерфейса [**ID3DXBuffer**](id3dxbuffer.md) .

</dd> <dt>

*ппеффектинстанцес* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Указатель на буфер, содержащий массив экземпляров эффектов, по одному на группу атрибутов в возвращенной сетке. Экземпляр Effect — это конкретный экземпляр сведений о состоянии, используемый для инициализации результата. См. [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md). Дополнительные сведения о доступе к буферу см. в разделе [**ID3DXBuffer**](id3dxbuffer.md).

</dd> <dt>

*пнумматериалс* \[ заполняет\]
</dt> <dd>

Тип: **пдворд**

Указатель, содержащий количество материалов в сетке.

</dd> <dt>

*ппмеш* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***

Адрес указателя на интерфейс [**ID3DXPatchMesh**](id3dxpatchmesh.md) , представляющий загруженную сетку.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarks

Для файлов сетки, не содержащих сведений об экземпляре влияния, экземпляры эффектов по умолчанию будут сформированы на основе сведений о материалах в файле. x. Экземпляр действия по умолчанию будет иметь значения по умолчанию, соответствующие элементам структуры [**D3DMATERIAL9**](d3dmaterial9.md) .

Имя текстуры по умолчанию также заполняется, но обрабатывается по-другому. Имя будет иметь значение Texture0@Name , соответствующее переменной Effect с именем "Texture0" с заметкой "имя". Он будет содержать строковое имя файла для текстуры.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции сетки](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md)
</dt> <dt>

[**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)
</dt> </dl>

 

 
