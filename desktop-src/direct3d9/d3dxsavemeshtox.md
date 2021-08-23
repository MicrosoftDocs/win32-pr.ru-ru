---
description: Сохраняет сетку в файл. x.
ms.assetid: 6d9cbca8-3847-4e15-95d4-9df3f8269665
title: Функция D3DXSaveMeshToX (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveMeshToX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 668131237def6078d775d0002f624b035ad29e21b9a49399b673933dc63e5b5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988443"
---
# <a name="d3dxsavemeshtox-function"></a>Функция D3DXSaveMeshToX

Сохраняет сетку в файл. x.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXSaveMeshToX(
  _In_       LPCTSTR            pFilename,
  _In_       LPD3DXMESH         pMesh,
  _In_ const DWORD              *pAdjacency,
  _In_ const D3DXMATERIAL       *pMaterials,
  _In_ const D3DXEFFECTINSTANCE *pEffectInstances,
  _In_       DWORD              NumMaterials,
  _In_       DWORD              Format
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфиленаме* \[ окне\]
</dt> <dd>

Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Указатель на строку, указывающую имя файла. Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР. В противном случае строковый тип данных разрешается в LPCSTR. См. заметки.

</dd> <dt>

*пмеш* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**

Указатель на интерфейс [**ID3DXMesh**](id3dxmesh.md) , представляющий сетку для сохранения в файл. x.

</dd> <dt>

*паджаценци* \[ окне\]
</dt> <dd>

Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***

Указатель на массив из трех DWORD на грань, который указывает три соседа для каждой грани в сети. Этот параметр может иметь **значение NULL**.

</dd> <dt>

*пматериалс* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXMATERIAL**](d3dxmaterial.md) \***

Указатель на массив структур [**D3DXMATERIAL**](d3dxmaterial.md) , содержащий сведения о материалах, которые должны быть сохранены в файле. x.

</dd> <dt>

*пеффектинстанцес* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md) \***

Указатель на массив экземпляров эффектов, по одному на группу атрибутов в сетке. Этот параметр может иметь **значение NULL**. Экземпляр Effect — это конкретный экземпляр сведений о состоянии, используемый для инициализации результата. Дополнительные сведения см. в разделе [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).

</dd> <dt>

*Нумматериалс* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Число структур [**D3DXMATERIAL**](d3dxmaterial.md) в массиве *пматериалс* .

</dd> <dt>

*Формат* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Сочетание формата файла и параметров сохранения при сохранении файла. x. См. раздел [константы файла D3DX X](dx9-graphics-reference-d3dx-x-file-constants.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Remarks

Параметр компилятора также определяет версию функции. Если определен Юникод, вызов функции разрешается в D3DXSaveMeshToXW. В противном случае вызов функции разрешается в D3DXSaveMeshToXA, так как используются строки ANSI.

Формат файла по умолчанию — binary; Однако если файл указан как как двоичный, так и текстовый файл, он будет сохранен как текстовый файл. Независимо от формата файла, можно также использовать сжатый формат для уменьшения размера файла.

Ниже приведен типичный пример кода использования этой функции.


```
ID3DXMesh*    m_pMesh;           // Mesh object to be saved to a .x file
D3DXMATERIAL* m_pMaterials;      // Array of material structs in the mesh
DWORD         m_dwNumMaterials;  // Number of material structs in the mesh
    
DWORD dwFormat = D3DXF_FILEFORMAT_BINARY;  // Binary-format .x file (default)
// DWORD dwFormat = D3DXF_FILEFORMAT_TEXT; // Text-format .x file
    
// Load mesh into m_pMesh and determine values of m_pMaterials and 
// m_dwNumMaterials with calls to D3DXLoadMeshxxx or other D3DX functions
    
// ...
        
D3DXSaveMeshToX(
    L"outputxfilename.x",
    m_pMesh,
    NULL,
    m_pMaterials,
    NULL,
    m_dwNumMaterials,
    dwFormat );
```



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

 

 
